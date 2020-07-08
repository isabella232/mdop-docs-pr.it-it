---
title: Informazioni sulla scheda Registro virtuale
description: Informazioni sulla scheda Registro virtuale
author: dansimp
ms.assetid: ca8d837f-8218-4f86-95fd-13a44dccd022
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 77decee4a8e07333b466db0a1bd0513efe859c9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819895"
---
# Informazioni sulla scheda Registro virtuale


Durante la sequenziazione viene creato un registro di sistema virtuale. Nella scheda **Registro di sistema virtuale** vengono visualizzate tutte le chiavi del registro di sistema e i valori necessari per l'esecuzione di un pacchetto di applicazione sequenziata. Usare questa scheda per aggiungere, modificare ed eliminare le chiavi del registro di sistema e i valori del registro di sistema.

È anche possibile scegliere di ignorare le chiavi del sistema di hosting selezionando **Sostituisci chiave locale**oppure è possibile creare una visualizzazione unita della chiave dall'ambiente virtuale selezionando **Unisci con chiave locale**.

Le modifiche apportate alla scheda **Impostazioni** del registro di sistema virtuale influiscono sulle applicazioni che fanno parte del pacchetto di applicazione sequenziata specifico, ma non influiscono sul funzionamento di altre applicazioni in streaming o installate localmente nel client Desktop Application Virtualization.

**Nota**  Prestare attenzione quando si modificano i valori e le chiavi del registro di sistema virtuali. La modifica di queste chiavi e valori potrebbe rendere inutilizzabile il pacchetto di applicazioni sequenziate.

 

Nel riquadro sinistro della scheda **Registro di sistema virtuale** viene visualizzato l'elenco completo dei registri virtuali creati durante la sequenziazione di un'applicazione.

## Colonne


<a href="" id="name"></a>**Nome**  
Nome per la voce nel registro di sistema virtuale.

<a href="" id="type"></a>**Tipo**  
Modalità di archiviazione dei dati da parte della voce.

<a href="" id="data"></a>**Dati**  
Valore archiviato dalla voce.

<a href="" id="attributes"></a>**Attributi**  
Visualizza gli attributi del file.

## Argomenti correlati


[Come modificare le informazioni sulla chiave del Registro di sistema virtuale](how-to-modify-virtual-registry-key-information.md)

[Console di Sequencer](sequencer-console.md)

 

 





