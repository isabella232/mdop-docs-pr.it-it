---
title: Architettura di alto livello
description: Architettura di alto livello
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827295"
---
# Architettura di alto livello


Questa sezione descrive l'architettura di sistema di alto livello e la progettazione di componenti di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Architettura di sistema


MED-V migliora Windows Virtual PC per l'esecuzione di due sistemi operativi su un dispositivo, l'aggiunta del recapito delle immagini virtuali, il provisioning basato su criteri di gruppo e la gestione centralizzata. Con MED-V puoi configurare, distribuire e gestire facilmente le immagini di PC virtuali di Windows aziendali in qualsiasi desktop basato su Windows che esegua Windows 7 Professional, Enterprise o Windows 7 Ultimate. La soluzione MED-V include i componenti seguenti:

<a href="" id="---------------med-v-host"></a> **Host MED-V**  
Un ambiente Windows 7 che include un agente host MED-V, un sistema ESD (Electronic Software Distribution), un sistema di gestione del registro e un guest MED-V. L'host MED-V interagisce con l'ospite MED-V in modo che sia possibile elaborare alcune funzioni di configurazione e le informazioni di sistema.

<a href="" id="-------------------med-v-host-agent"></a> **Agente host MED-V**  
Il software MED-V contenuto nell'host MED-V che fornisce un canale per comunicare con l'ospite MED-V. Offre anche funzionalità come la configurazione e la pubblicazione delle applicazioni prima volta.

**Nota**  Dopo aver installato MED-V e i relativi componenti necessari, è necessario configurarlo. La configurazione di MED-V viene indicata come configurazione per la prima volta.

 

<a href="" id="esd-system"></a>**Sistema ESD**  
Il metodo di distribuzione del software esistente che consente di distribuire e installare i file del pacchetto dell'area di lavoro MED-V creati da MED-V.

<a href="" id="registry-management-system"></a>**Sistema di gestione del registro**  
Metodo esistente per la gestione delle impostazioni e delle preferenze dei criteri di gruppo.

<a href="" id="windows-virtual-pc-image"></a>**Immagine di un PC virtuale Windows**  
Una macchina virtuale definita dall'amministratore che contiene i componenti seguenti:

<a href="" id="corporate-operating-system"></a>**Sistema operativo aziendale**  
Sistema operativo aziendale standard.

<a href="" id="management-and-security-tools"></a>**Strumenti di gestione e sicurezza**  
Gli strumenti di gestione e sicurezza standard, ad esempio la protezione da virus.

<a href="" id="-----------------------med-v-guest"></a> **Guest MED-V**  
Un ambiente Windows XP SP3, come parte di un PC virtuale Windows in uso in Windows 7 che contiene i componenti seguenti:

<a href="" id="---------------------------med-v-guest-agent"></a> **Agente guest MED-V**  
Il software MED-V contenuto nell'guest MED-V che fornisce un canale per comunicare con l'host MED-V. Supporta inoltre l'agente host MED-V con funzioni come l'esecuzione della configurazione per la prima volta.

**Nota**  L'agente guest MED-V viene installato automaticamente durante la configurazione per la prima volta.

 

<a href="" id="esd-client"></a>**Client ESD**  
Una parte facoltativa del sistema ESD che installa pacchetti software e segnala lo stato al sistema ESD.

## Argomenti correlati


[Pianificazione per la compatibilità del sistema operativo dell'applicazione](planning-for-application-operating-system-compatibility.md)

[Preparare l'ambiente di distribuzione per MED-V](prepare-the-deployment-environment-for-med-v.md)

 

 





