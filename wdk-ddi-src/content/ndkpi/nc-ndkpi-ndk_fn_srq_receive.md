---
UID: NC:ndkpi.NDK_FN_SRQ_RECEIVE
title: NDK_FN_SRQ_RECEIVE
author: windows-driver-content
description: The NdkSrqReceive (NDK_FN_SRQ_RECEIVE) function posts a receive request on an NDK shared receive queue (SRQ).
old-location: netvista\ndk_fn_srq_receive.htm
old-project: netvista
ms.assetid: 1D615DEA-5599-4A3D-AEE7-BDBFE9D40C47
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: _NDIS_WWAN_VISIBLE_PROVIDERS, NDIS_WWAN_VISIBLE_PROVIDERS, *PNDIS_WWAN_VISIBLE_PROVIDERS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ndkpi.h
req.include-header: Ndkpi.h
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: NdkSrqReceive
req.alt-loc: ndkpi.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: <=DISPATCH_LEVEL
req.typenames: NDIS_WWAN_VISIBLE_PROVIDERS, *PNDIS_WWAN_VISIBLE_PROVIDERS
---

# NDK_FN_SRQ_RECEIVE callback



## -description
The <i>NdkSrqReceive</i> (<i>NDK_FN_SRQ_RECEIVE</i>) function posts a receive request on an NDK shared receive queue (SRQ).



## -prototype

````
NDK_FN_SRQ_RECEIVE NdkSrqReceive;

NTSTATUS NdkSrqReceive(
  _In_     NDK_SRQ                        *pNdkSrq,
  _In_opt_ PVOID                          RequestContext,
           _In_reads_(nSge) const NDK_SGE *pSgl,
  _In_     ULONG                          nSge
)
{ ... }
````


## -parameters

### -param pNdkSrq [in]

A pointer to an NDK shared receive queue (SRQ) object
(<a href="..\ndkpi\ns-ndkpi-_ndk_srq.md">NDK_SRQ</a>).


### -param RequestContext [in, optional]

A context value to be returned in the <b>RequestContext</b> member of the <a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a> structure for this request.



### -param pSgl 

An array of SGE structures (<a href="..\ndkpi\ns-ndkpi-_ndk_sge.md">NDK_SGE</a>) that represent the buffers to receive incoming data.



### -param nSge [in]

The number of SGE structures in the array  that is specified in the <i>pSgl</i>
parameter.


## -returns
The 
     <i>NdkSrqReceive</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The receive request was posted successfully. A completion entry will be queued to the completion queue (CQ) when the request is completed.

<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred. 

 


## -remarks
<i>NdkSrqReceive</i> posts a receive request to a shared receive queue (SRQ).


## -see-also
<dl>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_sge.md">NDK_SGE</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_srq.md">NDK_SRQ</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_SRQ_RECEIVE callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

