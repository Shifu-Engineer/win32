﻿---
Description: 'Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.'
ms.assetid: '9426D235-65E1-40BA-94E9-CF0C49263E6F'
title: 'MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property'
---

# MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property

Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.



Data type

PROPVARIANT type (vt)

PROPVARIANT member

**ULONG**

VT\_UI4

**ulVal**



## Remarks

Use this property to configure the Media Foundation HTTP byte stream. To set the property, pass an [**IPropertyStore**](properties.IPropertyStore) pointer to the source resolver. For more information, see [Configuring a Media Source](configuring-a-media-source.md).

The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration. This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.

## Requirements



|                   |                                                                                    |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Properties](media-foundation-properties.md)
</dt> </dl>

 

 



