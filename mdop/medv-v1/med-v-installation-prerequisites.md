---
title: Prerequisiti per l'installazione di MED-V
description: Prerequisiti per l'installazione di MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824966"
---
# Prerequisiti per l'installazione di MED-V


Di seguito sono riportati i prerequisiti per l'installazione di MED-V:

[Requisiti di Active Directory](#bkmk-activedirectoryrequirements)

[Database report](#bkmk-howtoinstallthereportdatabase)

[Configurazione software antivirus/backup](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 SP1](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Requisiti di Active Directory


Quando si configura il server MED-V, se gli utenti non fanno parte dello stesso dominio a cui appartiene il server, è necessario impostare un trust tra i domini.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>Come installare il database del report


Il database del report è necessario per archiviare tutti i registri dell'area di lavoro MED-V. Il database del log viene quindi usato per generare report MED-V. Per informazioni sui report, vedere [report di MED-V](med-v-reporting.md).

SQL Server può essere installato nello stesso server del server MED-V o in un server remoto. Se si esegue l'installazione in un server remoto, vedere [installazione di SQL Server in un server remoto](#bkmk-installingsqlserveronaremoteserver).

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>Installazione di SQL Server in un server remoto

**Per installare SQL Server in un server remoto**

1.  Configurare le operazioni seguenti nel server remoto:

    -   Nome istanza: istanza predefinita

    -   Modalità di autenticazione: modalità mista

    -   Utente: l'utente predefinito creato è "sa"

    -   Password: password desiderata

    -   Impostazioni regole di confronto: impostazione predefinita

    -   Errore nelle impostazioni del report utilizzo: impostazione predefinita

2.  Installare i file seguenti nel server MED-V:

    -   Per installare i prerequisiti per la raccolta di oggetti Management Pack per Microsoft SQL Server2008, scaricare [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) dall'area download Microsoft.

    -   Per installare i prerequisiti per la raccolta di oggetti Management Pack per Microsoft SQL Server2005, scaricare [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) dall'area download Microsoft.

    -   Per installare i file dll necessari per Microsoft SQL Server2008, scaricare [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) dall'area download Microsoft.

    -   Per installare i file dll necessari per Microsoft SQL Server2005, scaricare [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) dall'area download Microsoft.

    -   Per installare i pacchetti di installazione autonomi che offrono un valore aggiuntivo per SQL Server2008, scaricare il [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) dall'area download Microsoft.

    -   Per installare i pacchetti di installazione autonomi che offrono un valore aggiuntivo per SQL Server2005, scaricare il [Feature Pack per Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) dall'area download Microsoft.

    Per altre informazioni su questi file, vedere [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) nell'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) o [Feature Pack per Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) nell'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Configurazione software antivirus/backup


Per evitare che l'attività antivirus incida sulle prestazioni del desktop virtuale, è consigliabile escludere i tipi di file della macchina virtuale seguenti da qualsiasi elaborazione di antivirus o backup in esecuzione nell'host:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Come installare e configurare Microsoft Virtual PC2007 SP1


**Importante**  Se nel computer host è presente Virtual PC per Windows, disinstallarlo prima di installare Virtual PC2007 SP1.

 

**Per installare Microsoft Virtual PC2007 SP1**

1.  Scaricare Virtual PC2007 SP1 dall'area download Microsoft [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).

2.  Eseguire il file di installazione nel computer host e seguire la procedura guidata.

3.  Installare l'aggiornamento di Virtual PC2007 SP1 nel computer host in modalità elevata.

    Per altre informazioni, vedere [la descrizione del pacchetto di hotfix per Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).

    **Nota**  È necessario l'aggiornamento virtuale di PC2007 SP1 per l'uso di Virtual PC2007 SP1.

     

## Argomenti correlati


[Configurazioni supportate](supported-configurationsmedv-orientation.md)

 

 





