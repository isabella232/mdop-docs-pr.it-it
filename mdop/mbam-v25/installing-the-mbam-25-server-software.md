---
title: Installazione del software per il server di MBAM 2.5
description: Installazione del software per il server di MBAM 2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823395"
---
# Installazione del software per il server di MBAM 2.5


Questo argomento descrive come installare il software per server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 usando la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker o usando i parametri della riga di comando. Ripetere il processo di installazione del server per ogni server in cui si stanno configurando le caratteristiche del server MBAM 2,5. Dopo aver completato l'installazione, vedere [configurazione delle funzionalità del server MBAM 2,5](configuring-the-mbam-25-server-features.md) per la procedura relativa alla configurazione delle funzionalità del server.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prima di iniziare</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Esaminare le informazioni sulla pianificazione di MBAM 2,5</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architettura di alto livello per MBAM 2.5</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Informazioni su come recuperare i file di log</p></td>
<td align="left"><p>Per impostazione predefinita, i file di log vengono creati nella cartella% Temp% del computer locale. Per scrivere i file di log in una posizione specifica anziché nella <strong> cartella% Temp </strong> %, usare l' <strong> </strong> &lt; <em> argomento posizione/log </em> &gt; .</p>
<p>Altri eventi potrebbero essere registrati nel Visualizzatore eventi nei <strong> nodi di mbam-setup </strong> o <strong> mbam-Web in </strong> <strong> applicazioni e servizi per i registri di &gt; Microsoft &gt; Windows </strong> . Ad esempio, se si disinstalla MBAM, il programma di disinstallazione disinstallerà anche MBAM-Setup e MBAM-web logs in EventViewer.</p></td>
</tr>
</tbody>
</table>

 

## Installazione del software MBAM 2,5 Server tramite la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker


Seguire questa procedura per installare il software MBAM server usando la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

**Per installare il software del server MBAM 2,5 tramite la procedura guidata**

1.  Nel server in cui si vuole installare MBAM eseguire **MBAMserversetup.exe** per avviare la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

2.  Nella pagina di **benvenuto** fare clic su **Avanti**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Scegliere se usare Microsoft Update quando si controllano gli aggiornamenti e quindi fare clic su **Avanti**.

5.  Scegliere se partecipare al programma Analisi utilizzo software e quindi fare clic su **Avanti**.

6.  Per avviare l'installazione, fare clic su **Installa**.

7.  Per configurare le caratteristiche del server dopo l'installazione del software MBAM server, selezionare la casella di controllo **Esegui la configurazione del server mbam dopo la chiusura della procedura guidata** . In alternativa, è possibile configurare MBAM in seguito usando il collegamento di **configurazione del server mbam** creato dall'installazione del server nel menu **Start** .

8.  Fai clic su **Fine**.

## Installazione del software del server MBAM 2,5 tramite una finestra del prompt dei comandi


Al prompt dei comandi digitare un comando simile al comando seguente per installare il software del server MBAM.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

La tabella seguente descrive i parametri della riga di comando per l'installazione del software del server MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Valore di parametro</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>True false</p></td>
<td align="left"><p>Vero-partecipare al programma di Customer Improvement Experience, che consente a Microsoft di identificare quali funzionalità di MBAM migliorare.</p>
<p>Falso: non partecipare al programma esperienza di miglioramento del cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>True false</p></td>
<td align="left"><p>True: usare Microsoft Update per proteggere il computer e aggiornarlo per Windows e altri prodotti Microsoft, tra cui MBAM.</p>
<p>Falso: non usare Microsoft Update</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Percorso&gt;</p></td>
<td align="left"><p>Posizione in cui si vuole installare MBAM.</p>
<p>Esempio:</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>True false</p></td>
<td align="left"><p>Vero-continuare la procedura di disinstallazione di MBAM, anche se le caratteristiche non vengono rimosse.</p>
<p>False (impostazione predefinita) se l'azione di disinstallazione personalizzata non riesce a rimuovere una caratteristica aggiunta di MBAM server, la disinstallazione non riesce e MBAM rimane installato.</p>
<p>In entrambi i casi, tutte le funzionalità che sono state rimosse correttamente durante il tentativo di disinstallare MBAM rimangono rimosse.</p></td>
</tr>
</tbody>
</table>

 



## Argomenti correlati


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)

[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





