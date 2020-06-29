---
title: Migrazione ad App-V 5.1 da una versione precedente
description: Migrazione ad App-V 5.1 da una versione precedente
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805062"
---
# Migrazione ad App-V 5.1 da una versione precedente


Con Microsoft Application Virtualization (App-V) 5,1, puoi eseguire la migrazione dell'infrastruttura App-V 4,6 o dell'app-v 5,0 esistente nell'infrastruttura più flessibile, integrata e più facile da gestire dell'App-V 5,1.
Tuttavia, non è possibile eseguire la migrazione direttamente da App-V 4. x a App-V 5,1, per prima cosa è necessario eseguire la migrazione a App-V 5,0. Per altre informazioni sulla migrazione da App-V 4. x a App-V 5,0, vedere [migrazione da una versione precedente](migrating-from-a-previous-version-app-v-50.md)  

**Nota**  I pacchetti App-V 5,1 sono esattamente gli stessi dei pacchetti App-V 5,0. Non è stato modificato il formato del pacchetto tra le versioni e quindi non è necessario convertire i pacchetti App-V 5,0 in pacchetti App-V 5,1.

Per altre informazioni sulle differenze tra App-V 4,6 e App-V 5,1, Vedi le **differenze tra la sezione App-v 4,6 e App-v 5,0** di [About app-v 5,0](about-app-v-50.md).

 

## <a href="" id="bkmk-pkgconvimprove"></a>Miglioramenti apportati al convertitore di pacchetti App-V 5,1


Ora puoi usare il convertitore di pacchetti per convertire i pacchetti App-V 4,6 che contengono script e le informazioni del registro di sistema e gli script dei file di origine. OSD ora sono inclusi nell'output del convertitore di pacchetti.

Puoi anche usare il `–OSDsToIncludeInPackage` parametro con il `ConvertFrom-AppvLegacyPackage` cmdlet per specificare quali informazioni sui file OSD vengono convertite e inserite nel nuovo pacchetto.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuovo in App-V 5,1</th>
<th align="left">Prima dell'App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>I nuovi file XML vengono creati in corrispondenza dei file OSD associati a un pacchetto; questi file includono le informazioni seguenti:</p>
<ul>
<li><p>variabili di ambiente</p></li>
<li><p>scorciatoie</p></li>
<li><p>associazioni di tipi di file</p></li>
<li><p>informazioni sul Registro di sistema</p></li>
<li><p>script</p></li>
</ul>
<p>Ora è possibile scegliere di aggiungere informazioni da un sottoinsieme dei file OSD nella directory di origine al pacchetto usando il <code>-OSDsToIncludeInPackage</code> parametro.</p></td>
<td align="left"><p>Le informazioni del registro di sistema e gli script inclusi nei file OSD associati a un pacchetto non sono inclusi nell'output del convertitore di pacchetti.</p>
<p>Il convertitore di pacchetti compilerebbe il nuovo pacchetto con le informazioni provenienti da tutti i file OSD nella directory di origine.</p></td>
</tr>
</tbody>
</table>

 

### Istruzione di conversione di esempio

Per informazioni sul nuovo processo, vedere l'istruzione del convertitore di pacchetti di esempio seguente `ConvertFrom-AppvLegacyPackage` .

**Se la directory di origine (\\\\OldPkgStore\\ContosoApp) include le operazioni seguenti:**

-   ContosoApp. SFT

-   ContosoApp.msi

-   ContosoApp. sprj

-   ContosoApp\_manifest.xml

-   X. OSD

-   Y. OSD

-   Z. OSD

**E si esegue questo comando:**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**Il codice seguente viene creato nella directory di destinazione (\\\\NewPkgStore\\ContosoApp):**

