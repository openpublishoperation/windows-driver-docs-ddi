---
UID: NS:ntddrilapitypes.RILCALLVIDEOMEDIASTATE
title: RILCALLVIDEOMEDIASTATE
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcallvideomediastate.htm
old-project: netvista
ms.assetid: f40b9989-a911-4b89-a5a3-dda9a225b576
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RILCALLVIDEOMEDIASTATE, RILCALLVIDEOMEDIASTATE, *LPRILCALLVIDEOMEDIASTATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddrilapitypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RILCALLVIDEOMEDIASTATE
req.alt-loc: ntddrilapitypes.h
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
req.typenames: RILCALLVIDEOMEDIASTATE, *LPRILCALLVIDEOMEDIASTATE
---

# RILCALLVIDEOMEDIASTATE structure



## -description
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.



## -syntax

````
typedef struct _RILCALLVIDEOMEDIASTATE {
  DWORD                  dwParams;
  RILCALLMEDIADIRECTION  dwPeerCapabilities;
  DWORD                  dwFlags;
  DWORD                  dwContextID;
} RILCALLVIDEOMEDIASTATE, RILCALLVIDEOMEDIASTATE;
````


## -struct-fields

### -field dwParams


### -field dwPeerCapabilities


### -field dwFlags


### -field dwContextID


## -remarks
