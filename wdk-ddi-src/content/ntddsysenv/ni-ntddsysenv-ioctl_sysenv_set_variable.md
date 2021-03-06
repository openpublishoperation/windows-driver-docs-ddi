---
UID: NI:ntddsysenv.IOCTL_SYSENV_SET_VARIABLE
title: IOCTL_SYSENV_SET_VARIABLE
author: windows-driver-content
description: Sets the value of the specified system environment variables using SysEnv device.
old-location: kernel\ioctl_ioctl_sysenv_set_variable.htm
old-project: kernel
ms.assetid: 2BA555D8-CFD3-4D27-BC38-3B261D2F95EF
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: _STORAGE_ZONE_GROUP, *PSTORAGE_ZONE_GROUP, STORAGE_ZONE_GROUP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddsysenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IOCTL_SYSENV_SET_VARIABLE
req.alt-loc: Ntddsysenv.h
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
req.typenames: *PSTORAGE_ZONE_GROUP, STORAGE_ZONE_GROUP
---

# IOCTL_SYSENV_SET_VARIABLE IOCTL



## -description

Sets the value of the specified system environment variables using
    SysEnv device.




Sets the value of the specified system environment variables using
    SysEnv device.




## -ioctlparameters

### -input-buffer
A pointer to a  <a href="..\ntddsysenv\ns-ntddsysenv-_xvariable_name_and_value.md">XVARIABLE_NAME_AND_VALUE</a> structure that contains the information to set.


### -input-buffer-length
The size of the <a href="..\ntddsysenv\ns-ntddsysenv-_xvariable_name_and_value.md">XVARIABLE_NAME_AND_VALUE</a> structure.


### -output-buffer

<text></text>

### -output-buffer-length

<text></text>

### -in-out-buffer

<text></text>

### -inout-buffer-length

<text></text>

### -status-block
I/O Status block
<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff542894">Creating IOCTL Requests in Drivers</a>
</dt>
<dt>
<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendinternalioctlotherssynchronously.md">WdfIoTargetSendInternalIoctlOthersSynchronously</a>
</dt>
<dt>
<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendinternalioctlsynchronously.md">WdfIoTargetSendInternalIoctlSynchronously</a>
</dt>
<dt>
<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendioctlsynchronously.md">WdfIoTargetSendIoctlSynchronously</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IOCTL_SYSENV_SET_VARIABLE control code%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

