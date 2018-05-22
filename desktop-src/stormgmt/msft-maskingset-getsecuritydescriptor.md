---
title: GetSecurityDescriptor method of the MSFT\_MaskingSet class
description: Retrieves the security descriptor that controls access to the masking set object instance.
ms.assetid: '8738053D-3852-4EB9-9297-48428030CFEF'
keywords: ["GetSecurityDescriptor method Windows Storage Management API", "GetSecurityDescriptor method Windows Storage Management API , MSFT_MaskingSet class", "MSFT_MaskingSet class Windows Storage Management API , GetSecurityDescriptor method"]
topic_type:
- apiref
api_name:
- MSFT_MaskingSet.GetSecurityDescriptor
api_location:
- Root\Microsoft\Windows\Storage
api_type:
- COM
---

# GetSecurityDescriptor method of the MSFT\_MaskingSet class

Retrieves the security descriptor that controls access to the masking set object instance.

## Syntax


```mof
UInt32 GetSecurityDescriptor(
  [out]�String SecurityDescriptor,
  [out]�String ExtendedStatus
);
```



## Parameters

<dl> <dt>

*SecurityDescriptor* \[out\]
</dt> <dd>

A Security Descriptor Definition Language (SDDL) formatted string describing the access control list of the object. This parameter is required and cannot be NULL.

</dd> <dt>

*ExtendedStatus* \[out\]
</dt> <dd>

A string that contains an embedded [**MSFT\_StorageExtendedStatus**](msft-storageextendedstatus.md) object.

This parameter allows the storage provider to return extended (implementation-specific) error information.

</dd> </dl>

## Return value

<dl> <dt>

**Success** (0)
</dt> <dt>

**Not Supported** (1)
</dt> <dt>

**Unspecified Error** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Failed** (4)
</dt> <dt>

**Invalid Parameter** (5)
</dt> <dt>

**Access denied** (40001)
</dt> <dt>

**There are not enough resources to complete the operation.** (40002)
</dt> <dt>

**Cannot connect to the storage provider.** (46000)
</dt> <dt>

**The storage provider cannot connect to the storage subsystem.** (46001)
</dt> </dl>

## Requirements



|                                     |                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�8 \[desktop apps only\]<br/>                                                |
| Minimum supported server<br/> | Windows Server�2012 \[desktop apps only\]<br/>                                      |
| Namespace<br/>                | Root\\Microsoft\\Windows\\Storage<br/>                                              |
| MOF<br/>                      | <dl> <dt>Storagewmi.mof</dt> </dl> |



## See also

<dl> <dt>

[**MSFT\_MaskingSet**](msft-maskingset.md)
</dt> </dl>

�

�




