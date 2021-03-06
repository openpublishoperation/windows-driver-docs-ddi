---
UID: NF:dbgeng.IDebugSymbols3.GetOffsetByLineWide
title: IDebugSymbols3::GetOffsetByLineWide method
author: windows-driver-content
description: The GetOffsetByLineWide method returns the location of the instruction that corresponds to a specified line in the source code.
old-location: debugger\getoffsetbylinewide.htm
old-project: debugger
ms.assetid: ba09333e-84a5-4166-a859-e09c0cf74347
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: IDebugSymbols3, IDebugSymbols3::GetOffsetByLineWide, GetOffsetByLineWide
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IDebugSymbols3.GetOffsetByLineWide
req.alt-loc: dbgeng.h
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
req.typenames: *PDOT4_ACTIVITY, DOT4_ACTIVITY
---

# IDebugSymbols3::GetOffsetByLineWide method



## -description
The <b>GetOffsetByLineWide</b>  method returns the location of the instruction that corresponds to a specified line in the source code.



## -syntax

````
HRESULT GetOffsetByLineWide(
  [in]  ULONG    Line,
  [in]  PCWSTR   File,
  [out] PULONG64 Offset
);
````


## -parameters

### -param Line [in]

Specifies the line number in the source file.


### -param File [in]

Specifies the file name of the source file.


### -param Offset [out]

Receives the location in the target's virtual address space of an instruction for the specified line.


## -returns
This method may also return other error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.
<dl>
<dt><b>S_OK</b></dt>
</dl>The method was successful.

 


## -remarks
A line in a source file might correspond to multiple instructions and this method can return any one of these instructions.

For more information about source files, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560141">Using Source Files</a>.


## -see-also
<dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546995">GetLineByOffset</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols3::GetOffsetByLineWide method%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

