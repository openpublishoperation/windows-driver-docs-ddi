---
UID: NE:d3dkmthk._D3DKMT_TDRDBGCTRLTYPE
title: _D3DKMT_TDRDBGCTRLTYPE
author: windows-driver-content
description: The D3DKMT_TDRDBGCTRLTYPE enumeration type contains values that affect the behavior of the operating system's Timeout Detection and Recovery (TDR) process in a call to the OpenGL D3DKMTEscape function.
old-location: display\d3dkmt_tdrdbgctrltype.htm
old-project: display
ms.assetid: d3a6dfcc-e318-4fd0-85e0-5a0cc13fd00f
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _D3DKMT_TDRDBGCTRLTYPE, D3DKMT_TDRDBGCTRLTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: D3DKMT_TDRDBGCTRLTYPE
req.alt-loc: d3dkmthk.h
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
req.typenames: D3DKMT_TDRDBGCTRLTYPE
---

# _D3DKMT_TDRDBGCTRLTYPE enumeration



## -description
<b>Do not use the D3DKMT_TDRDBGCTRLTYPE enumeration; it is for testing purposes only.</b>

The <b>D3DKMT_TDRDBGCTRLTYPE</b> enumeration type contains values that affect the behavior of the operating system's Timeout Detection and Recovery (TDR) process in a call to the OpenGL <a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtescape.md">D3DKMTEscape</a> function.



## -syntax

````
typedef enum _D3DKMT_TDRDBGCTRLTYPE { 
  D3DKMT_TDRDBGCTRLTYPE_FORCETDR          = 0,
  D3DKMT_TDRDBGCTRLTYPE_DISABLEBREAK      = 1,
  D3DKMT_TDRDBGCTRLTYPE_ENABLEBREAK       = 2,
  D3DKMT_TDRDBGCTRLTYPE_UNCONDITIONAL     = 3,
  D3DKMT_TDRDBGCTRLTYPE_VSYNCTDR          = 4,
  D3DKMT_TDRDBGCTRLTYPE_GPUTDR            = 5,
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WIN8)
  D3DKMT_TDRDBGCTRLTYPE_FORCEDODTDR       = 6,
  D3DKMT_TDRDBGCTRLTYPE_FORCEDODVSYNCTDR  = 7,
  D3DKMT_TDRDBGCTRLTYPE_ENGINETDR         = 8

#endif } D3DKMT_TDRDBGCTRLTYPE;
````


## -enum-fields

### -field D3DKMT_TDRDBGCTRLTYPE_FORCETDR

Simulate a TDR.


### -field D3DKMT_TDRDBGCTRLTYPE_DISABLEBREAK

Disable DebugBreak on timeout.


### -field D3DKMT_TDRDBGCTRLTYPE_ENABLEBREAK

Enable DebugBreak on timeout.


### -field D3DKMT_TDRDBGCTRLTYPE_UNCONDITIONAL

Disables all safety conditions (e.g. check for consecutive recoveries).


### -field D3DKMT_TDRDBGCTRLTYPE_VSYNCTDR

Simulate a Vsync TDR.


### -field D3DKMT_TDRDBGCTRLTYPE_GPUTDR

Simulate a GPU TDR.


### -field D3DKMT_TDRDBGCTRLTYPE_FORCEDODTDR

Simulate a display-only present TDR.

Supported starting with Windows 8.


### -field D3DKMT_TDRDBGCTRLTYPE_FORCEDODVSYNCTDR

Simulate a display-only VSync TDR.

Supported starting with Windows 8.


### -field D3DKMT_TDRDBGCTRLTYPE_ENGINETDR

Simulate an engine TDR.

Supported starting with Windows 8.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_escape.md">D3DKMT_ESCAPE</a>
</dt>
<dt>
<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtescape.md">D3DKMTEscape</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMT_TDRDBGCTRLTYPE enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

