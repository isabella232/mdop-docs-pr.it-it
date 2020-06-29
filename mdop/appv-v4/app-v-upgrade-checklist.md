---
title: Elenco di controllo aggiornamento di App-V
description: Elenco di controllo aggiornamento di App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819736"
---
# Elenco di controllo aggiornamento di App-V


Prima di provare a eseguire l'aggiornamento a Microsoft Application Virtualization (App-V) 4,5 o versioni successive, è necessario aggiornare tutte le versioni precedenti a App-V 4,1 in App-V 4,1. È consigliabile pianificare prima di tutto l'aggiornamento dei client e quindi aggiornare i componenti del server. I client App-V che sono stati aggiornati a App-V 4,5 continuano a funzionare con i server App-V che non sono ancora stati aggiornati. Le versioni precedenti del client non sono supportate nei server che sono stati aggiornati a App-V 4,5.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Riferimento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiornare i client App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)">Come aggiornare Application Virtualization Client</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiornare i server e il database App-V.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Se si dispone di più di un server di accesso alla condivisione del database App-V, è necessario che tutti i server vengano disattivati durante l'aggiornamento del database. Devi seguire le normali procedure aziendali per l'aggiornamento del database, ma ti consigliamo di testare l'aggiornamento del database usando una copia di backup del database prima in un server di test. Devi quindi selezionare uno dei server per il primo aggiornamento, che aggiornerà lo schema del database. Dopo che il database di produzione è stato aggiornato correttamente, è possibile aggiornare il software App-V sugli altri server.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Come aggiornare i server e i componenti del sistema</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiornare il servizio Web di gestione App-V.</p>
<p>Questo passaggio si applica solo se il servizio Web di gestione si trova in un server distinto, che richiede l'esecuzione del programma di installazione del server nel server separato per l'aggiornamento del servizio Web di gestione. In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà automaticamente il servizio Web di gestione.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Come aggiornare i server e i componenti del sistema</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiornare la console di gestione di App-V.</p>
<p>Questo passaggio si applica solo se la console di gestione si trova in un computer separato, per cui è necessario eseguire il programma di installazione del server in tale computer separato per aggiornare la console. In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà la console di gestione.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Come aggiornare i server e i componenti del sistema</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiornare l'App-V Sequencer.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)">Come eseguire l'aggiornamento di Application Virtualization Sequencer</a></p></td>
</tr>
</tbody>
</table>



## Considerazioni aggiuntive sull'aggiornamento


-   Tutti i pacchetti di applicazioni virtuali sequenziati nella versione 4,2 non dovranno essere di nuovo sequenziati per l'uso con la versione 4,5. Tuttavia, è consigliabile aggiornare i pacchetti virtuali al formato di Microsoft Application Virtualization 4,5 se si desidera applicare elenchi di controllo di accesso (ACL) predefiniti o generare un file di Windows Installer. Si tratta di un processo semplice e richiede solo che il pacchetto di applicazione virtuale esistente venga aperto e salvato con l'App-V 4,5 Sequencer. Questa operazione può essere automatizzata usando l'interfaccia della riga di comando App-V Sequencer. Per altre informazioni, vedere [come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

-   Una delle caratteristiche del sequencer di 4,5 è la possibilità di creare file di Windows Installer (con estensione msi) come punti di controllo per l'interoperabilità dei pacchetti di applicazioni virtuali con sistemi ESD (Electronic Software Distribution), come Microsoft endpoint Configuration Manager. I file di Windows Installer precedenti creati con lo strumento MSI per la virtualizzazione delle applicazioni installato in un client App-V 4,1 o 4,2 che viene successivamente aggiornato a App-V 4,5 continueranno a funzionare, anche se non possono essere installati nel client App-V 4,5. Tuttavia, non possono essere rimossi o aggiornati a meno che non vengano aggiornati nel sequencer di App-V 4,5. Il pacchetto originale App-V precedente a 4,5 deve essere aperto nell'App-V 4,5 Sequencer e quindi salvato come file di Windows Installer.

    **Nota**  
    Se il client App-V 4,2 è già stato aggiornato a App-V 4,5, è possibile eseguire lo script di una soluzione alternativa per conservare i pacchetti della versione 4,2 nei client della versione 4,5 e consentire loro di gestirli. Questo script deve copiare due file, msvcp71.dll e msvcr71.dll, nella cartella di installazione di App-V e impostare i valori della chiave del registro di sistema seguenti nella chiave del registro di sistema: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

    "ClientVersion" = "4.2.1.20"

    "GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (una posizione di scrittura globale)



