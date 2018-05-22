---
title: CLUSCTL\_RESOURCE\_PROVIDER\_STATE\_CHANGE control code
description: TBD. Resource DLLs receive this control code as a parameter to the ResourceControl callback function. Because the control code is internal, applications cannot use it in a control code function.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: '7d8bf1c9-3236-40e5-9299-c9926a1204fb'
ms.prod: 'windows-server-dev'
ms.technology: 'failover-clustering'
ms.tgt_platform: multiple
keywords: ["CLUSCTL_RESOURCE_PROVIDER_STATE_CHANGE control code Failover Cluster"]
topic_type:
- apiref
api_name:
- CLUSCTL_RESOURCE_PROVIDER_STATE_CHANGE
api_location:
- ClusAPI.h
api_type:
- HeaderDef
---

# CLUSCTL\_RESOURCE\_PROVIDER\_STATE\_CHANGE control code

TBD. Resource DLLs receive this [control code](about-control-codes.md) as a parameter to the [**ResourceControl**](resourcecontrol.md) callback function. Because the control code is internal, applications cannot use it in a control code function.

## Parameters

This control code has no parameters.

## Return value

This control code does not return a value.

## Remarks

ClusAPI.h defines the 32 bits of CLUSCTL\_RESOURCE\_PROVIDER\_STATE\_CHANGE (0x01500052) as follows.



| Component                 | Bit location     | Value                                                    |
|---------------------------|------------------|----------------------------------------------------------|
| Object code<br/>    | 24�31<br/> | **CLUS\_OBJECT\_RESOURCE** (0x1)<br/>              |
| Global bit<br/>     | 23<br/>    | **CLUS\_NOT\_GLOBAL** (0x0)<br/>                   |
| Modify bit<br/>     | 22<br/>    | **CLUS\_MODIFY** (0x1)<br/>                        |
| User bit<br/>       | 21<br/>    | **CLCTL\_CLUSTER\_BASE** (0x0)<br/>                |
| Type bit<br/>       | 20<br/>    | External (0x0)<br/>                                |
| Operation code<br/> | 0�23<br/>  | **CLCTL\_PROVIDER\_STATE\_CHANGE** (0x500052)<br/> |
| Access code<br/>    | 0�1<br/>   | **CLUS\_ACCESS\_WRITE** (0x2)<br/>                 |



�

For more information, see [Control Code Architecture](control-code-architecture.md).

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                            |
| Minimum supported server<br/> | Windows Server�2008 Datacenter, Windows Server�2008 Enterprise<br/>            |
| Header<br/>                   | <dl> <dt>ClusAPI.h</dt> </dl> |



## See also

<dl> <dt>

[Internal Resource Control Codes](internal-resource-control-codes.md)
</dt> <dt>

[**ClusterResourceControl**](clusterresourcecontrol.md)
</dt> </dl>

�

�




