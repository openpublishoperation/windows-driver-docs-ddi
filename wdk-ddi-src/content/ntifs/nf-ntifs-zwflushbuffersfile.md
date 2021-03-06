---
UID: NF:ntifs.ZwFlushBuffersFile
title: ZwFlushBuffersFile function
author: windows-driver-content
description: The ZwFlushBuffersFile routine is called by a file system filter driver to send a flush request for the specified file to the file system.
old-location: kernel\zwflushbuffersfile.htm
old-project: kernel
ms.assetid: b6ac1458-775d-4f73-86a1-30bfbf2256cc
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: ZwFlushBuffersFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: ZwFlushBuffersFile,NtFlushBuffersFile
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL (see Remarks section)
req.typenames: TOKEN_TYPE
---

# ZwFlushBuffersFile function



## -description
The <b>ZwFlushBuffersFile</b> routine is called by a file system filter driver to send a flush request for the specified file to the file system.



## -syntax

````
NTSTATUS ZwFlushBuffersFile(
  _In_  HANDLE           FileHandle,
  _Out_ PIO_STATUS_BLOCK IoStatusBlock
);
````


## -parameters

### -param FileHandle [in]

Handle returned by <a href="..\wdm\nf-wdm-zwcreatefile.md">ZwCreateFile</a> or <a href="..\wdm\nf-wdm-zwopenfile.md">ZwOpenFile</a> for the file whose buffers will be flushed. This parameter is required and cannot be <b>NULL</b>.


### -param IoStatusBlock [out]

Address of the caller's I/O status block. This parameter is required and cannot be <b>NULL</b>.


## -returns
<b>ZwFlushBuffersFile</b> returns STATUS_SUCCESS or an appropriate NTSTATUS value, such as one of the following:
<dl>
<dt><b>STATUS_MEDIA_WRITE_PROTECTED</b></dt>
</dl>The file resides on a write-protected volume; this is an error code.
<dl>
<dt><b>STATUS_VOLUME_DISMOUNTED</b></dt>
</dl>The file resides on a volume that is not currently mounted; this is an error code.

 


## -remarks
A file system filter driver can call <b>ZwFlushBuffersFile</b> to issue an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549235">IRP_MJ_FLUSH_BUFFERS</a> request to the file system for a given file. The flush operation is synchronous.

Minifilter drivers should call <a href="..\fltkernel\nf-fltkernel-fltflushbuffers.md">FltFlushBuffers</a> instead of calling <b>ZwFlushBuffersFile</b>. 

Callers of <b>ZwFlushBuffersFile</b> must be running at IRQL = PASSIVE_LEVEL and <a href="https://msdn.microsoft.com/0578df31-1467-4bad-ba62-081d61278deb">with special kernel APCs enabled</a>.

For calls from kernel-mode drivers, the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a Windows Native System Services routine can behave differently in the way that they handle and interpret input parameters. For more information about the relationship between the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a routine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>.


## -see-also
<dl>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltflushbuffers.md">FltFlushBuffers</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549235">IRP_MJ_FLUSH_BUFFERS</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwcreatefile.md">ZwCreateFile</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwopenfile.md">ZwOpenFile</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ZwFlushBuffersFile routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

