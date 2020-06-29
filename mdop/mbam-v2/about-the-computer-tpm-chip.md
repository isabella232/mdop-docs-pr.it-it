---
title: Informazioni sul chip TPM del computer
description: Informazioni sul chip TPM del computer
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823535"
---
# Informazioni sul chip TPM del computer


BitLocker offre ulteriore protezione quando viene usato con un chip TPM (Trusted Platform Module). Il chip TPM è un componente hardware installato in molti computer più recenti dai produttori di computer. Microsoft BitLocker Administration and Monitoring (MBAM) USA BitLocker, oltre al chip TPM, per fornire ulteriore protezione dei dati e per assicurarsi che il computer non sia stato manomesso.

## Come configurare il TPM


Quando si avvia la crittografia guidata unità BitLocker nel computer, BitLocker verifica se l'organizzazione ha configurato BitLocker per l'uso di un chip TPM. Se BitLocker trova un chip TPM compatibile, potrebbe essere richiesto di riavviare il computer per abilitare il chip TPM per l'uso. Non appena il computer viene riavviato, seguire le istruzioni per configurare il chip TPM nel BIOS (il BIOS è un livello pre-Windows del software del computer).

Dopo la configurazione di BitLocker, è possibile accedere ad altre informazioni sul chip TPM aprendo lo strumento di opzioni di crittografia BitLocker nel pannello di controllo di Windows e quindi selezionando **Amministrazione TPM**.

**Nota**  Per accedere a questo strumento, è necessario disporre delle credenziali amministrative nel computer.

 

In un errore del TPM, una modifica del BIOS o alcuni aggiornamenti di Windows, BitLocker bloccherà il computer e richiederà di contattare il supporto tecnico per sbloccarlo. È necessario specificare il nome del computer e il dominio del computer. Help desk può fornire un file di password che può essere usato per sbloccare il computer.

## Risoluzione dei problemi relativi al TPM


Se si verifica un errore di TPM, la modifica nel BIOS o alcuni aggiornamenti di Windows, BitLocker bloccherà il computer e richiederà di contattare il supporto tecnico per sbloccarlo. È necessario specificare il nome del computer e il dominio del computer. Il supporto tecnico può fornire un file di password che può essere usato per sbloccare il computer.

## Argomenti correlati


[Aiutare gli utenti finali a gestire BitLocker](helping-end-users-manage-bitlocker.md)

[Uso di PIN o password](using-your-pin-or-password.md)

 

 





