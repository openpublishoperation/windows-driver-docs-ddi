---
UID: NF:wdfdevice.WdfDeviceAddRemovalRelationsPhysicalDevice
title: WdfDeviceAddRemovalRelationsPhysicalDevice function
author: windows-driver-content
description: The WdfDeviceAddRemovalRelationsPhysicalDevice method indicates that a specified device must be removed when another specified device is removed.
old-location: wdf\wdfdeviceaddremovalrelationsphysicaldevice.htm
old-project: wdf
ms.assetid: 4638905f-cefb-4bf0-aa00-64f2f096dc22
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: WdfDeviceAddRemovalRelationsPhysicalDevice
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
req.alt-api: WdfDeviceAddRemovalRelationsPhysicalDevice
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

# WdfDeviceAddRemovalRelationsPhysicalDevice function



## -description
<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfDeviceAddRemovalRelationsPhysicalDevice</b> method indicates that a specified device must be removed when another specified device is removed. 



## -syntax

````
NTSTATUS WdfDeviceAddRemovalRelationsPhysicalDevice(
  _In_ WDFDEVICE      Device,
  _In_ PDEVICE_OBJECT PhysicalDevice
);
````


## -parameters

### -param Device [in]

A handle to a framework device object.


### -param PhysicalDevice [in]

A pointer to a caller-supplied <a href="..\wdm\ns-wdm-_device_object.md">DEVICE_OBJECT</a> structure that represents a physical device object (PDO).


## -returns
If the operation succeeds, <b>WdfDeviceAddRemovalRelationsPhysicalDevice</b> returns STATUS_SUCCESS. Additional return values include:
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl><i>PhysicalDevice</i> is <b>NULL</b>.
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>A memory allocation failed.

 

The method might return other <a href="https://msdn.microsoft.com/library/windows/hardware/ff557697">NTSTATUS values</a>.

A bug check occurs if the driver supplies an invalid object handle.


## -remarks
The <i>PhysicalDevice</i> parameter points to a PDO of a device whose drivers must be removed when the drivers for <i>Device</i> are removed. Typically, both devices are controlled by the calling driver. Do not report the child devices of the device object specified in <i>Device</i> because when the Plug and Play manager removes a parent device, it also removes the device's children.

Your driver can call <b>WdfDeviceAddRemovalRelationsPhysicalDevice</b> multiple times to add multiple devices to the list of devices that must be removed when <i>Device</i> is removed. The order in which the specified devices are removed is not defined.

The following code example adds the device that <b>pPdo</b> identifies to the list of devices that must be removed when the device that <b>device</b> specifies is removed.


## -see-also
<dl>
<dt>
<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceremoveremovalrelationsphysicaldevice.md">WdfDeviceRemoveRemovalRelationsPhysicalDevice</a>
</dt>
<dt>
<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceclearremovalrelationsdevices.md">WdfDeviceClearRemovalRelationsDevices</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfDeviceAddRemovalRelationsPhysicalDevice method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

