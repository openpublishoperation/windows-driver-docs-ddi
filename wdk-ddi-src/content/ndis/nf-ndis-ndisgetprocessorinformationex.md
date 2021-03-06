---
UID: NF:ndis.NdisGetProcessorInformationEx
title: NdisGetProcessorInformationEx function
author: windows-driver-content
description: The NdisGetProcessorInformationEx function retrieves information about the CPU topology of the local computer.
old-location: netvista\ndisgetprocessorinformationex.htm
old-project: netvista
ms.assetid: 9af21f56-d93d-4130-888c-c7009dc2854d
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: NdisGetProcessorInformationEx
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
req.alt-api: NdisGetProcessorInformationEx
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
req.irql: <= DISPATCH_LEVEL
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisGetProcessorInformationEx function



## -description
The 
  <b>NdisGetProcessorInformationEx</b> function retrieves information about the CPU topology of the local
  computer.



## -syntax

````
NDIS_STATUS NdisGetProcessorInformationEx(
  _In_opt_  NDIS_HANDLE                    NdisHandle,
  _Out_opt_ PNDIS_SYSTEM_PROCESSOR_INFO_EX SystemProcessorInfo,
  _Inout_   PSIZE_T                        Size
);
````


## -parameters

### -param NdisHandle [in, optional]

An NDIS driver or instance handle that was obtained during caller initialization. For example, a
     miniport driver can use the NDIS handle that it obtained from the 
     <a href="..\ndis\nf-ndis-ndismregisterminiportdriver.md">
     NdisMRegisterMiniportDriver</a> or 
     <a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a> functions.
     Other NDIS drivers can use the handles from the following functions:
     

<dl>
<dd>

<a href="..\ndis\nf-ndis-ndisregisterprotocoldriver.md">NdisRegisterProtocolDriver</a>


</dd>
<dd>

<a href="..\ndis\nf-ndis-ndisopenadapterex.md">NdisOpenAdapterEx</a>


</dd>
<dd>

<a href="..\ndis\nf-ndis-ndisfregisterfilterdriver.md">NdisFRegisterFilterDriver</a>


</dd>
<dd>

<a href="..\ndis\nc-ndis-filter_attach.md">FilterAttach</a>


</dd>
</dl>

### -param SystemProcessorInfo [out, optional]

A pointer to a caller-allocated buffer where NDIS puts the 
     <a href="..\ntddndis\ns-ntddndis-_ndis_system_processor_info_ex.md">
     NDIS_SYSTEM_PROCESSOR_INFO_EX</a> structure and an array of 
     <a href="..\ntddndis\ns-ntddndis-_ndis_processor_info_ex.md">NDIS_PROCESSOR_INFO_EX</a> structures
     that contain information about the CPU topology of the local computer. The caller provides the length of
     the buffer in the 
     <i>Size</i> parameter.


### -param Size [in, out]

A pointer to a value that is the size, in bytes, of the buffer that the caller provided. When the
     function returns, this value contains either the amount of data that NDIS put in the buffer or the
     required size of the buffer if the buffer was too short.


## -returns
<b>NdisGetProcessorInformationEx</b> can return one of the following status values:
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>The operation completed successfully.
<dl>
<dt><b>NDIS_STATUS_BUFFER_TOO_SHORT</b></dt>
</dl>The size of the buffer at the 
       <i>Size</i> parameter was too small. In this case, NDIS provides the required buffer size in the 
       <i>Size</i> member.

 


## -remarks
NDIS drivers call the 
    <b>NdisGetProcessorInformationEx</b> function to retrieve information about the processors on the local
    computer.


## -see-also
<dl>
<dt>
<a href="..\ndis\nc-ndis-filter_attach.md">FilterAttach</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a>
</dt>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_system_processor_info_ex.md">NDIS_SYSTEM_PROCESSOR_INFO_EX</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisfregisterfilterdriver.md">NdisFRegisterFilterDriver</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismregisterminiportdriver.md">NdisMRegisterMiniportDriver</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisopenadapterex.md">NdisOpenAdapterEx</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisregisterprotocoldriver.md">NdisRegisterProtocolDriver</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisGetProcessorInformationEx function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

