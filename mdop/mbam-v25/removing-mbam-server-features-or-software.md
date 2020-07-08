---
title: Rimozione di software o funzionalità del server di MBAM
description: Rimozione di software o funzionalità del server di MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824976"
---
# Rimozione di software o funzionalità del server di MBAM


Queste istruzioni spiegano come rimuovere software e funzionalità da Microsoft BitLocker Administration and Monitoring (MBAM). Se si rimuovono le caratteristiche del server MBAM, solo le caratteristiche configurate vengono rimosse dal server, non dal software server MBAM. Se si rimuove il software MBAM server, il software e tutte le funzionalità di MBAM Server configurate in tale server vengono rimosse.

**Nota**  Per evitare la rimozione accidentale dei dati, MBAM non fornisce alcun meccanismo per rimuovere i database; è necessario eseguire questa operazione manualmente.

 

## <a href="" id="bkmk-removeserverfeatures"></a>Rimozione delle caratteristiche del server MBAM


Puoi usare uno dei metodi seguenti per rimuovere le caratteristiche del server MBAM configurate:

-   Configurazione guidata server MBAM

-   Cmdlet di Windows PowerShell

### Uso della configurazione guidata di MBAM server per rimuovere le caratteristiche

Seguire queste istruzioni per usare la configurazione guidata di MBAM server per rimuovere le caratteristiche del server MBAM configurate da un server.

**Per rimuovere le caratteristiche di MBAM tramite la procedura guidata**

1.  Nel server in cui si vogliono rimuovere le caratteristiche selezionare la **configurazione di mbam server** per aprire la configurazione guidata.

2.  Fare clic su **Rimuovi funzionalità**, selezionare le caratteristiche da rimuovere e quindi fare clic su **Avanti**. Una pagina di **Riepilogo** Visualizza le caratteristiche selezionate per la rimozione.

3.  Fare clic su **Rimuovi** per iniziare a rimuovere le funzionalità e quindi fare clic su **Chiudi**.

### Uso di Windows PowerShell per rimuovere le caratteristiche

Usare i passaggi seguenti come guida generale per rimuovere le caratteristiche del server MBAM usando i cmdlet di Windows PowerShell.

**Per rimuovere le caratteristiche di MBAM tramite Windows PowerShell**

1.  Prima di rimuovere qualsiasi funzionalità, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.

2.  Usare i cmdlet seguenti per rimuovere le caratteristiche del server MBAM:

    -   Disable-MbamReport

    -   Disable-MbamWebApplication

    -   Disable-MbamCMIntegration

    Per ottenere assistenza per i cmdlet di Windows PowerShell, digitare **Get-Help** &lt; *cmdlet* &gt; oppure vedere la pagina [Microsoft Desktop Optimization Pack Automation con Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) per i cmdlet di Windows PowerShell di mbam.

## Rimozione del software del server MBAM


Usare la procedura seguente per rimuovere il software MBAM server e le funzionalità di MBAM Server configurate nel server.

**Per rimuovere il software del server MBAM**

1.  Nel server in cui si vuole disinstallare il software MBAM Server eseguire **MBAMserversetup.exe** per avviare la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

2.  Selezionare **Disinstalla**e seguire le istruzioni rimanenti per completare il processo di disinstallazione del software del server mbam.



## Argomenti correlati


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)

 

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



