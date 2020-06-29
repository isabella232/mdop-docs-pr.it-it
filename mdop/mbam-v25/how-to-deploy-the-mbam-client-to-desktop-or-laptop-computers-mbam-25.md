---
title: Come distribuire il client MBAM a computer desktop o portatili
description: Come distribuire il client MBAM a computer desktop o portatili
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824476"
---
# Come distribuire il client MBAM a computer desktop o portatili


Questo argomento spiega come distribuire il client MBAM in modo che i computer degli utenti finiscano. È possibile distribuire il client MBAM tramite un sistema di distribuzione elettronica del software, ad esempio Active Directory Domain Services o MicrosoftSystemCenterConfiguration Manager.

Per distribuire il client MBAM come parte di una distribuzione di Windows, vedere [come abilitare BitLocker tramite mbam come parte di una distribuzione di Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).

Prima di avviare la distribuzione di MBAM client, esaminare le [configurazioni supportate di mbam 2,5](mbam-25-supported-configurations.md).

**Per distribuire il client MBAM in computer desktop o portatili**

1.  Individuare i file di installazione del client MBAM forniti con il software MBAM.

2.  Usare servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale come MicrosoftSystemCenterConfiguration Manager per distribuire il pacchetto di Windows Installer in computer di destinazione.

3.  Configurare le impostazioni di distribuzione o di criteri di gruppo per eseguire il file di installazione del client MBAM.

    Dopo aver completato l'installazione, il client MBAM applica le impostazioni dei criteri di gruppo ricevute da un controller di dominio per avviare le funzioni di crittografia e gestione unità BitLocker.

    **Importante**  Il client MBAM non avvia le azioni di crittografia unità BitLocker se è attiva una connessione di protocollo desktop remoto. Tutte le connessioni della console remota devono essere chiuse e un utente deve avere effettuato l'accesso a una sessione di console fisica prima dell'inizio della crittografia unità BitLocker.

     


## Argomenti correlati
[Distribuzione del client di MBAM 2.5](deploying-the-mbam-25-client.md)

[Pianificazione della distribuzione del client di MBAM 2.5](planning-for-mbam-25-client-deployment.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





