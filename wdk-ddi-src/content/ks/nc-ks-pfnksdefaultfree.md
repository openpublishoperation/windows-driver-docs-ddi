---
UID: NC:ks.PFNKSDEFAULTFREE
title: PFNKSDEFAULTFREE
author: windows-driver-content
description: An AVStream minidriver's AVStrMiniAllocatorFreeFrame routine frees the specified frame.
old-location: stream\avstrminiallocatorfreeframe.htm
old-project: stream
ms.assetid: ac8dd796-bc14-4b63-a0cb-5200cc1f0ce2
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: NpdBrokerUninitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ks.h
req.include-header: Ks.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows XP and later operating systems and DirectX 8.0 and later DirectX versions.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: AVStrMiniAllocatorFreeFrame
req.alt-loc: ks.h
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
req.typenames: KEYWORDSELECTOR
---

# PFNKSDEFAULTFREE callback



## -description
An AVStream minidriver's <i>AVStrMiniAllocatorFreeFrame</i> routine frees the specified frame.



## -prototype

````
PFNKSDEFAULTFREE AVStrMiniAllocatorFreeFrame;

VOID AVStrMiniAllocatorFreeFrame(
  _In_ PVOID Context,
  _In_ PVOID Buffer
)
{ ... }
````


## -parameters

### -param Context [in]

Pointer to the allocator's context structure created in <a href="..\ks\nc-ks-pfnkspininitializeallocator.md">AVStrMiniInitializeAllocator</a>.


### -param Buffer [in]

Pointer to the frame to be freed.


## -returns
None


## -remarks
The minidriver specifies this routine's address in the <b>Free</b> member of its <a href="..\ks\ns-ks-_ksallocator_dispatch.md">KSALLOCATOR_DISPATCH</a> structure. The minidriver passes this structure to the class driver in <a href="..\ks\ns-ks-_kspin_dispatch.md">KSPIN_DISPATCH</a>.

AVStream calls <i>AVStrMiniFree</i> to free a frame, passing as parameters the context structure set in the initialization dispatch and a pointer to the frame to free.

For more information, see <a href="https://msdn.microsoft.com/07812703-a66f-450a-b28e-4cf765267c4a">KS Allocators</a>.


## -see-also
<dl>
<dt>
<a href="..\ks\nc-ks-pfnkspininitializeallocator.md">AVStrMiniInitializeAllocator</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksallocator_dispatch.md">KSALLOCATOR_DISPATCH</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20PFNKSDEFAULTFREE routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

