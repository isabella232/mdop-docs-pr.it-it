---
title: Migrazione da una versione precedente
description: Migrazione da una versione precedente
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805067"
---
# Migrazione da una versione precedente


Con App-V 5,0 puoi eseguire la migrazione dell'infrastruttura App-V 4,6 esistente a quella più flessibile, integrata e più facile da gestire dell'infrastruttura App-V 5,0.

Quando si pianifica la strategia di migrazione, prendere in considerazione le sezioni seguenti:

**Nota**  Per altre informazioni sulle differenze tra App-V 4,6 e App-V 5,0, Vedi le **differenze tra la sezione App-v 4,6 e App-v 5,0** di [About app-v 5,0](about-app-v-50.md).

 

## Conversione di pacchetti creati con una versione precedente di App-V


Usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni precedenti di App-V. Il convertitore di pacchetti usa PowerShell per convertire i pacchetti e può aiutare a automatizzare il processo se sono presenti molti pacchetti che richiedono la conversione.

**Importante**  Dopo aver convertito un pacchetto esistente, è consigliabile testare il pacchetto prima di distribuire il pacchetto per verificare che il processo di conversione abbia avuto esito positivo.

 

**Informazioni utili prima di convertire i pacchetti esistenti**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problema</th>
<th align="left">Soluzione alternativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gli script di pacchetto non vengono convertiti.</p></td>
<td align="left"><p>Testare il pacchetto convertito. Se necessario, convertire lo script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le override dell'impostazione del registro di sistema non vengono convertite.</p></td>
<td align="left"><p>Testare il pacchetto convertito. Se necessario, aggiungere di nuovo gli override del registro di sistema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>I pacchetti virtuali che usano DSC non sono collegati dopo la conversione.</p></td>
<td align="left"><p>Collegare i pacchetti usando i gruppi di connessioni. Vedere <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> gestione dei gruppi di connessioni </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>I conflitti di variabili di ambiente vengono rilevati durante la conversione.</p></td>
<td align="left"><p>Risolvere i conflitti nel <strong> file OSD associato </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>I percorsi hardcoded vengono rilevati durante la conversione.</p></td>
<td align="left"><p>I percorsi hardcoded sono difficili da convertire correttamente. Il convertitore di pacchetti rileverà e restituirà pacchetti con file che contengono percorsi hardcoded. Visualizzare il file con il percorso hardcoded e determinare se il pacchetto richiede il file. In questo caso, è consigliabile ripetere la sequenza del pacchetto.</p></td>
</tr>
</tbody>
</table>

 

Quando si converte un pacchetto, verificare la mancanza di file o tasti di scelta rapida. Individuare l'elemento nel pacchetto App-V 4,6. Potrebbe essere un percorso hardcoded. Convertire il percorso.

**Nota**  È consigliabile usare il sequencer App-V 5,0 per la conversione di applicazioni o applicazioni critiche che devono sfruttare le funzionalità. Vedere [come sequenziare una nuova applicazione con App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).

Se un pacchetto convertito non si apre dopo averlo convertito, è anche consigliabile ripetere la sequenza dell'applicazione usando il sequencer App-V 5,0.

 

[Come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## Migrazione dei client


Nella tabella seguente viene visualizzato il metodo consigliato per l'aggiornamento dei client.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiornare l'ambiente a App-V 4.6 SP2</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Installare il client App-V 5,0 con la coesistenza abilitata.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenziare e distribuire pacchetti App-V 5,0. Se necessario, Annulla la pubblicazione di pacchetti App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">Come sequenziare una nuova applicazione con App-V 5,0 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Importante**  È necessario eseguire App-V 4.6 SP3 per usare la modalità di coesistenza. Inoltre, quando si sequenzia un pacchetto, è necessario configurare l'impostazione dell'autorità di gestione, che si trova nella **Configurazione utente** nella sezione **Configurazione utente** .

 

## Migrazione dell'infrastruttura completa del server App-V 5,0


Non esiste un metodo diretto per eseguire l'aggiornamento a un'infrastruttura App-V 5,0 completa. Usare le informazioni nella sezione seguente per informazioni sull'aggiornamento del server App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiornare l'ambiente in App-V 4.6 SP3.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuire App-V 5,0 versione del client.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">Come distribuire il client App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare App-V 5,0 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">Come distribuire il server App-V 5,0 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Eseguire la migrazione dei pacchetti esistenti.</p></td>
<td align="left"><p>Vedere i <strong> pacchetti di conversione creati con una versione precedente della sezione App-V </strong> di questo articolo.</p></td>
</tr>
</tbody>
</table>

 

## Altre attività di migrazione


È anche possibile eseguire altre attività di migrazione, come la riconfigurazione dei punti finali e l'apertura di un pacchetto creato con una versione precedente in un computer che esegue il client App-V 5,0. I collegamenti seguenti includono ulteriori informazioni sull'esecuzione di queste attività.

[Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## Altre risorse per l'esecuzione di attività di migrazione App-V


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

[Procedura di aggiornamento del server di gestione di Microsoft App-V 5,1 semplificata](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





