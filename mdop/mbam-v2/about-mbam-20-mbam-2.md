---
title: Informazioni su MBAM 2.0
description: Informazioni su MBAM 2.0
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824316"
---
# Informazioni su MBAM 2.0


Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 offre un'interfaccia amministrativa semplificata per la crittografia unità BitLocker. BitLocker offre una protezione avanzata per il furto di dati o l'esposizione ai dati per i computer persi o rubati. BitLocker crittografa tutti i dati archiviati nel volume del sistema operativo Windows e nei volumi di dati configurati.

## Informazioni su MBAM 2.0


BitLockerAdministration e Monitoring 2.0 applica le opzioni per i criteri di crittografia di BitLocker impostate per l'organizzazione, monitora la conformità dei computer client con tali criteri e segnala lo stato di crittografia sia dell'organizzazione che dei singoli computer. Inoltre, MBAM consente di accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando il loro BIOS o il record di avvio cambia.

**Nota**  BitLocker non è descritto in dettaglio in questa guida. Per una panoramica di BitLocker, vedere [Cenni preliminari su BitLocker Drive Encryption](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

I gruppi seguenti potrebbero essere interessati all'uso di MBAM per gestire BitLocker:

-   Amministratori, professionisti IT per la sicurezza e responsabili della conformità che hanno la responsabilità di garantire che i dati riservati non vengano divulgati senza autorizzazione

-   Amministratori responsabili della sicurezza dei computer in uffici remoti o succursali

-   Amministratori responsabili per i computer client che eseguono Windows

## <a href="" id="what-s-new-in-mbam-2-0"></a>Novità di MBAM 2.0


MBAM 2.0 offre le nuove caratteristiche e funzionalità seguenti.

### Integrazione di System Center Configuration Manager con MBAM

MBAM ora supporta l'integrazione con System Center Configuration Manager. Questa integrazione Sposta l'infrastruttura di conformità di MBAM nell'ambiente nativo di Configuration Manager. Gli amministratori IT che usano Configuration Manager nella propria organizzazione possono ora visualizzare lo stato di conformità della propria azienda in Microsoft Management Console ed eseguire il drill-up dei report per visualizzare singoli computer.

### La compatibilità hardware è disponibile solo nella topologia di integrazione di Configuration Manager

L'integrazione di Configuration Manager con MBAM consente alle funzionalità di Configuration Manager che consentono o vietano l'uso di alcuni tipi di hardware con MBAM e offre maggiore flessibilità rispetto alla compatibilità hardware disponibile in MBAM 1,0. Gli amministratori IT possono creare le proprie raccolte per limitare l'hardware e distribuire la previsione di configurazione di MBAM in tali raccolte. La compatibilità hardware MBAM che era presente in MBAM 1,0 è ora disponibile solo nella topologia di gestione configurazione di mbam ed è gestito da Configuration Manager.

### Criteri flessibili per i protettori

I computer già crittografati con un Protector, ad esempio TPM + PIN o auto-Unlock e password, che ricevono un criterio di MBAM che richiede un sottoinsieme di tale crittografia, ad esempio TPM o sblocco automatico, sono considerati conformi. Nell'esempio precedente, il PIN e la password non verrebbero rimossi automaticamente, a meno che l'amministratore IT non definisca esplicitamente queste caratteristiche non più consentite.

I computer non crittografati e che ricevono un criterio MBAM, ad esempio TPM o sblocco automatico, vengono crittografati di conseguenza. Gli utenti che hanno gli amministratori locali possono usare gli strumenti BitLocker (elemento del pannello di controllo BitLocker Drive Encryption o Manage-bde) per aggiungere o modificare le protezioni esistenti, ad esempio TPM + PIN o auto-Unlock e password. Rimangono conformi a meno che i criteri di MBAM li definiscano in modo specifico.

### Possibilità di aggiornare il client MBAM

Il client di Windows Installer di MBAM 2.0 rileva la versione del client esistente ed esegue i passaggi necessari per eseguire l'aggiornamento al client MBAM 2.0 dalle versioni precedenti.

### Possibilità di aggiornare il server MBAM dalle versioni precedenti

È possibile aggiornare l'infrastruttura del server MBAM 2.0 dalle versioni precedenti di MBAM come segue:

**Sostituzione del server sul posto manuale** : è necessario disinstallare manualmente l'infrastruttura server di mbam esistente e quindi installare l'infrastruttura del server MBAM 2,0. Non è necessario rimuovere i database per eseguire l'aggiornamento. Devi invece selezionare i database esistenti, che la versione precedente del client MBAM ha creato. L'installazione di aggiornamento di MBAM 2.0 esegue quindi la migrazione dei database esistenti a MBAM 2,0.

**Aggiornamento client distribuito** : se si usa la topologia di mbam autonoma, è possibile aggiornare gradualmente i client mbam dopo l'installazione dell'infrastruttura del Server MBAM 2,0. Il server MBAM 2,0 rileva la versione del client esistente ed esegue i passaggi necessari per eseguire l'aggiornamento al client 2,0.

Dopo aver aggiornato l'infrastruttura server MBAM 2,0, i client MBAM 1,0 continuano a segnalare al server MBAM 2,0 con successo, i dati di recupero escrowing, ma la conformità sarà basata sui criteri in MBAM 1,0. È necessario aggiornare i client a MBAM 2,0 per avere i computer client con precisione segnalare la conformità con i criteri di MBAM 2,0. Puoi aggiornare i client al client MBAM 2,0 senza disinstallare il client precedente e il client inizierà a applicare i criteri di MBAM 2,0 e segnalarli.

Se si usa MBAM con Configuration Manager, è necessario aggiornare i client di MBAM 1,0 a MBAM 2,0.

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a>Supporto di MBAM per gli scenari aziendali di BitLocker nella piattaforma Windows 8

MBAM supporta il sistema operativo Windows 8 come piattaforma di destinazione per l'installazione del client MBAM. Questo supporto consente agli amministratori IT di installare l'agente MBAM, di crittografare le unità del sistema operativo Windows 8 e di segnalare la conformità dei computer. MBAM sfrutta le protezioni TPM e TPM + PIN per gestire il sistema operativo Windows 8 proprio come nel sistema operativo Windows 7. MBAM 2.0 aggiunge anche il supporto per la crittografia dei client Windows to go.

### Aggiunta del portale self-service

Gli utenti finali possono ora usare il portale self-service per recuperare le chiavi di ripristino. Il portale self-service può essere distribuito in un singolo server con le altre caratteristiche di MBAM o in un server separato che conferisce agli amministratori IT la flessibilità necessaria per esporre il portale self-server agli utenti, come richiesto. Dopo che il portale self-service esegue l'autenticazione degli utenti, gli utenti devono immettere solo le prime otto cifre dell'ID chiave di ripristino per ricevere la chiave di ripristino.

MBAM assicura anche la chiave consentendo agli utenti di recuperare le chiavi solo per i computer in cui sono utenti, riducendo così il rischio che altri utenti guadagnino un accesso non autorizzato.

### Possibilità di riprendere automaticamente la protezione da BitLocker da uno stato sospeso

MBAM non consente più agli amministratori IT di mantenere BitLocker sospesi e non protetti per periodi di tempo prolungati. Se un amministratore IT sospende BitLocker, MBAM la riattiva automaticamente quando il computer viene riavviato, riducendo così il rischio che il computer possa essere attaccato.

### Le unità dati fisse possono essere configurate per l'apertura automatica senza password

I criteri FDD (fixed data drive) ora possono essere configurati in modo da consentire lo sblocco automatico dell'unità senza una password. Agli utenti non viene richiesta una password prima che l'FDD venga crittografato e l'FDD sarà protetto e sbloccato automaticamente con l'unità del sistema operativo.

## <a href="" id="---------mbam-2-0-release-notes"></a> Note sulla versione di MBAM 2.0


Per altre informazioni e per notizie aggiornate che non sono incluse nella documentazione, vedere le [Note sulla versione per MBAM 2,0](release-notes-for-mbam-20-mbam-2.md).

## Come ottenere MBAM 2.0


Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP). I clienti aziendali possono ottenere MDOP con Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)

## Argomenti correlati


[Attività iniziali di MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





