---
title: Come modificare le proprietà di distribuzione
description: Come modificare le proprietà di distribuzione
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818065"
---
# Come modificare le proprietà di distribuzione


Puoi usare le procedure seguenti per modificare le informazioni sulla scheda **distribuzione** per un'applicazione che stai sequenziando, incluso l'URL del server di virtualizzazione dell'applicazione, i sistemi operativi richiesti dalle applicazioni virtualizzate e le opzioni di output per l'applicazione virtuale da installare.

**Per modificare l'URL del server**

1.  Selezionare il protocollo di flusso dalla casella di riepilogo a discesa.

2.  Immettere il nome host del server delle applicazioni virtuali o del bilanciamento del carico del gruppo Server. È possibile usare il nome host o l'indirizzo IP effettivo.

3.  Specifica il numero di porta in cui il server delle applicazioni virtuali o il bilanciamento del carico ascolteranno una richiesta client Desktop Application Virtualization per l'applicazione in streaming.

4.  Specificare il percorso relativo nel server delle applicazioni virtuali in cui è archiviato il pacchetto software.

**Per modificare i requisiti dei sistemi operativi dell'applicazione**

1.  Per aggiungere il sistema operativo o i sistemi operativi necessari, selezionarlo nell'elenco **disponibile** e fare clic sul pulsante freccia che punta al controllo elenco dei sistemi operativi **selezionati** .

2.  Per rimuovere un sistema operativo, selezionarlo nel controllo elenco **selezionato** e fare clic sul pulsante freccia che punta al controllo elenco sistemi operativi **disponibili** .

**Per modificare le opzioni di output dell'applicazione**

1.  Nell'elenco a discesa **algoritmo di compressione** selezionare il metodo di compressione da usare quando si esegue il flusso dell'applicazione.

2.  Selezionare la casella di controllo **applica descrittori di sicurezza** per verificare che i descrittori di sicurezza delle applicazioni con pacchetto vengano applicati durante la distribuzione.

3.  Seleziona **genera file Difference** per generare un file Difference per l'applicazione dalla versione sequenziata precedente.

4.  Selezionare **Genera pacchetto di Microsoft Windows Installer (MSI)** per creare un pacchetto di installazione.

## Argomenti correlati


[Informazioni sulla scheda Distribuzione](about-the-deployment-tab.md)

[Console di Sequencer](sequencer-console.md)

 

 





