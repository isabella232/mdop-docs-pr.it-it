---
title: Pianificazione della distribuzione di Application Virtualization Client
description: Pianificazione della distribuzione di Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815955"
---
# Pianificazione della distribuzione di Application Virtualization Client


Dopo aver deciso come pubblicare e distribuire pacchetti di applicazioni virtuali nei computer degli utenti finali, è consigliabile pianificare la distribuzione del software Application Virtualization Client.

Il client di virtualizzazione dell'applicazione è il componente che esegue effettivamente le applicazioni virtuali. L'Application Virtualization Client consente agli utenti di interagire con le icone e fare doppio clic su tipi di file per avviare un'applicazione virtuale. Gestisce anche il flusso del contenuto dell'applicazione da un server di flusso e lo memorizza nella cache prima di avviare l'applicazione. Il contenuto dell'applicazione è strutturato in modo che tutto il contenuto necessario per avviare l'applicazione e gestire l'interazione iniziale dell'utente venga trasmesso prima al computer dell'utente finale. Esistono due tipi diversi di software client per la virtualizzazione delle applicazioni: client di virtualizzazione delle applicazioni per Servizi Desktop remoto (in precedenza Servizi terminal), usato nei sistemi server Host sessione Desktop remoto (host RDSession) e nel client Desktop Application Virtualization, usato per tutti gli altri computer.

Il client di virtualizzazione dell'applicazione deve essere configurato in fase di installazione, nella console di gestione di Application Virtualization o tramite la riga di comando del programma di installazione, con una serie di impostazioni importanti, incluse le seguenti:

-   Posizioni delle icone per tutte le applicazioni.

-   Posizione del file OSD che contiene le informazioni sulla definizione del pacchetto.

-   Origine contenuto applicazione.

-   Protocollo di comunicazione da usare per il recupero degli elementi precedenti.

-   Metodo di gestione della dimensione della cache e della dimensione della cache da usare.

Per velocizzare la distribuzione del software Application Virtualization Client quando si usa una soluzione ESD (Electronic Software Distribution), le impostazioni precedenti devono essere definite con attenzione in anticipo. Questo aspetto è particolarmente importante quando si hanno computer in uffici diversi, in cui i client devono essere configurati per l'uso di percorsi di origine diversi.

**Nota**  
-   La posizione dell'icona e i valori dei file OSD sono un fattore importante da tenere in considerazione quando si sceglie il metodo di pubblicazione, se si usa Windows Installer o SFTMIME. L'impostazione per l'origine del contenuto dell'applicazione è definita dal metodo di flusso scelto.

-   Per assicurarti che la cache disponga di spazio sufficiente per tutti i pacchetti che potrebbero essere distribuiti, usa l'impostazione **USA soglia di spazio libero su disco** quando configuri il client in modo che la cache possa crescere in base alle esigenze. In alternativa, determinare in anticipo la quantità di spazio su disco necessaria per la cache di App-V e, al momento dell'installazione, impostare le dimensioni della cache di conseguenza. Per altre informazioni sulla funzionalità di gestione dello spazio della cache, vedere **come usare la caratteristica gestione dello spazio della cache** nella Guida alle operazioni di Microsoft Application Virtualization (App-V).

-   Durante le operazioni di pubblicazione e di flusso HTTP (S), i client App-V 4,5 SP1 usano le impostazioni del server proxy configurate in Internet Explorer nel computer dell'utente.

Per altre informazioni sulla configurazione dei parametri di installazione del client, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).

 

Infine, devi determinare come distribuire il software client Desktop Application Virtualization per i client desktop. Anche se è possibile distribuire manualmente il client Desktop Application Virtualization in ogni computer, la maggior parte delle organizzazioni dovrebbe eseguire questa operazione tramite un processo automatizzato. Un'organizzazione di medie o grandi dimensioni potrebbe avere un sistema ESD in uso e questo sarebbe il modo ideale per distribuire il client. Se non esiste alcun sistema ESD, è possibile usare il metodo standard per l'installazione del software nell'organizzazione. Le opzioni includono criteri di gruppo o varie tecniche di scripting. A seconda del numero e della dimensione degli uffici, questo processo di distribuzione può essere complesso ed è essenziale adottare un approccio strutturato per garantire che tutti i computer vengano installati da un client con la configurazione corretta.

## Argomenti correlati


[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)

[Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)

[Come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md)

[Come aggiornare Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Come disinstallare il client App-V](how-to-uninstall-the-app-v-client.md)

 

 





