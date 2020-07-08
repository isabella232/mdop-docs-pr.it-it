---
title: Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando
description: Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817896"
---
# Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando


Dopo la distribuzione e la configurazione del client Application Virtualization (App-V) durante l'installazione tramite la riga di comando, potrebbe essere necessario modificare una o più impostazioni di configurazione del client. Questa operazione viene eseguita modificando le chiavi del registro di sistema appropriate, usando uno dei metodi seguenti:

-   Uso diretto dell'editor del registro di sistema

-   Uso di un file reg

-   Uso di un linguaggio di scripting come VBScript o Windows PowerShell

È anche possibile usare un modello ADM. Per altre informazioni sul modello ADM, vedere <https://go.microsoft.com/fwlink/?LinkId=121835> .

**Attenzione**  Prestare attenzione quando si modifica il registro di sistema perché gli errori possono uscire dal computer in uno stato non utilizzabile. Assicurati di seguire le procedure aziendali standard correlate alle modifiche del registro di sistema. Verificare accuratamente tutte le modifiche proposte in un ambiente di test prima di distribuirle ai computer di produzione.

 

## In questa sezione


**Importante**  In un computer a 64 bit le chiavi e i valori descritti nelle sezioni seguenti saranno in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[Come reimpostare la cache di FileSystem](how-to-reset-the-filesystem-cache.md)  
Fornisce le informazioni necessarie per reimpostare la cache del FileSystem.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[Come modificare le dimensioni della cache di FileSystem](how-to-change-the-size-of-the-filesystem-cache.md)  
Spiega come modificare le dimensioni della cache.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[Come usare la funzionalità di gestione dello spazio della cache](how-to-use-the-cache-space-management-feature.md)  
Descrive come configurare la funzionalità di gestione dello spazio della cache.

<a href="" id="how-to-configure-the-client-log-file"></a>[Come configurare il file di registro del client](how-to-configure-the-client-log-file.md)  
Descrive i vari valori della chiave del registro di sistema che controllano il file di log del client e come è possibile modificarli.

<a href="" id="how-to-configure-user-permissions"></a>[Come configurare le autorizzazioni utente](how-to-configure-user-permissions.md)  
Identifica la chiave del registro di sistema che controlla le autorizzazioni utente e fornisce esempi di come modificare alcune autorizzazioni.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[Come configurare il client per il recupero del pacchetto dell'applicazione](how-to-configure-the-client-for-application-package-retrieval.md)  
Spiega come configurare il client per recuperare il contenuto del pacchetto, le icone e le associazioni di tipi di file da origini diverse e fornisce diversi esempi del formato di percorso corretto.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[Come configurare il client per la modalità di operazioni senza connessione](how-to-configure-the-client-for-disconnected-operation-mode.md)  
Vengono fornite informazioni su come configurare le varie impostazioni associate alla modalità operazioni disconnesse.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
Descrive i valori della chiave del registro di sistema che controllano le scelte rapide e le associazioni di tipi di file nel client App-V e fornisce informazioni dettagliate su come configurarle.

## Argomenti correlati


[Application Virtualization Client](application-virtualization-client.md)

 

 





