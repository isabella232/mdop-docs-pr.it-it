---
title: Come gestire manualmente le applicazioni virtuali
description: Come gestire manualmente le applicazioni virtuali
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817115"
---
# Come gestire manualmente le applicazioni virtuali


Puoi usare la console di gestione client Application Virtualization (App-V) per gestire le applicazioni virtuali nel client Desktop App-V o nel client App-V per Servizi Desktop remoto (in precedenza Servizi terminal). Gli amministratori di App-V possono usare eseguire le attività seguenti:

## Come caricare o scaricare un'applicazione App-V


Puoi usare le procedure seguenti per caricare o scaricare un'applicazione dalla cache, direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione dei client di virtualizzazione dell'applicazione. Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di applicazioni.

**Nota**  Quando carichi o scarichi un pacchetto, tutte le applicazioni nel pacchetto vengono caricate o rimosse dalla cache. Quando si carica un pacchetto, se non si dispone di spazio sufficiente nella cache per caricare le applicazioni, aumentare le dimensioni della cache. Per altre informazioni sulle dimensioni della cache, vedere [come modificare le dimensioni della cache e la denominazione della lettera dell'unità](how-to-change-the-cache-size-and-the-drive-letter-designation.md).

 

**Per caricare un'applicazione App-V**

1.  Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **carica** dal menu a comparsa.

2.  L'applicazione viene caricata automaticamente. Lo stato di avanzamento viene registrato nella colonna contrassegnata come **stato del pacchetto**. È necessario aggiornare la visualizzazione per verificare che il caricamento sia completo o per visualizzare lo stato di avanzamento.

**Per scaricare un'applicazione App-V**

1.  Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Scarica** dal menu a comparsa.

2.  L'applicazione viene scaricata automaticamente e la colonna **stato del pacchetto** viene aggiornata per riflettere la modifica.

## Come cancellare un'applicazione App-V


È possibile cancellare un'applicazione dalla console direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization. Quando si deseleziona un'applicazione, il sistema rimuove le impostazioni, i tasti di scelta rapida e le associazioni di tipi di file che corrispondono all'applicazione e rimuove anche l'applicazione dall'elenco di applicazioni dell'utente.

**Nota**  Quando si deseleziona un'applicazione dalla console, non è più possibile usare tale applicazione. Tuttavia, l'applicazione rimane nella cache ed è ancora disponibile per altri utenti nello stesso sistema. Dopo un aggiornamento della pubblicazione, le applicazioni deselezionate diventeranno di nuovo disponibili. Se sono presenti più applicazioni in un pacchetto, le impostazioni dell'utente non vengono rimosse finché tutte le applicazioni non vengono cancellate.

 

**Per cancellare un'applicazione dalla console**

1.  Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Cancella** dal menu a comparsa.

2.  Alla richiesta di conferma fare clic su **Sì** per rimuovere l'applicazione o fare clic su **No** per annullare l'operazione.

## Come ripristinare un'applicazione App-V


Per ripristinare un'applicazione selezionata, è possibile eseguire la procedura seguente direttamente dal riquadro dei **risultati** del nodo **applicazione** nella console di gestione client Application Virtualization. Quando si ripristina un'applicazione, si rimuovono le impostazioni utente personalizzate e si ripristinano le impostazioni predefinite. Questa azione non modifica né elimina i collegamenti o le associazioni di tipi di file e non rimuove l'applicazione dalla cache.

**Per ripristinare un'applicazione App-V**

1.  Posizionare il cursore nel riquadro **dei risultati** .

2.  Fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Ripristina** dal menu a comparsa.

3.  Alla richiesta di conferma fare clic su **Sì** per ripristinare l'applicazione o **No** per annullare l'annullamento.

## Come importare un'applicazione App-V


È possibile usare la procedura seguente per importare un'applicazione nella cache direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.

**Per importare un'applicazione App-V**

1.  Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Importa** dal menu a comparsa.

2.  Nella finestra **Sfoglia** passare al percorso del file del pacchetto per l'applicazione desiderata e quindi fare clic su **OK**.

    **Nota**  Se è già stato configurato un percorso di ricerca di importazione o se il file SFT si trova nello stesso percorso dell'ultima importazione riuscita, il passaggio 2 non è obbligatorio.

     

## Come bloccare o sbloccare un'applicazione App-V


È possibile usare le procedure seguenti per bloccare o sbloccare qualsiasi applicazione nella cache del client Desktop Application Virtualization o nel client per la cache dei Servizi Desktop remoto (in precedenza Servizi terminal). Non è possibile rimuovere un'applicazione bloccata dalla cache per creare spazio per le nuove applicazioni. Per rimuovere un'applicazione bloccata dalla cache client Desktop Application Virtualization o dal client per la cache dei Servizi Desktop remoto, è necessario prima di tutto sbloccarla.

**Per bloccare un'applicazione**

1.  Posizionare il cursore nel riquadro **dei risultati** .

2.  Fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **blocca** dal menu a comparsa. L'applicazione selezionata è bloccata nella cache.

**Per sbloccare un'applicazione**

1.  Posizionare il cursore nel riquadro **dei risultati** .

2.  Fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Sblocca** dal menu a comparsa. L'applicazione selezionata viene sbloccata nella cache e può essere rimossa.

## Come eliminare un'applicazione App-V


Quando si seleziona il nodo **dell'applicazione** nella console di gestione client Application Virtualization, nel riquadro dei **risultati** viene visualizzato un elenco di applicazioni. Puoi usare la procedura seguente per eliminare un'applicazione dal riquadro dei **risultati** , che rimuove anche l'applicazione dalla cache.

**Nota**  Quando si elimina un'applicazione, l'applicazione selezionata non sarà più disponibile per gli utenti di tale client. I tasti di scelta rapida e le associazioni di tipi di file sono nascosti e l'applicazione viene eliminata dalla cache. Tuttavia, se un'altra applicazione fa riferimento ai dati nei dati della cache del file System per l'applicazione selezionata, questi elementi non verranno eliminati.

Dopo un aggiornamento della pubblicazione, le applicazioni eliminate diventeranno di nuovo disponibili.

 

**Per eliminare un'applicazione**

1.  Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Elimina** dal menu a comparsa.

2.  Alla richiesta di conferma fare clic su **Sì** per rimuovere l'applicazione o fare clic su **No** per annullare l'operazione.

## Come modificare un'icona dell'applicazione App-V


È possibile usare la procedura seguente per modificare un'icona associata all'applicazione selezionata direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.

**Per modificare un'icona dell'applicazione**

1.  Posizionare il cursore nel riquadro **dei risultati** e fare clic con il pulsante destro del mouse sull'applicazione desiderata.

2.  Selezionare **Proprietà**.

3.  Nella scheda **generale** fare clic su **Cambia icona**.

4.  Selezionare l'icona desiderata oppure passare a un'altra posizione per selezionare l'icona. Dopo aver selezionato l'icona, fare clic su **OK**. La nuova icona viene visualizzata nel riquadro **dei risultati** .

## Come aggiungere un'applicazione App-V


È possibile usare la procedura seguente per aggiungere un'applicazione direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.

**Per aggiungere un'applicazione**

1.  Nel riquadro **risultati** fare clic con il pulsante destro del mouse e scegliere **nuova applicazione** dal menu a comparsa.

2.  Nella pagina della procedura guidata è possibile eseguire le attività seguenti:

    1.  **Icona cambia**: Visualizza un browser di icone standard di Windows. Individuare e selezionare l'icona desiderata.

    2.  **URL o percorso file OSD**: immettere un percorso assoluto locale, un percorso UNC completo (file condiviso o directory in una rete) o un URL http.

    3.  **(Pulsante Sfoglia OSD)**: Visualizza la finestra di dialogo standard di Windows **Open file** . Individuare il file desiderato.

3.  Fare clic su **fine** per aggiungere l'applicazione al riquadro **risultati** .

## Come pubblicare un collegamento a un'applicazione App-V


Puoi usare la procedura seguente per pubblicare i collegamenti a un'applicazione direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.

**Per pubblicare i collegamenti alle applicazioni**

1.  Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **nuovo collegamento** dal menu a comparsa per visualizzare la creazione guidata nuovo collegamento.

2.  Nella prima pagina della creazione guidata nuovo collegamento selezionare un'icona e specificare un nome per il collegamento.

    1.  **Icona cambia**: Visualizza un browser di icone standard di Windows. Individuare e selezionare l'icona desiderata.

    2.  **Titolo del collegamento**: immettere il nome che si vuole assegnare al collegamento. Questo campo viene impostato come predefinito per il nome e la versione esistenti dell'applicazione.

3.  Nella seconda pagina della procedura guidata determinare la posizione del collegamento pubblicato.

    1.  **Desktop**: selezionare questa casella di controllo per pubblicare il collegamento sul desktop.

    2.  **Barra di avvio veloce**: selezionare questa casella di controllo per pubblicare il collegamento sulla barra di avvio veloce.

    3.  **Menu Invia a**: selezionare questa casella di controllo per pubblicare il collegamento al menu **Invia a** .

    4.  **Programmi nel menu Start**: quando si seleziona la casella di controllo **menu Start** , questo campo diventa attivo. Lascia vuoto questo campo per pubblicare il collegamento direttamente nella radice della cartella programmi oppure immetti un nome di cartella o una gerarchia, ad esempio "My \ _Computer applicazioni \\Office". I collegamenti creati in questo modo sono disponibili solo per l'utente corrente.

    5.  **Altro percorso** e pulsante **Sfoglia** : quando si seleziona la casella di controllo **altro percorso** , questo campo diventa attivo. Immettere una posizione valida nel computer o in qualsiasi percorso UNC disponibile (file condiviso o directory in una rete). Il pulsante **Sfoglia** Visualizza una finestra di dialogo **Apri file** standard di Windows.

4.  Nella terza pagina della procedura guidata Immetti i parametri della riga di comando desiderati.

5.  Fare clic su **fine** per pubblicare i tasti di scelta rapida e quindi uscire dal riquadro **risultati** .

## Come aggiungere un'associazione di tipi di file per un'applicazione App-V


Puoi usare la procedura seguente per aggiungere un'associazione di tipi di file, usando il nodo **associazioni di tipi di file** nella console di gestione client Application Virtualization.

**Per aggiungere un'associazione di tipi di file**

1.  Fare clic con il pulsante destro del mouse sul nodo **associazioni tipo file** e scegliere **nuova associazione** dal menu a comparsa.

2.  Completare il primo passaggio della finestra di dialogo completando le informazioni seguenti e quindi fare clic su **Avanti**:

    1.  **Estensione**: immettere una nuova estensione del nome file. Questo campo è vuoto per impostazione predefinita.

    2.  **Creare un nuovo tipo di file con questa descrizione**: selezionare questo pulsante di opzione per immettere una nuova descrizione del tipo di file nel campo attivo. Questo pulsante è selezionato per impostazione predefinita e il campo attivo è vuoto.

    3.  **Applica questo tipo di file a tutti gli utenti**: selezionare questa casella di controllo quando si vuole che l'associazione sia globale per tutti gli utenti. Per impostazione predefinita, questa casella è deselezionata.

    4.  **Collegare questa estensione a un tipo di file esistente**: selezionare questo pulsante di opzione per associare l'estensione a un tipo di file esistente. Selezionare un tipo di file nell'elenco a discesa. Quando si sceglie questa opzione, il **successivo** viene modificato in **fine**.

3.  Completare il secondo passaggio della finestra di dialogo completando le informazioni seguenti e quindi fare clic su **fine** per tornare alla console di gestione client:

    1.  **Icona cambia**: fare clic su questo pulsante per modificare l'icona dell'applicazione. Selezionare una delle icone disponibili oppure passare a una nuova posizione e selezionare un'icona.

    2.  **Aprire i file con l'applicazione selezionata**: selezionare questo pulsante di opzione per aprire il file con un'applicazione esistente. Scegliere un'applicazione nell'elenco a discesa delle applicazioni disponibili.

    3.  **Aprire il file con l'associazione descritta in questo file OSD**: selezionare questo pulsante di opzione per specificare un file OSD (Open Software Descriptor) che determina l'applicazione usata per aprire il file. Usare il pulsante Sfoglia per selezionare una posizione esistente oppure immettere un percorso o un URL in formato HTTP in questo campo.

## Come eliminare un'associazione di tipi di file per un'applicazione App-V


Per eliminare un'associazione di tipi di file, è possibile usare la procedura seguente. Il nodo **associazioni tipo di file** è un livello sotto il nodo **Application Virtualization** nel riquadro **ambito** . Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di associazioni di tipi di file.

**Per rimuovere un'associazione di tipi di file**

1.  Nel riquadro **risultati** fare clic con il pulsante destro del mouse sull'estensione dell'associazione del tipo di file che si desidera eliminare.

2.  Selezionare **Elimina** dal menu a comparsa.

3.  Fare clic su **Sì** per eliminare l'associazione oppure fare clic su **No** per tornare al riquadro **risultati** .

## Argomenti correlati


[Application Virtualization Client](application-virtualization-client.md)

 

 





