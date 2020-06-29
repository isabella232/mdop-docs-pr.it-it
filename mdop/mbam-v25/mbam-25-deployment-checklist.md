---
title: Elenco di controllo per la distribuzione di MBAM 2.5
description: Elenco di controllo per la distribuzione di MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822835"
---
# Elenco di controllo per la distribuzione di MBAM 2.5


Puoi usare questo elenco di controllo per aiutarti durante la distribuzione di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker con una topologia autonoma.

**Nota**  
Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da considerare quando si distribuiscono le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker. È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Attività</th>
<th align="left">Riferimenti</th>
<th align="left">Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare e completare tutte le fasi di pianificazione per preparare l'ambiente per la distribuzione di MBAM.</p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)">Elenco di controllo per la pianificazione di MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare le informazioni sulle configurazioni supportate per verificare che MBAM supporti i computer client e server selezionati.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Installare il software del server MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Configurare le caratteristiche del server MBAM:</p>
<ul>
<li><p>Database di conformità e audit e database di ripristino</p></li>
<li><p>Rapporti</p></li>
<li><p>Applicazioni Web</p></li>
<li><p>Topologia di integrazione di Configuration Manager (necessaria solo se si esegue MBAM con questa topologia)</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Prendere nota dei nomi dei server in cui si configura ogni funzionalità. Userai queste informazioni durante il processo di configurazione.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)">Configurazione delle funzionalità server di MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Convalidare la configurazione di MBAM.</p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)">Convalida della configurazione delle funzionalità del server di MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Copiare il modello dei criteri di gruppo di MBAM e modificare le impostazioni dei criteri di gruppo.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copiando i modelli di criteri di gruppo di MBAM 2,5 </a> e <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> modificando le impostazioni dei criteri di gruppo di MBAM 2,5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Distribuire il software del client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)">Distribuzione del client di MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## Argomenti correlati


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)




## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




