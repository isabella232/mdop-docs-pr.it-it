---
title: Uso di Client Management Console di App-V 5.0
description: Uso di Client Management Console di App-V 5.0
author: dansimp
ms.assetid: 36398307-57dd-40f3-9d4f-b09f44fd37c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8541e5bc59334b9074a3940dad7cdf0114205d4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804845"
---
# Uso di Client Management Console di App-V 5.0


Questo argomento fornisce informazioni su come configurare e gestire il client App-V 5,0.

## Modificare la configurazione client App-V 5,0


Il client App-V 5,0 ha impostazioni associate che possono essere configurate per determinare il modo in cui il client verrà eseguito nell'ambiente. È possibile gestire queste impostazioni nel computer che esegue il client o tramite PowerShell o criteri di gruppo. Per altre informazioni su come modificare il client usando PowerShell o configurazione di criteri di gruppo, vedere [come modificare la configurazione del client tramite PowerShell](how-to-modify-client-configuration-by-using-powershell.md).

## <a href="" id="the-app-v-5-0-client-management-console-"></a>Console di gestione client App-V 5,0


Puoi ottenere informazioni sul client App-V 5,0 o eseguire attività specifiche usando la console di gestione client App-V 5,0. Molte delle attività che è possibile eseguire nella console di gestione client possono essere eseguite anche tramite PowerShell. I cmdlet di PowerShell associati per ogni azione vengono visualizzati anche nella tabella seguente. Per altre informazioni sull'uso di PowerShell, vedere [amministrazione di App-V tramite PowerShell](administering-app-v-by-using-powershell.md).

La console di gestione client contiene le schede principali descritte di seguito.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">TAB</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Panoramica</p></td>
<td align="left"><p>La <strong> </strong> scheda Panoramica contiene gli elementi seguenti:</p>
<ul>
<li><p>Update: usare il <strong> </strong> riquadro Aggiorna per aggiornare un'applicazione virtualizzata o per ricevere un nuovo pacchetto virtualizzato.</p>
<p>L' <strong> Ultimo aggiornamento </strong> Visualizza la versione corrente del pacchetto virtualizzato.</p></li>
<li><p>Scaricare tutte le applicazioni virtuali: usare <strong> il </strong> riquadro download per scaricare tutti i pacchetti di cui è stato eseguito il provisioning per l'utente corrente.</p>
<p>(Cmdlet di PowerShell associato: <strong> Mount-AppvClientPackage </strong> )</p>
<p></p></li>
<li><p>Lavorare offline: usare questo riquadro per disabilitare tutti gli aggiornamenti automatici e manuali delle applicazioni virtuali.</p>
<p>(Cmdlet di PowerShell associato: <strong> Set-AppvPublishServer-UserRefreshEnabled-GlobalRefreshEnabled </strong> )</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App virtuali</p></td>
<td align="left"><p>La <strong> scheda App virtuali </strong> Visualizza tutti i pacchetti che sono stati pubblicati per l'utente. È anche possibile fare clic su un pacchetto specifico e vedere tutte le applicazioni che fanno parte del pacchetto. In questo modo vengono visualizzate informazioni sui pacchetti attualmente in uso e sulla quantità di ogni pacchetto scaricato nel computer. È anche possibile avviare e arrestare i download del pacchetto. È inoltre possibile ripristinare lo stato dell'utente. Un ripristino eliminerà tutti i dati utente associati a un pacchetto.</p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gruppi di connessioni app</p></td>
<td align="left"><p>Nella <strong> scheda gruppi di connessioni app </strong> vengono visualizzati tutti i gruppi di connessioni disponibili per l'utente corrente. Fare clic su un gruppo di connessioni specifico per visualizzare tutti i pacchetti che fanno parte del gruppo selezionato. Vengono visualizzate informazioni sui gruppi di connessioni già in uso e sulla quantità di contenuto del gruppo di connessioni scaricate nel computer. È inoltre possibile avviare e arrestare i download del gruppo di connessioni. Puoi usare questa sezione per avviare un ripristino. Un ripristino rimuoverà tutto lo stato dell'utente associato a un gruppo di connessioni.</p>
<p>(Cmdlet di PowerShell associati: download- <strong> Mount-AppvClientConnectionGroup </strong> . Repair- <strong> AppvClientConnectionGroup </strong> .)</p>
<p></p></td>
</tr>
</tbody>
</table>

 

[Come accedere a Client Management Console](how-to-access-the-client-management-console.md)

[Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-beta.md)






## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





