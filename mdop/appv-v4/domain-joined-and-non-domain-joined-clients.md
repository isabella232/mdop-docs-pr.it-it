---
title: Client aggiunti e non aggiunti a un dominio
description: Client aggiunti e non aggiunti a un dominio
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821635"
---
# Client aggiunti e non aggiunti a un dominio


Il client Desktop App-V può essere configurato per consentire la connessione a una rete indipendentemente dal fatto che il client sia collegato al dominio o non sia stato aggiunto un dominio.

## Client appartenenti a un dominio


I client che fanno parte di un dominio, ma all'esterno della rete interna, possono comunicare con l'infrastruttura App-V usando una connessione VPN. Quando si vuole consentire agli utenti di uscire dalla rete interna ma di comunicare ancora in un'infrastruttura App-V, l'ambiente richiede pochissima configurazione. Poiché gli utenti fanno già parte del dominio, devi semplicemente assicurarti che le credenziali memorizzate nella cache siano supportate nel client. Questa è la configurazione predefinita e tutte le modifiche apportate a questa impostazione possono essere eseguite da criteri di gruppo.

Come accennato nella Guida alle procedure consigliate di App-V Security, l'utente tenterà di inviare il proprio ticket utente all'infrastruttura App-V per l'autenticazione. Se il ticket è scaduto, verrà ripristinato l'uso di NTLM e le credenziali memorizzate nella cache nel computer. Per consentire il roaming, gli amministratori devono garantire che il server di pubblicazione a cui si accede internamente sia disponibile con lo stesso nome esternamente affinché i nomi vengano risolti in modo corretto.

## Client non appartenenti a un dominio


I client che non sono collegati a un dominio, ma devono comunicare nell'infrastruttura di App-V, devono essere configurati in modo che l'autenticazione per l'infrastruttura App-V abbia esito positivo. Il client desktop di App-V non consente la richiesta di conferma per il processo di aggiornamento della pubblicazione, quindi il client deve essere configurato per presentare le credenziali appropriate per l'App-V Management Server.

Il server di pubblicazione, configurato per l'aggiornamento della pubblicazione dal client non appartenente al dominio, richiede che il nome esterno che l'accesso ai client sia configurato come nome comune o un nome alternativo soggetto (SAN) nel certificato del server di pubblicazione.

## Argomenti correlati


[Come assegnare le credenziali appropriate per Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

[Come assegnare le credenziali appropriate per Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





