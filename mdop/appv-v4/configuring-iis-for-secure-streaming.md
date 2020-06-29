---
title: Configurazione di IIS per lo streaming sicuro
description: Configurazione di IIS per lo streaming sicuro
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821885"
---
# Configurazione di IIS per lo streaming sicuro


Con il rilascio di Microsoft Application Virtualization (App-V) versione 4,5, è possibile usare i protocolli HTTP e HTTPS per la trasmissione di pacchetti di applicazioni ai client App-V. Questa opzione consente alle organizzazioni di sfruttare l'ulteriore scalabilità che IIS offre in genere. Quando si usa IIS come server di streaming, è possibile proteggere le comunicazioni tra il client e il server tramite HTTPS anziché HTTP.

**Nota**  Se si vuole eseguire il flusso delle applicazioni da un file server, è consigliabile migliorare la sicurezza delle comunicazioni per i pacchetti dell'applicazione. Questa operazione può essere eseguita tramite IPsec. Per altre informazioni, vedere gli argomenti seguenti nella raccolta TechNet:

-   Per Windows Server2003, <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Per Windows Server 2008 <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## Tipi MIME


Quando si usa IIS per eseguire il flusso di applicazioni virtuali con HTTP o HTTPS, per supportare App-V, è necessario aggiungere i seguenti tipi MIME al server IIS:

-   . OSD = TXT

-   . SFT = binario

Usare gli articoli della Knowledge base seguenti come indicazioni per l'aggiunta di tipi MIME:

IIS 6,0: <https://go.microsoft.com/fwlink/?LinkId=151973>

IIS 7,0: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Autenticazione Kerberos


Quando usi l'autenticazione HTTP o HTTPS e Kerberos per eseguire il flusso di file ICO, OSD o SFT, stai migliorando la sicurezza dell'ambiente. Tuttavia, per supportare l'autenticazione Kerberos in IIS, è necessario configurare un nome SPN (Service Principal Name) appropriato. Lo `setspn.exe` strumento è disponibile per Windows Server2003 dagli strumenti di supporto del CD di installazione ed è incorporato in Windows Server2008.

Per creare un SPN, eseguire `setspn.exe` da un prompt dei comandi durante l'accesso come membro di amministratori di dominio, ad esempio `setspn.exe –A HTTP/FQDN of Server ServerName` .

## Argomenti correlati


[Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





