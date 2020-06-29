---
title: Scenario di distribuzione end-to-end per MED-V 2.0
description: Scenario di distribuzione end-to-end per MED-V 2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826175"
---
# Scenario di distribuzione end-to-end per MED-V 2.0


Questo scenario di esempio per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di distribuire i componenti MED-V nell'organizzazione usando più scenari da capo a fine. Questo scenario di esempio può essere considerato un caso di studio che consente di inserire i singoli scenari e le singole procedure nel contesto.

Questa sezione fornisce informazioni di base e indicazioni per la distribuzione di componenti MED-V come soluzione end-to-end nell'organizzazione.

## Scenario dettagliato di distribuzione di MED-V


Gli argomenti di questo scenario dettagliato includono i seguenti:

-   Le [configurazioni supportate in Med-v 2,0](med-v-20-supported-configurations.md) illustrano i requisiti necessari per installare ed eseguire Microsoft Enterprise Desktop VIRTUALIZATION (MED-v) 2.0 nell'ambiente. In questo argomento vengono specificati i requisiti del sistema operativo, i requisiti di configurazione e i requisiti dell'area di lavoro MED-V. Questo argomento include anche informazioni sulla localizzazione sulle lingue supportate da MED-V 2,0.

-   [Panoramica sulla distribuzione di Med-v 2,0](med-v-20-deployment-overview.md) illustra informazioni generali e istruzioni per l'installazione e la distribuzione di Med-v in tutta l'organizzazione. I componenti MED-V sono basati su client e vengono recapitati e gestiti usando l'infrastruttura e i processi esistenti dell'organizzazione. Questo argomento offre una panoramica della soluzione MED-V che include informazioni sui file di installazione di MED-V e sui componenti MED-V distribuiti. Questo argomento offre anche una panoramica di alto livello sul processo di installazione e distribuzione di MED-V.

-   [Preparare l'ambiente di distribuzione per MED-v](prepare-the-deployment-environment-for-med-v.md) descrive come preparare l'ambiente per una distribuzione di 2,0 Med-v. In questa sezione vengono descritti i prerequisiti necessari per l'ambiente MED-V, ad esempio Microsoft Windows 7 e un'infrastruttura Active Directory in cui si usano i criteri di gruppo per consentire la gestione e la configurazione centralizzata di sistemi operativi, applicazioni e impostazioni degli utenti. Questa sezione descrive anche i prerequisiti che è necessario avere per l'installazione e la distribuzione di MED-V 2,0 in tutta l'organizzazione, ad esempio Windows Virtual PC e l'aggiornamento di Windows Virtual PC richiesto.

-   [Distribuire i componenti Med-v](deploy-the-med-v-components.md) descrive i diversi modi in cui è possibile installare tutti i file di installazione necessari e i componenti Med-v in tutta l'organizzazione. Per installare e distribuire MED-V, eseguire in genere le operazioni seguenti:

    1.  Installare il **Packager area di lavoro MED-v** nel computer amministratore che verrà usato per compilare i pacchetti dell'area di lavoro MED-v. Per altre informazioni, vedere [come installare il Packager area di lavoro MED-V](how-to-install-the-med-v-workspace-packager.md).

    2.  Creare e testare i pacchetti dell'area di lavoro MED-V. Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-v](create-a-med-v-workspace-package.md) e [testare il pacchetto area di lavoro MED-v](testing-the-med-v-workspace-package.md).

    3.  Distribuire MED-V in tutta l'organizzazione usando il metodo esistente della società per la distribuzione delle applicazioni. Per altre informazioni, vedere [distribuzione del pacchetto area di lavoro MED-V](deploying-the-med-v-workspace-package.md).

## Argomenti correlati


[Distribuzione di MED-V](deployment-of-med-v.md)

[Scenario di pianificazione end-to-end per MED-V 2.0](end-to-end-planning-scenario-for-med-v-20.md)

[Scenario di operazioni end-to-end per MED-V 2.0](end-to-end-operations-scenario-for-med-v-20.md)

 

 





