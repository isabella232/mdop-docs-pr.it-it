---
title: Considerazioni sulla sicurezza per DaRT 7.0
description: Considerazioni sulla sicurezza per DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822735"
---
# Considerazioni sulla sicurezza per DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 include funzionalità che consentono a un amministratore di eseguire gli strumenti DaRT in remoto per risolvere i problemi di un computer dell'utente finale. Nelle versioni precedenti di DaRT, un tecnico o un amministratore dell'help desk dovevano essere fisicamente in un computer per gli utenti finali ed eseguire il boot in DaRT usando il CD o il DVD che includeva l'immagine di ripristino DaRT. A questo punto, il tecnico o l'amministratore dell'help desk può eseguire le stesse procedure in remoto.

Anche in DaRT7, oltre alla masterizzazione di un CD o DVD, è ora possibile salvare l'immagine ISO (International Organization for Standardizzation) in un'unità flash USB. È anche possibile inserire l'immagine ISO in una rete o includerne il contenuto come partizione di ripristino in un disco rigido del computer.

La caratteristica di **connessione remota** in DaRT7 consente agli utenti finali di accedere a Dart usando uno di questi nuovi metodi di distribuzione. Di conseguenza, possono avviare più facilmente le freccette e accedere agli strumenti DaRT.

Le nuove funzionalità di DaRT7 garantiscono molto più flessibilità nel modo in cui usi dardo nell'azienda. Tuttavia, crea anche il proprio set di problemi di sicurezza che devono essere affrontati. Quando si configura dardo, è consigliabile prendere in considerazione i seguenti suggerimenti per la sicurezza.

## Per mantenere la sicurezza quando si crea l'immagine di ripristino delle freccette


Quando si crea l'immagine di ripristino delle freccette, è possibile selezionare gli strumenti da includere. Per motivi di sicurezza, potresti voler limitare l'accesso degli utenti finali agli strumenti DaRT più potenti, come la cancellazione del disco e il fabbro. In DaRT7 è possibile disabilitare determinati strumenti durante la configurazione e renderli ancora disponibili per gli agenti dell'helpdesk quando l'utente finale avvia la funzionalità di connessione remota.

È anche possibile configurare l'immagine del dardo in modo che l'opzione per avviare una sessione di connessione remota sia l'unico strumento disponibile per un utente finale.

**Importante**  Dopo aver stabilito la connessione remota, tutti gli strumenti inclusi nell'immagine di ripristino, inclusi quelli non disponibili per l'utente finale, saranno disponibili per l'agente helpdesk che lavora al computer finale-utente.

 

Per altre informazioni su come includere gli strumenti nell'immagine di ripristino delle freccette, vedere [come usare la creazione guidata immagine di ripristino di freccette per creare l'immagine di ripristino](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).

## Per semplificare la sicurezza, crittografando l'immagine di ripristino delle freccette


Se si usa una delle opzioni di distribuzione nuove in DaRT7, ad esempio il salvataggio in un'unità flash USB o la creazione di una partizione remota o di una partizione di ripristino, è possibile includere il metodo preferito della società per la crittografia dell'unità nell'ISO. Ciò consentirà di verificare che un utente finale non possa usare la funzionalità di DaRT per ottenere l'accesso all'immagine di ripristino. E farà anche in modo che gli utenti non autorizzati non possano avviare il dardo in computer appartenenti a un altro utente.

Il metodo di crittografia deve essere distribuito e abilitato in tutti i computer.

**Nota**  DaRT7 supporta BitLocker nativamente.

 

## Per semplificare la sicurezza tra due computer durante la connessione remota


Per impostazione predefinita, la comunicazione tra due computer che hanno stabilito una sessione di **connessione remota** potrebbe non essere crittografata. Pertanto, per semplificare la sicurezza tra i due computer, è consigliabile che entrambi i computer facciano parte della stessa rete.

## Argomenti correlati


[Operazioni relative a DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





