---
UID: NE:ks.KS_SEEKING_CAPABILITIES
title: KS_SEEKING_CAPABILITIES
author: windows-driver-content
description: .
old-location: stream\ks_seeking_capabilities.htm
old-project: stream
ms.assetid: 345ADD1F-2002-4F9C-942C-212CADCF84E5
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: KS_SEEKING_CAPABILITIES, KS_SEEKING_CAPABILITIES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ks.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KS_SEEKING_CAPABILITIES
req.alt-loc: Ks.h
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
req.typenames: KS_SEEKING_CAPABILITIES
---

# KS_SEEKING_CAPABILITIES enumeration



## -description




## -syntax

````
typedef enum  { 
  KS_SEEKING_CanSeekAbsolute   = 0x1,
  KS_SEEKING_CanSeekForwards   = 0x2,
  KS_SEEKING_CanSeekBackwards  = 0x4,
  KS_SEEKING_CanGetCurrentPos  = 0x8,
  KS_SEEKING_CanGetStopPos     = 0x10,
  KS_SEEKING_CanGetDuration    = 0x20,
  KS_SEEKING_CanPlayBackwards  = 0x40
} KS_SEEKING_CAPABILITIES;
````


## -enum-fields

### -field KS_SEEKING_CanSeekAbsolute


### -field KS_SEEKING_CanSeekForwards


### -field KS_SEEKING_CanSeekBackwards


### -field KS_SEEKING_CanGetCurrentPos


### -field KS_SEEKING_CanGetStopPos


### -field KS_SEEKING_CanGetDuration


### -field KS_SEEKING_CanPlayBackwards


## -remarks
