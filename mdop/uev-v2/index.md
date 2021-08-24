---
title: Microsoft User Experience Virtualization (UE-V) 2.x
description: Microsoft User Experience Virtualization (UE-V) 2.x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 79748e04ae1a59afdc8f9dae3c5dc77c50e3c253
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910541"
---
# <a name="microsoft-user-experience-virtualization-ue-v-2x"></a>Microsoft User Experience Virtualization (UE-V) 2.x

>[!NOTE]
>Questa documentazione è una versione di UE-V inclusa in Microsoft Desktop Optimization Pack (MDOP). Per informazioni sulla versione più recente di UE-V inclusa in Windows 10 Enterprise, vedere [Informazioni di base con UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Acquisire e centralizzare le impostazioni dell'applicazione degli utenti Windows impostazioni del sistema operativo implementando Microsoft User Experience Virtualization (UE-V) 2.0 o 2.1. Applica quindi queste impostazioni ai dispositivi a cui gli utenti accedono nell'organizzazione, ad esempio computer desktop, portatili o sessioni VDI (Virtual Desktop Infrastructure).

**Con UE-V è possibile...**

-   Specificare le impostazioni dell'applicazione e del desktop da sincronizzare

-   Recapitare in qualsiasi momento le impostazioni agli utenti, indipendentemente dalla posizione nell'azienda da cui gli utenti lavorano

-   Creare modelli personalizzati per le applicazioni di terze parti o line-of-business

-   Ripristinare le impostazioni dopo la sostituzione o l'aggiornamento dell'hardware o dopo aver ripristinato lo stato iniziale di una macchina virtuale

## <a name="components-of-ue-v-2x"></a>Componenti di UE-V 2.x


Questo diagramma mostra il modo in cui i UE-V distribuiti funzionano insieme per sincronizzare le impostazioni.

![Diagramma dell'architettura uev2.](images/uev2archdiagram.gif)

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
<td align="left"><p><strong>UE-V Agente</strong></p></td>
<td align="left"><p>Installato in ogni computer che deve sincronizzare le impostazioni, l'agente UE-V monitora le applicazioni registrate e il sistema operativo per eventuali modifiche alle impostazioni, quindi sincronizza tali impostazioni <strong> </strong> tra i computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Impostazioni pacchetti</strong></p></td>
<td align="left"><p>Le impostazioni delle applicazioni Windows vengono archiviate in pacchetti <strong> </strong> di impostazioni creati dall'UE-V Agent. I pacchetti di impostazioni vengono creati, archiviati localmente e copiati nel percorso dell'archivio impostazioni.</p>
<ul>
<li><p>I valori delle impostazioni per <strong> le applicazioni desktop vengono </strong> archiviati quando l'utente chiude l'applicazione.</p></li>
<li><p>I valori Windows vengono archiviati quando l'utente si disconnette, quando il computer è bloccato o quando l'utente si disconnette in remoto <strong> </strong> da un computer.</p></li>
</ul>
<p>Il provider di sincronizzazione determina quando le impostazioni dell'applicazione o del sistema operativo vengono lette <strong> Impostazioni pacchetti </strong> e sincronizzate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Impostazioni di archiviazione</strong></p></td>
<td align="left"><p>Si tratta di una condivisione di rete standard a cui gli utenti possono accedere. L UE-V agent verifica il percorso e crea una cartella di sistema nascosta in cui archiviare e recuperare le impostazioni utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Impostazioni di percorso</strong></p></td>
<td align="left"><p>UE-V i file XML come modelli di percorso delle impostazioni per monitorare e sincronizzare le impostazioni dell'applicazione desktop e Windows desktop tra computer utente. Per impostazione predefinita, alcuni modelli di percorso delle impostazioni sono inclusi in UE-V . È inoltre possibile creare, modificare o convalidare modelli di percorso delle impostazioni personalizzate gestendo <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> la sincronizzazione delle impostazioni per le applicazioni </a> personalizzate.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Impostazioni modelli di percorso non sono necessari per le Windows app.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows app</strong></p></td>
<td align="left"><p>Impostazioni per Windows app vengono acquisite e applicate in modo dinamico. Lo sviluppatore dell'app specifica le impostazioni sincronizzate per ogni app. UE-V determina quali app Windows abilitate per la sincronizzazione delle impostazioni usando un elenco gestito di app. Per impostazione predefinita, questo elenco include la maggior parte Windows app.</p>
<p>Puoi aggiungere o rimuovere applicazioni nell'Windows app seguendo le procedure illustrate <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> qui.</p></td>
</tr>
</tbody>
</table>



### <a name="managing-settings-synchronization-for-custom-applications"></a><a href="" id="customapps"></a>Gestione Impostazioni sincronizzazione per applicazioni personalizzate

Utilizzare questi UE-V per creare e gestire modelli personalizzati per le applicazioni line-of-business o di terze parti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Generatore</strong></p></td>
<td align="left"><p>Utilizzare il generatore UE-V per creare modelli di percorso delle <strong> impostazioni personalizzate che è quindi possibile distribuire ai computer degli </strong> utenti. Il generatore UE-V consente inoltre di modificare un modello esistente o convalidare un modello creato utilizzando un altro editor XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Impostazioni modelli</strong></p></td>
<td align="left"><p>Il catalogo dei modelli di impostazioni è un percorso di cartella UE-V computer o una condivisione di rete <strong> SMB (Server Message Block) in cui sono archiviati i modelli di percorso </strong> delle impostazioni personalizzate. L UE-V agent controlla questa posizione una volta al giorno, recupera modelli nuovi o aggiornati e ne aggiorna il comportamento di sincronizzazione.</p>
<p>Se si utilizzano solo i modelli di percorso UE-V impostazioni predefinite, un catalogo di modelli di impostazioni non è necessario. Per ulteriori informazioni sui cataloghi di distribuzione delle impostazioni, vedere <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> Configure a UE-V settings template catalog </a> .</p></td>
</tr>
</tbody>
</table>



![processo generatore ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-synchronized-by-default"></a>Impostazioni Sincronizzato per impostazione predefinita


UE-V sincronizza le impostazioni per queste applicazioni per impostazione predefinita. Per un elenco completo e informazioni più dettagliate, vedere Impostazioni sincronizzati automaticamente [in una UE-V distribuzione.](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)

Microsoft Office 2013 (UE-V 2.1 SP1 e 2.1)

Microsoft Office 2010 (UE-V 2.1 SP1, 2.1 e 2.0)

Microsoft Office 2007 (solo UE-V 2.0)

Internet Explorer 8, 9 e 10

Internet Explorer 11 in UE-V 2.1 SP1 e 2.1

Molte Windows, ad esempio Xbox

Molte Windows desktop, ad esempio Blocco note

Molte Windows, ad esempio sfondo del desktop o sfondo

**Nota**  
È inoltre possibile [personalizzare i UE-V per sincronizzare le](https://technet.microsoft.com/library/dn458942.aspx) impostazioni per le applicazioni diverse da quelle sincronizzate per impostazione predefinita.



## <a name="compare-ue-v-to-other-microsoft-products"></a>Confrontare UE-V altri prodotti Microsoft


Usa questa tabella per confrontare UE-V sincronizzazione dei profili in Windows 7, Sincronizza profili in Windows 8 e la funzionalità sincronizza pc Impostazioni dell'account Microsoft.

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
<th align="left">Sincronizzare i profili Windows 7</th>
<th align="left">Sincronizzare i profili Windows 8</th>
<th align="left">Sincronizzare i profili Windows 10</th>
<th align="left">Account Microsoft</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 e 2.1 SP1</th>
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
<td align="left"><p>Sincronizzare le impostazioni tra app fisiche e virtuali</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizzare Windows impostazioni dell'app</p></td>
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
<td align="left"><p>Sincronizzare le modifiche delle impostazioni a intervalli regolari</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurazione minima per il programma di installazione</p></td>
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
<td align="left"><p>Supporta l'attributo Di Active Directory del computer primario</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizza le impostazioni tra VDI (Virtual Desktop Infrastructure)/Remote Desktop Services (RDS) e desktop remoti</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Spazio di archiviazione illimitato</p></td>
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
<td align="left"><p>Backup/ripristino per i Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Parziale</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## <a name="ue-v-2x-release-notes"></a>UE-V Note sulla versione 2.x


Per ulteriori informazioni e per le notizie più aggiornate che non sono contenute nella documentazione, vedere

-   [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <a name="other-resources-for-this-product"></a>Altre risorse per questo prodotto


-   [Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Preparare una UE-V 2.x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Amministrazione di UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Risoluzione dei UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### <a name="more-information"></a>Altre informazioni

<a href="" id="mdop-techcenter-page"></a>[Pagina TechCenter MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Informazioni sulle informazioni e sulle risorse MDOP più recenti.

<a href="" id="mdop-information-experience"></a>[MdOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Trova documentazione, video e altre risorse per le tecnologie MDOP. Puoi anche [inviarci commenti e suggerimenti](mailto:MDOPDocs@microsoft.com) o informazioni sugli aggiornamenti seguendoci su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter.](https://go.microsoft.com/fwlink/p/?LinkId=242447)














