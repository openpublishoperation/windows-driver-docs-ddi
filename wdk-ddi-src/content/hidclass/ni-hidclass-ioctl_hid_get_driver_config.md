---
UID: NI:hidclass.IOCTL_HID_GET_DRIVER_CONFIG
title: IOCTL_HID_GET_DRIVER_CONFIG
author: windows-driver-content
description: The IOCTL_HID_GET_DRIVER_CONFIG request retrieves the driver configuration.
old-location: hid\ioctl_hid_get_driver_config.htm
old-project: hid
ms.assetid: F648EF1E-2673-499D-81BF-03B7B2148FA2
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: _HDAUDIO_STREAM_FORMAT, *PHDAUDIO_STREAM_FORMAT, HDAUDIO_STREAM_FORMAT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: hidclass.h
req.include-header: Hidclass.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IOCTL_HID_GET_DRIVER_CONFIG
req.alt-loc: hidclass.h
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
req.typenames: *PHDAUDIO_STREAM_FORMAT, HDAUDIO_STREAM_FORMAT
---

# IOCTL_HID_GET_DRIVER_CONFIG IOCTL



## -description
The <b>IOCTL_HID_GET_DRIVER_CONFIG</b> 
   request retrieves the driver configuration.

This IOCTL is reserved for system use.



## -ioctlparameters

### -input-buffer

<text></text>

### -input-buffer-length

<text></text>

### -output-buffer

<text></text>

### -output-buffer-length

<text></text>

### -in-out-buffer

<text></text>

### -inout-buffer-length

<text></text>

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code. 
For more information, see [XREF-LINK:NTSTATUS Values].

## -remarks
