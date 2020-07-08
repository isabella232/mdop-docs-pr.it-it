---
title: Informazioni sulla risoluzione dei problemi per Application Virtualization Client
description: Informazioni sulla risoluzione dei problemi per Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815195"
---
# Informazioni sulla risoluzione dei problemi per Application Virtualization Client


Questo argomento include le informazioni che è possibile usare per risolvere diversi problemi relativi al client Application Virtualization (App-V).

## L'aggiornamento della pubblicazione è molto lento


Se l'aggiornamento della pubblicazione in un computer specifico richiede molto più tempo del previsto e se il client è configurato per l'uso dell'impostazione **IconSourceRoot** , determinare se **IconSourceRoot** contiene un URL non valido. Un URL non valido causerà ritardi molto lunghi durante l'aggiornamento della pubblicazione.

## Gli utenti non possono connettersi al server e accedere alla modalità operazioni disconnesse


Quando usi un server di gestione App-V configurato con il protocollo RTSPs, se gli utenti non riescono a connettersi e entrano in modalità operativa disconnessa, determina se il certificato usato nel server è valido. Un certificato non valido impedirà agli utenti di connettersi e causerà la modalità operativa disconnessa.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>Gli utenti avvertono prestazioni lente quando le applicazioni non vengono completamente memorizzate nella cache


Quando le applicazioni non vengono completamente memorizzate nella cache, gli utenti potrebbero occasionalmente avere prestazioni temporanee lente o intermittenti quando avviano o usano l'applicazione. È possibile che si verifichino diversi motivi, ad esempio quando il client App-V è in fase di caricamento automatico di un'applicazione o quando viene elaborata una richiesta fuori sequenza. Quando le applicazioni vengono completamente memorizzate nella cache, questi problemi non si verificheranno più.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>Errore visualizzato dopo la rimozione di un aggiornamento


È necessario usare il formato di comando di Windows Installer 3,1 corretto per rimuovere un aggiornamento dal client App-V, come indicato di seguito:

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

L'uso del formato di comando precedente `msiexec /package <GUID> /uninstall <GUID>` causerà l'errore 6003 "Application Virtualization Client non è stato possibile avviare".

## Codice di errore 0A-0000E01E si verifica quando si tenta di avviare un'applicazione


Codice di errore 0A-0000E01E indica che il pacchetto dell'applicazione sequenziata potrebbe essere danneggiato. La soluzione consiste nel risequenziare il pacchetto.

## Gli utenti non possono accedere ai file creati nell'unità Q:


Se gli utenti salvano i file nell'unità **Q:** non possono recuperarli perché non hanno diritti di lettura per l'unità. Gli utenti non devono salvare i file nell'unità **Q:** .

## All'utente viene richiesto un errore 1D1


Quando l'URL del flusso di file non viene impostato correttamente nel file OSD (Open Software Descriptor), il client App-V restituisce un errore 1d1 anziché un errore "file non trovato". Questo errore indica che l'avvio dell'applicazione non è riuscito e che l'utente è stato costretto alla modalità operativa disconnessa. Correggere l'URL di flusso di file.

## Icone non corrette associate ad alcune applicazioni


Quando un'icona deve essere usata in un'operazione di pubblicazione, il client App-V determina prima di tutto se ha già una copia memorizzata nella cache dell'icona, cercando nella cache delle icone di un elemento il cui percorso di origine originale corrisponde al percorso dell'icona assegnato all'operazione di pubblicazione. Se il client App-V trova una corrispondenza, utilizzerà l'icona già memorizzata nella cache; in caso contrario, la nuova icona verrà scaricata nella cache. Se il percorso dell'icona è una directory di Scratch o se viene riutilizzata per nuove icone o pacchetti, la ricerca nella cache potrebbe selezionare l'icona sbagliata da un'operazione precedente.

## Quando si avvia un'applicazione agli utenti vengono richieste le credenziali


Se un utente tenta di avviare un'applicazione virtuale a cui l'amministratore di sistema ha accesso limitato, è possibile che venga chiesto di immettere le credenziali per l'utente. L'utente deve digitare il nome utente e la password per un account che disponga delle autorizzazioni per avviare l'applicazione e quindi premere INVIO.

## L'aggiornamento della pubblicazione non riesce dopo l'aggiornamento del client App-V alla versione 4,5


Se la directory dei dati utente è stata precedentemente inserita in una posizione non standard (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nomeutente*%), gli utenti che non hanno privilegi di amministratore nel computer troveranno che l'aggiornamento della pubblicazione non riesce dopo l'aggiornamento del client App-V. Durante l'aggiornamento, la directory di dati globali di App-V client e tutte le relative sottodirectory sono configurate con diritti di accesso limitato solo per gli amministratori. Per evitare questo problema, è possibile modificare la directory dei dati utente prima di eseguire l'aggiornamento in modo che non sia una sottodirectory della directory globale dei dati.

## Riavvio necessario dopo l'installazione non riuscita


Se l'installazione del client non riesce per qualsiasi motivo e se i successivi tentativi di installazione del client non riescono, controllare il log di Windows Installer per verificare se viene visualizzato un errore "sftplay non riuscito, errore = 1072". In questo caso, riavviare il computer prima di provare a installare di nuovo il client.

## Ripristino di un'applicazione virtuale danneggiata


Se per qualsiasi motivo un pacchetto di applicazione virtuale installato con un file di pacchetto di Windows Installer (MSI) viene danneggiato, reinstallare il pacchetto. La funzione di ripristino disponibile in Windows Installer non aggiornerà i volumi degli utenti.

## Argomenti correlati


[Riferimento per Application Virtualization Client](application-virtualization-client-reference.md)

 

 





