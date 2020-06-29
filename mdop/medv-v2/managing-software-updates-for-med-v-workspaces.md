---
title: Gestione degli aggiornamenti software per le aree di lavoro MED-V
description: Gestione degli aggiornamenti software per le aree di lavoro MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824815"
---
# Gestione degli aggiornamenti software per le aree di lavoro MED-V


Sono disponibili diverse opzioni per fornire gli aggiornamenti software per le applicazioni nell'area di lavoro MED-V distribuita.

**Nota**  Per informazioni su come specificare le impostazioni di configurazione che definiscono la modalità di ricezione degli aggiornamenti automatici in MED-V, vedere [gestione degli aggiornamenti automatici per le aree di lavoro MED-v](managing-automatic-updates-for-med-v-workspaces.md).

 

**Aggiornamento del software in un'area di lavoro MED-V**

1.  **Uso di un sistema elettronico di distribuzione del software**

    Se l'organizzazione usa un sistema ESD (Electronic Software Distribution System) per distribuire il software, è possibile usarlo per ottenere gli aggiornamenti software per le applicazioni nelle aree di lavoro MED-V così come vengono forniti gli aggiornamenti per le applicazioni nei computer fisici.

2.  **Uso di criteri di gruppo**

    Se l'organizzazione distribuisce il software tramite criteri di gruppo, è possibile usarlo per ottenere gli aggiornamenti software per le applicazioni nelle aree di lavoro MED-V così come vengono forniti gli aggiornamenti per le applicazioni nei computer fisici.

3.  **Uso della virtualizzazione delle applicazioni (APP-V)**

    Se si usa MED-V insieme a App-V, è possibile specificare gli aggiornamenti software per le applicazioni nell'area di lavoro MED-V seguendo i passaggi richiesti da App-V per l'aggiornamento del software. Per altre informazioni, Vedi [virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

4.  **Aggiornamento del software nell'immagine principale**

    Anche se non è considerata una procedura consigliata per MED-V, è possibile installare gli aggiornamenti software per le applicazioni nell'immagine principale. Dopo aver installato gli aggiornamenti, è possibile ridistribuire l'area di lavoro MED-V all'organizzazione come è stata distribuita in origine.

    **Importante**  Questo metodo di gestione degli aggiornamenti software non è consigliabile. Inoltre, se aggiorni il software nell'immagine principale e Ridistribuisci l'area di lavoro MED-V all'interno dell'organizzazione, la prima volta che la configurazione deve essere eseguita di nuovo e tutti i dati salvati nella macchina virtuale andranno perduti.

     

## Argomenti correlati


[Gestione degli aggiornamenti automatici per le aree di lavoro MED-V](managing-automatic-updates-for-med-v-workspaces.md)

[Come verificare la pubblicazione delle applicazioni](how-to-test-application-publishing.md)

[Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





