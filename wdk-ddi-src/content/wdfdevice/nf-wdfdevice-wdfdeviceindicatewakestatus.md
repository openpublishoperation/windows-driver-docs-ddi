---
UID: NF:wdfdevice.WdfDeviceIndicateWakeStatus
title: WdfDeviceIndicateWakeStatus function
author: windows-driver-content
description: The WdfDeviceIndicateWakeStatus method informs the framework that the calling bus driver has stopped waiting for a specified device to trigger a wake signal on the bus.
old-location: wdf\wdfdeviceindicatewakestatus.htm
old-project: wdf
ms.assetid: 6581a309-1a6d-4795-a55c-327215ea18ee
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: WdfDeviceIndicateWakeStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfdevice.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 
req.alt-api: WdfDeviceIndicateWakeStatus
req.alt-loc: Wdf01000.sys,Wdf01000.sys.dll
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (see Framework Library Versioning.)
req.dll: 
req.irql: <= DISPATCH_LEVEL
req.typenames: WDF_STATE_NOTIFICATION_TYPE
req.product: Windows 10 or later.
---

# WdfDeviceIndicateWakeStatus function



## -description
<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfDeviceIndicateWakeStatus</b> method informs the framework that the calling bus driver has stopped waiting for a specified device to trigger a wake signal on the bus.



## -syntax

````
NTSTATUS WdfDeviceIndicateWakeStatus(
  _In_ WDFDEVICE Device,
  _In_ NTSTATUS  WaitWakeStatus 
);
````


## -parameters

### -param Device [in]

A handle to a framework device object. 


### -param WaitWakeStatus  [in]

An NTSTATUS status value. If the device triggered a wake signal, the caller must set this value to STATUS_SUCCESS or another status value for which <a href="https://msdn.microsoft.com/fe823930-e3ff-4c95-a640-bb6470c95d1d">NT_SUCCESS</a>(<i>WaitWakeStatus</i>) equals <b>TRUE</b>. If the device did not trigger a wake signal or if an error was detected, the caller must provide a status value for which NT_SUCCESS(<i>WaitWakeStatus</i>) equals <b>FALSE</b>. For more information, see the following Remarks section. 


## -returns
If the operation succeeds, <b>WdfDeviceIndicateWakeStatus</b> returns STATUS_SUCCESS. Additional return values include:
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl><i>WaitWakeStatus</i> is STATUS_PENDING or STATUS_CANCELLED.

<dl>
<dt><b>STATUS_INVALID_DEVICE_REQUEST</b></dt>
</dl>The driver stack was not set up to wait for the device to trigger a wake signal.

<dl>
<dt><b>STATUS_INVALID_DEVICE_STATE</b></dt>
</dl>The calling driver is not responsible for waiting for the device to trigger a wake signal.

 

The method might return other <a href="https://msdn.microsoft.com/library/windows/hardware/ff557697">NTSTATUS values</a>.

A bug check occurs if the driver supplies an invalid object handle.


## -remarks
If <a href="https://msdn.microsoft.com/fe823930-e3ff-4c95-a640-bb6470c95d1d">NT_SUCCESS</a>(<i>WaitWakeStatus</i>) equals <b>TRUE</b>, the framework will restore the device and system to their working states. If NT_SUCCESS(<i>WaitWakeStatus</i>) equals <b>FALSE</b>, the device and system will remain in their current states.

For more information about calling the <b>WdfDeviceIndicateWakeStatus</b> method, see <a href="https://msdn.microsoft.com/519dcd1a-9975-48b1-a032-04348b903ac5">Supporting System Wake-Up</a>.

The following code example informs the framework that the specified device has triggered a wake signal.</p>