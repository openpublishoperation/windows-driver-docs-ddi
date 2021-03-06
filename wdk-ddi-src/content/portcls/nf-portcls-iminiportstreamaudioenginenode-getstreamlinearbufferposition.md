---
UID: NF:portcls.IMiniportStreamAudioEngineNode.GetStreamLinearBufferPosition
title: IMiniportStreamAudioEngineNode::GetStreamLinearBufferPosition method
author: windows-driver-content
description: Gets the number of bytes that the DMA has fetched from the audio buffer since the beginning of the stream.
old-location: audio\iminiportstreamaudioenginenode_getstreamlinearbufferposition.htm
old-project: audio
ms.assetid: C1C91ECE-7AFF-468B-84AE-9D289EECE1E1
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IMiniportStreamAudioEngineNode, IMiniportStreamAudioEngineNode::GetStreamLinearBufferPosition, GetStreamLinearBufferPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portcls.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IMiniportStreamAudioEngineNode.GetStreamLinearBufferPosition
req.alt-loc: Portcls.h
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
req.typenames: PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IMiniportStreamAudioEngineNode::GetStreamLinearBufferPosition method



## -description
	Gets the number of bytes that the DMA has fetched from the audio buffer since the beginning of the stream.



## -syntax

````
NTSTATUS GetStreamLinearBufferPosition(
  [out] ULONGLONG *pullLinearBufferPosition
);
````


## -parameters

### -param pullLinearBufferPosition [out]

The number of bytes that the DMA has fetched.


## -returns
<b>GetStreamLinearBufferPosition</b> returns S_OK, if the call was successful. Otherwise, the method returns an appropriate error code.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\portcls\nn-portcls-iminiportstreamaudioenginenode.md">IMiniportStreamAudioEngineNode</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IMiniportStreamAudioEngineNode::GetStreamLinearBufferPosition method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

