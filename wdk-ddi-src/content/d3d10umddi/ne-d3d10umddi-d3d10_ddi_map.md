---
UID: NE:d3d10umddi.D3D10_DDI_MAP
title: D3D10_DDI_MAP
author: windows-driver-content
description: The D3D10_DDI_MAP enumeration type contains values that identify the access levels to map to a subresource in a call to the driver's ResourceMap function.
old-location: display\d3d10_ddi_map.htm
old-project: display
ms.assetid: f544ae60-b9c4-497c-8cb5-a2f9500a0cde
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: D3D10_DDI_MAP, D3D10_DDI_MAP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: D3D10_DDI_MAP
req.alt-loc: d3d10umddi.h
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
req.typenames: D3D10_DDI_MAP
---

# D3D10_DDI_MAP enumeration



## -description
The D3D10_DDI_MAP enumeration type contains values that identify the access levels to map to a subresource in a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_resourcemap.md">ResourceMap</a> function.



## -syntax

````
typedef enum D3D10_DDI_MAP { 
  D3D10_DDI_MAP_READ               = 1,
  D3D10_DDI_MAP_WRITE              = 2,
  D3D10_DDI_MAP_READWRITE          = 3,
  D3D10_DDI_MAP_WRITE_DISCARD      = 4,
  D3D10_DDI_MAP_WRITE_NOOVERWRITE  = 5
} D3D10_DDI_MAP;
````


## -enum-fields

### -field D3D10_DDI_MAP_READ

Read access is requested for the CPU to the subresource.


### -field D3D10_DDI_MAP_WRITE

Write access is requested for the CPU to the subresource.


### -field D3D10_DDI_MAP_READWRITE

Read and write access is requested for the CPU to the subresource.


### -field D3D10_DDI_MAP_WRITE_DISCARD

Write access is requested for the CPU to the subresource. However, the contents of the subresource become undefined during this operation because the requesting application might completely write over the entire region of memory. You can use this access level only with dynamic resources. 


### -field D3D10_DDI_MAP_WRITE_NOOVERWRITE

Write access is requested for the CPU to the subresource. However, the requesting application will not overwrite any data that was previously used by the GPU. You can use this access level only with dynamic vertex and index buffers. 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_resourcemap.md">ResourceMap</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3D10_DDI_MAP enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

