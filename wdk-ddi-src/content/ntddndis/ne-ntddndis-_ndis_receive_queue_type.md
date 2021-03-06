---
UID: NE:ntddndis._NDIS_RECEIVE_QUEUE_TYPE
title: _NDIS_RECEIVE_QUEUE_TYPE
author: windows-driver-content
description: The NDIS_RECEIVE_QUEUE_TYPE enumeration identifies the type of a receive queue.
old-location: netvista\ndis_receive_queue_type.htm
old-project: netvista
ms.assetid: 8ee28daf-2719-42bc-ab2e-6dcfa7f0e04b
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: _NDIS_RECEIVE_QUEUE_TYPE, NDIS_RECEIVE_QUEUE_TYPE, *PNDIS_RECEIVE_QUEUE_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddndis.h
req.include-header: Ndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.20 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: NDIS_RECEIVE_QUEUE_TYPE
req.alt-loc: Ntddndis.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.typenames: NDIS_RECEIVE_QUEUE_TYPE, *PNDIS_RECEIVE_QUEUE_TYPE
---

# _NDIS_RECEIVE_QUEUE_TYPE enumeration



## -description
The <b>NDIS_RECEIVE_QUEUE_TYPE</b> enumeration identifies the type of a receive queue.



## -syntax

````
typedef enum _NDIS_RECEIVE_QUEUE_TYPE { 
  NdisReceiveQueueTypeUnspecified,
  NdisReceiveQueueTypeVMQueue,
  NdisReceiveQueueTypeMaximum
} NDIS_RECEIVE_QUEUE_TYPE, *PNDIS_RECEIVE_QUEUE_TYPE;
````


## -enum-fields

### -field NdisReceiveQueueTypeUnspecified

The receive queue type is not specified.


### -field NdisReceiveQueueTypeVMQueue

This value specifies a virtual machine (VM) receive queue.


### -field NdisReceiveQueueTypeMaximum

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


## -remarks
The NDIS_RECEIVE_QUEUE_TYPE enumeration is used in the 
    <b>QueueType</b> member of the 
    <a href="..\ntddndis\ns-ntddndis-_ndis_receive_queue_parameters.md">
    NDIS_RECEIVE_QUEUE_PARAMETERS</a> and 
    <a href="..\ntddndis\ns-ntddndis-_ndis_receive_queue_info.md">
    NDIS_RECEIVE_QUEUE_INFO</a> structures.


## -see-also
<dl>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_receive_queue_info.md">NDIS_RECEIVE_QUEUE_INFO</a>
</dt>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_receive_queue_parameters.md">NDIS_RECEIVE_QUEUE_PARAMETERS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_RECEIVE_QUEUE_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

