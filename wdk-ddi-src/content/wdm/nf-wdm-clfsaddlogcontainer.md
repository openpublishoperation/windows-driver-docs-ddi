---
UID: NF:wdm.ClfsAddLogContainer
title: ClfsAddLogContainer function
author: windows-driver-content
description: The ClfsAddLogContainer routine adds a container to a CLFS log.
old-location: kernel\clfsaddlogcontainer.htm
old-project: kernel
ms.assetid: 05ab9817-3f49-4ab5-b35d-1c89f5fe6e44
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: ClfsAddLogContainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Server 2003 R2, Windows Vista, and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: ClfsAddLogContainer
req.alt-loc: Clfs.sys,Ext-MS-Win-fs-clfs-l1-1-0.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfs.lib
req.dll: Clfs.sys
req.irql: <= APC_LEVEL
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# ClfsAddLogContainer function



## -description
The <b>ClfsAddLogContainer</b> routine adds a container to a CLFS log.



## -syntax

````
NTSTATUS ClfsAddLogContainer(
  _In_ PLOG_FILE_OBJECT plfoLog,
  _In_ PULONGLONG       pcbContainer,
  _In_ PUNICODE_STRING  puszContainerPath
);
````


## -parameters

### -param plfoLog [in]

A pointer to a <a href="..\wdm\ns-wdm-_file_object.md">LOG_FILE_OBJECT</a> structure that represents the log to which the container will be added. The caller previously obtained this pointer by calling <a href="..\wdm\nf-wdm-clfscreatelogfile.md">ClfsCreateLogFile</a>.


### -param pcbContainer [in]

A pointer to a ULONGLONG-typed variable. The role of this parameter depends on whether the log currently has at least one container.

<ul>
<li>
If the log currently has no containers, the caller supplies a positive integer that is the requested size, in bytes, of the new container. CLFS creates a container that is the requested size rounded up to a multiple of 512KB (for a dedicated log) or 1MB (for a multiplexed log).

</li>
<li>
If the log currently has at least one container and this parameter is the <b>NULL</b> pointer, CLFS creates a new container that is the same size as the existing containers. (All containers in a log must be the same size.)

</li>
<li>
If the log currently has at least one container and this parameter is a valid pointer, the caller supplies a positive integer that is the requested size, in bytes, of the new container. The requested size is rounded up to a multiple of 512KB (for a dedicated log) or 1MB (for a multiplexed log). If the rounded-up size is at least as large as the existing container size, CLFS creates a new container that is the same size as the existing containers. On successful return, this parameter receives the existing container size. If the rounded-up size is less than the existing container size, <b>ClfsAddLogContainer</b> fails.

</li>
</ul>

### -param puszContainerPath [in]

A pointer to a <a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structure that supplies the path name for the new container. The path can be absolute or relative to the location of the base log file. Paths that are relative to the base log file must begin with CLFS_CONTAINER_RELATIVE_PREFIX, which is the string literal (L"%BLF%\\").


## -returns
<b>ClfsAddLogContainer</b> returns STATUS_SUCCESS if it succeeds; otherwise, it returns one of the error codes defined in Ntstatus.h.


## -remarks
A container is a contiguous extent on stable storage. For example, a container could be a contiguous file on disk. A log is a set of containers along with a base log file. For more information about containers, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541862">CLFS Stable Storage</a>. 

A container specified by a path that is relative to the base log file must be in the same directory as the base log file or a subdirectory of the base log file. The directories "." and ".." are not allowed in a relative path.

A log can have some containers with absolute paths and other containers with relative paths.

Containers are created in a non-compressed mode and are initialized with zeros.

A log must have at least two containers before any I/O can be performed on it.

For an explanation of CLFS concepts and terminology, see <a href="https://msdn.microsoft.com/a9685648-b08c-48ca-b020-e683068f2ea2">Common Log File System</a>. 


## -see-also
<dl>
<dt>
<a href="..\wdm\nf-wdm-clfsremovelogcontainer.md">ClfsRemoveLogContainer</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-clfsaddlogcontainerset.md">ClfsAddLogContainerSet</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ClfsAddLogContainer routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

