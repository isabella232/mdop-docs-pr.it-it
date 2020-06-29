---
title: Note sulla versione di MED-V 1.0
description: Note sulla versione di MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826595"
---
# Note sulla versione di MED-V 1.0


## Problemi noti di MED-V


Questa sezione fornisce le informazioni più aggiornate sui problemi generali della piattaforma Microsoft Enterprise Desktop Virtualization (MED-V). Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando possibile, questi problemi verranno risolti in versioni successive.

### I download di file non seguono le regole di reindirizzamento Web

I download di file non seguono le regole di reindirizzamento Web impostate in un criterio di area di lavoro MED-V.

### Quando si espande una finestra dell'applicazione console-pubblicata a schermo intero, scompare

Se si espande un'applicazione pubblicata da console (ad esempio cmd.exe) a schermo intero all'interno di un'area di lavoro MED-V configurata in modalità di integrazione perfetta, la finestra dell'applicazione potrebbe scomparire o non rispondere.

### Quando si lavora in modalità desktop completo, le posizioni delle icone sul desktop non vengono salvate

Quando si lavora in modalità desktop completo, le modifiche della posizione manuale delle icone sul desktop non vengono salvate tra le sessioni dell'area di lavoro MED-V.

### Un'immagine locale e un'immagine di test con lo stesso nome non possono esistere nello stesso dominio

Se un'immagine locale viene unita al dominio e l'amministratore crea una nuova versione della stessa immagine con lo stesso nome del computer di un'immagine di test, quando l'immagine di test si unisce al dominio, l'azione di join Domain non riesce o riesce e l'immagine locale viene rimossa dal dominio.

### MED-V non supporta le funzionalità di Windows Aero

MED-V non supporta le funzionalità Windows Aero, ad esempio Aero Flip 3D.

### La console di gestione può essere usata da un solo utente Windows per computer

La console di gestione MED-V può essere usata solo dagli amministratori e dall'utente Windows che ha installato l'applicazione di gestione.

### L'utilità di configurazione del server MED-V Verifica la connettività di Microsoft SQL Server in contesto utente anziché in contesto del servizio MED-V Server

MED-V usa il contesto del servizio MED-V Server per raccogliere report dal database di report di Microsoft SQL Server. L'utilità di configurazione del server MED-V Verifica il database e verifica la stringa di connessione del database. Non convalidare l'accesso del servizio MED-V Server al database.

 

 





