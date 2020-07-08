---
title: Note sulla versione di App-V 5.0 SP3
description: Note sulla versione di App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804893"
---
# Note sulla versione di App-V 5.0 SP3


Di seguito sono riportati i problemi noti di Microsoft Application Virtualization (App-V) 5,0 SP3.

## I file del server non vengono eliminati dopo una nuova installazione di App-V 5,0 SP3 server


Se si disinstalla il server App-V 5,0 SP1 e quindi si installa il server App-V 5,0 SP3, l'installazione non riesce e viene installata la versione errata del server di gestione. Vengono visualizzati gli errori seguenti:

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

Il problema si verifica perché i file del server non vengono eliminati quando si disinstalla l'App-V 5,0 SP1, quindi il processo di installazione di App-V 5,0 SP3 esegue erroneamente un aggiornamento anziché una nuova installazione.

**Soluzione alternativa**: eliminare la chiave del registro di sistema seguente prima di iniziare l'installazione di App-V 5,0 SP3:

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## L'esecuzione di query su servizi di dominio Active Directory può causare un funzionamento non corretto delle applicazioni


Quando si ricevono pacchetti aggiornati eseguendo una query su servizi di dominio Active Directory per le appartenenze ai gruppi aggiornati, può causare un funzionamento non corretto delle applicazioni se le applicazioni dipendono dal token di accesso dell'utente. Inoltre, le frequenti query di appartenenza ai gruppi possono causare l'overload del controller di dominio. Per altre informazioni sui token di accesso degli utenti, vedere [token di accesso](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).

**Soluzione alternativa**: attendere che l'utente si disconnetta e quindi rieseguire l'accesso prima di eseguire una query per le appartenenze ai gruppi aggiornate. Non usare la chiave del registro di sistema, descritta nel [pacchetto hotfix 2 per Microsoft Application Virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087), per eseguire query per le appartenenze ai gruppi aggiornate.






## Argomenti correlati


[Informazioni su App-V 5.0 SP3](about-app-v-50-sp3.md)

 

 





