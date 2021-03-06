---
UID: NF:ucmmanager.UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT
title: UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT function
author: windows-driver-content
description: Initializes a UCM_CONNECTOR_TYPEC_ATTACH_PARAMS structure.
old-location: buses\ucm_connector_typec_attach_params_init.htm
old-project: usbref
ms.assetid: C360556B-5A28-4FC3-9304-6000061A1D69
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ucmmanager.h
req.include-header: Ucmcx.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 1.15
req.umdf-ver: 2.15
req.alt-api: UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT
req.alt-loc: Ucmmanager.h
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
req.typenames: *PPORT_DATA_1, PORT_DATA_1
req.product: Windows 10 or later.
---

# UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT function



## -description
Initializes a <a href="..\ucmmanager\ns-ucmmanager-_ucm_connector_typec_attach_params.md">UCM_CONNECTOR_TYPEC_ATTACH_PARAMS</a> structure.



## -syntax

````
FORCEINLINE void UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT(
  _Out_ PUCM_CONNECTOR_TYPEC_ATTACH_PARAMS Config,
  _In_  UCM_TYPE_C_PORT_STATE              PortPartnerType
);
````


## -parameters

### -param Config [out]

Pointer to a caller-allocated <a href="..\ucmmanager\ns-ucmmanager-_ucm_connector_typec_attach_params.md">UCM_CONNECTOR_TYPEC_ATTACH_PARAMS</a> structure to initialize.


### -param PortPartnerType [in]

A <a href="..\ucmtypes\ne-ucmtypes-_ucm_typec_partner.md">UCM_TYPE_C_PORT_STATE</a>-typed flag that indicates the state of the partner port.


## -returns
This function does not return a value.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\ucmmanager\nf-ucmmanager-ucmconnectortypecattach.md">UcmConnectorTypeCAttach</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UCM_CONNECTOR_TYPEC_ATTACH_PARAMS_INIT function%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

