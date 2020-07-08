---
title: Distribuzione di UE-V 1.0
description: Distribuzione di UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827146"
---
# Distribuzione di UE-V 1.0


È disponibile una serie di configurazioni di distribuzione diverse supportate da Microsoft User Experience Virtualization (UE-V). Questa sezione include informazioni generali e procedure dettagliate per consentire di eseguire correttamente le attività che è necessario completare in diverse fasi della distribuzione.

## Informazioni sulla distribuzione per UE-V


Una distribuzione di UE-V richiede una posizione di archiviazione delle impostazioni in una condivisione di rete e un agente UE-V installato in tutti i computer che sincronizzano le impostazioni. I modelli di criteri di gruppo UE-V possono essere usati per gestire le impostazioni di UE-V. Gli argomenti seguenti descrivono come distribuire queste funzionalità.

[Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

Tutte le distribuzioni di UE-V richiedono una posizione di archiviazione delle impostazioni in cui si trovano i pacchetti di impostazioni che contengono i valori di impostazione sincronizzati.

[Distribuzione dell'agente di UE-V](deploying-the-ue-v-agent.md)

Per sincronizzare le impostazioni tramite UE-V, un computer deve avere l'agente UE-V installato ed eseguito.

[Installazione di modelli ADMX di Criteri di gruppo di UE-V](installing-the-ue-v-group-policy-admx-templates.md)

È possibile usare criteri di gruppo per preconfigurare le impostazioni di UE-V prima di distribuire l'agente UE-V e la configurazione standard di UE-V.

## Informazioni sulla distribuzione per la distribuzione di modelli personalizzati


Se si prevede di creare modelli di posizione personalizzati per le applicazioni diverse dalle applicazioni Microsoft incluse in UE-V, ad esempio applicazioni line-of-business, è possibile distribuire un catalogo di modelli di impostazioni ed è necessario installare il generatore UE-V per creare questi modelli. Per altre informazioni, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

[Installazione di Generatore UE-V](installing-the-ue-v-generator.md)

Usa il generatore UE-V per creare, modificare e convalidare modelli di posizione personalizzati che consentono di sincronizzare le impostazioni delle applicazioni diverse dalle applicazioni predefinite.

[Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0](deploying-the-settings-template-catalog-for-ue-v-10.md)

Se è necessario distribuire modelli di posizione delle impostazioni personalizzate per supportare applicazioni diverse dalle applicazioni predefinite nell'agente UE-V, è necessario configurare un catalogo di modelli di impostazioni per archiviarli.

[Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

Se è necessario sincronizzare applicazioni diverse dalle applicazioni predefinite nell'agente UE-V, i modelli di posizione di impostazione personalizzati creati con il generatore UE-V possono essere distribuiti nel catalogo dei modelli di impostazioni di UE-V.

**Nota**  La distribuzione di modelli personalizzati richiede un catalogo di modelli di impostazioni. I modelli di applicazione Microsoft predefiniti vengono distribuiti con l'agente UE-V.

 

## Argomenti per questo prodotto


[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Attività iniziali di User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

[Risoluzione dei problemi di UE-V 1.0](troubleshooting-ue-v-10.md)

 

 





