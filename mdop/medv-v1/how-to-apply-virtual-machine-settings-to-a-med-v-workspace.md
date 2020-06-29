---
title: Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V
description: Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825975"
---
# Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V


Ogni area di lavoro MED-V deve avere un'immagine di Microsoft Virtual PC associata. Le impostazioni della macchina virtuale consentono di assegnare un'immagine Virtual PC e di impostare altre proprietà della macchina virtuale.

Tutte le impostazioni della macchina virtuale sono configurate nel modulo **criteri** , nella scheda **Impostazioni macchina virtuale** .

**Per applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V per configurare.

2.  Configurare le proprietà della macchina virtuale come descritto nella tabella seguente.

3.  Nel menu **criteri** selezionare **commit**.

**Proprietà della macchina virtuale**

Impostazioni della *macchina virtuale* della descrizione della proprietà

Immagine assegnata

Immagine effettiva di Microsoft Virtual PC assegnata all'area di lavoro MED-V. Il menu contiene un elenco di tutte le immagini di Virtual PC disponibili. I tipi di immagine seguenti si trovano nell'elenco delle immagini **attive** :

-   **Immagini di test locali**: immagini nel computer locale non ancora imballate. Questi nomi di immagine sono seguiti dalla parola "test" tra parentesi (test) e sono solo per scopi di test.

-   **Immagini**imballate locali: immagini confezionate nel computer locale. Queste immagini sono seguite dalla parola "local" tra parentesi (local) e non possono essere scaricate dai client finché l'amministratore non le carica nel server.

    È possibile selezionare un'immagine locale se si sta creando un pacchetto che verrà distribuito al client tramite elementi multimediali rimovibili, ad esempio USB o DVD.

-   **Immagini imballate sul server**: immagini presenti nel server e disponibili per il download dai client. Fare clic su Aggiorna per aggiornare l'elenco immagini.

    **Nota**  Ogni immagine dell'area di lavoro MED-V può essere usata solo da un utente di Windows.

     

L'area di lavoro è persistente

Selezionare questa casella di controllo per configurare l'area di lavoro MED-V come persistente. In un'area di lavoro MED-V persistente, quando l'area di lavoro MED-V viene interrotta, le modifiche e le aggiunte all'area di lavoro MED-v vengono salvate nell'area di lavoro MED-V.

Per un'area di lavoro di dominio MED-V, questa opzione deve essere selezionata.

**Nota**  Questa impostazione non deve essere modificata dopo la distribuzione di un'area di lavoro MED-V agli utenti.

 

Arrestare la VM quando si arresta l'area di lavoro

Selezionare questa casella di controllo per arrestare la macchina virtuale quando si arresta l'area di lavoro MED-V. Se questa casella di controllo è deselezionata, al termine di ogni sessione la macchina virtuale non viene arrestata, ma accetta invece uno snapshot della macchina virtuale. Dopo l'avvio di una nuova sessione, Windows viene avviato dallo snapshot, ovvero Windows non viene riavviato e non è necessario alcun accesso.

**Nota**  Questa proprietà è abilitata solo se l' **area di lavoro è permanente** selezionata.

 

Accedere a Windows in VM usando le credenziali MED-V (SSO)

Selezionare questa casella di controllo per accedere a Windows nella macchina virtuale usando le credenziali MED-V immesse durante l'accesso al client MED-V.

**Nota**  Questa proprietà è abilitata solo quando è selezionata l' **area di lavoro persistente** .

 

Area di lavoro è revertible

Selezionare questa casella di controllo per configurare l'area di lavoro MED-V come revertible. In un'area di lavoro di revertible MED-V, al termine di ogni sessione (ovvero quando l'utente interrompe l'area di lavoro MED-V), l'area di lavoro MED-V ripristina lo stato originale durante la distribuzione. Nessuna modifica o aggiunta che l'utente ha eseguito viene salvata nell'area di lavoro MED-V tra le sessioni.

**Nota**  Questa impostazione non deve essere modificata dopo la distribuzione di un'area di lavoro MED-V agli utenti.

 

Sincronizzare il fuso orario dell'area di lavoro con host

Selezionare questa casella di controllo per sincronizzare il fuso orario nell'area di lavoro MED-V con l'host.

La sincronizzazione funziona in modo diverso a seconda che l'area di lavoro MED-V sia permanente o revertible, come indicato di seguito:

-   In un'area di lavoro MED-V persistente, il fuso orario cerca prima di eseguire la sincronizzazione con il server. Se l'operazione non riesce, viene sincronizzata con l'host.

-   In un'area di lavoro di revertible MED-V, il fuso orario viene sincronizzato con l'host.

*Bloccare le impostazioni*

Bloccare l'area di lavoro nell'evento standby/ibernazione host

Selezionare questa casella di controllo per bloccare automaticamente l'area di lavoro MED-V quando il computer host entra in standby o in ibernazione.

Bloccare l'area di lavoro dopo

Selezionare questa casella di controllo per bloccare l'area di lavoro MED-V quando l'area di lavoro MED-V è inattiva per un periodo di tempo specificato. Quando l'opzione è selezionata, la casella numero è abilitata. Immettere il numero di minuti di tempo di inattività prima di bloccare l'area di lavoro MED-V.

**Nota**  Il tempo di inattività fa riferimento alle applicazioni di area di lavoro MED-V (non alle applicazioni host).

 

*Impostazioni di aggiornamento delle immagini*

Mantieni solo

Selezionare questa casella di controllo per limitare il numero di versioni di immagini obsolete da conservare.

Quando l'opzione è selezionata, la casella numero è abilitata. Immettere il numero di versioni precedenti da conservare.

Suggerisci aggiornamento quando è disponibile una nuova versione

Selezionare questa casella di controllo per suggerire (ma non forzare) un aggiornamento quando è disponibile una nuova versione dell'immagine.

I client devono usare il trasferimento trim durante il download di immagini per l'area di lavoro

Selezionare questa casella di controllo per abilitare il trasferimento Trim (per altre informazioni, vedere [tecnologia di trasferimento Trim Med-v](med-v-trim-transfer-technology-medvv2.md)) durante il download di immagini associate all'area di lavoro MED-v. Se questa casella di controllo è deselezionata, verrà scaricata l'immagine completa.

**Nota**  Trim Transfer richiede l'indicizzazione del disco rigido, che può richiedere molto tempo. È consigliabile usare il trasferimento di trim quando l'indicizzazione del disco rigido è più efficiente del download della nuova versione dell'immagine, ad esempio quando si scarica una versione di immagine simile alla versione esistente.

 

 

## Argomenti correlati


[Creazione di un'immagine MED-V](creating-a-med-v-image.md)

[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





