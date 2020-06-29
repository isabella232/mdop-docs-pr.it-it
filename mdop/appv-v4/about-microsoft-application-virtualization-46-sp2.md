---
title: Informazioni su Microsoft Application Virtualization 4.6 SP2
description: Informazioni su Microsoft Application Virtualization 4.6 SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820016"
---
# Informazioni su Microsoft Application Virtualization 4.6 SP2


Microsoft Application Virtualization (App-V) 4.6 SP2 offre diversi miglioramenti e nuove funzionalità, descritti in questo argomento.

**Attenzione**  Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema. Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows. Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat). Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti. Cambiare il registro di sistema a proprio rischio.

 

**Supporto per Windows 8 e Windows Server 2012**

App-V 4.6 SP2 aggiunge il supporto per i Servizi Desktop remoto di Windows 8 e Windows Server 2012.

**Supporto per la coesistenza con client App-V 5,0**

App-V 4.6 SP2 offre il supporto per la coesistenza con il client Microsoft Application Virtualization 5,0. Esaminare la documentazione di App-V 5,0 per istruzioni su come configurare il client App-V 5,0 per la coesistenza con il client App-V 4.6 SP2. Per altre informazioni su App-V 5,0, vedere [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) in TechNet.

**Possibilità di virtualizzare Adobe Reader X con la modalità protetta**

È possibile virtualizzare Adobe Reader X con la funzionalità modalità protetta attivata usando le procedure seguenti. In precedenza è stata necessario disabilitare la modalità protetta per virtualizzare Adobe Reader X.

Prima di avviare l'App-V Sequencer, creare il seguente valore del registro di sistema in HKEY \ _LOCAL \ _MACHINE directory \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nome</p></td>
<td align="left"><p>Tipo</p></td>
<td align="left"><p>Dati</p></td>
<td align="left"><p>Descrizione</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableVFSPassthrough</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Impostare questo valore su <strong> 1 per </strong> avviare Adobe Reader X in modalità protetta durante la fase di avvio.</p></td>
</tr>
</tbody>
</table>

 

**Nota**  In un computer che gestisce un sistema operativo a 64 bit, creare il valore di registro in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.

 

Per ogni file OSD nel pacchetto di Adobe Reader X, aggiungere gli elementi seguenti nell' &lt; &gt; elemento policy:

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**Nuovo parametro della riga di comando sequencer**

Quando si crea un Acceleratore pacchetto (PA) tramite la GUI sequencer, è possibile selezionare un file RTF o TXT che fornisca indicazioni per il packaging e la distribuzione agli amministratori che applicano l'Acceleratore pacchetto. Questa funzionalità è ora disponibile usando la CLI Sequencer.

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

Specificare un percorso di un file RTF o TXT che fornisca indicazioni per il packaging e la distribuzione durante la creazione di un Acceleratore pacchetto.

**La segnalazione degli errori delle applicazioni Microsoft non deve più essere installata**

Quando si installa il client App-V 4.6 SP2 usando setup.msi, non è più necessario installare segnalazione errori applicazioni Microsoft (dw20shared.msi). App-V 4.6 SP2 ora usa la segnalazione degli errori Microsoft. Per altre informazioni, vedere [come installare il client App-V usando Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).

**Feedback dei clienti e aggiornamento cumulativo**

App-V 4.6 SP2 include un rollup di correzioni per risolvere i problemi rilevati dalla versione App-V 4,6 SP1. App-V 4.6 SP2 contiene le correzioni più recenti fino a Microsoft Application Virtualization 4,6 SP1 hotfix 6.

## In questa sezione


<a href="" id="app-v-4-6-sp2-release-notes"></a>[Note sulla versione di App-V 4.6 SP2](https://go.microsoft.com/fwlink/?LinkId=267600)  
Fornisce le informazioni più aggiornate sui problemi noti di App-V 4.6 SP2.

 

 





