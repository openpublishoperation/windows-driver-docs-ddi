---
UID: NF:ndis.NdisGroupActiveProcessorMask
title: NdisGroupActiveProcessorMask function
author: windows-driver-content
description: The NdisGroupActiveProcessorMask function returns the currently active processor mask for the specified group.
old-location: netvista\ndisgroupactiveprocessormask.htm
old-project: netvista
ms.assetid: 92a50a96-8bfb-4d5d-8f24-dd29794e55b1
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: NdisGroupActiveProcessorMask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Universal
req.target-min-winverclnt: Supported in NDIS 6.20 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: NdisGroupActiveProcessorMask
req.alt-loc: ndis.lib,ndis.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndis.lib
req.dll: 
req.irql: Any level
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisGroupActiveProcessorMask function



## -description
The 
  <b>NdisGroupActiveProcessorMask</b> function returns the currently active processor mask for the specified
  group.



## -syntax

````
KAFFINITY NdisGroupActiveProcessorMask(
   USHORT Group
);
````


## -parameters

### -param Group 

A USHORT value that identifies a processor group in the local computer system.


## -returns
<b>NdisGroupActiveProcessorMask</b> returns the currently active processor mask for the specified group
     as a 
     <b>KAFFINITY</b> bitmap. In an environment that allows for hot-add functionality, this bitmap can change
     during runtime.


## -remarks
An NDIS driver might call the 
    <b>NdisGroupActiveProcessorMask</b> function during initialization before it allocates resources.

The 
    <b>KAFFINITY</b> value that 
    <b>NdisGroupActiveProcessorMask</b> returns can change at runtime on SKUs that support hot-add
    functionality for CPUs.

To obtain an active processor count, call the 
    <a href="..\ndis\nf-ndis-ndisgroupactiveprocessorcount.md">
    NdisGroupActiveProcessorCount</a> function.


## -see-also
<dl>
<dt>
<a href="..\ndis\nf-ndis-ndisgroupactiveprocessorcount.md">
   NdisGroupActiveProcessorCount</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndissystemactiveprocessorcount.md">
   NdisSystemActiveProcessorCount</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndissystemprocessorcount.md">NdisSystemProcessorCount</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisGroupActiveProcessorMask function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

