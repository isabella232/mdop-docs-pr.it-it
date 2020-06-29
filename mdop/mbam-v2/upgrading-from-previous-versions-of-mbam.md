---
title: Aggiornamento da versioni precedenti di MBAM
description: Aggiornamento da versioni precedenti di MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823806"
---
# Aggiornamento da versioni precedenti di MBAM


È possibile aggiornare l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) a MBAM 2.0, con la topologia autonoma o di Configuration Manager, eseguendo le operazioni seguenti:

-   **Sostituzione del server sul posto manuale** -per aggiornare il server mbam, disinstallare manualmente mbam usando il programma di installazione o il pannello di controllo e quindi installare l'infrastruttura di MBAM 2.0. Non è necessario rimuovere i database. La disinstallazione del server MBAM 1,0 lascia intatti i database di MBAM. Se specifichi gli stessi database che MBAM 1,0 stava usando, l'installazione di MBAM 2.0 mantiene i dati di MBAM 1,0 nei database e converte i database in modo che funzionino con MBAM 2.0.

-   **Aggiornamento client distribuito** : se si usa la topologia di mbam autonoma, è possibile aggiornare gradualmente i client mbam dopo l'installazione dell'infrastruttura del Server MBAM 2,0. Il server MBAM 2,0 rileva la versione del client esistente ed esegue i passaggi necessari per eseguire l'aggiornamento al client 2,0.

    Dopo aver aggiornato l'infrastruttura server MBAM 2,0, i client MBAM 1,0 continuano a segnalare al server MBAM 2,0 con successo, i dati di recupero escrowing, ma la conformità sarà basata sui criteri in MBAM 1,0. È necessario aggiornare i client a MBAM 2,0 per avere i computer client con precisione segnalare la conformità con i criteri di MBAM 2,0. Puoi aggiornare i client al client MBAM 2,0 senza disinstallare il client precedente e il client inizierà a applicare i criteri di MBAM 2,0 e segnalarli.

    Se si usa MBAM con Configuration Manager, è necessario aggiornare i client di MBAM 1,0 a MBAM 2,0.

## Aggiornamento di MBAM da un'architettura a due server


Usare le istruzioni seguenti per eseguire l'aggiornamento da una versione precedente di MBAM quando si usa un'architettura a due server, in cui un server ospita i componenti di Microsoft SQL Server e l'altro server ospita i siti Web e i servizi.

**Per aggiornare MBAM da un'architettura a due server**

1.  Nel pannello di controllo del server con le caratteristiche di SQL Server selezionare **programmi e funzionalità**e quindi disinstallare l' **amministrazione e il monitoraggio di Microsoft BitLocker**. Il database di ripristino e il database di conformità e controllo restano invariati.

2.  Eseguire **MBAMSetup.exe** per la versione MBAM 2,0, facoltativamente selezionare il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** selezionare la topologia di integrazione **autonoma** o **System Center Configuration Manager** e quindi fare clic su **Avanti**.

5.  Nella pagina **selezionare le caratteristiche da installare** deselezionare le caratteristiche server **self-service** e **amministrazione e monitoraggio server** e quindi fare clic su **Avanti**.

6.  Attendere che i controlli dei prerequisiti finiscano e quindi fare clic su **Avanti**. Se viene rilevato un prerequisito mancante, risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.

7.  Nell' **account di fornitura usato per accedere alla pagina database mbam** , specificare il nome del computer per il server che ospiterà i siti e i servizi e quindi fare clic su **Avanti**.

8.  Nella pagina **Configura database di ripristino** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino. Devi anche specificare la posizione in cui verranno individuati i file di database e le informazioni di log.

9.  Fai clic su **Next** per continuare.

10. Nella pagina **Configura il database di conformità e controllo** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo.

11. Fai clic su **Next** per continuare.

12. Nella pagina **configurare i report di conformità e controllo** specificare l'istanza di SQL Server Reporting Services in cui verranno installati i report di conformità e controllo e specificare un account utente di dominio e una password per accedere al database di conformità e controllo. Configurare la password per l'account per non scadere mai. L'account utente può accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.

13. Fai clic su **Next** per continuare.

14. Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**. Ciò non consente di attivare gli aggiornamenti automatici in Windows. Se in precedenza si è scelto di usare Microsoft Update per questo prodotto o un altro prodotto, la pagina Microsoft Update non viene visualizzata.

15. Nella pagina **Riepilogo installazione** esaminare le caratteristiche che verranno installate e quindi fare clic su **Installa** per avviare l'installazione.

**Per disinstallare le funzionalità di amministrazione e monitoraggio del server e per completare l'aggiornamento**

1.  Nel computer che ospita le funzionalità di amministrazione e monitoraggio del server selezionare **programmi e funzionalità**nel pannello di controllo e quindi disinstallare mbam per rimuovere i siti e i servizi installati in precedenza.

2.  Eseguire la **MBAMSetup.exe** per la versione 2,0, facoltativamente selezionare il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** selezionare la topologia di integrazione **autonoma** o **System Center Configuration Manager** e quindi fare clic su **Avanti**.

5.  Nella pagina **selezionare le caratteristiche da installare** deselezionare le caratteristiche **del database di ripristino** e della **conformità e del database di controllo** e **conformità e controllo dei report** e quindi fare clic su **Avanti**.

6.  Attendere che i controlli dei prerequisiti finiscano e quindi fare clic su **Avanti**. Se viene rilevato un prerequisito mancante, risolvere prima di tutto i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.

7.  Nella pagina **Configura sicurezza comunicazioni di rete** scegliere se usare la crittografia SSL (Secure Socket Layer) per i siti Web e i servizi. Se si decide di crittografare la comunicazione, selezionare il certificato dell'autorità di certificazione (CA) da usare per la crittografia.

    **Nota**  Il certificato deve essere creato prima di questo passaggio per consentire di selezionarlo in questa pagina.

     

8.  Nella pagina **Configura il percorso della pagina database dello stato di conformità** specificare il nome dell'istanza di SQL Server e il nome del database in cui sono archiviati i dati di conformità e controllo. Devi anche specificare la posizione in cui verranno individuati i file di database e le informazioni di log.

9.  Fai clic su **Next** per continuare.

10. Nella pagina **Configura il percorso della pagina del database di ripristino** specificare il nome dell'istanza di SQL Server e il nome del database in cui sono archiviati i dati di ripristino.

11. Fai clic su **Next** per continuare.

12. Nella pagina **configurare i report di conformità e controllo** immettere l'URL dell'istanza di report configurata nell'altro server. Usare il pulsante **test** per verificare che sia possibile raggiungere il sito.

13. Fai clic su **Next** per continuare.

14. Nella pagina **Configura il portale self-service** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il portale self-service.

    **Nota**  Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.

     

15. Nella pagina **Configura il server di amministrazione e monitoraggio** specificare la directory virtuale desiderata per il sito Web dell'help desk.

16. Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**. Questo passaggio non consente di attivare gli aggiornamenti automatici in Windows. Se in precedenza si è scelto di usare Microsoft Update per questo prodotto o un altro prodotto, la pagina Microsoft Update non viene visualizzata.

17. Nella pagina **Riepilogo installazione** esaminare le caratteristiche che verranno installate e quindi fare clic su **Installa** per avviare l'installazione.

18. Per verificare che l'aggiornamento sia stato eseguito correttamente, verifica che sia possibile raggiungere ogni sito da un altro computer del dominio.

## Aggiornamento del client MBAM nei computer degli utenti finali


Per aggiornare i computer degli utenti finali al client MBAM 2,0, eseguire **MbamClientSetup.exe** su ogni computer client. Il programma di installazione aggiorna automaticamente il client al client MBAM 2,0. È possibile installare il client MBAM tramite un sistema di distribuzione elettronica del software, strumenti come servizi di dominio Active Directory o System Center Configuration Manager.

Per convalidare l'aggiornamento del client, eseguire le operazioni seguenti:

1.  Attendere il completamento del ciclo di Reporting configurato e quindi avviare **SQL Server Management Studio** nel computer SQL Server.

2.  Nel computer SQL Server avviare **SQL Server Management Studio**.

3.  Verificare che la tabella **RecoveryAndHardwareCore. Machines** contenga una riga che mostra il nome del computer dell'utente finale.

## Argomenti correlati


[Distribuzione di MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





