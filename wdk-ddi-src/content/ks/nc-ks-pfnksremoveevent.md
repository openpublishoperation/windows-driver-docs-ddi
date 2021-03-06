---
UID: NC:ks.PFNKSREMOVEEVENT
title: PFNKSREMOVEEVENT
author: windows-driver-content
description: An AVStream minidriver's AVStrMiniRemoveEvent routine is called when a client requests to be removed from the notification queue for an event. This routine is optional.
old-location: stream\avstrminiremoveevent.htm
old-project: stream
ms.assetid: dee4ce19-9dc8-4728-855b-eadb5bca0fc2
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: NpdBrokerUninitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ks.h
req.include-header: Ks.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows XP and later operating systems and DirectX 8.0 and later DirectX versions.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: AVStrMiniRemoveEvent
req.alt-loc: ks.h
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
req.typenames: KEYWORDSELECTOR
---

# PFNKSREMOVEEVENT callback



## -description
An AVStream minidriver's <i>AVStrMiniRemoveEvent</i> routine is called when a client requests to be removed from the notification queue for an event. This routine is optional.



## -prototype

````
PFNKSREMOVEEVENT AVStrMiniRemoveEvent;

VOID AVStrMiniRemoveEvent(
  _In_ PFILE_OBJECT          FileObject,
  _In_ struct _KSEVENT_ENTRY *EventEntry
)
{ ... }
````


## -parameters

### -param FileObject [in]

Pointer to the file object for which to remove the event.


### -param EventEntry [in]

Pointer to an AVStream-generated <a href="..\ks\ns-ks-_ksevent_entry.md">KSEVENT_ENTRY</a> structure.


## -returns
<i>AVStrMiniRemoveEvent</i> must return STATUS_SUCCESS.


## -remarks
The minidriver specifies this routine's address in the <b>RemoveHandler</b> member of a <a href="..\ks\ns-ks-ksevent_item.md">KSEVENT_ITEM</a> structure. <a href="https://msdn.microsoft.com/7add2055-8d3f-432d-8aa1-44459ac197dd">Event Handling in AVStream</a> describes how the minidriver provides this structure to the class driver.

If the minidriver provides <i>AVStrMiniRemoveEvent</i> and either:

Does not specify an <b>AddHandler </b><i>or</i>

Specifies an <b>AddHandler</b> that calls <b>Ks</b><i>Xxx</i><b>AddEvent</b>

then the minidriver's <i>AVStrMiniRemoveEvent</i> must call <a href="..\wdm\nf-wdm-removeentrylist.md">RemoveEntryList</a> with a pointer to the LIST_ENTRY structure in the <a href="..\ks\ns-ks-_ksevent_entry.md">KSEVENT_ENTRY</a> structure:

Otherwise, your <i>AVStrMiniRemoveEvent</i> should reverse the steps taken in the <b>AddHandler</b>.


## -see-also
<dl>
<dt>
<a href="..\ks\ns-ks-kseventdata.md">KSEVENTDATA</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksevent_entry.md">KSEVENT_ENTRY</a>
</dt>
<dt>
<a href="..\ks\ns-ks-ksevent_item.md">KSEVENT_ITEM</a>
</dt>
<dt>
<a href="..\ks\ns-ks-ksautomation_table_.md">KSAUTOMATION_TABLE</a>
</dt>
<dt>
<a href="..\ks\nf-ks-ksfilteraddevent.md">KsFilterAddEvent</a>
</dt>
<dt>
<a href="..\ks\nf-ks-kspinaddevent.md">KsPinAddEvent</a>
</dt>
<dt>
<a href="..\ks\nf-ks-ksfiltergenerateevents.md">KsFilterGenerateEvents</a>
</dt>
<dt>
<a href="..\ks\nf-ks-kspingenerateevents.md">KsPinGenerateEvents</a>
</dt>
<dt>
<a href="..\ks\nc-ks-pfnksaddevent.md">AVStrMiniAddEvent</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20PFNKSREMOVEEVENT routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

