---
title: Gestione delle stampanti in un'area di lavoro MED-V
description: Gestione delle stampanti in un'area di lavoro MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826116"
---
# Gestione delle stampanti in un'area di lavoro MED-V


In Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, il reindirizzamento della stampante offre agli utenti finali un'esperienza di stampa coerente tra la macchina virtuale MED-V e il computer host.

In questo argomento vengono fornite informazioni su come gestire la stampa in un'area di lavoro MED-V.

## Gestione delle stampanti nelle aree di lavoro MED-V


Nella maggior parte dei casi, MED-V gestisce automaticamente il reindirizzamento della stampante. Al termine della configurazione per la prima volta, MED-V identifica tutte le stampanti di rete installate nell'host, recupera i driver corrispondenti dal server di stampa della rete e, se disponibile, installa i driver rilevanti nell'area di lavoro MED-V. Dopo aver trovato e installato tutti i driver, MED-V riavvia l'area di lavoro MED-V. Solo dopo il riavvio dell'area di lavoro MED-V, le stampanti host sono presenti e disponibili nel guest, in genere in pochi minuti.

**Nota**  Se le applicazioni sono in uso nell'area di lavoro MED-V, viene chiesto all'utente finale di consentire al riavvio di continuare o di rinviarlo fino a un secondo momento. Se non sono in uso applicazioni, il riavvio è automatico e non viene visualizzato per l'utente finale.

 

Ogni volta che MED-V viene riavviato, controlla se le nuove stampanti sono installate nell'host e, se presenti, recupera i driver corrispondenti dal server di stampa della rete e li installa nel guest. MED-V riavvia quindi l'area di lavoro MED-V proprio come al termine della configurazione per la prima volta.

**Importante**  Dopo aver installato i driver rilevanti per l'ospite, le stampanti diventano visibili solo dopo che il riavvio si è verificato.

 

Se in qualsiasi momento non è possibile localizzare o installare un driver, è necessario che sia installato manualmente nel guest per consentire alla stampante di rete di essere disponibile per l'utente finale.

L'elenco seguente offre alcune indicazioni aggiuntive:

**MED-V gestisce solo le stampanti di rete**. I driver per le stampanti installate localmente nell'host non vengono installati automaticamente nell'ospite.

**MED-V installa solo i driver della stampante se presenti nel server di stampa**. Se non viene trovato, i driver della stampante devono essere installati manualmente.

**Le stampanti installate manualmente nel guest non sono accessibili all'host**. Per impostazione predefinita, MED-V supporta solo il reindirizzamento della stampante dall'ospite all'host.

**Avviso**  Se una stampante è installata manualmente nel guest e la stessa stampante viene installata in seguito nell'host, il risultato è che la stampante viene installata due volte nel guest. Per evitare questa situazione, una procedura consigliata per MED-V consiste nel gestire il reindirizzamento della stampante in un solo modo: disabilitare il reindirizzamento e installare le stampanti manualmente nell'ospite o abilitare il reindirizzamento e non installare le stampanti manualmente nell'ospite.

 

## Argomenti correlati


[Gestire le impostazioni dell'area di lavoro MED-V](manage-med-v-workspace-settings.md)

 

 





