---
title: Configurazione del centro impostazioni società per UE-V 2. x
description: Configurazione del centro impostazioni società per UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823295"
---
# Configurazione del centro impostazioni società per UE-V 2. x


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 includono una nuova applicazione, il centro impostazioni società, che consente agli utenti di gestire le impostazioni per la sincronizzazione. Il centro impostazioni società viene installato con l'agente UE-V. Gli utenti accedono al centro impostazioni società nel pannello di controllo, nel menu **Start** o nella schermata **Start** e tramite l'icona dell'area di notifica UE-V. Il centro impostazioni società Visualizza le impostazioni sincronizzate e consente agli utenti di visualizzare lo stato di sincronizzazione di UE-V. Gli utenti possono usare il centro impostazioni società per selezionare le applicazioni o le funzionalità di Windows che sincronizzano le impostazioni tra i computer. Possono anche fare clic sul pulsante **Sincronizza ora** per sincronizzare tutte le impostazioni immediatamente. L'amministratore può anche includere un collegamento per il supporto nel centro impostazioni società.

## Informazioni sul centro impostazioni società


L'applicazione desktop del centro impostazioni società offre agli utenti informazioni sulla sincronizzazione delle impostazioni di UE-V. Il centro impostazioni società è accessibile in diversi modi:

-   Icona dell'area di notifica con l'impostazione di criteri di gruppo **icona vassoio** o configurazione di Windows PowerShell attivata, nell'area di notifica viene visualizzata l'icona UE-V. Fare clic sull'icona UE-V per aprire il centro impostazioni società.

    **Nota**  L'icona dell'area di notifica può essere disabilitata usando le impostazioni seguenti:

    -   Impostazione di criteri di gruppo: `Policy Tray Icon`

    -   Cmdlet di Windows PowerShell: `TrayIconEnabled`

    -   Elemento di configurazione nel pacchetto di configurazione UE-V per SystemCenter2012 ConfigurationManager: `Tray icon enabled`

     

-   Applicazione Pannello di controllo: nel pannello di controllo passare a **aspetto e personalizzazione**e quindi fare clic su **centro impostazioni società**.

-   Notifica primo utilizzo-se non disabilitato, l'agente UE-V avvisa l'utente che le impostazioni sono ora sincronizzate quando l'agente UE-V viene eseguito per la prima volta in un computer. Fare clic sulla finestra di dialogo notifica per aprire il centro impostazioni società.

-   La schermata **Start** o il menu **Start** include un collegamento al centro impostazioni società. Una ricerca per il centro impostazioni società trova l'applicazione.

## Configurazione del collegamento supporto nel centro impostazioni società


Il centro impostazioni società può includere un collegamento ipertestuale che gli utenti possono fare clic per ottenere supporto con i problemi di sincronizzazione delle impostazioni di UE-V. Questo collegamento può aprire qualsiasi protocollo URL valido, ad esempio http://per una pagina Web o mailto://per un messaggio di posta elettronica. Il collegamento supporto può essere configurato tramite criteri di gruppo, Windows PowerShell o il pacchetto di configurazione di System Center 2012 Configuration Manager UE-V.

**Come configurare il collegamento supporto per il centro impostazioni società**

1.  Aprire lo strumento di gestione preferito:

    -   **Criteri di gruppo** : se non è già stato fatto, scaricare il modello ADMX per la versione UE-V 2 da [modelli amministrativi di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).

    -   **Windows PowerShell** : in un computer con l'agente UE-V installato aprire **Windows PowerShell**. Per altre informazioni sull'amministrazione di UE-V tramite Windows PowerShell, vedere [amministrazione di UE-v 2. x con Windows PowerShell e WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).

    -   **System Center 2012 Configuration Pack per Microsoft User Experience Virtualization (UE-v)** -importare il pacchetto di configurazione UE-v e seguire la documentazione del pacchetto di configurazione per creare elementi di configurazione. Per altre informazioni sul pacchetto di configurazione UE-V, vedere [configurazione di UE-v 2. x con System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

2.  Modificare le impostazioni per i criteri seguenti:

    -   **Contattare il testo del collegamento it** -questa impostazione specifica il testo del collegamento ipertestuale URL contatto nel centro impostazioni società. Se si abilita questa impostazione, il centro impostazioni società Visualizza il testo specificato nel collegamento all'URL del contatto.

        -   Impostazioni di criteri di gruppo: `Contact IT Link Text`

        -   Cmdlet di Windows PowerShell: `ContactITDescription`

        -   Elemento di configurazione del pacchetto di configurazione: `IT contact descriptive text`

    -   **URL del contatto it** -questa impostazione specifica l'URL per il collegamento contatto it nel centro impostazioni società in un protocollo URL valido, ad esempio http://per una pagina web o mailto://per un messaggio di posta elettronica.

        -   Impostazioni di criteri di gruppo: `Contact IT URL`

        -   Cmdlet di Windows PowerShell: `ContactITUrl`

        -   Elemento di configurazione del pacchetto di configurazione: `IT contact URL`

3.  Distribuire le impostazioni ai computer degli utenti usando lo strumento di gestione.






 

 





