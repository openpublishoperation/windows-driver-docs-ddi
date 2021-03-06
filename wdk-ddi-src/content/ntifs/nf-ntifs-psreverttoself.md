---
UID: NF:ntifs.PsRevertToSelf
title: PsRevertToSelf function
author: windows-driver-content
description: The PsRevertToSelf routine ends the calling thread's impersonation of a client.
old-location: ifsk\psreverttoself.htm
old-project: ifsk
ms.assetid: 21ae3a61-55c6-437d-8c1e-84d720de9dd5
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: PsRevertToSelf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h, FltKernel.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows XP and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: PsRevertToSelf
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
req.typenames: TOKEN_TYPE
---

# PsRevertToSelf function



## -description
The <b>PsRevertToSelf</b> routine ends the calling thread's impersonation of a client.



## -syntax

````
VOID PsRevertToSelf(void);
````


## -parameters


## -returns
None

None

None


## -remarks
A server thread can impersonate a client by calling the <a href="..\ntifs\nf-ntifs-psimpersonateclient.md">PsImpersonateClient</a> routine. When the thread is done impersonating the client, it can call the <b>PsRevertToSelf</b> routine to end all impersonations.


## -see-also
<dl>
<dt>
<a href="..\ntifs\nf-ntifs-psimpersonateclient.md">PsImpersonateClient</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20PsRevertToSelf routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

