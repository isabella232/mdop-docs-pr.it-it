---
title: Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti
description: Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817915"
---
# Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti


I criteri di pubblicazione di collegamento e di associazione dei tipi di file (FTA) sono definiti e controllati dal file XML di pubblicazione, che viene inviato ai client da un server di pubblicazione durante un'operazione di aggiornamento della pubblicazione. Quando il client riceve queste informazioni, aggiunge tutti i dati appena pubblicati relativi alle applicazioni, ad esempio le icone e accordi. Vengono quindi rimossi tutti i dati di pubblicazione obsoleti.

In App-V versione 4,6 sono stati definiti due valori della chiave del registro di sistema per consentire agli amministratori di controllare questo comportamento. Per impostazione predefinita, i tasti di scelta rapida creati localmente tramite la console client vengono ora mantenuti.

## Come modificare il collegamento e il comportamento FTA


Sono stati definiti due nuovi valori del registro di sistema DWORD per la chiave del registro di sistema client Configuration, "FileTypePolicy" e "ShortcutPolicy". Questi valori del registro di sistema DWORD non sono presenti per impostazione predefinita, ma possono essere aggiunti manualmente. La chiave del registro di configurazione si trova in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

Nella tabella seguente sono definiti quattro valori di criteri che si applicano a entrambi i valori della chiave del registro di sistema. L'elenco seguente mostra i valori numerici per le impostazioni del registro di sistema e il comportamento applicato ai tipi di file o ai tasti di scelta rapida in un'operazione di aggiornamento della pubblicazione.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nome</p></td>
<td align="left"><p>Tipo</p></td>
<td align="left"><p>Dati (esempi)</p></td>
<td align="left"><p>Descrizione</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileTypePolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0x2 (App-V 4,6)</p></td>
<td align="left"><p>(0x0)-"ClientOnly"-rimuovere eventuali elementi esistenti dalla stessa origine informazioni di pubblicazione e conservare solo gli elementi aggiunti localmente</p>
<p>(0x1)-"ServerOnly"-rimuove gli elementi obsoleti della stessa origine informazioni di pubblicazione e gli elementi aggiunti localmente e aggiunge i nuovi elementi</p>
<p>(0x2)-"ClientAndServer"-rimuovere gli elementi obsoleti dalla stessa origine informazioni di pubblicazione, conservare gli elementi aggiunti localmente e aggiungere i nuovi elementi (impostazione predefinita, se non presente per l'App-V 4,6)</p>
<p>(0x3)-"NoChange"-non apportare modifiche ai tipi di file o alle scelte rapide da tastiera</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ShortcutPolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0x2</p></td>
<td align="left"><p>(0x0)-"ClientOnly"-rimuovere eventuali elementi esistenti dalla stessa origine informazioni di pubblicazione e conservare solo gli elementi aggiunti localmente</p>
<p>(0x1)-"ServerOnly"-Rimuovi gli elementi obsoleti dalla stessa origine informazioni di pubblicazione e gli elementi aggiunti localmente e Aggiungi i nuovi elementi</p>
<p>(0x2)-"ClientAndServer"-rimuovere gli elementi obsoleti dalla stessa origine informazioni di pubblicazione, conservare gli elementi aggiunti localmente e aggiungere i nuovi elementi (impostazione predefinita, se non presente)</p>
<p>(0x3)-"NoChange"-non apportare modifiche ai tipi di file o alle scelte rapide da tastiera</p></td>
</tr>
</tbody>
</table>

 

**Nota**  I valori di testo fanno riferimento ai valori degli attributi XML nel file XML di pubblicazione.È possibile impostare questi valori manualmente se è stata implementata una soluzione di pubblicazione HTTP personalizzata.

 

 

 





