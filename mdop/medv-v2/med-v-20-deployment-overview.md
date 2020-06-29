---
title: Panoramica della distribuzione di MED-V 2.0
description: Panoramica della distribuzione di MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826106"
---
# Panoramica della distribuzione di MED-V 2.0


Questa sezione contiene informazioni generali e istruzioni su come installare e distribuire Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Panoramica


MED-V 2,0 si basa su un modello di applicazione, in cui è possibile usare gli stessi metodi usati per distribuire le applicazioni per la distribuzione e la gestione di MED-V. Una soluzione MED-V distribuita include due componenti: l'agente host MED-V e l'agente guest. L'agente host MED-V è installato sul desktop di Windows 7 e l'agente guest MED-V viene installato in Windows XP all'interno dell'area di lavoro MED-V. MED-V include anche un Packager area di lavoro MED-V che fornisce le informazioni e gli strumenti necessari per la creazione e la configurazione delle aree di lavoro MED-V.

**Importante**  
MED-V supporta solo l'installazione di Packager area di lavoro MED-V, dell'agente host MED-V e dell'area di lavoro MED-V per tutti gli utenti. L'installazione di MED-V per l'utente corrente selezionando **ALLUSERS = ""** causa errori nell'installazione dei componenti e nella configurazione dell'area di lavoro MED-v.



### File di installazione di MED-V

MED-V include i file di installazione seguenti, necessari per l'uso di MED-V:

**File di installazione dell'agente host MED-V**

Il file di installazione dell'agente host è denominato MED-V\_HostAgent\_Setup.exe. Questo file è distribuito e installato in ogni computer dell'utente finale pertinente nell'ambito della distribuzione a livello aziendale di MED-V.

**File di installazione del Packager area di lavoro MED-V**

Il file di installazione del Packager area di lavoro MED-V è denominato MED-V\_WorkspacePackager\_Setup.exe. Usare questo file per installare il Packager area di lavoro MED-V in un computer in cui sono presenti i diritti e le autorizzazioni di amministratore. L'amministratore desktop usa il Packager area di lavoro MED-V per creare e gestire aree di lavoro MED-V.

**Nota**  
L'agente guest MED-V viene installato automaticamente durante la configurazione per la prima volta.



### Processo di distribuzione di MED-V

Di seguito è riportata una panoramica di alto livello sul processo di installazione e distribuzione di MED-V:

1.  Installare il Packager area di lavoro MED-V nel computer in cui sono presenti credenziali amministrative e che verrà usato per compilare i pacchetti dell'area di lavoro MED-V. Per altre informazioni, vedere [come installare il Packager area di lavoro MED-V](how-to-install-the-med-v-workspace-packager.md).

2.  Preparare l'immagine MED-V e creare i pacchetti dell'area di lavoro MED-v tramite Packager area di lavoro MED-V. Per altre informazioni, vedere [operazioni per MED-V](operations-for-med-v.md).

3.  Distribuire i componenti MED-V necessari in tutta l'organizzazione. I componenti necessari di MED-V sono Windows Virtual PC, l'agente host MED-V e l'area di lavoro MED-V.

**Importante**  
L'installazione dei componenti MED-V richiede le credenziali amministrative. Se un utente finale sta installando MED-V, viene chiesto di immettere le credenziali amministrative. In alternativa, le credenziali amministrative possono essere fornite nel contesto se si sta eseguendo l'installazione usando un sistema ESD (Electronic Software Distribution).



### Componenti MED-V

I componenti MED-V distribuiti in tutta l'organizzazione sono conformi alle seguenti:

**Windows Virtual PC**

Funzioni MED-V all'interno di immagini PC virtuali Windows per la soluzione di compatibilità. Sono necessari Windows Virtual PC e l'aggiornamento per Windows 7 (KB977206). Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

**File di installazione dell'agente host MED-V**

MED-V\_HostAgent\_Setup.exe.

**File di installazione dell'area di lavoro MED-V**

I file di installazione dell'area di lavoro MED-V vengono creati quando si compila il pacchetto dell'area di lavoro MED-V che è costituito dai seguenti:

Un programma eseguibile setup.exe che esegue l'installazione dell'area di lavoro MED-V

Un &lt; programma di installazione di MED-V \ _workspace \ _name &gt; . msi

Un &lt; VHD \ _filename &gt; file MEDV, che è il disco rigido virtuale compresso

File per le impostazioni di configurazione ( &lt; area di lavoro \ _name &gt; . reg e &lt; Workspace \ _name &gt; . ps1)

Per distribuire MED-V, copiare tutti i file di installazione necessari nel computer host o in una condivisione a cui è possibile accedere dal computer host. Eseguire i file di installazione del componente per Windows Virtual PC, l'agente host MED-V e l'area di lavoro MED-V. Avviare quindi l'agente host MED-V per completare la prima configurazione di MED-V.

È possibile eseguire l'installazione manualmente. Tuttavia, ti consigliamo di usare un metodo di distribuzione elettronica del software per automatizzare la distribuzione dei componenti. Per altre informazioni, vedere [come distribuire un'area di lavoro MED-V tramite un sistema di distribuzione elettronica del software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).

**Nota**  
Per informazioni sugli argomenti della riga di comando disponibili per controllare le opzioni di installazione, vedere [Opzioni della riga di comando per i file di installazione di MED-V](command-line-options-for-med-v-installation-files.md).



## Passaggi di distribuzione


Quando si distribuisce MED-V in tutta l'organizzazione, sono presenti due considerazioni principali: installazione e configurazione per la prima volta.

