---
UID: NF:rilapi.RIL_VerifyUiccLock
title: RIL_VerifyUiccLock function
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\ril_verifyuicclock.htm
old-project: netvista
ms.assetid: e32e4b7d-715b-4eae-832f-314980ab89b3
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RIL_VerifyUiccLock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rilapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RIL_VerifyUiccLock
req.alt-loc: rilapi.h
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
req.typenames: *PRH_QUERY_CONNECTION_PROPERTIES_OUTPUT_BUFFER, RH_QUERY_CONNECTION_PROPERTIES_OUTPUT_BUFFER
req.product: Windows 10 or later.
---

# RIL_VerifyUiccLock function



## -description
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 

            



## -syntax

````
HRESULT  RIL_VerifyUiccLock(
   HRIL                         hRil,
   LPVOID                       lpContext,
   const RILUICCLOCKCREDENTIAL  lpVerification
);
````


## -parameters

### -param hRil 


### -param lpContext 


### -param lpVerification 


## -returns
If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## -remarks
