---
title: Creazione di un'immagine di Windows Virtual PC per MED-V
description: Creazione di un'immagine di Windows Virtual PC per MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804413"
---
# Creazione di un'immagine di Windows Virtual PC per MED-V


Prima di poter consegnare un'area di lavoro MED-V agli utenti, è necessario prima di tutto preparare un disco rigido virtuale che si usa per creare il pacchetto di installazione dell'area di lavoro MED-V per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. Per preparare il disco rigido virtuale necessario, è necessario creare un'immagine di PC virtuale Windows che contiene il sistema operativo, gli aggiornamenti e il software necessari per consentire di distribuire in seguito le informazioni di reindirizzamento degli URL e delle applicazioni agli utenti. In questa sezione vengono fornite indicazioni su come creare il disco rigido virtuale.

Per creare un'immagine virtuale per MED-V, è necessario seguire questa procedura.

1.  [Creare un'immagine di Windows Virtual PC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [Installare Windows XP nell'immagine](#bkmk-installingwindowsxpontovpc)

3.  [Installare .NET Framework nell'immagine](#bkmk-installingnet)

4.  [Applicare gli aggiornamenti all'immagine](#bkmk-applypatchestovpc)

5.  [Installare i componenti di integrazione](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Creazione di un'immagine di Windows Virtual PC


Per creare un'immagine di Windows Virtual PC, vedere la documentazione di Windows Virtual PC:

-   [Home page di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .

-   [Guida di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

In alternativa, se si ha già un file Windows Imaging (WIM) che si vuole usare come base per l'immagine virtuale, è possibile convertirlo in un VHD che si usa per creare l'area di lavoro MED-V. Per altre informazioni su come convertire un WIM in un disco rigido virtuale, vedere [supporto del VHD nativo in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .

**Importante**  MED-V supporta solo un disco rigido virtuale per ogni macchina virtuale e una sola partizione in ogni disco virtuale.

 

Dopo aver creato il disco rigido virtuale, installare Windows XP nell'immagine.

## <a href="" id="bkmk-installingwindowsxpontovpc"></a>Installazione di Windows XP in un'immagine di Windows Virtual PC


MED-V richiede che Windows XP SP3 sia installato nell'immagine PC virtuale Windows prima di creare l'area di lavoro MED-V.

Per altre informazioni su come installare Windows XP, vedere [creare una macchina virtuale e installare un sistema operativo guest](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .

## <a href="" id="bkmk-installingnet"></a>Installazione di .NET Framework 3,5 SP1 in un'immagine di Windows Virtual PC


È necessario installare manualmente .NET Framework 3,5 SP1 e l'aggiornamento di KB959209 nell'immagine di Windows Virtual PC preparata per l'uso con MED-V. L'aggiornamento [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) affronta diversi problemi noti di compatibilità delle applicazioni.

## <a href="" id="bkmk-applypatchestovpc"></a>Applicazione degli aggiornamenti all'immagine di Windows Virtual PC


Dopo aver installato Windows XP nella propria macchina virtuale, installare gli aggiornamenti necessari di Windows XP nell'immagine, ad esempio SP3. È anche possibile installare alcuni aggiornamenti facoltativi per migliorare le prestazioni.

**Importante**  MED-V richiede che Windows XP SP3 sia in uso nel sistema operativo guest.

 

**Avviso**  Quando si installano gli aggiornamenti in Windows XP, assicurarsi di rimanere nella versione di Internet Explorer nell'ospite che si intende usare nell'area di lavoro MED-V. Ad esempio, se si intende eseguire Internet Explorer 6 nell'area di lavoro MED-V, verificare che gli eventuali aggiornamenti installati non includano Internet Explorer 7 o Internet Explorer 8. Inoltre, è consigliabile configurare il registro di sistema per evitare aggiornamenti automatici dall'aggiornamento di Internet Explorer.

 

### Installazione di un aggiornamento delle prestazioni facoltativo

Anche se è facoltativo, è consigliabile installare il seguente aggiornamento per l' [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) . Questo aggiornamento aumenta le prestazioni delle cartelle condivise in una sessione di Servizi terminal:

**Nota**  L'aggiornamento è pubblicamente disponibile. Tuttavia, potrebbe essere richiesto di accettare un contratto per i servizi Microsoft. Seguire le istruzioni sulle pagine Web successive per recuperare questo hotfix.

 

### Configurazione di un aggiornamento delle prestazioni di criteri di gruppo

Per impostazione predefinita, i criteri di gruppo vengono scaricati in un computer un byte alla volta. Ciò causa ritardi durante l'aggiunta di MED-V al dominio. Per aumentare le prestazioni dei criteri di gruppo, impostare il valore della chiave del registro di sistema seguente nel registro di sistema:

Sottochiave del registro di sistema: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Voce: BufferPolicyReads

Digitare: DWORD

Valore: 1

## <a href="" id="bkmk-installintegration"></a>Installazione di componenti di integrazione


Windows Virtual PC include il pacchetto componenti integrativi. In questo articolo vengono fornite caratteristiche che migliorano l'interazione tra l'ambiente virtuale e il computer fisico. Ad esempio, il pacchetto componenti integrativi consente di passare al mouse tra l'host e i computer guest.

**Importante**  MED-V richiede l'installazione del pacchetto componenti integrativi.

 

Quando si configura l'immagine virtuale per l'uso con MED-V, è necessario installare manualmente il pacchetto componenti integrativi nel sistema operativo guest per rendere disponibili le caratteristiche di integrazione.

Per altre informazioni su come installare e usare il pacchetto componenti integrativi, vedere quanto segue:

-   [Installare o aggiornare il pacchetto componenti integrativi](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .

-   [Informazioni sulle caratteristiche di integrazione](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .

### Installazione di aggiornamento RemoteApp

Dopo aver installato il pacchetto componenti integrativi, viene chiesto di installare l'aggiornamento seguente: "aggiornamento per Windows XP SP3 per abilitare RemoteApp". Questo è un componente obbligatorio per MED-V.

**Importante**  Se non viene chiesto di installare l'aggiornamento RemoteApp, è necessario scaricarlo e installarlo manualmente. Per altre informazioni e istruzioni su come scaricare questo aggiornamento, vedere [aggiornamento per Windows XP SP3 per abilitare RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .

 

### Abilitazione del desktop remoto

Per impostazione predefinita, il desktop remoto è abilitato dopo l'installazione del pacchetto componenti integrativi. Affinché MED-V sia operativo, verificare che desktop remoto sia abilitato e non distribuire criteri di gruppo che la disabilitano.

Per informazioni su come abilitare Desktop remoto, vedere [abilitare o disabilitare Desktop remoto](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .

## Personalizzazione di Internet Explorer tramite il kit di amministrazione di Internet Explorer


Se si vuole, è possibile usare Internet Explorer Administration Kit per personalizzare Internet Explorer nel sistema operativo guest. Per altre informazioni, vedere il [Kit di amministrazione e la guida alla distribuzione di Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).

**Avviso**  È consigliabile considerare i problemi di sicurezza associati alla personalizzazione di Internet Explorer nell'area di lavoro MED-V. Per altre informazioni, vedere [procedure consigliate per la sicurezza per le operazioni MED-V](security-best-practices-for-med-v-operations.md).

 

Dopo aver installato il disco rigido virtuale con un sistema operativo guest aggiornato, è possibile installare le applicazioni nell'immagine.

## Argomenti correlati


[Installazione di applicazioni in un'immagine di Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md)

[Configurazione di un'immagine di Windows Virtual PC per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





