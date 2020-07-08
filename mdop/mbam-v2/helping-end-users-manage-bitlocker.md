---
title: Aiutare gli utenti finali a gestire BitLocker
description: Aiutare gli utenti finali a gestire BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824776"
---
# Aiutare gli utenti finali a gestire BitLocker


Il contenuto di un computer smarrito o rubato è vulnerabile all'accesso non autorizzato, che può presentare un rischio per la sicurezza sia per le persone che per le aziende. Microsoft BitLocker Administration and Monitoring (MBAM) USA BitLocker per impedire l'accesso non autorizzato bloccando il computer per facilitare la protezione dei dati riservati dagli utenti malintenzionati.

## Che cos'è BitLocker?


La crittografia unità BitLocker può consentire la protezione delle unità di sistema operativo, delle unità dati e delle unità rimovibili, ad esempio un'unità thumb USB, crittografando le unità. A seconda del modo in cui BitLocker è configurato, gli utenti potrebbero dover specificare una chiave (una password o un PIN) per sbloccare le informazioni archiviate nelle unità crittografate.

Quando si aggiungono nuovi file a un'unità crittografata con BitLocker, BitLocker li crittografa automaticamente. I file restano crittografati solo quando vengono archiviati nell'unità crittografata. I file copiati in un'altra unità o computer vengono decrittografati. Se si condividono file con altri utenti, ad esempio tramite una rete, questi file vengono crittografati durante l'archiviazione nell'unità crittografata, ma è possibile accedervi in genere dagli utenti autorizzati.

Se si crittografa l'unità del sistema operativo, BitLocker controlla il computer durante l'avvio per tutte le condizioni che potrebbero rappresentare un rischio per la sicurezza, ad esempio una modifica del BIOS o le modifiche apportate ai file di avvio. Se viene rilevato un potenziale rischio di sicurezza, BitLocker bloccherà l'unità del sistema operativo e richiederà una chiave di ripristino di BitLocker speciale per sbloccarla. Verificare di aver creato questo tasto di ripristino quando si attiva BitLocker per la prima volta. In caso contrario, è possibile perdere definitivamente l'accesso ai file.

Se si crittografano le unità dati (fisse o rimovibili), è possibile sbloccare un'unità crittografata con una password o una smart card oppure impostare l'unità per l'apertura automatica quando si accede al computer.

Oltre alle password e ai pin, BitLocker può usare il chip TPM (Trusted Platform Module) fornito in molti computer più recenti. Il chip TPM viene usato per verificare che il computer non sia stato manomesso prima che BitLocker sblocchi l'unità del sistema operativo. Durante il processo di crittografia potrebbe essere necessario abilitare il chip TPM. Quando si avvia il computer, BitLocker chiede al TPM le chiavi per l'unità e lo sblocca. Per abilitare il chip TPM, sarà necessario riavviare il computer e quindi modificare un'impostazione nel BIOS, un livello precedente a Windows del software del computer. Per altre informazioni sul TPM, vedere [informazioni sul chip TPM per il computer](about-the-computer-tpm-chip.md).

Quando il computer è protetto da BitLocker, potrebbe essere necessario immettere un PIN o una password ogni volta che il computer viene riattivato dalla sospensione o dall'avvio. Il supporto tecnico per la società o l'organizzazione può essere utile se si dimentica il PIN o la password.

Per disattivare BitLocker temporaneamente, è possibile sospenderlo o definitivamente decrittografando l'unità.

**Nota**  Poiché BitLocker crittografa l'intera unità e non solo i singoli file, prestare particolare attenzione quando si muovono dati riservati tra le unità. Se si trasferisce un file da un'unità protetta da BitLocker a un'unità non crittografata, il file non sarà più crittografato.

 

## Informazioni sull'applicazione di opzioni di crittografia BitLocker


Per sbloccare le unità disco rigido nel computer e gestire il PIN e le password, usare l'applicazione opzioni di crittografia BitLocker nel pannello di controllo di Windows seguendo la procedura descritta in questo articolo. È possibile immettere le password per sbloccare le unità protette e verificare lo stato di BitLocker delle unità collegate tramite questa applicazione.

**Per aprire l'applicazione opzioni di crittografia BitLocker**

1.  Fare clic sul pulsante **Start**e selezionare **Pannello di controllo**. Il pannello di controllo viene aperto in una nuova finestra.

2.  Nel **Pannello di controllo**selezionare **sistema e sicurezza**.

3.  Selezionare le **Opzioni di crittografia BitLocker** per aprire l'applicazione opzioni di crittografia BitLocker.

    Per una descrizione delle opzioni disponibili, vedere la sezione seguente.

## Opzioni nell'applicazione opzioni di crittografia BitLocker


L'applicazione opzioni di crittografia BitLocker nel pannello di controllo consente di gestire il PIN e le password, che BitLocker usa per proteggere il computer.

**Crittografia unità BitLocker-unità disco fisse:**

In questa sezione è possibile visualizzare informazioni sulle unità disco rigido connesse al computer e sullo stato di crittografia di BitLocker corrente.

-   **Gestire il pin** : consente di modificare il PIN usato da BitLocker per sbloccare l'unità del sistema operativo.

-   **Gestire la password** : consente di modificare la password usata da BitLocker per sbloccare le altre unità interne.

**Crittografia unità BitLocker-unità esterne:**

In questa sezione è possibile visualizzare informazioni sulle unità esterne, ad esempio un'unità thumb USB, connessa al computer e lo stato di crittografia corrente di BitLocker.

-   **Gestire la password** : consente di modificare la password usata da BitLocker per sbloccare le altre unità interne.

**Avanzate**

-   **Amministrazione TPM** : apre lo strumento di Amministrazione TPM in una finestra separata. Da qui è possibile configurare le attività di TPM comuni e ottenere informazioni sul chipset TPM. Per accedere a questo strumento, è necessario disporre delle autorizzazioni amministrative per il computer.

-   **Gestione disco** -aprire lo strumento Gestione disco. Da qui è possibile visualizzare le informazioni per tutti i dischi rigidi collegati al computer e configurare le partizioni e le opzioni di unità. Per accedere a questo strumento, è necessario disporre di diritti amministrativi nel computer.

 

 





