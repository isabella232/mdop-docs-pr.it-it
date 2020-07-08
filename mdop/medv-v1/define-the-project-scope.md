---
title: Definire l'ambito di progetto
description: Definire l'ambito di progetto
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823645"
---
# Definire l'ambito di progetto


Quando si definisce l'ambito del progetto, determinare quanto segue:

1.  Utenti finali di MED-V: la posizione e il numero di utenti finali vengono usati per determinare la posizione delle installazioni client MED-V e il numero di istanze di MED-V, nonché il numero e la posizione dei repository di immagini MED-V.

2.  Le immagini della macchina virtuale (VM) che devono essere gestite da MED-V per determinare il metodo di distribuzione delle immagini e la posizione dei repository di immagini.

3.  Le aspettative del livello di servizio dell'organizzazione, per determinare i requisiti di prestazioni e tolleranza d'errore per il server e il database MED-V, nonché per il repository di immagini.

4.  Convalidare con l'azienda: verificare che l'infrastruttura pianificata influenzi l'azienda in modo completo.

## Definire gli utenti finali di MED-V


Prima di tutto, determinare dove si trovano gli utenti finali, nonché il numero di utenti in ogni posizione. In secondo luogo, ottenere un diagramma di infrastruttura di rete che visualizza le posizioni utente e la larghezza di banda disponibile per tali posizioni. In terzo luogo, scoprire se gli utenti viaggiano tra le posizioni. Se gli utenti viaggiano, potrebbero essere necessarie ulteriori capacità nella progettazione dell'infrastruttura server e dei repository di immagini.

## Determinare le immagini MED-V da gestire con MED-V


Dopo avere definito gli utenti finali di MED-V, determinare quali VM verranno gestite da MED-V per gli utenti in ogni posizione.

Se una delle macchine virtuali è archiviata in una raccolta centralizzata, determinare la posizione della raccolta in modo che possa essere valutata per l'uso come repository MED-V.

## <a href="" id="determine-the-organization-s-service-level-expectations"></a>Determinare le aspettative del livello di servizio dell'organizzazione


Per ogni area di lavoro MED-V, nota il periodo di tempo accettabile per il caricamento di una nuova immagine e per la distribuzione dei tempi per gli aggiornamenti critici.

Se applicabile, registrare le aspettative del livello di servizio per i report MED-V, da usare nella progettazione dell'infrastruttura server.

## Convalidare con il business


Chiedere agli stakeholder aziendali e ai proprietari delle applicazioni le seguenti domande:

-   Esistono immagini esistenti che possono essere combinate? Ad esempio, se l'applicazione A su WindowsXP è un'immagine VPC e l'applicazione B su WindowsXP è un'altra immagine VPC, forse una singola immagine può contenere entrambe le applicazioni, riducendo così lo spazio del repository e la larghezza di banda necessaria per il download delle immagini.

-   Le applicazioni in ambito licenziabili e supportate possono essere distribuite in una VM da MED-V? Verificare che il fornitore dell'applicazione assicuri che le condizioni di licenza e supporto tecnico non vengano violate consegnando l'applicazione tramite MED-V.

 

 





