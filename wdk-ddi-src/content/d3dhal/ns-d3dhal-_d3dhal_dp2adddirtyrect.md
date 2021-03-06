---
UID: NS:d3dhal._D3DHAL_DP2ADDDIRTYRECT
title: _D3DHAL_DP2ADDDIRTYRECT
author: windows-driver-content
description: DirectX 8.1 and later versions only. D3DHAL_DP2ADDDIRTYRECT is used to specify that a portion of a 2D resource--a 2D texture or cube texture--was dirtied in system memory. Therefore, this 2D texture must be reloaded into video memory before being used.
old-location: display\d3dhal_dp2adddirtyrect.htm
old-project: display
ms.assetid: b3bddb3a-2a07-4ca8-8452-be20d983fe6f
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _D3DHAL_DP2ADDDIRTYRECT, D3DHAL_DP2ADDDIRTYRECT, *LPD3DHAL_DP2ADDDIRTYRECT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dhal.h
req.include-header: D3dhal.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: D3DHAL_DP2ADDDIRTYRECT
req.alt-loc: d3dhal.h
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
req.typenames: D3DHAL_DP2ADDDIRTYRECT
---

# _D3DHAL_DP2ADDDIRTYRECT structure



## -description

   DirectX 8.1 and later versions only.
   

D3DHAL_DP2ADDDIRTYRECT is used to specify that a portion of a 2D resource--a 2D texture or cube texture--was dirtied in system memory. Therefore, this 2D texture must be reloaded into video memory before being used. 



## -syntax

````
typedef struct _D3DHAL_DP2ADDDIRTYRECT {
  DWORD dwSurface;
  RECTL rDirtyArea;
} D3DHAL_DP2ADDDIRTYRECT, *LPD3DHAL_DP2ADDDIRTYRECT;
````


## -struct-fields

### -field dwSurface

Specifies the handle to the managed 2D resource that contains a dirtied 2D texture.


### -field rDirtyArea

Specifies the 2D texture that was marked as dirtied. This is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure.


## -remarks
D3DHAL_DP2ADDDIRTYRECT, along with the DP2OP_ADDDIRTYRECT token, is used only for driver managed resources and surfaces. D3DHAL_DP2ADDDIRTYRECT is never sent unless the driver indicates that it manages resources. To indicate that it manages resources, the driver must set the DDCAPS2_CANMANAGERESOURCE bit, in addition to the DDCAPS2_CANMANAGETEXTURE bit, in the <b>dwCaps2</b> member of a DDCORECAPS structure. The driver specifies this <a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a> structure in the <b>ddCaps</b> member of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551627">DD_HALINFO</a> structure when the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a> function is called to initialize the DirectDraw component of the driver.


## -see-also
<dl>
<dt>
<a href="..\d3dhal\ns-d3dhal-_d3dhal_dp2command.md">D3DHAL_DP2COMMAND</a>
</dt>
<dt>
<a href="..\d3dhal\ne-d3dhal-_d3dhal_dp2operation.md">D3DHAL_DP2OPERATION</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551627">DD_HALINFO</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DHAL_DP2ADDDIRTYRECT structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

