---
title: Considerazioni sulla sicurezza per DaRT 8.0
description: Considerazioni sulla sicurezza per DaRT 8.0
author: dansimp
ms.assetid: 45ef8164-fee7-41a1-9a36-de4e3264e7a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02d32d926c0def7d33bebd399cd380eed4e8385e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804420"
---
# Considerazioni sulla sicurezza per DaRT 8.0


Questo argomento contiene una breve panoramica sugli account e i gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0. Per altre informazioni, seguire i collegamenti contenuti in questo articolo.

## Considerazioni generali sulla sicurezza


**Comprendere i rischi per la sicurezza**. DaRT 8,0 include funzionalità che consentono a un amministratore o a un lavoratore dell'help desk di eseguire gli strumenti DaRT in remoto per risolvere i problemi di un computer dell'utente finale. È inoltre possibile salvare l'immagine ISO (International Organization for Standardizzation) in un'unità flash USB o inserire l'immagine ISO in una rete per includerne il contenuto come partizione di ripristino nel disco rigido di un computer. Queste funzionalità garantiscono flessibilità, ma creano anche potenziali rischi per la sicurezza da tenere in considerazione durante la configurazione di DaRT.

**Proteggere fisicamente i computer**. Quando gli amministratori e i dipendenti dell'help desk non sono fisicamente al computer, dovrebbero bloccare i computer e usare uno screen saver protetto.

**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**. Rimanere informati sui nuovi aggiornamenti per i sistemi operativi iscrivendoti al servizio di notifica della sicurezza <https://go.microsoft.com/fwlink/?LinkId=28819> .

## Limitare l'accesso degli utenti finali agli strumenti DaRT


Quando si crea l'immagine di ripristino delle freccette, è possibile selezionare gli strumenti da includere. Per motivi di sicurezza, potresti voler limitare l'accesso degli utenti finali agli strumenti DaRT più potenti, come la cancellazione del disco e il fabbro. In DaRT 8,0 puoi disabilitare alcuni strumenti durante la configurazione e renderli ancora disponibili per aiutare gli operatori del servizio di assistenza quando l'utente finale avvia la funzionalità di connessione remota.

È anche possibile configurare l'immagine del dardo in modo che l'opzione per avviare una sessione di connessione remota sia l'unico strumento disponibile per un utente finale.

**Importante**  Dopo aver stabilito la connessione remota, tutti gli strumenti inclusi nell'immagine di ripristino, inclusi quelli non disponibili per l'utente finale, saranno disponibili per qualsiasi lavoratore dell'help desk che sta lavorando al computer finale-utente.

 

Per altre informazioni su come includere gli strumenti nell'immagine di ripristino delle freccette, vedere [Panoramica degli strumenti in dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

## Proteggere l'immagine di ripristino delle freccette


Se si distribuisce l'immagine di ripristino delle freccette salvarla in un'unità flash USB o creando una partizione remota o una partizione di ripristino, è possibile includere il metodo preferito della società per la crittografia dell'unità nell'ISO. La crittografia dell'ISO consente di garantire che gli utenti finali non possano usare le funzionalità DaRT se dovessero avere accesso all'immagine di ripristino e assicura che gli utenti non autorizzati non possano avviare il dardo in computer appartenenti a un altro utente. Se si usa un metodo di crittografia, assicurarsi di distribuirlo e abilitarlo in tutti i computer.

**Nota**  DaRT 8,0 supporta BitLocker in modalità nativa.

 

Per includere la crittografia unità, aggiungere i file della soluzione di crittografia quando si crea l'immagine di ripristino. La soluzione di crittografia deve essere in grado di essere eseguita su WinPE. Gli utenti finali che si avviano dall'ISO possono accedere alla soluzione di crittografia e sbloccare l'unità.

## Mantenere la sicurezza tra due computer quando si usa la connessione remota


Per impostazione predefinita, la comunicazione tra due computer che hanno stabilito una sessione di **connessione remota** potrebbe non essere crittografata. Pertanto, per semplificare la sicurezza tra i due computer, è consigliabile che entrambi i computer facciano parte della stessa rete.

## Argomenti correlati


[Sicurezza e privacy per DaRT 8.0](security-and-privacy-for-dart-80-dart-8.md)

 

 





