---
title: Configurare i prerequisiti di installazione
description: Configurare i prerequisiti di installazione
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819306"
---
# Configurare i prerequisiti di installazione


Le istruzioni seguenti sono prerequisiti per l'installazione e l'uso di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

[Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Aggiornamento di Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[Configurazione software antivirus/backup](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Come installare e configurare Windows Virtual PC


**Importante**  Se nel computer host esiste già una versione di Virtual PC per Windows, è necessario disinstallarla prima di installare Windows Virtual PC.

 

**Per installare Windows Virtual PC**

1.  Scaricare [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) dall'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .

2.  Eseguire il file di installazione nel computer host e seguire i passaggi della procedura guidata.

**Importante**  Windows Virtual PC include il pacchetto componenti integrativi, che offre funzionalità che migliorano l'interazione tra l'ambiente virtuale e il computer fisico. Ad esempio, consente di passare al mouse tra l'host e i computer guest. MED-V richiede l'installazione del pacchetto componenti integrativi.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Come installare e configurare l'aggiornamento di Windows Virtual PC


L'aggiornamento Microsoft associato all'articolo KB977206 Abilita la modalità Windows XP per i computer senza tecnologia HAV (hardware-Assisted Virtualization). È consigliabile installare questo aggiornamento perché alcune funzionalità di integrazione potrebbero non funzionare correttamente se il pacchetto componenti integrativi nel sistema operativo guest non corrisponde alla versione di Windows Virtual PC installata nel computer host.

**Importante**  Non è necessario installare questo aggiornamento quando si installa MED-V nei computer host che eseguono Windows 7 con Service Pack 1.

 

**Suggerimento**  Oltre all'aggiornamento elencato in questo articolo, è consigliabile rivedere tutti gli aggiornamenti di Windows Virtual PC disponibili e applicare gli aggiornamenti appropriati o necessari per l'ambiente.

 

**Per installare l'aggiornamento di Windows Virtual PC**

1.  Scaricare l'aggiornamento di Windows Virtual PC richiesto dall'area download Microsoft.

    [aggiornamento a 32 bit](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [aggiornamento a 64 bit](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  Eseguire il file di installazione nel computer host in modalità elevata e seguire i passaggi della procedura guidata.

    Per altre informazioni sul pacchetto di hotfix per Windows Virtual PC, vedere l' [articolo 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Come configurare il software antivirus/backup


Per evitare che l'attività antivirus incida sulle prestazioni del desktop virtuale, è consigliabile, dove è possibile, escludere i tipi di file della macchina virtuale seguenti da qualsiasi processo antivirus o di backup in esecuzione nel computer host:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. VHD

## Argomenti correlati


[Configurare i prerequisiti di ambiente](configure-environment-prerequisites.md)

[Architettura di alto livello](high-level-architecturemedv2.md)

[Configurazioni supportate di MED-V 2.0](med-v-20-supported-configurations.md)

 

 





