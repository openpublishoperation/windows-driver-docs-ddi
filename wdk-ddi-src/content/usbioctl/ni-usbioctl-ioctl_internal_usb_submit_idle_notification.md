---
UID: NI:usbioctl.IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION
title: IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION
author: windows-driver-content
description: The IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION I/O request is used by drivers to inform the USB bus driver that a device is idle and can be suspended.
old-location: buses\ioctl_internal_usb_submit_idle_notification.htm
old-project: usbref
ms.assetid: e7ce1448-223f-4aea-b5e7-70a3b2f58e77
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: _USB_HUB_TYPE, USB_HUB_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: usbioctl.h
req.include-header: Usbioctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION
req.alt-loc: Usbioctl.h
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
req.typenames: USB_HUB_TYPE
req.product: Windows 10 or later.
---

# IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION IOCTL



## -description

The <b>IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION</b> I/O request is used by drivers to inform the USB bus driver that a device is idle and can be suspended. 

When sending this IOCTL, caller must furnish a callback routine that does the actual suspension of the device. The USB bus driver will call this routine at PASSIVE_LEVEL when it is safe for the device to be powered down. If the device supports remote wake up and has no Wait/Wake IRP already pending, the callback routine should submit a Wait/Wake IRP to the bus driver for the device, before powering it down. 

For additional information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563907">Supporting Devices that Have Wake-Up Capabilities</a>


<b>IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION</b> is a kernel-mode I/O control request. This request targets the USB hub PDO. This request must be sent at an IRQL of PASSIVE_LEVEL.



The <b>IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION</b> I/O request is used by drivers to inform the USB bus driver that a device is idle and can be suspended. 

When sending this IOCTL, caller must furnish a callback routine that does the actual suspension of the device. The USB bus driver will call this routine at PASSIVE_LEVEL when it is safe for the device to be powered down. If the device supports remote wake up and has no Wait/Wake IRP already pending, the callback routine should submit a Wait/Wake IRP to the bus driver for the device, before powering it down. 

For additional information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563907">Supporting Devices that Have Wake-Up Capabilities</a>


<b>IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION</b> is a kernel-mode I/O control request. This request targets the USB hub PDO. This request must be sent at an IRQL of PASSIVE_LEVEL.



## -ioctlparameters

### -input-buffer
<b>Parameters.DeviceIoControl.Type3InputBuffer</b> should be a pointer to a <b>USB_IDLE_CALLBACK_INFO</b> structure. This structure should contain a pointer to the callback routine and a pointer to the callback routine context. 

The structure holding the callback information is defined in usbioctl.h as follows:


### -input-buffer-length
The size of a <b>USB_IDLE_CALLBACK_INFO</b> structure.


### -output-buffer
None.


### -output-buffer-length
None.


### -in-out-buffer

<text></text>

### -inout-buffer-length

<text></text>

### -status-block
I/O Status block
The bus or port driver sets <b>Irp-&gt;IoStatus.Status</b> to STATUS_SUCCESS or the appropriate error status.


## -remarks
