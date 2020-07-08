---
title: Pagina File di installazione
description: Pagina File di installazione
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816345"
---
# Pagina File di installazione


Usare la pagina **file di installazione** per specificare i file di installazione usati per creare il pacchetto di applicazione virtuale specificato nella pagina **Seleziona pacchetto** della procedura guidata. Se è stato creato un pacchetto di applicazione virtuale che contiene più applicazioni, è consigliabile copiare tutti i file di installazione necessari in una singola cartella nel computer in cui è installato Microsoft Application Virtualization Sequencer.

Questa pagina contiene gli elementi seguenti:

<a href="" id="original-installation-files"></a>**File di installazione originali**  
Fare clic su **Sfoglia** per specificare i file di installazione usati in origine per creare il pacchetto di applicazione virtuale. La directory padre specificata deve essere salvata localmente nel computer che esegue il sequencer e deve contenere tutti i file di installazione necessari o le sottocartelle che contengono i file di installazione. I file di installazione possono essere contenuti nella cartella padre o in una delle sottocartelle della cartella padre specificata.

<a href="" id="files-installed-on-local-system"></a>**File installati nel sistema locale**  
Fare clic su **Sfoglia** per specificare i file di installazione installati localmente nel computer in cui è in uso Sequencer. Puoi selezionare questa opzione solo se i file di installazione dell'applicazione sono stati installati nella posizione predefinita dell'applicazione.

**Nota**  Il percorso di installazione predefinito fornito dipende dalle condizioni seguenti:

 

-   Radice del pacchetto specificata quando il pacchetto è stato creato in origine.

-   Il percorso di installazione specificato in Windows Installer quando il pacchetto è stato creato in origine.

-   Percorso di installazione dell'applicazione predefinito.

Ad esempio, se la radice del pacchetto specificata è **Q:\\Office12** e durante l'installazione, il percorso di installazione predefinito viene modificato da **C:\\Programmi Files\\Office12** a **Q:\\Office12**, il percorso specificato durante la disidratazione deve essere **c:\\Programmi Files\\Office 12**.

Se la radice del pacchetto specificata è **Q:\\Microsoft** e durante l'installazione, la posizione di installazione predefinita viene modificata da **C:\\Programmi Files\\Office12** a **Q:\\Microsoft\\Office12**, il percorso specificato durante la disidratazione deve essere **c:\\Programmi file**.

Quando crei un pacchetto usando un acceleratore di pacchetto, ogni file nel pacchetto, ad esempio **Q:\\Office12\\file.txt** si trova nel computer locale sostituendo il pacchetto radice **Q:\\Office12** con il percorso predefinito specificato quando è stato creato l'acceleratore del pacchetto, ad esempio **c:\\Programmi Files\\Office12**. Nell'esempio precedente il file deve trovarsi in **c:\\programmi Files\\Office12\\file.txt**.

## Argomenti correlati


[Procedura guidata Crea Acceleratore pacchetto (AppV 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





