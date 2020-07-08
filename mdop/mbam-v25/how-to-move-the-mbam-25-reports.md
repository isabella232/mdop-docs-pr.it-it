---
title: Come spostare i report di MBAM 2.5
description: Come spostare i report di MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804192"
---
# Come spostare i report di MBAM 2.5


Usare queste procedure per trasferire la caratteristica report da un computer a un altro, ovvero per trasferire la caratteristica report dal server a al server B.

I passaggi di alto livello per lo spostamento della caratteristica report sono i seguenti:

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.

2.  Installare il software MBAM 2,5 Server sul server B e configurare la caratteristica report nel server B.

3.  Aggiornare i dati di connessione dei report nei server di amministrazione e monitoraggio di MBAM.

4.  Riprendere l'istanza del sito Web di amministrazione e monitoraggio di MBAM.

**Nota**  Per eseguire gli script di Windows PowerShell di esempio in questo argomento, è necessario aggiornare i criteri di esecuzione di Windows PowerShell per consentire l'esecuzione di script. Per istruzioni, vedere [eseguire script di Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .

 

**Arrestare il sito Web di amministrazione e monitoraggio di MBAM**

-   Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di amministrazione e monitoraggio.

    Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B**

1.  Installare il software MBAM server sul server B. Per istruzioni, vedere [installazione del software server MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **report** .

    In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamReport** per configurare i report.

    Per istruzioni su come configurare i report, vedere [come configurare i report di MBAM 2,5](how-to-configure-the-mbam-25-reports.md).

**Aggiornare i dati di connessione dei report nel server di amministrazione e monitoraggio**

1.  Nel server in cui è in corso la caratteristica report utilizzare la console di gestione di Internet Information Services (IIS) per aggiornare l'URL dei report.

2.  Espandere **amministrazione e monitoraggio di Microsoft BitLocker**e quindi selezionare il nodo **helpdesk** .

3.  Nella sezione **gestione** della **visualizzazione funzionalità**selezionare **editor di configurazione**.

4.  Nel campo **sezione** selezionare **appSettings**.

5.  Selezionare la riga della **raccolta** e quindi fare clic sul pulsante "ellissi" **(...)** all'estrema destra del riquadro per aprire l' **Editor della raccolta**.

6.  Nell' **Editor della raccolta**seleziona la riga che contiene **Microsoft. mbam. Reports. URL**e aggiorna il valore per **Microsoft. mbam. Reports. URL** per riflettere il nome del server per il server B.

    Se la caratteristica report è stata precedentemente configurata in un'istanza denominata di SQL Server Reporting Services, aggiungere o aggiornare il nome dell'istanza all'URL, ad esempio:

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando nel server di amministrazione e monitoraggio simile all'esempio di codice seguente.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    Usando le descrizioni nella tabella seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$SERVERNAME $</p></td>
    <td align="left"><p>Nome del server a cui sono stati spostati i report.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>Nome dell'istanza di SQL Server Reporting Services a cui sono stati spostati i report.</p></td>
    </tr>
    </tbody>
    </table>

     

**Riprendere l'istanza del sito Web di amministrazione e monitoraggio**

1.  Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di amministrazione e monitoraggio.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **Nota**  Per eseguire questo comando, è necessario aggiungere il modulo IIS per Windows PowerShell all'istanza corrente di Windows PowerShell.

     



## Argomenti correlati


[Come configurare i report di MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Spostamento delle funzionalità di MBAM 2.5 a un altro server](moving-mbam-25-features-to-another-server.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





