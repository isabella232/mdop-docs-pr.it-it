---
title: Elenco di controllo per l'aggiornamento di MED-V 1.0 SP1
description: Elenco di controllo per l'aggiornamento di MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827266"
---
# Elenco di controllo per l'aggiornamento di MED-V 1.0 SP1


Per aggiornare Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 to MED-V 1.0 Service Pack1 (SP1), è necessario aggiornare il client. Il server può essere aggiornato facoltativamente.

## Aggiornamento del server


**Per aggiornare il server MED-V 1.0 a MED-V 1.0 SP1**

1.  Eseguire il backup dei file seguenti che si trovano nella directory * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* :

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  Eseguire il backup del file * &lt; INSTALLDIR &gt; /Server/ServerSettings.xml* .

3.  Disinstallare il server MED-V 1.0.

4.  Installare il server MED-V 1.0 SP1.

5.  Ripristinare i file di backup nelle directory appropriate.

6.  Riavviare il servizio server MED-V.

**Nota**  Se la configurazione del server è stata modificata rispetto all'impostazione predefinita, i file potrebbero essere archiviati in una posizione diversa.

 

## Aggiornamento client


Per aggiornare il client MED-V 1.0 a MED-V 1.0 SP1, installare il file msp in un client MED-V 1.0. Il client e il MED-V vengono aggiornati automaticamente.

 

 





