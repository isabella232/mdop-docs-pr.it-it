---
title: Come installare e configurare il componente del server MED-V
description: Come installare e configurare il componente del server MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826976"
---
# Come installare e configurare il componente del server MED-V


Questa sezione spiega come [installare](#bkmk-howtoinstallthemedvserver) e [configurare](#bkmk-howtoconfigurethemedvserver) il server MED-V.

## <a href="" id="bkmk-howtoinstallthemedvserver"></a>Come installare il server MED-V


**Per installare il server MED-V**

1.  Installare il pacchetto server. msi MED-V.

    Il pacchetto MED-V Server. msi si chiama *MED-V\_Server\_x.msi*, dove x è il numero di versione.

    Ad esempio, *MED-V\_Server\_1.0.65.msi*.

2.  Quando viene visualizzata la schermata **iniziale della procedura guidata InstallShield** , fare clic su **Avanti**.

3.  Nella schermata **contratto di licenza** leggere il contratto di licenza, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.

    Verrà visualizzata la schermata **cartella di destinazione** con la cartella di installazione predefinita visualizzata.

    La cartella di installazione predefinita è *%SystemDrive%\\Program \\Programmi\\microsoft Enterprise Desktop Virtualization\\*.

    -   Per modificare la cartella in cui deve essere installato MED-V, fare clic su **Cambia** e selezionare una cartella esistente.

4.  Fai clic su **Avanti**.

5.  Nella schermata **pronto per l'installazione** fare clic su **Installa**.

    Viene avviata l'installazione del server MED-V. Questo può richiedere diversi minuti e la schermata potrebbe non visualizzare il testo. Durante l'installazione vengono visualizzate diverse schermate di stato. Se viene visualizzato un messaggio, seguire le istruzioni fornite.

6.  Quando viene visualizzata la schermata **completamento guidata InstallShield** , fare clic su **fine** per completare la procedura guidata.

**Nota**  
Se si sta installando il server MED-V tramite Desktop remoto Microsoft, usare la sintassi seguente: **mstsc/admin**. Verificare che la sessione RDP sia rivolta alla console.



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a>Come configurare il server MED-V


Le impostazioni del server seguenti possono essere configurate:

-   [Connessioni](#bkmk-configuringconnections)

-   [Immagini](#bkmk-configuringimages)

-   [Autorizzazioni](#bkmk-configuringpermissions)

-   [Rapporti](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a>Configurazione delle connessioni

**Per configurare le connessioni**

1.  Nel menu Start di Windows selezionare **tutti i programmi &gt; Med-v &gt; Med-v Server Configuration Manager**.

    **Nota**  
    Nota: se è stata selezionata la casella di controllo **Avvia Gestione configurazione server MED-v** durante l'installazione del server, la gestione configurazione di Med-v Server viene avviata automaticamente dopo il completamento dell'installazione del server.



~~~
The MED-V Server Configuration Manager appears.
~~~

2. Nella scheda **connessioni** configurare le impostazioni di connessione client seguenti:

   -   **Abilitare le connessioni non crittografate (http), tramite la porta**, selezionare questa casella di controllo per abilitare le connessioni non crittografate con una porta specificata. Nella casella porta immettere la porta del server in cui accettare connessioni non crittografate (http).

   -   **Abilitare le connessioni crittografate (HTTPS) tramite la porta**: selezionare questa casella di controllo per abilitare le connessioni crittografate con una porta specificata. Nella casella porta immettere la porta del server in cui accettare connessioni crittografate (HTTPS).

       HTTPS è una configurazione facoltativa che può essere impostata per garantire transazioni sicure tra il server MED-V e i client MED-V. Per configurare HTTPS, è necessario eseguire le procedure seguenti:

       -   Configurare un certificato nel server.

       -   Associa il certificato del server alla porta specificata usando netsh. Per informazioni, vedere le operazioni seguenti:

           -   [Comandi Netsh per HTTP (Hypertext Transfer Protocol)](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [Procedura: configurare una porta con un certificato SSL](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [Procedura: configurare una porta con un certificato SSL](https://msdn.microsoft.com/library/ms733791.aspx)

3. Fai clic su **OK**.

### <a href="" id="bkmk-configuringimages"></a>Configurazione di immagini

**Per configurare le immagini**

1.  Fare clic sulla scheda **Immagini** .

2.  Configurare le impostazioni di gestione delle immagini seguenti:

    -   **Directory VMS**: directory della macchina virtuale (directory in cui sono archiviate le immagini). Questo campo contiene un percorso UNC della directory delle immagini nel server di distribuzione delle immagini che dovrebbe essere accessibile dal server MED-V.

    -   **URL VMS**: la posizione del server in cui sono archiviate le immagini.

3.  Fai clic su **OK**.

### <a href="" id="bkmk-configuringpermissions"></a>Configurazione delle autorizzazioni

**Per configurare le autorizzazioni**

1.  Fare clic sulla scheda **autorizzazioni** .

2.  È disponibile un elenco di tutti gli utenti che possono eseguire l'accesso. Per applicare le autorizzazioni di lettura e scrittura a un utente, selezionare la casella di controllo accanto all'utente. Per applicare le autorizzazioni di sola lettura a un utente, deselezionare la casella di controllo.

3.  Per aggiungere utenti o gruppi di dominio, fare clic su **Aggiungi**.

    Verrà visualizzata la finestra di dialogo **Immetti nomi utente o di gruppo** .

    1.  Selezionare utenti o gruppi di dominio eseguendo una delle operazioni seguenti:

        -   Nel campo **Immetti nomi utente o gruppo** Digitare un utente o un gruppo esistente nel dominio oppure esistere come utente o gruppo locale nel computer. Quindi fare clic su **Controlla nomi** per risolverlo con il nome completo esistente.

        -   Fare clic su **trova** per aprire la finestra di dialogo standard **Seleziona utenti o gruppi** . Quindi Seleziona utenti o gruppi di dominio.

    2.  Fai clic su **OK**.

4.  Per rimuovere utenti o gruppi di dominio, selezionare un utente o un gruppo e fare clic su **Rimuovi**.

5.  Fai clic su **OK**.

### <a href="" id="bkmk-configuringreports"></a>Configurazione di report

**Per configurare i report**

1.  Fare clic sulla scheda **report** .

2.  Per supportare i report, selezionare **Abilita report**.

3.  Nella casella **stringa di connessione** immettere una stringa di connessione per il database MSSQL.

    -   Quando SQL Server è installato in un server remoto, usare la stringa di connessione seguente:

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **Nota**  
        Nota: per connettersi a SQL Express, usare: `Data Source=<ServerName>\sqlexpress.`



4.  Per creare il database, fare clic su **Crea database**.

5.  Per verificare la connessione, fare clic su **Test connessione**.

6.  Per configurare le opzioni di cancellazione del database, fare clic su **Cancella opzioni**.

    Verrà visualizzata la finestra di dialogo **Cancella Opzioni database** .

    1.  Scegliere una delle opzioni seguenti:

        -   **Cancellare i dati antecedenti**: cancellare tutti i dati antecedenti al numero di giorni specificato; nella casella numero immettere un numero di giorni.

        -   **Cancellare tutti i dati da database**: cancellare tutti i dati esistenti nel database.

        -   **Drop database**: eliminare il database.

    2.  Fare clic su **OK** per applicare le modifiche e chiudere la finestra di dialogo.

7.  Fare clic su **OK** per salvare le modifiche oppure su **Annulla** per chiudere la finestra di dialogo senza salvare le modifiche.

8.  Se richiesto, riavviare il servizio server MED-V per applicare le modifiche alle impostazioni di rete.

## Argomenti correlati


[Configurazioni supportate](supported-configurationsmedv-orientation.md)

[Progettare l'infrastruttura del server MED-V](design-the-med-v-server-infrastructure.md)









