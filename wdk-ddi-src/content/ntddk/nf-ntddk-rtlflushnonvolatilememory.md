---
UID: NF:ntddk.RtlFlushNonVolatileMemory
title: RtlFlushNonVolatileMemory function
author: windows-driver-content
description: The routine RtlFlushNonVolatileMemory optimally flushes the given non-volatile memory region.
old-location: ifsk\rtlflushnonvolatilememory.htm
old-project: ifsk
ms.assetid: 759CDFAA-D939-44E7-AE03-E3ED90F8E09D
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: RtlFlushNonVolatileMemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntddk.h
req.include-header: Winnt.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RtlFlushNonVolatileMemory
req.alt-loc: ntddk.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
req.typenames: WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---

# RtlFlushNonVolatileMemory function



## -description
The  routine <b>RtlFlushNonVolatileMemory</b> optimally flushes the given non-volatile memory region.



## -syntax

````
NTSTATUS RtlFlushNonVolatileMemory(
   _In_ PVOID                   NvToken,
   _In_reads_bytes_(Size) PVOID NvBuffer,
   _In_ SIZE_T                  Size,
   _In_ ULONG                   Flags
);
````


## -parameters

### -param NvToken 

 A pointer to an opaque structure that has
        information about various properties of the non-volatile memory region which <a href="..\ntddk\nf-ntddk-rtlgetnonvolatiletoken.md">RtlGetNonVolatileToken</a> had returned.


### -param NvBuffer 

A pointer to the non-volatile memory to flush. This should be user addresses obtained from
        a file mapping object.


### -param Size 

The length, in bytes, of the non-volatile memory buffer <b>NvBuffer</b> points to.


### -param Flags 

One of the following flags can be specified:

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FLUSH_NV_MEMORY_IN_FLAG_NO_DRAIN

</td>
<td>
Specifies that this routine does not need to wait for the flush to drain.

</td>
</tr>
</table>
 


## -returns
The routine <b>RtlFreeNonVolatileToken</b> returns one of the status codes:
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl><b>NvToken</b> is an invalid pointer or token.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The request was successful.

 


## -remarks
 This routine <b>RtlFlushNonVolatileMemory</b> can also add more context to <b>NvToken</b> to help verifiers. This routine is currently not supported for Windows Server until the next major release of Windows Server. 


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/EA1C2DF3-591C-407A-ABBF-DE615466A498">RtlDrainNonVolatileFlush</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/169C5F41-B372-4056-AAC5-53DD0582A563">RtlFlushNonVolatileMemoryRanges</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/8E083814-7408-47D2-A811-2DCBDCD13097">RtlFreeNonVolatileToken</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/A9E866D4-C47F-4926-A838-EDB739CF1185">RtlGetNonVolatileToken</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/49DDDEF8-F949-4674-A18B-9BB091D163C2">RtlWriteNonVolatileMemory</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RtlFlushNonVolatileMemory routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

