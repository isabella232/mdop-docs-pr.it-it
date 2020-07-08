---
title: Distribuzione del client MBAM 2.0
description: Distribuzione del client MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823446"
---
# Distribuzione del client MBAM 2.0


Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione elettronica del software, ad esempio servizi di dominio Active Directory, oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.

A seconda di quando si distribuisce il client di amministrazione e monitoraggio di Microsoft BitLocker, è possibile abilitare la crittografia BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito configurando criteri di gruppo e distribuendo il software del client MBAM usando un sistema di distribuzione del software aziendale.

## Distribuire il client MBAM in computer desktop o portatili


Dopo la configurazione dei criteri di gruppo, è possibile usare un prodotto del sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager 2012 o Active Directory Domain Services per distribuire i file di installazione di Windows Installer di MBAM client in computer di destinazione. È possibile distribuire il client usando i file MbamClientSetup.exe a 32 bit o 64 bit oppure i file di MBAMClient.msi a 32 bit o 64 bit, forniti con il software MBAM. Per altre informazioni sulla distribuzione di oggetti Criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).

[Come distribuire il client MBAM a computer desktop o portatili](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## Distribuire il client MBAM come parte di una distribuzione di Windows


Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente, è possibile installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che vengano scritti i dati degli utenti. Il vantaggio di questo processo è che ogni computer è quindi conforme alla crittografia BitLocker. Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer. Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente. Se i criteri di gruppo sono stati configurati per richiedere un PIN, viene chiesto agli utenti di impostare un PIN dopo la ricezione dei criteri di gruppo.

[Come distribuire il client MBAM come parte di una distribuzione di Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## Come usare una riga di comando per installare il client MBAM


Questa sezione spiega come installare il client MBAM usando una riga di comando.

[Come usare una riga di comando per installare il client MBAM](how-to-use-a-command-line-to-install-the-mbam-client.md)

## Altre risorse per la distribuzione del client MBAM


Distribuzione di [mbam 2,0](deploying-mbam-20-mbam-2.md)[Planning per MBAM 2,0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)

 

 





