---
title: Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager
description: Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804233"
---
# Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager


Questo argomento spiega come configurare l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) per usare la topologia di integrazione di System Center Configuration Manager, che si integra con MBAM con Configuration Manager.

Le istruzioni spiegano come configurare l'integrazione di Configuration Manager usando:

-   Cmdlet di Windows PowerShell

-   Configurazione guidata server MBAM

Le istruzioni si basano sull'architettura consigliata nell' [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Prima di iniziare la configurazione:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Dove ottenere le istruzioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Esaminare l'architettura consigliata per MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Esaminare le configurazioni supportate per MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Completare i prerequisiti necessari per ogni server.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installare il software MBAM server su ogni server in cui verrà configurata una caratteristica del server MBAM.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Per questa topologia, è necessario installare la console di Configuration Manager nel computer in cui si sta installando il software del server MBAM.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rivedere i prerequisiti di Windows PowerShell (applicabile solo se si intende usare i cmdlet di Windows PowerShell per configurare MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Per configurare l'integrazione di Configuration Manager con Windows PowerShell**

1.  Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.

2.  Usare il cmdlet **Enable-MbamCMIntegration** di Windows PowerShell per configurare i report. Per ottenere informazioni su questo cmdlet, digitare **Get-Help Enable-MbamCMIntegration**.

**Per configurare l'integrazione di System Center Configuration Manager tramite la procedura guidata**

1.  Nel server in cui si vuole configurare la funzionalità di integrazione di System Center Configuration Manager, avviare la configurazione guidata di MBAM server. È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.

2.  Fare clic su **Aggiungi nuove funzionalità**, selezionare **integrazione di System Center Configuration Manager**e quindi fare clic su **Avanti**.

    La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per l'integrazione di Configuration Manager.

3.  Se il controllo dei prerequisiti è riuscito, fare clic su **Avanti** per continuare. In caso contrario, risolvere i prerequisiti mancanti e quindi fare di **nuovo clic su Controlla prerequisiti**.

4.  Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Server di SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nome di dominio completo (FQDN) del server con il ruolo del punto di servizio Reporting. Questo è il server a cui sono distribuiti i report di MBAM Configuration Manager.</p>
    <p>Se non specifichi un server, i report di Configuration Manager verranno distribuiti nel server locale.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Istanza di SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nome dell'istanza di SQL Server Reporting Services (SSRS) in cui vengono distribuiti i report di Configuration Manager.</p>
    <p>Se non specifichi un'istanza, i report di Configuration Manager verranno distribuiti nel nome dell'istanza di SSRS predefinita. Il valore immesso viene ignorato se nel server è installato System Center 2012 Configuration Manager.</p></td>
    </tr>
    </tbody>
    </table>



5.  Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.

    **Nota**  
    Per creare uno script di Windows PowerShell delle voci appena apportate, fare clic su **Esporta script di PowerShell** e salvare lo script.



6.  Fare clic su **Aggiungi** per aggiungere la funzionalità di integrazione di Configuration Manager al server e quindi fare clic su **Chiudi**.



## Argomenti correlati


[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Convalida della configurazione delle funzionalità del server di MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






