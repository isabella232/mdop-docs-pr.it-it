---
title: Compattazione del disco rigido virtuale MED-V
description: Compattazione del disco rigido virtuale MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823276"
---
# Compattazione del disco rigido virtuale MED-V


Anche se è facoltativo, puoi compattare il disco rigido virtuale (VHD) per recuperare spazio su disco vuoto e ridurre le dimensioni del VHD prima di configurare l'immagine di Windows Virtual PC.

**Importante**  Prima di procedere, creare una copia di backup dell'immagine di Windows XP.

 

**Preparazione del disco rigido virtuale**

1.  Aprire l'immagine di Windows XP.

    Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**, Windows **Virtual PC**e quindi fare doppio clic sull'immagine di Windows XP.

2.  Cancellare la cache DLL.

    1.  Al prompt dei comandi nella macchina virtuale digitare **sfc/cachesize = 1**.

    2.  Riavviare la macchina virtuale.

    3.  Al prompt dei comandi nella macchina virtuale digitare **sfc/purgecache**.

3.  Eliminare i file non necessari, ad esempio i programmi di disinstallazione, i file temporanei, i file di log, i file di pagina, le cartelle condivise e così via.

4.  Disattivare Ripristino configurazione di sistema. È anche possibile specificare questo passaggio nel file Sysprep. inf.

    1.  Nel **Pannello di controllo**fare doppio clic su **sistema**e quindi selezionare la scheda **Ripristino configurazione di sistema** .

    2.  Selezionare **Disattiva Ripristino configurazione di sistema**e quindi fare clic su **OK**.

5.  Impostare le dimensioni massime del log eventi e cancellare tutti gli eventi.

    1.  Aprire il Visualizzatore eventi.

        Fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, fare doppio clic su **strumenti di amministrazione**e quindi fare doppio clic su **Visualizzatore eventi**.

    2.  Fare clic con il pulsante destro del mouse su **applicazione**e scegliere **Proprietà**.

    3.  Nell'area **dimensioni log** impostare la **dimensione massima del log** su 512KB e quindi selezionare **Sovrascrivi eventi in base alle esigenze**.

    4.  Fare clic su **Cancella log**. Nella finestra di dialogo **Visualizzatore eventi** che viene visualizzata fare clic su **No**.

    5.  Nella finestra **Proprietà** fare clic su **OK**.

    6.  Ripetere i passaggi da a a e per i registri di **sicurezza** e di **sistema** .

6.  Eseguire lo strumento di pulizia disco.

    Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Accessori**, **strumenti di sistema**e quindi fare clic su **pulizia disco**.

7.  Configurare il file di pagina in base alle esigenze per le applicazioni.

    1.  Nel **Pannello di controllo**fare doppio clic su **sistema**e quindi selezionare la scheda **Avanzate** .

    2.  Nell'area **prestazioni** fare clic su **Impostazioni**.

    3.  Nell'area **memoria virtuale** fare clic su **Cambia**.

    4.  Configurare le impostazioni del file di pagina.

8.  Arrestare l'immagine di Windows XP.

**Deframmentazione e pre-compattazione del disco rigido virtuale**

1.  Nel **Pannello di controllo** nel computer host che sta usando Windows 7 fare clic **su strumenti di amministrazione**, fare doppio clic su **Gestione computer**e quindi su **Gestione disco**.

2.  Usando la console Gestione disco, allegare (montare) il disco rigido virtuale e quindi deframmentare il disco.

3.  Usando uno strumento di estrazione ISO, Estrai il precompact. ISO nella cartella componenti virtuali di PC\\Integration Files\\Windows cartella.

4.  Usare il programma precompact.exe per comprimere il disco rigido virtuale di Windows XP.

5.  Se si usa la console Gestione disco, scollegare il disco rigido virtuale.

**Compattazione del disco rigido virtuale**

1.  Aprire Windows Virtual PC.

    Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**e quindi fare clic su **Virtual PC Windows**.

2.  Fare clic con il pulsante destro del mouse sull'immagine di Windows XP e scegliere **Impostazioni**.

3.  Fare clic su **disco rigido** per quello corrispondente all'immagine di Windows XP e quindi fare clic su **modifica**.

4.  Fare clic su **disco rigido virtuale compatto**.

5.  Fare clic su **compatta** e quindi su **OK**.

Creare una copia di backup del disco rigido virtuale compattato.

## Argomenti correlati


[Configurazione di un'immagine di Windows Virtual PC per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Documentazione tecnica su MED-V](technical-reference-for-med-v.md)

 

 





