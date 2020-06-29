---
title: Come usare il portale del supporto tecnico
description: Come usare il portale del supporto tecnico
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826326"
---
# Come usare il portale del supporto tecnico


Il sito Web di amministrazione e monitoraggio di MBAM, denominato anche portale help desk, è un'interfaccia amministrativa per la crittografia unità BitLocker installata come parte dell'infrastruttura del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM). Nelle sezioni seguenti viene descritto come usare questo sito Web per esaminare i report, recuperare le unità degli utenti finali e gestire i TPMs degli utenti finali.

## <a href="" id="bkmk-reports"></a>Rapporti


MBAM raccoglie informazioni da Active Directory e computer client, che consente di eseguire report diversi per monitorare l'uso e la conformità di BitLocker. Usando la sezione **report** del sito Web amministrazione e monitoraggio, è possibile generare report sulla conformità aziendale, sui singoli computer e sulle attività di ripristino delle chiavi. Per una descrizione di ogni report, vedere [informazioni sui report di mbam](understanding-mbam-reports-mbam-2.md).

**Per accedere ai report**

1.  Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio di MBAM.

2.  Selezionare **report** nel riquadro sinistro.

3.  Nella barra dei menu superiore selezionare il tipo di report che si vuole generare. Per salvare i report, fare clic sul pulsante **Esporta** nella barra dei menu report.

Per altre informazioni su come eseguire i report di MBAM, vedere [come generare report di mbam](how-to-generate-mbam-reports-mbam-2.md).

## <a href="" id="bkmk-drirec"></a>Ripristino unità


La funzionalità di **recupero unità** del sito Web amministrazione e monitoraggio consente agli utenti con ruoli di amministratore specifici, ad esempio gli utenti del supporto tecnico, di accedere ai dati chiave di ripristino raccolti dal client mbam. Questi dati possono essere usati per accedere a un'unità protetta da BitLocker quando BitLocker entra in modalità di ripristino. Per istruzioni su come recuperare un'unità in modalità di ripristino, vedere [come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).

È anche possibile recuperare le unità che sono state spostate o danneggiate:

-   [Come recuperare un'unità spostata](how-to-recover-a-moved-drive-mbam-2.md)

-   [Come recuperare un'unità danneggiata](how-to-recover-a-corrupted-drive-mbam-2.md)

Per altre informazioni su come recuperare un'unità protetta da BitLocker, vedere [eseguire la gestione di BitLocker con mbam](performing-bitlocker-management-with-mbam-mbam-2.md).

## <a href="" id="bkmk-manatpm"></a>Gestisci TPM


La funzionalità Gestisci TPM del sito Web di amministrazione e monitoraggio offre agli utenti determinati ruoli di amministratore, ad esempio gli utenti di "MBAM helpdesk", accedono ai dati del TPM raccolti dal client MBAM. In un blocco TPM un amministratore può usare il sito Web di amministrazione e monitoraggio per recuperare il file di password necessario per sbloccare il TPM. Per istruzioni su come reimpostare un TPM dopo un blocco TPM, vedere [come reimpostare un blocco TPM](how-to-reset-a-tpm-lockout-mbam-2.md).

## <a href="" id="bkmk-helpdesk"></a> MBAM help desk attività


È possibile usare il sito Web di amministrazione e monitoraggio per molte attività amministrative, ad esempio la gestione dell'hardware protetto da BitLocker, il recupero delle unità e l'uso di report. Per impostazione predefinita, l'URL del sito Web di amministrazione e monitoraggio è http:// &lt; *MBAMAdministrationServername* &gt; , anche se è possibile personalizzarlo durante il processo di installazione.

**Nota**  Per accedere alle varie funzionalità offerte dal sito Web di amministrazione e monitoraggio, è necessario disporre dei ruoli appropriati associati al proprio account utente. Per altre informazioni sulla comprensione dei ruoli utente, vedere [come gestire i ruoli di amministratore di mbam](how-to-manage-mbam-administrator-roles-mbam-2.md).

 

Usare i collegamenti seguenti per trovare informazioni sulle attività che è possibile eseguire tramite il sito Web amministrazione e monitoraggio:

-   [Come ripristinare un blocco del TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [Come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [Come recuperare un'unità spostata](how-to-recover-a-moved-drive-mbam-2.md)

-   [Come recuperare un'unità danneggiata](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [Come determinare lo stato della crittografia BitLocker nei computer smarriti](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





