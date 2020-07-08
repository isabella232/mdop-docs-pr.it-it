---
title: Scenario di operazioni end-to-end per MED-V 2.0
description: Scenario di operazioni end-to-end per MED-V 2.0
author: dansimp
ms.assetid: 1d87f5f3-9fc5-4731-8bd1-c155714f34ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90a7c2135ad27040ed87dac980b67321eb771574
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826166"
---
# Scenario di operazioni end-to-end per MED-V 2.0


Questo scenario di esempio per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di distribuire e gestire MED-V usando più scenari da capo a fine. Questo scenario di esempio può essere considerato un caso di studio che consente di inserire i singoli scenari e le singole procedure nel contesto.

Questa sezione fornisce informazioni di base e indicazioni per la creazione, la distribuzione e la gestione delle aree di lavoro MED-V come soluzione end-to-end nell'organizzazione.

## Scenario dettagliato delle operazioni MED-V


Le procedure dettagliate seguite in uno scenario di operazioni MED-V includono le seguenti:

-   La [creazione di un'immagine di PC virtuale Windows per MED-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc) consente di creare e configurare un'immagine di PC virtuale Windows per MED-v. Prima di poter consegnare un'area di lavoro MED-V agli utenti, è necessario prima di tutto preparare un disco rigido virtuale (VHD) che si usa per creare il pacchetto di installazione dell'area di lavoro MED-V per MED-V.

-   La [creazione di un'immagine di Windows Virtual PC per MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingwindowsxpontovpc) consente di installare il sistema operativo Windows XP SP3 nell'immagine del PC virtuale Windows. MED-V richiede che Windows XP SP3 sia installato nell'immagine PC virtuale Windows prima di creare l'area di lavoro MED-V.

-   La [creazione di un'immagine di PC virtuale Windows per MED-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingnet) consente di installare manualmente .net Framework 3,5 SP1 e l'aggiornamento di KB959209 nell'immagine di Windows Virtual PC preparata per l'uso con Med-v. MED-V richiede .NET Framework 3,5 SP1 e l'aggiornamento [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) affronta diversi problemi noti di compatibilità delle applicazioni.

-   La [creazione di un'immagine di Windows Virtual PC per MED-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-applypatchestovpc) consente di aggiornare l'immagine di Windows XP con gli aggiornamenti software più recenti e gli altri hotfix necessari o importanti per l'uso di Med-v.

-   La [creazione di un'immagine di PC virtuale Windows per MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installintegration) consente di installare il pacchetto componenti integrativi nell'immagine di Windows XP. Queste caratteristiche consentono di migliorare l'interazione tra l'ambiente virtuale e il computer fisico.

-   [L'installazione di applicazioni in un'immagine di Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md) consente di installare alcuni tipi di software nell'immagine di Windows XP utili quando si esegue MED-V, ad esempio un sistema di distribuzione del software elettronico e un software antivirus.

-   La [configurazione di un'immagine PC virtuale di Windows per MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md) illustra come configurare l'immagine usando Sysprep per assicurarsi che sia pronta per l'uso con Med-v. L'immagine MED-V preparata viene quindi usata per creare il pacchetto dell'area di lavoro MED-V.

-   [Creare un pacchetto di area di lavoro MED-v](create-a-med-v-workspace-package.md) come creare il pacchetto dell'area di lavoro MED-v distribuito in tutta l'organizzazione. Si distribuisce il pacchetto dell'area di lavoro MED-V per installare l'area di lavoro MED-V nei computer degli utenti finali. Un'area di lavoro MED-V è l'ambiente desktop Windows XP da cui gli utenti finali interagiscono con la macchina virtuale fornita da MED-V.

-   [Il test del pacchetto area di lavoro MED-v](testing-the-med-v-workspace-package.md) illustra come creare un ambiente di test in cui è possibile testare la funzionalità del pacchetto dell'area di lavoro MED-v, ad esempio le impostazioni di configurazione per la prima volta e la pubblicazione dell'applicazione. Dopo aver completato il test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuirlo in tutta l'organizzazione.

-   [La distribuzione del pacchetto area di lavoro MED-v](deploying-the-med-v-workspace-package.md) descrive come distribuire l'area di lavoro MED-v usando un sistema di distribuzione elettronica del software o in un'immagine di Windows 7. Oppure, se si preferisce, questa sezione illustra anche come distribuire manualmente l'area di lavoro MED-V.

-   Le [aree di lavoro di monitor Med-v](monitor-med-v-workspaces.md) spiegano come monitorare la distribuzione delle aree di lavoro MED-v per determinare se la configurazione per la prima volta è stata completata correttamente. Il monitoraggio del successo della configurazione iniziale è importante perché MED-V non è in uno stato utilizzabile finché la configurazione iniziale non è stata completata correttamente. Questa sezione Mostra anche che puoi configurare l'ambiente per rilevare le modifiche alla rete che possono influire su MED-V.

-   [Gestire le applicazioni di area di lavoro MED-v](manage-med-v-workspace-applications.md) consente di installare e rimuovere o pubblicare e annullare la pubblicazione di applicazioni in un'area di lavoro MED-v distribuita. Questa sezione illustra anche come aggiornare manualmente il software in un'area di lavoro MED-V e come gestire gli aggiornamenti automatici. L'area di lavoro MED-V è una macchina virtuale che contiene un sistema operativo distinto il cui processo di aggiornamento automatico del software deve essere gestito esattamente come i computer fisici dell'organizzazione.

-   Gestire le recensioni di [Reindirizzamento URL di Med-v](manage-med-v-url-redirection.md) come aggiungere e rimuovere le impostazioni di reindirizzamento degli indirizzi Web nell'area di lavoro MED-v distribuita. È possibile aggiungere o rimuovere le informazioni di reindirizzamento degli URL tramite il registro di sistema oppure ricostruendo l'area di lavoro MED-V. È anche possibile usare la procedura guidata in Packager area di lavoro MED-V per gestire il reindirizzamento degli indirizzi Web.

-   [Gestire le impostazioni di area di lavoro MED-v](manage-med-v-workspace-settings.md) come visualizzare e modificare le impostazioni di configurazione di Med-v tramite Packager area di lavoro MED-v. Questa sezione elenca tutte le chiavi del registro di sistema MED-V configurabili e include il tipo, l'impostazione predefinita e la descrizione di ognuno. Questa sezione include anche informazioni su come gestire le stampanti nelle aree di lavoro MED-V. In MED-V 2,0, il reindirizzamento della stampante offre agli utenti un'esperienza di stampa coerente tra la macchina virtuale MED-V e il computer host.

## Argomenti correlati


[Operazioni per MED-V](operations-for-med-v.md)

[Scenario di pianificazione end-to-end per MED-V 2.0](end-to-end-planning-scenario-for-med-v-20.md)

[Scenario di distribuzione end-to-end per MED-V 2.0](end-to-end-deployment-scenario-for-med-v-20.md)

 

 





