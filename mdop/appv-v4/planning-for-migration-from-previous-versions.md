---
title: Pianificazione della migrazione da versioni precedenti
description: Pianificazione della migrazione da versioni precedenti
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815926"
---
# Pianificazione della migrazione da versioni precedenti


Prima di provare a eseguire l'aggiornamento a Microsoft Application Virtualization 4.5 o versioni successive, è necessario aggiornare una versione precedente a 4.1 alla versione 4.1. È consigliabile pianificare prima di tutto aggiornare i client e quindi aggiornare i componenti del server. I client che sono stati aggiornati a 4.5 continueranno a funzionare con i server di virtualizzazione delle applicazioni che non sono ancora stati aggiornati. Le versioni precedenti del client non sono supportate nei server che sono stati aggiornati a 4.5. Per altre informazioni sull'aggiornamento dei componenti di sistema, vedere [considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni](application-virtualization-deployment-and-upgrade-considerations.md).

Per garantire una migrazione efficace, i componenti del sistema di virtualizzazione dell'applicazione devono essere aggiornati nell'ordine seguente:

1.  **Client di Microsoft Application Virtualization.** Per istruzioni dettagliate sull'aggiornamento, vedere [come aggiornare l'Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).

2.  **Server e database di Microsoft Application Virtualization.** Per istruzioni dettagliate sull'aggiornamento, vedere [come aggiornare i server e i componenti di sistema](how-to-upgrade-the-servers-and-system-components.md).

    **Nota**  Se si dispone di più di un server per l'accesso alla rete di virtualizzazione dell'applicazione, è necessario che tutti questi server vengano disattivati durante l'aggiornamento del database. È consigliabile seguire le normali procedure aziendali per l'aggiornamento del database, ma è consigliabile testare l'aggiornamento del database usando una copia di backup del database per la prima volta in un server di test. Devi quindi selezionare uno dei server per il primo aggiornamento, che aggiornerà lo schema del database. Dopo che il database di produzione è stato aggiornato correttamente, è possibile aggiornare gli altri server.

     

3.  **Servizio Web Microsoft Application Virtualization Management.** Questo passaggio si applica solo se il servizio Web di gestione si trova in un server distinto, che richiede l'esecuzione del programma di installazione del server nel server separato per l'aggiornamento del servizio Web. In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà automaticamente il servizio Web di gestione.

4.  **Microsoft Application Virtualization Management Console.** Questo passaggio si applica solo se la console di gestione si trova in un computer separato, per cui è necessario eseguire il programma di installazione del server in tale computer separato per aggiornare la console. In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà la console di gestione.

5.  **Microsoft Application Virtualization Sequencer.** Per istruzioni dettagliate, vedere [come installare Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md). Tutti i pacchetti di applicazioni virtuali sequenziati nella versione 4.2 non dovranno essere risequenziati per l'uso con la versione 4.5. Tuttavia, è consigliabile aggiornare i pacchetti virtuali al formato Microsoft Application Virtualization 4.5 se si desidera applicare elenchi di controllo di accesso (ACL) predefiniti o generare un file di Windows Installer. Si tratta di un processo semplice e richiede solo che il pacchetto di applicazione virtuale esistente venga aperto e salvato con il sequencer 4.5. Questo può essere automatizzato usando l'interfaccia della riga di comando di Application Virtualization Sequencer.

## <a href="" id="app-v-4-6-client-package-support-"></a>Supporto del pacchetto client App-V 4.6


Puoi distribuire pacchetti creati in versioni precedenti di client App-V a App-V 4.6. È tuttavia necessario modificare il file **OSD** associato in modo che includa le informazioni appropriate per il sistema operativo e l'architettura di chip. Usare i valori seguenti.

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

 

Per eseguire un pacchetto di 32 bit appena creato, è necessario sequenziare l'applicazione in un computer che esegue un sistema operativo a 32 bit con l'App-V 4.6 Sequencer installato. Dopo aver sequenziato l'applicazione, nella console sequencer selezionare la scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.

