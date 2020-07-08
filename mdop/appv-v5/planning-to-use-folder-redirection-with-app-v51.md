---
title: Pianificazione per l'uso del reindirizzamento delle cartelle con App-V
description: Pianificazione per l'uso del reindirizzamento delle cartelle con App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804936"
---
# Pianificazione per l'uso del reindirizzamento delle cartelle con App-V


Microsoft Application Virtualization (App-V) 5,1 supporta l'uso del reindirizzamento delle cartelle, una funzionalità che consente agli utenti e agli amministratori di reindirizzare il percorso di una cartella in una nuova posizione.

Questo argomento contiene le sezioni seguenti:

-   [Requisiti per l'uso del reindirizzamento delle cartelle](#bkmk-folder-redir-reqs)

-   [Come configurare il reindirizzamento delle cartelle per l'uso con App-V](#bkmk-folder-redir-cfg)

-   [Funzionamento del reindirizzamento delle cartelle con App-V](#bkmk-folder-redir-works)

-   [Panoramica del reindirizzamento delle cartelle](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>Requisiti e scenari non supportati per l'uso del reindirizzamento delle cartelle


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Requisiti</p></td>
<td align="left"><p>Per usare il reindirizzamento delle cartelle% AppData%, è necessario:</p>
<ul>
<li><p>Avere un pacchetto di App-V che include una cartella di file system virtuale AppData.</p></li>
<li><p>Abilitare il reindirizzamento delle cartelle e reindirizzare le cartelle degli utenti a una cartella condivisa, in genere una cartella di rete.</p></li>
<li><p>Eseguire il roaming sia o nessuna delle opzioni seguenti:</p>
<ul>
<li><p>File in%appdata%\Microsoft\AppV\Client\Catalog</p></li>
<li><p>Impostazioni del registro di sistema in HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</p>
<p>Per altre informazioni, Vedi <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> pubblicazione delle applicazioni e interazione tra client </a> .</p></li>
</ul></li>
<li><p>Verificare che le cartelle seguenti siano disponibili per ogni utente che accede al computer in cui è in uso il client App-V 5,0 SP2 o versione successiva:</p>
<ul>
<li><p>% AppData% è configurato per il percorso di rete desiderato (con o senza <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> supporto per i file offline </a> ).</p></li>
<li><p>% LocalAppData% è configurato nella cartella locale desiderata.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Scenari non supportati</p></td>
<td align="left"><ul>
<li><p>Configurazione di% LocalAppData% come unità di rete.</p></li>
<li><p>Reindirizzamento del menu Start a una singola cartella per più utenti.</p></li>
<li><p>Se il roaming AppData (% AppData%) viene reindirizzato a una condivisione di rete non disponibile, le applicazioni App-V non verranno avviate nel modo seguente:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione App-V</th>
<th align="left">Descrizione scenario</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>In App-V 5,0 tramite App-V 5,0 SP2 Plus hotfix</p></td>
<td align="left"><p>Questo errore si verificherà indipendentemente dal fatto che i file offline siano abilitati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>In App-V 5,0 SP3 e versioni successive</p></td>
<td align="left"><p>Se la condivisione di rete non disponibile è stata abilitata per i file offline, l'applicazione App-V verrà avviata correttamente.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>Come configurare il reindirizzamento delle cartelle per l'uso con App-V


Il reindirizzamento delle cartelle può essere applicato a cartelle diverse, ad esempio desktop, documenti personali, immagini personali e così via. Tuttavia, l'unica cartella che influisce sull'uso delle applicazioni App-V è la cartella AppData Roaming dell'utente (% AppData%). Puoi applicare il reindirizzamento delle cartelle a qualsiasi altra cartella supportata senza influire su App-V.

## <a href="" id="bkmk-folder-redir-works"></a>Funzionamento del reindirizzamento delle cartelle con App-V


La tabella seguente descrive il funzionamento del reindirizzamento delle cartelle quando% AppData% viene reindirizzato a una rete e dopo aver soddisfatto i requisiti elencati in precedenza in questo articolo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Stato ambiente virtuale</th>
<th align="left">Azione che si verifica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Quando l'ambiente virtuale viene avviato</p></td>
<td align="left"><p>La cartella AppData di Virtual File System (VFS) viene mappata alla cartella AppData locale (% LocalAppData%) invece della cartella AppData mobile dell'utente (% AppData%).</p>
<ul>
<li><p>LocalAppData contiene una cache locale della cartella AppData mobile dell'utente per il pacchetto in uso. La cache locale si trova in:</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>Gli ultimi dati della cartella AppData Roaming dell'utente vengono copiati e sostituiti dai dati attualmente presenti nella cache locale.</p></li>
<li><p>Mentre l'ambiente virtuale è in esecuzione, i dati continueranno a essere salvati nella cache locale. I dati vengono serviti solo in% LocalAppData% e non vengono spostati o sincronizzati con% AppData% fino a quando l'utente finale non arresta il computer.</p></li>
<li><p>Le voci nella cartella AppData vengono effettuate usando il contesto utente e non il contesto di sistema.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Il reindirizzamento delle cartelle client App-V a volte non riesce a trasferire i file da% AppData% a% LocalAppData%. Vedere <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> Note sulla versione per App-V 5,0 SP2 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Quando l'ambiente virtuale si arresta</p></td>
<td align="left"><p>I dati memorizzati nella cache locale in AppData (roaming) vengono compressi e copiati nella cartella AppData di roaming "reale" in% AppData%. Un indicatore di data e ora, che indica l'ultimo caricamento noto, viene salvato contemporaneamente come chiave del registro di sistema in:</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>Per ottenere la ridondanza, App-V mantiene le tre copie più recenti dei dati compressi in% AppData%.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>Panoramica del reindirizzamento delle cartelle


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Scopo</p></td>
<td align="left"><p>Consente agli utenti finali di lavorare con i file, che sono stati reindirizzati a un'altra cartella, come se i file fossero ancora presenti nell'unità locale.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Il reindirizzamento delle cartelle consente agli utenti e agli amministratori di reindirizzare il percorso di una cartella a un percorso di rete. I documenti nella cartella sono disponibili per l'utente da qualsiasi computer della rete.</p>
<ul>
<li><p>Il reindirizzamento delle cartelle consente agli utenti e agli amministratori di reindirizzare il percorso di una cartella a un percorso di rete. I documenti nella cartella sono disponibili per l'utente da qualsiasi computer della rete.</p></li>
<li><p>Il nuovo percorso può essere una cartella nel computer locale o una cartella in una rete condivisa.</p></li>
<li><p>Il reindirizzamento delle cartelle aggiorna immediatamente i file, mentre i dati mobili vengono in genere sincronizzati quando l'utente accede o disconnette.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Esempio di utilizzo</p></td>
<td align="left"><p>È possibile reindirizzare la cartella documenti, che in genere viene archiviata nel disco rigido locale del computer&#39;s, in un percorso di rete. L'utente può accedere ai documenti nella cartella da qualsiasi computer della rete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Altre risorse</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">Panoramica del reindirizzamento delle cartelle</a></p></td>
</tr>
</tbody>
</table>
















