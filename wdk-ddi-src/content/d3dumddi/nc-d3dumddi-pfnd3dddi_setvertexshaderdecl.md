---
UID: NC:d3dumddi.PFND3DDDI_SETVERTEXSHADERDECL
title: PFND3DDDI_SETVERTEXSHADERDECL
author: windows-driver-content
description: The SetVertexShaderDecl function sets the vertex shader declaration so that all of the subsequent drawing operations use that declaration.
old-location: display\setvertexshaderdecl.htm
old-project: display
ms.assetid: 6387d632-78e2-4594-a58a-b11b2e831cc0
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _DXGK_PTE, DXGK_PTE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: SetVertexShaderDecl
req.alt-loc: d3dumddi.h
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
req.typenames: DXGK_PTE
---

# PFND3DDDI_SETVERTEXSHADERDECL callback



## -description
The <i>SetVertexShaderDecl</i> function sets the vertex shader declaration so that all of the subsequent drawing operations use that declaration.



## -prototype

````
PFND3DDDI_SETVERTEXSHADERDECL SetVertexShaderDecl;

__checkReturn HRESULT APIENTRY SetVertexShaderDecl(
  _In_ HANDLE hDevice,
  _In_ HANDLE hShaderHandle
)
{ ... }
````


## -parameters

### -param hDevice [in]

 A handle to the display device (graphics context).


### -param hShaderHandle [in]

 A handle to the vertex shader declaration object.


## -returns
<i>SetVertexShaderDecl</i> returns S_OK or an appropriate error result if the vertex shader declaration is not successfully set.


## -remarks
After setting the vertex shader declaration, all of the drawing operations use that declaration until another declaration is selected.


## -see-also
<dl>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicefuncs.md">D3DDDI_DEVICEFUNCS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DDDI_SETVERTEXSHADERDECL callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