-   ContosoApp. AppV

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**Nell'esempio precedente:**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Questi file della directory di origine...</th>
<th align="left">... vengono convertiti in questi file di directory di destinazione...</th>
<th align="left">... e conterrà questi elementi</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
<li><p>Z. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variabili di ambiente</p></li>
<li><p>Scorciatoie</p></li>
<li><p>Associazioni di tipi di file</p></li>
<li><p>Informazioni sul Registro di sistema</p></li>
<li><p>Script</p></li>
</ul></td>
<td align="left"><p>Ogni file OSD viene convertito in un file XML separato corrispondente che contiene gli elementi elencati nel formato di configurazione della distribuzione di App-V 5,1. Questi elementi possono quindi essere copiati da questi file XML e inseriti nella configurazione di distribuzione o nei file di configurazione dell'utente come desiderato.</p>
<p>In questo esempio sono presenti tre file XML, corrispondenti ai tre file OSD nella directory di origine. Ogni file XML contiene le variabili di ambiente, i tasti di scelta rapida, le associazioni dei tipi di file, le informazioni del registro di sistema e gli script nel file OSD corrispondente.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp. AppV</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variabili di ambiente</p></li>
<li><p>Scorciatoie</p></li>
<li><p>Associazioni di tipi di file</p></li>
</ul></td>
<td align="left"><p>Le informazioni dei file OSD specificati nel <code>-OSDsToIncludeInPackage</code> parametro vengono convertite e inserite all'interno del pacchetto. Il convertitore compila quindi il file di configurazione della distribuzione e il file di configurazione dell'utente con il contenuto del pacchetto, così come fa l'App-V Sequencer durante la sequenziazione di un nuovo pacchetto.</p>
<p>In questo esempio, le variabili di ambiente, i tasti di scelta rapida e le associazioni di tipi di file inclusi in X. OSD e Y. OSD sono stati convertiti e inseriti nel pacchetto App-V e alcune di queste informazioni sono state incluse anche nei file di configurazione della distribuzione e configurazione utente. X. OSD e Y. OSD sono stati usati perché sono stati inclusi come argomenti per il <code>-OSDsToIncludeInPackage</code> parametro. Nessuna informazione da Z. OSD è stata inclusa nel pacchetto, perché non è stata inclusa come uno di questi argomenti.</p></td>
</tr>
</tbody>
</table>

 

## Conversione di pacchetti creati con una versione precedente di App-V


Usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni di App-V precedenti a App-V 5,0. Il convertitore di pacchetti usa PowerShell per convertire i pacchetti e può aiutare a automatizzare il processo se sono presenti molti pacchetti che richiedono la conversione.

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
<td align="left"><p>I pacchetti virtuali che usano DSC non sono collegati dopo la conversione.</p></td>
<td align="left"><p>Collegare i pacchetti usando i gruppi di connessioni. Vedere <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> gestione dei gruppi di connessioni </a> .</p></td>
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

 

Quando si converte un pacchetto, verificare la mancanza di file o tasti di scelta rapida. Individuare l'elemento nel pacchetto App-V 4,6. Potrebbe anche essere un percorso hardcoded. Convertire il percorso.

**Nota**  È consigliabile usare il sequencer App-V 5,1 per la conversione di applicazioni o applicazioni critiche che devono sfruttare le funzionalità. Vedere [come sequenziare una nuova applicazione con App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).

Se un pacchetto convertito non si apre dopo averlo convertito, è anche consigliabile ripetere la sequenza dell'applicazione usando il sequencer App-V 5,1.

 

[Come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

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
<td align="left"><p>Aggiornare l'ambiente alla versione più recente di App-V 4.6</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Installare il client App-V 5,1 con la coesistenza abilitata.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenziare e distribuire pacchetti App-V 5,1. Se necessario, Annulla la pubblicazione di pacchetti App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">Come sequenziare una nuova applicazione con App-V 5,1 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Importante**  È necessario eseguire la versione più recente di App-V 4.6 per usare la modalità di coesistenza. Inoltre, quando si sequenzia un pacchetto, è necessario configurare l'impostazione dell'autorità di gestione, che si trova nella **Configurazione utente** nella sezione **Configurazione utente** .

 

## Migrazione dell'infrastruttura completa del server App-V 5,1


Non esiste un metodo diretto per eseguire l'aggiornamento a un'infrastruttura App-V 5,1 completa. Usare le informazioni nella sezione seguente per informazioni sull'aggiornamento del server App-V.

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
<td align="left"><p>Aggiornare l'ambiente alla versione più recente di App-V 4.6.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuire App-V 5,1 versione del client.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">Come distribuire il client App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare App-V 5,1 server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">Come distribuire il server App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Eseguire la migrazione dei pacchetti esistenti.</p></td>
<td align="left"><p>Vedere i <strong> pacchetti di conversione creati con una versione precedente della sezione App-V </strong> di questo articolo.</p></td>
</tr>
</tbody>
</table>

 

## Altre attività di migrazione


È anche possibile eseguire altre attività di migrazione, come la riconfigurazione dei punti finali e l'apertura di un pacchetto creato con una versione precedente in un computer che esegue il client App-V 5,1. I collegamenti seguenti includono ulteriori informazioni sull'esecuzione di queste attività.

[Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per un utente specifico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## Altre risorse per l'esecuzione di attività di migrazione App-V


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

[Procedura di aggiornamento del server di gestione di Microsoft App-V 5,1 semplificata](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