**Importante**  Le applicazioni sequenziate in un computer che eseguono un sistema operativo a 64 bit devono essere distribuite nei computer che eseguono un sistema operativo a 64 bit. I nuovi pacchetti a 32 bit creati con l'App-V 4.6 Sequencer non verranno eseguiti nei computer che eseguono il client App-V 4,5.

 

Per eseguire nuovi pacchetti a 64 bit nel client App-V 4.6, è necessario sequenziare l'applicazione in un computer che esegue App-V 4.6 Sequencer e che esegue un sistema operativo a 64 bit. Dopo aver sequenziato l'applicazione, nella console sequencer selezionare la scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.

La tabella seguente elenca le versioni client in cui verranno eseguiti i pacchetti creati con le varie versioni del sequencer.

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
<th align="left"></th>
<th align="left">Sequenziato tramite l'App-V 4,2 Sequencer</th>
<th align="left">Sequenziato tramite l'App-V 4,5 Sequencer</th>
<th align="left">Sequenziato tramite l'app 32 bit-V 4,6 Sequencer</th>
<th align="left">Sequenziato tramite l'app 64 bit-V 4,6 Sequencer</th>
<th align="left">Sequenziato tramite il sequencer App-V 4,6 SP1 di 32 bit</th>
<th align="left">Sequenziato tramite il sequencer App-V 4,6 SP1 di 64 bit</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Client di 4,2</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
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
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client di 4,6 (32 bit)</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client di 4,6 (64 bit)</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client SP1 di 4,6</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client di 4,6 SP1 (64 bit)</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
</tbody>
</table>

 

¹ si applica a tutte le versioni del client App-V 4.5, tra cui App-V 4.5, App-V 4.5 CU1 e App-V 4.5 SP1.

## Considerazioni aggiuntive sulla migrazione


Una delle caratteristiche dell'App-V 4.5 Sequencer è la possibilità di creare file di Windows Installer (con estensione msi) come punti di controllo per l'interoperabilità dei pacchetti di applicazioni virtuali con sistemi ESD (Electronic Software Distribution), come Microsoft endpoint Configuration Manager. I file di Windows Installer precedenti creati con lo strumento MSI per la virtualizzazione delle applicazioni installati in un client App-V 4.1 o 4.2 che viene successivamente aggiornato a 4.5 continueranno a funzionare, anche se non possono essere installati nel client 4.5. Tuttavia, non possono essere rimossi o aggiornati a meno che non vengano aggiornati nel sequencer 4.5. Il pacchetto di applicazione virtuale pre-4,5 originale deve essere aperto nel sequencer 4.5 e quindi salvato come file di Windows Installer.

**Nota**  Se il client App-V 4.2 è già stato aggiornato a 4.5, è possibile usare lo script come soluzione alternativa per conservare i 4.2 pacchetti in 4,5 client e consentire loro di gestirli. Questo script deve copiare due file, msvcp71.dll e msvcr71.dll, nella cartella di installazione di App-V e impostare i valori della chiave del registro di sistema seguenti nella chiave del registro di sistema \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

"ClientVersion" = "4.2.1.20"

"GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (una posizione di scrittura globale)

 

I file di Windows Installer generati dall'App-V 4,5 Sequencer visualizzano il messaggio di errore "questo pacchetto richiede Microsoft Application Virtualization Client 4,5 o versione successiva" quando si tenta di eseguirli in un client App-V 4,6. Aprire il vecchio pacchetto con l'App-V 4,5 SP1 Sequencer o l'App-V 4,6 Sequencer e generare un nuovo file MSI per il pacchetto.

Tutti i report 4.2 creati e salvati verranno sovrascritti quando il server viene aggiornato a 4.5. Se è necessario conservare questi report, è necessario salvare una copia di backup del file SftMMC. msc che si trova nella cartella di SoftGrid Management Console nel server e usare tale copia per sostituire il nuovo SftMMC. msc installato durante l'aggiornamento.

Per altre informazioni sull'aggiornamento dalle versioni precedenti, vedere [aggiornamento alle domande frequenti su Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## Argomenti correlati


[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 





