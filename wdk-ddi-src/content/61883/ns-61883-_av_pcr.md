---
UID: NS:61883._AV_PCR
title: _AV_PCR
author: windows-driver-content
description: The AV_PCR structure specifies settings for an input or output plug.
old-location: ieee\av_pcr.htm
old-project: IEEE
ms.assetid: f6d3f95b-7484-4a6b-9b7e-69f6172b7a12
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: _AV_PCR, AV_PCR, *PAV_PCR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: 61883.h
req.include-header: 61883.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: AV_PCR
req.alt-loc: 61883.h
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
req.typenames: AV_PCR, *PAV_PCR
---

# _AV_PCR structure



## -description
The AV_PCR structure specifies settings for an input or output plug.



## -syntax

````
typedef struct _AV_PCR {
  union {
    OPCR  oPCR;
    IPCR  iPCR;
    ULONG ulongData;
  };
} AV_PCR, *PAV_PCR;
````


## -struct-fields

### -field oPCR

Contains an <a href="https://msdn.microsoft.com/library/windows/hardware/ff537441">OPCR</a> structure that contains initialization values for an output plug. 


### -field iPCR

Contains an <a href="https://msdn.microsoft.com/library/windows/hardware/ff537348">IPCR</a> structure that contains initialization values for an input plug.


### -field ulongData

Reserved for internal use.


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536995">Av61883_SetPlug</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536961">Av61883_CreatePlug</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [IEEE\buses]:%20AV_PCR structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

