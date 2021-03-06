---
UID: NF:wiamdef.wiasGetDrvItem
title: wiasGetDrvItem function
author: windows-driver-content
description: The wiasGetDrvItem function retrieves a driver item.
old-location: image\wiasgetdrvitem.htm
old-project: image
ms.assetid: c09924ef-cd2c-419c-81d5-bbd40b886767
ms.author: windowsdriverdev
ms.date: 1/17/2018
ms.keywords: wiasGetDrvItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: wiasGetDrvItem
req.alt-loc: Wiaservc.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.typenames: *PDEVICEDIALOGDATA2, *LPDEVICEDIALOGDATA2, DEVICEDIALOGDATA2
req.product: Windows 10 or later.
---

# wiasGetDrvItem function



## -description
The <b>wiasGetDrvItem </b>function retrieves a driver item.



## -syntax

````
HRESULT _stdcall wiasGetDrvItem(
  _In_  BYTE        *pWiasContext,
  _Out_ IWiaDrvItem **ppDrvItem
);
````


## -parameters

### -param pWiasContext [in]

Pointer to a WIA item context.


### -param ppDrvItem [out]

Pointer to a memory location that receives the address of an <a href="..\wiamindr_lh\nn-wiamindr_lh-iwiadrvitem.md">IWiaDrvItem Interface</a>.


## -returns
On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).


## -remarks


## -see-also
<dl>
<dt>
<a href="..\wiamdef\nf-wiamdef-wiasgetrootitem.md">wiasGetRootItem</a>
</dt>
<dt>
<a href="..\wiamdef\nf-wiamdef-wiascreatedrvitem.md">wiasCreateDrvItem</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [image\image]:%20wiasGetDrvItem function%20 RELEASE:%20(1/17/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

