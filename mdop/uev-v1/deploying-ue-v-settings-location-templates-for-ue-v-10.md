---
title: Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0
description: Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827125"
---
# Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0


Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate dalla virtualizzazione dell'esperienza utente. UE-V include un set di modelli standard, oltre a uno strumento, il generatore UE-V, che consente di creare modelli di posizione delle impostazioni personalizzate. Dopo aver creato un modello di posizione delle impostazioni, è consigliabile testarlo per verificare che le impostazioni dell'applicazione scorrano correttamente in un ambiente di test. Puoi quindi distribuire il modello di posizione delle impostazioni in modo sicuro ai computer dell'organizzazione.

I modelli di posizione delle impostazioni possono essere distribuiti tramite ESD (Enterprise Software Distribution), preferenze di criteri di gruppo o configurando un catalogo di modelli di impostazioni UE-V. I modelli distribuiti tramite ESD o criteri di gruppo devono essere registrati tramite WMI o PowerShell di UE-V. I modelli archiviati nella posizione del catalogo dei modelli di impostazioni vengono automaticamente registrati dall'agente UE-V.

## Distribuire i modelli di posizione delle impostazioni con un percorso catalogo di modelli di impostazioni


Il percorso del catalogo dei modelli della posizione delle impostazioni di UE-V può essere definito usando i metodi seguenti: criteri di gruppo, l'installazione dell'agente parametri della riga di comando, WMI o PowerShell. Dopo aver definito il percorso del catalogo dei modelli, l'agente UE-V recupera i modelli nuovi o aggiornati da questa posizione. L'agente UE-V controlla la posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli presenti nella cartella. I modelli che sono stati aggiunti o aggiornati in questa cartella dall'ultimo controllo vengono registrati dall'agente UE-V. L'agente UE-V annulla anche la registrazione dei modelli rimossi dalla cartella. I modelli sono registrati e non registrati una volta al giorno dall'utilità di pianificazione.

**Per usare il percorso del catalogo delle impostazioni per distribuire i modelli di posizione delle impostazioni di UE-V**

1.  Passare alla cartella della condivisione di rete definita come catalogo dei modelli di impostazioni.

2.  Aggiungere, rimuovere o aggiornare i modelli di posizione delle impostazioni nel catalogo dei modelli di impostazioni per riflettere la configurazione del modello di agente UE-V desiderata per i computer UE-V.

3.  I modelli nei computer vengono aggiornati giornalmente in base alle modifiche apportate al catalogo dei modelli di impostazioni.

4.  Aprire un prompt dei comandi con privilegi elevati e passare a **% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 o x64 &gt; **, quindi eseguire **ApplySettingsTemplateCatalog.exe** per aggiornare manualmente i modelli in un computer che esegue l'agente UE-V.

## Argomenti correlati


[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Distribuzione di UE-V 1.0](deploying-ue-v-10.md)

[Pianificazione delle applicazioni da sincronizzare con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





