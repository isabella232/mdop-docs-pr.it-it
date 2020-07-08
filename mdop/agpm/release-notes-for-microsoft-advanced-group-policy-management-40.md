---
title: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0
description: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0
author: dansimp
ms.assetid: 44c19e61-c8e8-48aa-a2c2-20396d14d5bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c4a279893d4da4121e422af99e7c1708a0126b4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820395"
---
# Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0


Ottobre 2009

## Informazioni su Microsoft Advanced Group Policy Management 4,0


Gestione avanzata Criteri di gruppo di Microsoft (Advanced Group Policy Management) 4,0 estende le funzionalità di Group Policy Management Console (GPMC). Advanced Group Policy Management offre un controllo completo delle modifiche e una gestione migliorata degli oggetti Criteri di gruppo.

I documenti seguenti possono essere utili per iniziare a usare Advanced Group Policy Management 4,0.

-   Per una panoramica delle funzionalità di Advanced Group Policy Management, vedere [Panoramica della gestione dei criteri di gruppo avanzati di Microsoft](https://go.microsoft.com/fwlink/?LinkID=162671) ( https://go.microsoft.com/fwlink/?LinkID=162671) .

-   Per informazioni su come si differenzia Advanced Group Policy Management 4,0 da Advanced Group Policy Management 3,0, vedere [novità di Advanced Group Policy management 4,0](https://go.microsoft.com/fwlink/?LinkId=160058) ( https://go.microsoft.com/fwlink/?LinkId=160058) .

-   Per informazioni su come determinare se Advanced Group Policy 4,0 Management, Advanced Group Policy Management 3,0 o Advanced Group Policy Management 2,5 è appropriato per l'ambiente, vedere [scelta della versione di Advanced Group Policy Management da installare](https://go.microsoft.com/fwlink/?LinkId=145981) ( https://go.microsoft.com/fwlink/?LinkId=145981) .

-   Per istruzioni di base su come installare Advanced Group Policy Management e uno scenario di esempio per l'uso di Advanced Group Policy Manager, vedere [Guida dettagliata per Microsoft Advanced Group Policy managment 4,0](https://go.microsoft.com/fwlink/?LinkID=153505) ( https://go.microsoft.com/fwlink/?LinkID=153505) . Questa guida è progettata principalmente per aiutare gli analizzatori e gli utenti per la prima volta.

-   Per informazioni su come eseguire l'aggiornamento da una versione precedente di Advanced Group Policy Management o da indicazioni dettagliate su come pianificare la distribuzione di Advanced Group Management Manager nell'organizzazione, vedere la [Guida alla pianificazione di Microsoft Advanced criteri di gruppo 4,0](https://go.microsoft.com/fwlink/?LinkID=156883) ( https://go.microsoft.com/fwlink/?LinkID=156883) .

-   Per informazioni su come usare Advanced Group Policy Management per eseguire attività specifiche, vedere la Guida di gestione di criteri di gruppo avanzati di 4,0, disponibile anche in TechNet come [Guida operativa per Advanced Group Policy manager 4,0](https://go.microsoft.com/fwlink/?LinkId=159872) ( https://go.microsoft.com/fwlink/?LinkId=159872) .

## Altre informazioni


Per altre informazioni su Advanced Group Policy Management, vedere quanto segue:

-   [Raccolta TechNet di gestione criteri di gruppo avanzata](https://go.microsoft.com/fwlink/?LinkID=146846) (https://go.microsoft.com/fwlink/?LinkID=146846)

-   [Microsoft Desktop Optimization Pack TechCenter](https://go.microsoft.com/fwlink/?LinkId=159870) (https://www.microsoft.com/technet/mdop)

-   [Criteri di gruppo TechCenter](https://go.microsoft.com/fwlink/?LinkId=145531) (https://www.microsoft.com/gp)

## Commenti e suggerimenti


È possibile inviare commenti e suggerimenti su Advanced Group Policy Management al [Forum dei criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=145532) ( https://go.microsoft.com/fwlink/?LinkId=145532) .

## Problemi noti di Advanced Group Policy Management 4,0


### Il comando importa da produzione non importa le impostazioni in un oggetto Criteri di controllo Estratto

Se si modifica un GPO nell'ambiente di produzione, è necessario importare il GPO dalla produzione per aggiornare il GPO nell'archivio offline. Il comando **Importa da produzione** è progettato per consentire l'esecuzione di un backup finale della produzione prima di completare la modifica, in modo da poter eseguire il rollback al backup della produzione, se necessario.

Se l'oggetto Criteri di controllo è estratto quando si esegue il comando **Importa da produzione** , le modifiche alla produzione non vengono incorporate nella versione estratta dell'oggetto Criteri di controllo. La versione importata del GPO viene tuttavia aggiunta alla cronologia dell'oggetto Criteri di controllo, anche se tale versione non è disponibile per la modifica. Quando l'oggetto Criteri di controllo è archiviato, tale versione sostituirà la versione importata nell'archivio, ma entrambi sono disponibili nella cronologia del GPO.

**Soluzione alternativa:** Verificare che l'oggetto Criteri di controllo sia archiviato prima di importarlo dalla produzione. Se l'oggetto Criteri di controllo non è stato archiviato prima dell'importazione, è possibile usare il comando **Annulla estrazione** per annullare le modifiche e tornare alla versione dell'oggetto Criteri di ricerca importato dalla produzione.

### I GPO estratti non possono essere modificati per diversi minuti in un ambiente che usa una topologia di Active Directory di più siti

Advanced Group Policy Management usa un modello client/server. Il server Advanced Group Policy Management e il client Advanced Group Policy Management determinano il controller di dominio più vicino per le operazioni di criteri di gruppo. Quando si estrae un oggetto Criteri di ricerca con un client Advanced Group Policy Management, è in realtà il server Advanced Group Policy Management che controlla l'oggetto GPO dall'archivio offline in una cartella temporanea nella cartella SYSVOL.

Se il server Advanced Group Policy Management e il client Advanced Group Policy Management si trovano in siti diversi, l'oggetto GPO Estratto temporaneo potrebbe non essere presente nel controller di dominio del sito locale per diversi minuti o fino a 30 minuti a causa della latenza della replica SYSVOL. In questo caso, non è possibile modificare l'oggetto Criteri di controllo estratto tramite GPMC su un client Advanced Group Policy Management fino a quando non si è verificata la replica SYSVOL dell'oggetto Criteri di controllo Estratto.

**Soluzione alternativa:** Come procedura consigliata, è consigliabile posizionare i client Advanced Group Policy Management nello stesso sito del server Advanced Group Policy Management a cui si connettono in modo che non sia necessario attendere la replica di SYSVOL prima di poter modificare un oggetto Criteri di ricerca Estratto.

### Advanced Group Policy Management non è in grado di leggere il limite di backup se l'account non dispone delle autorizzazioni per l'archivio

In un client Advanced Group Policy Management, se si accede utilizzando un account che non è stato delegato alle autorizzazioni per l'Archivio Advanced Group Policy Manager, avviare la console Gestione criteri di gruppo e quindi fare clic su **Cambia controllo**, viene visualizzato il messaggio di errore seguente.

``` syntax
Failed to read backup purge limit for this domain. 

The following error occurred: 
You do not have sufficient permissions to perform this operation. 
Microsoft.Agpm.AccessDeniedException (80070005)
```

**Soluzione alternativa:** Contattare un amministratore Advanced Group Policy Management (controllo completo) e richiedere che deleghino l'accesso a Advanced Group Policy Management per il proprio account. Se si è un amministratore della Advanced Group Policy Management, accedere utilizzando un account a cui è assegnato il ruolo di amministratore Advanced Group Policy Management in modo da poter delegare l'accesso per l'account aggiuntivo. Per altre informazioni, vedere "delega dell'accesso a livello di dominio all'archivio" nella Guida di Advanced Group Policy Management.

## Informazioni sul copyright delle note sulla versione


Le informazioni contenute in questo documento, incluso l'URL e altri riferimenti a siti Web Internet, sono soggette a modifiche senza preavviso e vengono fornite solo a scopo informativo. L'intero rischio dell'uso o dei risultati dell'uso di questo documento rimane con l'utente e Microsoft Corporation non rilascia alcuna garanzia, espressa o implicita. Nell'esempio le aziende, le organizzazioni, i prodotti, gli utenti e gli eventi descritti in questo documento sono fittizi. Nessuna associazione con una società, un'organizzazione, un prodotto, una persona o un evento reale è intesa o deve essere dedotta. Rispettare tutte le leggi sul copyright applicabili è responsabilità dell'utente. Senza limitare i diritti in diritto d'autore, nessuna parte di questo documento può essere riprodotta, archiviata o introdotta in un sistema di recupero o trasmessa in qualsiasi forma o con qualsiasi mezzo (elettronica, meccanica, fotocopie, registrazione o altro) o per qualsiasi scopo, senza l'espressa autorizzazione scritta di Microsoft Corporation.

Microsoft può avere brevetti, applicazioni di brevetto, marchi, copyright o altri diritti di proprietà intellettuale che coprono argomenti in questo documento. Fatta eccezione per quanto espressamente specificato in un contratto di licenza scritta da Microsoft, l'arredamento di questo documento non offre alcuna licenza per questi brevetti, marchi, copyright o altre proprietà intellettuali.



Microsoft, MS-DOS, Windows, WindowsServer e Windows Vista sono marchi registrati o marchi di MicrosoftCorporation negli Stati Uniti e/o in altri paesi.

I nomi delle società e dei prodotti effettivamente menzionati nel presente documento possono essere i marchi dei rispettivi proprietari.

 

 





