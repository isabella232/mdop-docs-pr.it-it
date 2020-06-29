---
title: Risoluzione dei problemi di autorizzazione dei certificati
description: Risoluzione dei problemi di autorizzazione dei certificati
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815206"
---
# Risoluzione dei problemi di autorizzazione dei certificati


Dopo l'installazione di App-V 4.5, se la chiave privata non è stata configurata con l'ACL appropriato per il servizio di rete, viene registrato un evento nel log eventi di NT e viene inserita una voce nel `Sft-server.log` file.

## Messaggi di errore


### Windows Server2003

ID evento 36870: si è verificato un errore irreversibile durante il tentativo di accesso alla chiave privata delle credenziali del server SSL. Il codice di errore restituito dal modulo crittografico è 0x80090016.

### Windows Server2008

ID evento 36870: si è verificato un errore irreversibile durante il tentativo di accesso alla chiave privata delle credenziali del server SSL. Il codice di errore restituito dal modulo crittografico è 0x8009030d.

## SFT-server. log


L'errore seguente viene inserito nel `sft-server.log` file che si trova nella `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` Directory:

Non è stato possibile caricare il certificato. Codice di errore \ [-2146893043 \]. Verificare che l'account del servizio di rete disponga dell'accesso corretto al certificato e al file della chiave privata corrispondente.

 

 





