---
UID: NS:rilapitypes.RILTDSCDMAMRL
title: RILTDSCDMAMRL
author: windows-driver-content
description: This structure represents RILTDSCDMAMRL, which is a TD_SCDMA network measurement report.
old-location: netvista\riltdscdmamrl.htm
old-project: netvista
ms.assetid: 26399c62-c17a-40ad-964e-144badc55614
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RILTDSCDMAMRL, RILTDSCDMAMRL, *LPRILTDSCDMAMRL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rilapitypes.h
req.include-header: Rilapitypes.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RILTDSCDMAMRL
req.alt-loc: rilapitypes.h
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
req.typenames: RILTDSCDMAMRL, *LPRILTDSCDMAMRL
req.product: Windows 10 or later.
---

# RILTDSCDMAMRL structure



## -description

## -syntax

````
struct RILTDSCDMAMRL {
  DWORD dwParams;
  DWORD dwMobileCountryCode;
  DWORD dwMobileNetworkCode;
  DWORD dwLocationAreaCode;
  DWORD dwCellID;
  DWORD dwUARFCN;
  DWORD dwCellParameterID;
  DWORD dwRSCP;
  DWORD dwPathLoss;
};
````


## -struct-fields

### -field dwParams

A bitwise combination of <a href="..\rilapitypes\ne-rilapitypes-riltdscdmamrlparammask.md">RILTDSCDMAMRLPARAMMASK</a> that indicates which members of the structure contain valid data. A member of the structure is valid if the corresponding bit flag is set.


### -field dwMobileCountryCode

(Reserved for future use) Mobile country code (0...999).


### -field dwMobileNetworkCode

(Reserved for future use) Mobile Network Code (0...999).


### -field dwLocationAreaCode

(Reserved for future use) Location Area Code (0...65535).


### -field dwCellID

(Reserved for future use) Cell identity 28 bits (0...268435455). 


### -field dwUARFCN

Channel number (0...16383).


### -field dwCellParameterID

Cell parameter ID (0...127).


### -field dwRSCP

Received signal code power of serving cell. Range −128...−25 in units of 1dBm in Q8 L3 filtered.


### -field dwPathLoss

Path loss of serving cell (46...173)


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn946511">Cellular COM structures</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20RILTDSCDMAMRL structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