-   I file di Windows Installer generati dall'App-V 4,5 Sequencer visualizzano il messaggio di errore "questo pacchetto richiede Microsoft Application Virtualization Client 4,5 o versione successiva" quando si tenta di eseguirli in un client App-V 4,6. Aprire il vecchio pacchetto con l'App-V 4,5 SP1 Sequencer o l'App-V 4,6 Sequencer e generare un nuovo file MSI per il pacchetto.

-   Tutti i report di versione 4,2 creati e salvati verranno sovrascritti quando il server viene aggiornato alla versione 4,5. Se è necessario conservare questi report, è necessario salvare una copia di backup del file SftMMC. msc che si trova nella cartella di SoftGrid Management Console nel server e usare tale copia per sostituire il nuovo SftMMC. msc installato durante l'aggiornamento.

-   Per altre informazioni sull'aggiornamento dalle versioni precedenti, vedere [aggiornamento alle domande frequenti su Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## <a href="" id="app-v-4-6-client-package-support-"></a>Supporto del pacchetto client App-V 4,6


Puoi distribuire pacchetti creati in versioni precedenti di App-V ai client App-V 4,6. È tuttavia necessario modificare il file OSD associato in modo che includa le informazioni appropriate per il sistema operativo e l'architettura di chip. I valori seguenti possono essere usati:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valore OS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;VALORE OS = "Win2003TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALORE OS = "Win2003TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALORE OS = "Win2008TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALORE OS = "Win2008TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALORE OS = "Win2008R2TS64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALORE OS = "Win7"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALORE OS = "Win764"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALORE OS = "WinVista"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALORE OS = "WinVista64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALORE OS = "WinXP"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALORE OS = "WinXP64"/&gt;</p></td>
</tr>
</tbody>
</table>



Per eseguire un pacchetto di 32 bit appena creato, è necessario sequenziare l'applicazione in un computer che esegue un sistema operativo a 32 bit con l'App-V 4,6 Sequencer installato. Dopo aver sequenziato l'applicazione, nella console Sequencer fare clic sulla scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.

**Importante**  
Le applicazioni sequenziate in un computer che eseguono un sistema operativo a 64 bit devono essere distribuite nei computer che eseguono un sistema operativo a 64 bit. I nuovi pacchetti a 32 bit creati con l'App-V 4,6 Sequencer non vengono eseguiti nei computer che eseguono il client App-V 4,5.



Per eseguire nuovi pacchetti di 64 bit nel client App-V 4,6, è necessario sequenziare l'applicazione in un computer che esegue App-V 4,6 Sequencer e che esegue un sistema operativo a 64 bit. Dopo aver sequenziato l'applicazione, nella console Sequencer fare clic sulla scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.

La tabella seguente elenca le versioni client in cui verranno eseguiti i pacchetti creati con le varie versioni del sequencer.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Sequenziato tramite l'App-V 4,2 Sequencer</th>
<th align="left">Sequenziato tramite l'App-V 4,5 Sequencer</th>
<th align="left">Sequenziato tramite l'app 32 bit-V 4,6 Sequencer</th>
<th align="left">Sequenziato tramite l'app 64 bit-V 4,6 Sequencer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Client di 4,2</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,5 client ¹</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client di 4,6 (32 bit)</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client di 4,6 (64 bit)</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
</tbody>
</table>



¹ si applica a tutte le versioni del client App-V 4,5, tra cui App-V 4,5, App-V 4,5 CU1 e App-V 4,5 SP1.









