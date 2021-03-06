---
UID: NS:wwan._WWAN_DEVICE_SERVICE_RESPONSE
title: _WWAN_DEVICE_SERVICE_RESPONSE
author: windows-driver-content
description: The WWAN_DEVICE_SERVICE_RESPONSE structure represents a response from a device service.
old-location: netvista\wwan_device_service_response.htm
old-project: netvista
ms.assetid: FCDAEE07-B10E-491B-9BDB-49D77444281D
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: _WWAN_DEVICE_SERVICE_RESPONSE, WWAN_DEVICE_SERVICE_RESPONSE, *PWWAN_DEVICE_SERVICE_RESPONSE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with  Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: WWAN_DEVICE_SERVICE_RESPONSE
req.alt-loc: wwan.h
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
req.typenames: WWAN_DEVICE_SERVICE_RESPONSE, *PWWAN_DEVICE_SERVICE_RESPONSE
req.product: Windows 10 or later.
---

# _WWAN_DEVICE_SERVICE_RESPONSE structure



## -description
The WWAN_DEVICE_SERVICE_RESPONSE structure represents a response from a device service.



## -syntax

````
typedef struct _WWAN_DEVICE_SERVICE_RESPONSE {
  GUID  DeviceServiceGuid;
  ULONG ResponseID;
  ULONG uDataSize;
} WWAN_DEVICE_SERVICE_RESPONSE, *PWWAN_DEVICE_SERVICE_RESPONSE;
````


## -struct-fields

### -field DeviceServiceGuid

The GUID of the device service that the response originated from.


### -field ResponseID

The ID of the response.


### -field uDataSize

The size, in bytes, of the device service response data that follows the structure instance in memory. This value should not exceed the value of the <b>uMaxCommandDataSize</b> member of the <a href="..\wwan\ns-wwan-_wwan_supported_device_services.md">WWAN_SUPPORTED_DEVICE_SERVICES</a> structure.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\wwan\ns-wwan-_wwan_supported_device_services.md">WWAN_SUPPORTED_DEVICE_SERVICES</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20WWAN_DEVICE_SERVICE_RESPONSE structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

