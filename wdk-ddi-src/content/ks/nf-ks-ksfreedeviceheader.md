---
UID: NF:ks.KsFreeDeviceHeader
title: KsFreeDeviceHeader function
author: windows-driver-content
description: The KsFreeDeviceHeader function cleans up and frees a previously allocated device header.
old-location: stream\ksfreedeviceheader.htm
old-project: stream
ms.assetid: b7e30dde-ace5-47f0-a1e8-b8337ada1550
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: KsFreeDeviceHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ks.h
req.include-header: Ks.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KsFreeDeviceHeader
req.alt-loc: Ks.lib,Ks.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ks.lib
req.dll: 
req.irql: 
req.typenames: 
---

# KsFreeDeviceHeader function



## -description
The <b>KsFreeDeviceHeader</b> function cleans up and frees a previously allocated device header.



## -syntax

````
VOID KsFreeDeviceHeader(
  _In_ KSDEVICE_HEADER Header
);
````


## -parameters

### -param Header [in]

Indicates the device header to free that had been previously allocated by <b>KsAllocateDeviceHeader</b>.


## -returns
None


## -remarks


## -see-also
<dl>
<dt>
<a href="..\ks\nf-ks-ksallocatedeviceheader.md">KsAllocateDeviceHeader</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KsFreeDeviceHeader function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

