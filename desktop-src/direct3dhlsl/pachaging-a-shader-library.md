---
title: Packaging a shader library
description: Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.
ms.assetid: 'ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28'
---

# Packaging a shader library

Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.

**Objective:** To package a shader library to use for shader linking.

## Prerequisites

We assume that you are familiar with C++. You also need basic experience with graphics programming concepts.

**Time to complete:** 30 minutes.

## Instructions

### 1. Compiling your shader code

Compile your shader code with one of the compile functions. For example, the [HLSL shader compiler sample](http://go.microsoft.com/fwlink/?LinkId=321937) uses [**D3DCompile**](d3dcompile.md):


```C++
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &amp;codeBlob,
        &amp;errorBlob
        );
```



The source string contains the uncompiled ASCII HLSL code.

### 2. Load the compiled code into a shader library.

Call the [**D3DLoadModule**](d3dloadmodule.md) function to load the compiled code ([**ID3DBlob**](https://msdn.microsoft.com/library/windows/desktop/ff728743)) into a module ([**ID3D11Module**](https://msdn.microsoft.com/library/windows/desktop/dn280563)) that represents a shader library.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &amp;shaderLibrary));
```



### 3. Bind resources from source slots to destination slots.

Call the [**ID3D11Module::CreateInstance**](https://msdn.microsoft.com/library/windows/desktop/dn280608) method to create an instance ([**ID3D11ModuleInstance**](https://msdn.microsoft.com/library/windows/desktop/dn280564)) of the library so you can then define resource bindings for the instance.

Call the bind methods of [**ID3D11ModuleInstance**](https://msdn.microsoft.com/library/windows/desktop/dn280564) to bind the resources you need from source slots to destination slots. The resources can be textures, buffers, samplers, constant buffers, or UAVs. Typically, you will use the same slots as the source library.


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &amp;shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



This HLSL code from the [HLSL shader compiler sample](http://go.microsoft.com/fwlink/?LinkId=321937) shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](https://msdn.microsoft.com/library/windows/desktop/dn280564).

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## Summary and next steps

We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.

Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.

[Constructing a function-linking-graph and linking it to compiled code](constructing-a-function-linking-graph.md)

## Related topics

<dl> <dt>

[Using shader linking](using-shader-linking.md)
</dt> </dl>

 

 



