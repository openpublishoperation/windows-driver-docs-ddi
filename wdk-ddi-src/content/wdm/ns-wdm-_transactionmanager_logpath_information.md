---
UID: NS:wdm._TRANSACTIONMANAGER_LOGPATH_INFORMATION
title: _TRANSACTIONMANAGER_LOGPATH_INFORMATION
author: windows-driver-content
description: The TRANSACTIONMANAGER_LOGPATH_INFORMATION structure contains information about a transaction manager object.
old-location: kernel\transactionmanager_logpath_information.htm
old-project: kernel
ms.assetid: 53d7e8a9-fc89-4b11-8bbb-e9b5b0504f5e
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: _TRANSACTIONMANAGER_LOGPATH_INFORMATION, TRANSACTIONMANAGER_LOGPATH_INFORMATION, *PTRANSACTIONMANAGER_LOGPATH_INFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later operating system versions.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: TRANSACTIONMANAGER_LOGPATH_INFORMATION
req.alt-loc: Wdm.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL (see Remarks section)
req.typenames: TRANSACTIONMANAGER_LOGPATH_INFORMATION, *PTRANSACTIONMANAGER_LOGPATH_INFORMATION
req.product: Windows 10 or later.
---

# _TRANSACTIONMANAGER_LOGPATH_INFORMATION structure



## -description
The <b>TRANSACTIONMANAGER_LOGPATH_INFORMATION</b> structure contains information about a <a href="https://msdn.microsoft.com/af53cda4-e2ab-47df-9311-a4da2a2ee08d">transaction manager object</a>.



## -syntax

````
typedef struct _TRANSACTIONMANAGER_LOGPATH_INFORMATION {
  ULONG LogPathLength;
  WCHAR LogPath[1];
} TRANSACTIONMANAGER_LOGPATH_INFORMATION, *PTRANSACTIONMANAGER_LOGPATH_INFORMATION;
````


## -struct-fields

### -field LogPathLength

The number of elements in the <b>LogPath</b> member's character array.


### -field LogPath

A caller-allocated character array that receives the path and file name of the <a href="https://msdn.microsoft.com/d7ad0e16-d1f2-4c41-b647-95b5445c2708">log file stream</a> that is associated with a transaction manager.


## -remarks
The <b>TRANSACTIONMANAGER_LOGPATH_INFORMATION</b> structure is used with the <a href="..\wdm\nf-wdm-zwqueryinformationtransactionmanager.md">ZwQueryInformationTransactionManager</a> routine.


## -see-also
<dl>
<dt>
<a href="..\wdm\ne-wdm-_transactionmanager_information_class.md">TRANSACTIONMANAGER_INFORMATION_CLASS</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwqueryinformationtransactionmanager.md">ZwQueryInformationTransactionManager</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20TRANSACTIONMANAGER_LOGPATH_INFORMATION structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

