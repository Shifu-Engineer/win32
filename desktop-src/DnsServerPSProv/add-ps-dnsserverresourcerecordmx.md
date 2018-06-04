---
title: Add method of the PS\_DnsServerResourceRecordMX class
description: Add a mail exchanger (MX) resource record.
audience: developer
ms.assetid: b02c4e5c-b048-4970-ab90-d64a9ed0e032
ms.prod: windows-server-dev
ms.technology:
- dns-server
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- Add method
- Add method, PS_DnsServerResourceRecordMX class
- PS_DnsServerResourceRecordMX class, Add method
topic_type:
- apiref
api_name:
- PS_DnsServerResourceRecordMX.Add
api_location:
- DnsServerPSProvider.dll
api_type:
- COM
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Add method of the PS\_DnsServerResourceRecordMX class

Add a mail exchanger (MX) resource record.

## Syntax


```mof
uint32 Add(
  [in]  string                  Name,
  [in]  string                  MailExchange,
  [in]  uint16                  Preference,
  [in]  string                  ComputerName,
  [in]  datetime                TimeToLive,
  [in]  string                  ZoneName,
  [in]  boolean                 AgeRecord,
  [in]  boolean                 AllowUpdateAny,
  [in]  boolean                 PassThru,
  [in]  string                  ZoneScope,
  [in]  string                  VirtualizationInstance,
  [out] DnsServerResourceRecord cmdletOutput
);
```



## Parameters

<dl> <dt>

*Name* \[in\]
</dt> <dd>

The name of the record.

</dd> <dt>

*MailExchange* \[in\]
</dt> <dd>

Specifies the fully qualified domain name (FQDN) for a mail exchanger. The value entered here must resolve to a corresponding host (A) resource record in this zone.

</dd> <dt>

*Preference* \[in\]
</dt> <dd>

Specifies a numeric value (between 0 and 65535) that indicates the mail exchange server's priority with respect to the other mail exchange servers. Lower numbers are given greater preference.

</dd> <dt>

*ComputerName* \[in\]
</dt> <dd>

Specifies the remote computer on which to execute the command.

</dd> <dt>

*TimeToLive* \[in\]
</dt> <dd>

Specifies the Time-To-Live (TTL) setting for the resource record. (The default TTL is defined in SOA resource record). Indicates a length of time used by other DNS servers to determine how long to cache information for a record before expiring and discarding it.

</dd> <dt>

*ZoneName* \[in\]
</dt> <dd>

Specifies the name of the zone.

</dd> <dt>

*AgeRecord* \[in\]
</dt> <dd>

Specifies that this resource record is able to be aged and scavenged. If this command is used, this resource record is able to be aged and scavenged. If this command is not used, the resource record remains in the DNS database unless it is manually updated or removed.

</dd> <dt>

*AllowUpdateAny* \[in\]
</dt> <dd>

Allows any authenticated user to update DNS record with same owner name.

</dd> <dt>

*PassThru* \[in\]
</dt> <dd>

**true** to return the object that was modified by the method. By default, this method does not generate any output.

</dd> <dt>

*ZoneScope* \[in\]
</dt> <dd>

Name of the zone scope.

**Windows Server 2012:** Not supported.

</dd> <dt>

*VirtualizationInstance* \[in\]
</dt> <dd>

Unique identifier of the virtualization instance.

**Windows Server 2012 R2 and Windows Server 2012:** This parameter is unavailable prior to Windows Server 2016.

</dd> <dt>

*cmdletOutput* \[out\]
</dt> <dd>

Receives and embedded instance of the [**DnsServerResourceRecordMX**](dnsserverresourcerecordmx.md) class.

</dd> </dl>

## Requirements



|                                     |                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                          |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                                     |
| Namespace<br/>                | Root\\Microsoft\\Windows\\Dns<br/>                                                           |
| MOF<br/>                      | <dl> <dt>DnsServerPSProvider.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DnsServerPSProvider.dll</dt> </dl> |



## See also

<dl> <dt>

[**PS\_DnsServerResourceRecordMX**](ps-dnsserverresourcerecordmx.md)
</dt> </dl>

 

 




