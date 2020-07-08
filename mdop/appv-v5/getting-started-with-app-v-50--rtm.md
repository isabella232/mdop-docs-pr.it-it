---
title: Attività iniziali di App-V 5.0
description: Attività iniziali di App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805812"
---
# Attività iniziali di App-V 5.0


App-V 5,0 consente agli amministratori di distribuire, aggiornare e supportare le applicazioni come servizi in tempo reale, in base alle esigenze. Le singole applicazioni vengono trasformate da prodotti installati localmente in servizi gestiti centralmente e sono disponibili ovunque sia necessario, senza dover preconfigurare i computer o modificare le impostazioni del sistema operativo.

App-V è costituito dagli elementi seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Management Server</p></td>
<td align="left"><ul>
<li><p>Fornisce una posizione centrale per la gestione dell'infrastruttura App-V, che offre applicazioni virtuali sia al client desktop di App-V che al client Servizi Desktop remoto (in precedenza Servizi terminal).</p></li>
<li><p>USA Microsoft SQL Server® per il proprio archivio dati, in cui uno o più server di gestione di App-V possono condividere un singolo archivio dati di SQL Server.</p></li>
<li><p>Autentica le richieste e fornisce la sicurezza, la misurazione, il monitoraggio e la raccolta dei dati. Il server usa Active Directory e strumenti di supporto per la gestione di utenti e applicazioni.</p></li>
<li><p>Dispone di un sito di gestione basato su Silverlight®, che consente di configurare l'infrastruttura App-V da qualsiasi computer. È possibile aggiungere e rimuovere applicazioni, modificare i tasti di scelta rapida, assegnare le autorizzazioni di accesso a utenti e gruppi e creare gruppi di connessioni.</p></li>
<li><p>Consente la comunicazione tra la console di gestione Web App-V e l'archivio dati di SQL Server. Questi componenti possono essere installati in un singolo computer server o in uno o più computer separati, a seconda dell'architettura di sistema necessaria.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Publishing Server</p></td>
<td align="left"><ul>
<li><p>Fornisce i client App-V con le applicazioni aventi diritto per l'utente specifico</p></li>
<li><p>Ospita il pacchetto di applicazione virtuale per lo streaming.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Client Desktop App-V</p></td>
<td align="left"><ul>
<li><p>Recupera le applicazioni virtuali</p></li>
<li><p>Pubblica le applicazioni nei client</p></li>
<li><p>Configura e gestisce automaticamente gli ambienti virtuali in fase di esecuzione sugli endpoint di Windows.</p></li>
<li><p>Archivia le impostazioni dell'applicazione virtuale specifiche dell'utente, ad esempio il registro di sistema e le modifiche ai file, in ogni profilo utente&#39;s.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Client Servizi Desktop remoto (RDS) App-V</p></td>
<td align="left"><p>Consente ai server Host sessione Desktop remoto di usare le funzionalità del client Desktop App-V per le sessioni desktop condivise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequencer App-V</p></td>
<td align="left"><ul>
<li><p>È uno strumento basato su una procedura guidata usato per trasformare le applicazioni tradizionali in applicazioni virtuali.</p></li>
<li><p>Genera l'applicazione "Package", che è costituita da:</p>
<ol>
<li><p>un file di applicazione sequenziata (APPV)</p></li>
<li><p>file di Windows Installer (MSI) che può essere distribuito ai client configurati per l'operazione autonoma</p></li>
<li><p>Diversi file XML, inclusi Report.XML, PackageName_DeploymentConfig.XML e PackageName_UserConfig.XML. I file XML UserConfig e DeploymentConfig vengono usati per configurare le modifiche personalizzate al comportamento predefinito del pacchetto.</p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

Per altre informazioni su questi elementi, Vedi [architettura ad alto livello per App-V 5,0](high-level-architecture-for-app-v-50.md).

Se si è nuovi a questo prodotto, è consigliabile leggere accuratamente la documentazione. Prima di distribuirla in un ambiente di produzione, è consigliabile convalidare il piano di distribuzione in un ambiente di rete di test. Potresti anche prendere in considerazione l'assunzione di una classe sulle tecnologie rilevanti. Per altre informazioni sulle opportunità di formazione per Microsoft, vedere Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**Nota**  Una versione scaricabile della Guida di questo amministratore non è disponibile. Tuttavia, è possibile ottenere informazioni su una modalità speciale della raccolta TechNet che consente di selezionare gli articoli, raggrupparli in una raccolta e stamparli o esportarli in un file in <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .

 

Questa sezione della Guida dell'amministratore di App-V 5,0 include informazioni di alto livello su App-V 5,0 per offrirti una conoscenza di base del prodotto prima di iniziare la pianificazione della distribuzione.

## Guida introduttiva a App-V 5,0


-   [Informazioni su App-V 5.0](about-app-v-50.md)

    Offre una panoramica di alto livello su App-V 5,0 e su come può essere usata nell'organizzazione.

-   [Informazioni su App-V 5.0 SP1](about-app-v-50-sp1.md)

    Offre una panoramica di alto livello su App-V 5.0 SP1 e su come può essere usata nell'organizzazione.

-   [Informazioni su App-V 5.0 SP2](about-app-v-50-sp2.md)

    Offre una panoramica di alto livello su App-V 5.0 SP2 e su come può essere usata nell'organizzazione.

-   [Informazioni su App-V 5.0 SP3](about-app-v-50-sp3.md)

    Offre una panoramica di alto livello su App-V 5.0 SP2 e su come può essere usata nell'organizzazione.

-   [Valutazione di App-V 5.0](evaluating-app-v-50.md)

    Fornisce informazioni su come valutare al meglio l'App V 5,0 per l'uso nell'organizzazione.

-   [Architettura di alto livello per App-V 5.0](high-level-architecture-for-app-v-50.md)

    Fornisce una descrizione delle caratteristiche dell'App-V 5,0 e della loro collaborazione.

-   [Accessibilità per App-V 5.0](accessibility-for-app-v-50.md)

    Fornisce informazioni sulle caratteristiche e i servizi che rendono questo prodotto e la relativa documentazione più accessibile per gli utenti con disabilità.

## <a href="" id="other-resources-for-this-product-"></a>Altre risorse per questo prodotto


-   [Guida dell'amministratore di Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Pianificazione di App-V 5.0](planning-for-app-v-50-rc.md)

-   [Distribuzione di App-V 5.0](deploying-app-v-50.md)

-   [Operazioni per App-V 5.0](operations-for-app-v-50.md)

-   [Risoluzione dei problemi relativi ad App-V 5.0](troubleshooting-app-v-50.md)






 

 





