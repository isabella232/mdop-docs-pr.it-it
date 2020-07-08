---
title: Informazioni sui pacchetti di Application Virtualization
description: Informazioni sui pacchetti di Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820085"
---
# Informazioni sui pacchetti di Application Virtualization


Nella virtualizzazione delle applicazioni, un *pacchetto* è l'output del processo di sequenziazione. Si usano i pacchetti per la prima volta che si distribuiscono applicazioni nei server e quando si aggiornano le applicazioni con una nuova versione. I pacchetti consentono di controllare le versioni delle applicazioni virtuali nei server di gestione della virtualizzazione dell'applicazione. Un singolo pacchetto può contenere una o più applicazioni. Ogni pacchetto di applicazione contiene un set di file come unità indipendente.

## Gestione dei pacchetti


Dopo che il Sequencer crea un pacchetto di una o più applicazioni durante il processo, è possibile copiare i file generati dal sequencer in un server di gestione della virtualizzazione delle applicazioni e renderli disponibili per il flusso.

I pacchetti disponibili vengono visualizzati sotto il contenitore **pacchetti** nel riquadro sinistro della console di gestione di Application Virtualization. Quando si importa un'applicazione con un file di progetto sequencer (SPRJ) o un file OSD (Open Software Descriptor), nel contenitore **pacchetti** viene visualizzata una voce correlata. Dalla console di gestione di Application Virtualization Server è quindi possibile distribuire, aggiornare o eliminare pacchetti e versioni.

Ogni applicazione virtuale ha un pacchetto associato. Questo pacchetto include i file seguenti:

-   SFT-il file che trasmette l'applicazione ai client.

-   OSD: il file Open Software Descriptor contiene le informazioni necessarie per trovare e avviare l'applicazione.

-   ICO: il file icona che rappresenta visivamente l'applicazione in interfacce utente e tasti di scelta rapida.

-   SPRJ-il file di progetto Sequencer.

Quando si importa il file SPRJ, per impostazione predefinita tutte le applicazioni sequenziate sono disponibili per la distribuzione, ma le applicazioni non sono abilitate per il flusso. Puoi scegliere di eseguire il flusso di tutte o alcune delle applicazioni nel pacchetto. Se ad esempio è stato sequenziato e importato Microsoft Office, è possibile scegliere di non distribuire alcune applicazioni, ad esempio la procedura guidata Salva impostazioni personali. In questo caso, fare clic con il pulsante destro del mouse su ogni applicazione che si vuole distribuire, scegliere **Proprietà**e verificare che la casella **abilitato** sia deselezionata (vuota). Solo le applicazioni con la casella **attivata** verranno trasmesse ai computer client.

Dopo aver risequenziato un pacchetto e prodotto un nuovo file SFT per lo streaming, è possibile aggiornare il vecchio pacchetto in modo semplice e veloce tramite la console di gestione dei server Application Virtualization.

L'unico scenario operativo che richiede l'uso del nodo **packages** è quando si introduce una nuova versione (file SFT) per il pacchetto. Ogni volta che si importano applicazioni, si assegnano accessi e licenze alle applicazioni e così via, il sistema di virtualizzazione delle applicazioni tiene traccia di queste informazioni a livello di pacchetto. Ciò significa che quando si autorizza un utente a usare un'applicazione, si sta dando all'utente l'autorizzazione per eseguire qualsiasi applicazione nello stesso pacchetto.

### Versione del pacchetto

Una versione del pacchetto è rappresentata da un file SFT specifico. Quando si aggiorna un pacchetto (si applica un aggiornamento a un'applicazione o si aggiunge un'applicazione a un pacchetto), si genera un nuovo file SFT. Ogni volta che si crea un nuovo file SFT, si crea una nuova versione del pacchetto.

Quando si importano applicazioni tramite la console di gestione di Application Virtualization Server, il software crea automaticamente un pacchetto e una versione del pacchetto, se non sono già presenti.

## Argomenti correlati


[Informazioni sulle applicazioni di Application Virtualization](about-application-virtualization-applications.md)

[Informazioni su Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[Come gestire i pacchetti in Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