### Installazione

1.  **Windows Virtual PC** -durante l'installazione, MED-V controlla Windows Virtual PC e il relativo aggiornamento necessario per Windows 7 (KB977206). Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    È possibile installare questi come parte delle installazioni di Windows 7 prima di installare MED-V oppure installarli come parte della distribuzione MED-V. Tuttavia, MED-V non include un meccanismo per la distribuzione; devono essere distribuiti usando un sistema ESD (Electronic Software Distribution) o come parte dell'immagine di Windows 7.

    **Importante**  
    Quando si installano i componenti MED-V usando un file batch, è consigliabile specificare che Windows Virtual PC e Windows Virtual PC hotfix sono installati dopo l'agente host MED-V e i file del pacchetto dell'area di lavoro MED-V. Questo significa che Windows Update non causerà interferenze con il processo di installazione richiedendo un riavvio.



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. **Agente host MED-v** : installare l'agente host MED-v nel computer Windows 7 in cui verrà eseguito MED-v. Questa operazione deve essere installata prima di installare l'area di lavoro MED-V e verificare che sia installato Windows Virtual PC.

3. **Area di lavoro MED-v** : i file necessari per l'installazione vengono creati tramite il Packager area di lavoro MED-v, ovvero i file setup.exe, MEDV e MSI. Per installare l'area di lavoro MED-V, eseguire setup.exe; Questo trigger gli altri file come richiesto. L'installazione inserisce una voce nel registro di sistema sotto la chiave di esecuzione del computer locale per avviare l'agente host MED-V, che esegue sempre MED-V quando si avvia Windows.

   **Importante**  
   L'installazione dell'area di lavoro MED-V può essere eseguita in modo interattivo dall'utente finale o silenziosamente attraverso un sistema di distribuzione elettronica del software. L'installazione dell'area di lavoro MED-V richiede le credenziali amministrative, pertanto gli utenti finali devono essere amministratori dei loro computer per installare l'area di lavoro MED-V. In alternativa, un sistema di distribuzione del software elettronico viene eseguito in genere nel contesto di sistema e dispone di autorizzazioni sufficienti.



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### Configurazione per la prima volta

Dopo aver installato MED-V e i componenti necessari, è necessario configurare MED-V. La configurazione di MED-V è nota come configurazione per la prima volta. Usando il **Packager area di lavoro MED-V**puoi configurare la configurazione per la prima volta per l'esecuzione silenziosa o interattiva. La configurazione per la prima volta di MED-V richiede agli utenti finali di immettere la propria password per l'autenticazione nell'area di lavoro MED-V, ma in caso contrario può essere quasi invisibile per l'utente. Le notifiche vengono visualizzate nell'area di notifica, ad esempio quando la configurazione per la prima volta è completa e le applicazioni sono pronte. Di seguito sono riportate le azioni che si verificano durante la configurazione per la prima volta di MED-V:

1.  Il disco rigido virtuale deve essere configurato. La configurazione minima viene eseguita ed espande l'immagine di Windows XP. In genere, questo problema si verifica in una finestra nascosta, ma è possibile configurare MED-V per la visualizzazione durante questa configurazione.

2.  Al termine della configurazione minima, è possibile eseguire i comandi che è necessario avere per la configurazione aggiuntiva, ad esempio l'installazione del software ESD o di altre applicazioni o la configurazione dell'immagine. Queste operazioni possono essere chiamate nel file Sysprep. inf, ma non sono necessarie. Per altre informazioni, vedere [configurazione di un'immagine PC virtuale Windows per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

3.  Ftscompletion.exe viene eseguito come ultimo passaggio della configurazione. Questo processo completa la configurazione MED-V, aggiunge l'utente al gruppo RDP per consentire loro di accedere all'area di lavoro MED-V, copia i registri, segnala a MED-V che l'area di lavoro MED-V è pronta e quindi riavvia l'area di lavoro MED-V. Questo processo può anche aggiungere l'utente come amministratore dell'area di lavoro MED-V se è stato configurato quando è stata creata l'area di lavoro MED-V. Ftscompletion.exe viene in genere chiamato tramite il file Sysprep, inf, ma può essere eseguito anche tramite un altro metodo, ad esempio uno script. Tuttavia, Ftscompletion.exe deve essere l'ultima azione eseguita quando la workstation è configurata. Per altre informazioni, vedere [configurazione di un'immagine PC virtuale Windows per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

4.  Dopo aver riavviato l'area di lavoro MED-V Ftscompletion.exe, l'utente finale ha eseguito l'accesso. Se non è stata salvata la password durante la configurazione per la prima volta, viene chiesto di nuovo. L'area di lavoro MED-V viene quindi avviata e configurata per l'utente. La configurazione include l'applicazione di criteri di gruppo.

    È consigliabile applicare solo i criteri che hanno senso in un ambiente di compatibilità delle applicazioni per Windows XP. I criteri di personalizzazione desktop, ad esempio, in genere non devono essere applicati e devono essere disabilitati. Per altre informazioni su come consentire solo i profili locali, vedere [impostazioni di criteri di gruppo per i profili utente mobili](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

Dopo aver completato la configurazione per la prima volta, l'utente finale riceverà una notifica che le applicazioni pubblicate sono pronte. Sono quindi in grado di accedere alle applicazioni installate nell'area di lavoro MED-V dal menu **Start** .

## Argomenti correlati


[Preparare l'ambiente di distribuzione per MED-V](prepare-the-deployment-environment-for-med-v.md)

[Distribuzione di MED-V](deployment-of-med-v.md)









