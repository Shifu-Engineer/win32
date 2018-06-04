---
Description: Specifies whether the input stream is interlaced.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY\_COLORCONV\_MODE Property
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MFPKEY\_COLORCONV\_MODE Property

Specifies whether the input stream is interlaced.

## Constant for IPropertyBag

Available only by using [**IPropertyStore**](https://msdn.microsoft.com/windows/desktop/e995aaa1-d4c9-475f-b1fa-b9123cd5b653).

## Data Type

VT\_I4

## Default Value

Computed by the DSP from the source video.

## Applies To

-   [Color Converter DSP](colorconverter.md)

## Remarks

Use one of the following values.



| Value | Description |
|-------|-------------|
| 0     | Progressive |
| 2     | Interlaced  |



 

If this property is not set, the DSP uses the input media type to determine whether the video is interlaced. You can set this property to override the media type setting.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Properties](media-foundation-properties.md)
</dt> </dl>

 

 



