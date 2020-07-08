---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795815"
---
# Microsoft User Experience Virtualization (UE-V) 2. x

>[!NOTE]
>Questa documentazione è una versione di UE-V inclusa nel Microsoft Desktop Optimization Pack (MDOP). Per informazioni sulla versione più recente di UE-V inclusa in Windows 10 Enterprise, vedere Introduzione a [UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Acquisire e centralizzare le impostazioni delle applicazioni degli utenti e le impostazioni del sistema operativo Windows implementando Microsoft User Experience Virtualization (UE-V) 2,0 o 2,1. Applica quindi queste impostazioni agli utenti di dispositivi che accedono all'organizzazione, come computer desktop, laptop o sessioni VDI (Virtual Desktop Infrastructure).

**Con UE-V puoi...**

-   Specificare le impostazioni di applicazione e desktop da sincronizzare

-   Recapitare in qualsiasi momento le impostazioni agli utenti, indipendentemente dalla posizione nell'azienda da cui gli utenti lavorano

-   Creare modelli personalizzati per le applicazioni di terze parti o line-of-business

-   Recuperare le impostazioni dopo la sostituzione o l'aggiornamento dell'hardware oppure dopo aver ricreato una macchina virtuale nello stato iniziale

## Componenti di UE-V 2. x


Questo diagramma mostra il modo in cui i componenti UE-V distribuiti collaborano per sincronizzare le impostazioni.

![diagramma architetturale uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">Funzione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Agente UE-V</strong></p></td>
<td align="left"><p>Installato in tutti i computer che devono sincronizzare le impostazioni, l' <strong> agente UE-V </strong> monitora le applicazioni registrate e il sistema operativo per tutte le modifiche delle impostazioni, quindi Sincronizza le impostazioni tra i computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Pacchetti di impostazioni</strong></p></td>
<td align="left"><p>Le impostazioni delle applicazioni e le impostazioni di Windows sono archiviate in <strong> pacchetti </strong> di impostazioni creati dall'agente UE-V. I pacchetti di impostazioni vengono creati, archiviati localmente e copiati nel percorso dell'archivio impostazioni.</p>
<ul>
<li><p>I valori delle impostazioni per le <strong> applicazioni desktop </strong> vengono archiviati quando l'utente chiude l'applicazione.</p></li>
<li><p>I valori per <strong> le impostazioni di Windows </strong> vengono archiviati quando l'utente si disconnette, quando il computer è bloccato o quando l'utente si disconnette in remoto da un computer.</p></li>
</ul>
<p>Il provider di sincronizzazione determina quando le impostazioni dell'applicazione o del sistema operativo vengono lette dai <strong> pacchetti di impostazioni </strong> e sincronizzate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Posizione di archiviazione delle impostazioni</strong></p></td>
<td align="left"><p>Si tratta di una condivisione di rete standard a cui gli utenti possono accedere. L'agente UE-V Verifica la posizione e crea una cartella di sistema nascosta in cui archiviare e recuperare le impostazioni dell'utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Modelli di posizione delle impostazioni</strong></p></td>
<td align="left"><p>UE-V usa i file XML come modelli di posizione delle impostazioni per monitorare e sincronizzare le impostazioni delle applicazioni desktop e le impostazioni desktop di Windows tra i computer degli utenti. Per impostazione predefinita, alcuni modelli di posizione delle impostazioni sono inclusi in UE-V. È anche possibile creare, modificare o convalidare i modelli di posizione delle impostazioni personalizzate <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> gestendo la sincronizzazione delle impostazioni per le applicazioni personalizzate </a> .</p>
<div class="alert">
<strong>Nota</strong><br/><p>I modelli di posizione delle impostazioni non sono necessari per le app di Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Elenco delle app di Windows</strong></p></td>
<td align="left"><p>Le impostazioni per le app di Windows vengono acquisite e applicate in modo dinamico. Lo sviluppatore dell'app specifica le impostazioni sincronizzate per ogni app. UE-V determina quali app di Windows sono abilitate per la sincronizzazione delle impostazioni usando un elenco gestito di app. Per impostazione predefinita, questo elenco include la maggior parte delle app di Windows.</p>
<p>Puoi aggiungere o rimuovere applicazioni nell'elenco delle app di Windows seguendo le procedure illustrate in <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> questo articolo </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>Gestione della sincronizzazione delle impostazioni per le applicazioni personalizzate

Usa questi componenti UE-V per creare e gestire modelli personalizzati per le applicazioni di terze parti o line-of-business.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Generatore di UE-V</strong></p></td>
<td align="left"><p>Usa il <strong> Generatore UE-V </strong> per creare modelli di posizione personalizzati che puoi quindi distribuire ai computer degli utenti. Il generatore UE-V consente inoltre di modificare un modello esistente o di convalidare un modello creato usando un altro editor XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Catalogo di modelli di impostazioni</strong></p></td>
<td align="left"><p>Il catalogo dei modelli di <strong> impostazioni </strong> è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati i modelli di posizione delle impostazioni personalizzate. L'agente UE-V controlla questa posizione una volta al giorno, recupera i modelli nuovi o aggiornati e aggiorna il comportamento della sincronizzazione.</p>
<p>Se si usano solo i modelli di posizione predefiniti UE-V, il catalogo di un modello di impostazioni non è necessario. Per altre informazioni sui cataloghi di distribuzione delle impostazioni, vedere <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurare un catalogo di modelli di impostazioni UE-V </a> .</p></td>
</tr>
</tbody>
</table>



![processo generatore di UE-v](images/ue-vgeneratorprocess.gif)

## Impostazioni sincronizzate per impostazione predefinita


Per impostazione predefinita, la pagina UE-V sincronizza le impostazioni per queste applicazioni. Per un elenco completo e informazioni più dettagliate, vedere [Impostazioni sincronizzate automaticamente in una distribuzione di UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Applicazioni di Microsoft Office 2013 (UE-V 2,1 SP1 e 2,1)

Applicazioni di Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 e 2,0)

Applicazioni di Microsoft Office 2007 (solo UE-V 2,0)

Internet Explorer 8, 9 e 10

Internet Explorer 11 in UE-V 2,1 SP1 e 2,1

Molte applicazioni Windows, ad esempio Xbox

Molte applicazioni desktop di Windows, ad esempio Blocco note

Molte impostazioni di Windows, ad esempio sfondo desktop o wallpaper

**Nota**  
È anche possibile [personalizzare l'opzione UE-V per sincronizzare le impostazioni](https://technet.microsoft.com/library/dn458942.aspx) per le applicazioni diverse da quelle sincronizzate per impostazione predefinita.



## Confrontare UE-V con altri prodotti Microsoft


Usare questa tabella per confrontare l'opzione UE-V per sincronizzare i profili in Windows 7, sincronizzare i profili in Windows 8 e la caratteristica Impostazioni PC di sincronizzazione dell'account Microsoft.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Funzionalità</th>
<th align="left">Sincronizzare i profili con Windows 7</th>
<th align="left">Sincronizzare i profili con Windows 8</th>
<th align="left">Sincronizzare i profili con Windows 10</th>
<th align="left">Account Microsoft</th>
<th align="left">UE-V 2,0</th>
<th align="left">UE-V 2,1 e 2,1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sincronizzare le impostazioni tra più computer</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizzare le impostazioni tra le app fisiche e virtuali</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizzare le impostazioni delle app di Windows</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestire tramite WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizzare le modifiche delle impostazioni su base regolare</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurazione minima per l'installazione</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Supportato in computer non appartenenti a un dominio</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Supporta l'attributo Primary computer Active Directory</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizza le impostazioni tra Virtual Desktop Infrastructure (VDI)/Remote Desktop Services (RDS) e desktop RTF</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Spazio di archiviazione illimitato per l'impostazione</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scelta delle impostazioni dell'app da sincronizzare</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backup/ripristino per professionisti IT</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Parziale</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## Note sulla versione di UE-V 2. x


Per altre informazioni e per le ultime notizie che non hanno reso disponibile la documentazione, vedere

-   [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## Altre risorse per questo prodotto


-   [Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Risoluzione dei problemi relativi a UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### Altre informazioni

<a href="" id="mdop-techcenter-page"></a>[Pagina TechCenter di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Scopri le informazioni e le risorse più recenti di MDOP.

<a href="" id="mdop-information-experience"></a>[Esperienza di informazioni su MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Trovare documentazione, video e altre risorse per le tecnologie MDOP. È anche possibile [inviare commenti e suggerimenti](mailto:MDOPDocs@microsoft.com) per ricevere informazioni sugli aggiornamenti e seguirci su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).














