---
UID: NF:wiamindr_lh.IWiaDrvItem.FindChildItemByName
title: IWiaDrvItem::FindChildItemByName method
author: windows-driver-content
description: The IWiaDrvItem::FindChildItemByName method searches the driver item tree for a specific child item.
old-location: image\iwiadrvitem_findchilditembyname.htm
old-project: image
ms.assetid: 04f446f2-cd59-4191-be0c-60140ecee3b2
ms.author: windowsdriverdev
ms.date: 1/17/2018
ms.keywords: IWiaDrvItem, IWiaDrvItem::FindChildItemByName, FindChildItemByName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IWiaDrvItem.FindChildItemByName
req.alt-loc: wiamindr_lh.h
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
req.typenames: *PSCANWINDOW, SCANWINDOW
req.product: Windows 10 or later.
---

# IWiaDrvItem::FindChildItemByName method



## -description
The <b>IWiaDrvItem::FindChildItemByName</b> method searches the driver item tree for a specific child item.



## -syntax

````
HRESULT FindChildItemByName(
  [in]            BSTR        bstrChildItemName,
  [out, optional] IWiaDrvItem **ppIChildItem
);
````


## -parameters

### -param bstrChildItemName [in]

Specifies a string containing the name with path information of the child item to find.


### -param ppIChildItem [out, optional]

Points to a memory location that will receive the address of the found <b>IWiaDrvItem</b> child item. 


## -returns
If the method succeeds, it stores a pointer to the found child item in <i>ppIChildItem</i> and returns S_OK. If the method fails to find the child item, it returns S_FALSE. If the method fails for another reason, it returns a standard COM error code.


## -remarks
Minidrivers typically use this method to search a driver item tree for a specific child item when the child item's name is known. The child item's full name is obtained in the  method <a href="https://msdn.microsoft.com/library/windows/hardware/ff543881">IWiaDrvItem::GetFullItemName</a>.


## -see-also
<dl>
<dt>
<a href="..\wiamindr_lh\nn-wiamindr_lh-iwiadrvitem.md">IWiaDrvItem</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543881">IWiaDrvItem::GetFullItemName</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543870">IWiaDrvItem::FindItemByName</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [image\image]:%20IWiaDrvItem::FindChildItemByName method%20 RELEASE:%20(1/17/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

