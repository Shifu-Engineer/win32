---
title: SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class
description: Updates an integer property of a virtual desktop collection.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: '2ea27385-5100-4e88-ad11-df5e439d0815'
ms.prod: 'windows-server-dev'
ms.technology: 'remote-desktop-services'
ms.tgt_platform: multiple
keywords: ["SetInt32Property method Remote Desktop Services", "SetInt32Property method Remote Desktop Services , Win32_RDMSVirtualDesktopCollection class", "Win32_RDMSVirtualDesktopCollection class Remote Desktop Services , SetInt32Property method"]
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
---

# SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class

Updates an integer property of a virtual desktop collection.

## Syntax


```mof
uint32 SetInt32Property(
  [in]�string Key,
  [in]�sint32 Value
);
```



## Parameters

<dl> <dt>

*Key* \[in\]
</dt> <dd>

A key that identifies the property to update.

</dd> <dt>

*Value* \[in\]
</dt> <dd>

The new property value.

</dd> </dl>

## Return value

Returns 0 on success, otherwise returns a WMI error code.

## Requirements



|                                     |                                                                                             |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                   |
| Minimum supported server<br/> | Windows Server�2012<br/>                                                              |
| Namespace<br/>                | Root\\CIMv2\\rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## See also

<dl> <dt>

[**Win32\_RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

�

�




