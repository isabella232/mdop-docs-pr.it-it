---
title: Come modificare i sistemi operativi associati a un file di Windows Installer esistente
description: Come modificare i sistemi operativi associati a un file di Windows Installer esistente
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816955"
---
# Come modificare i sistemi operativi associati a un file di Windows Installer esistente


Usare la procedura seguente per modificare le versioni del sistema operativo associate a un file di Windows Installer (**MSI**) esistente creato tramite App-V Sequencer.

**Per modificare i sistemi operativi di un file di Windows Installer esistente**

1.  Installare App-V Sequencer in un computer nell'ambiente in cui è installato solo il sistema operativo. In alternativa, è possibile installare il sequencer in un computer che gestisce un ambiente virtuale, ad esempio Microsoft Virtual PC. Questo metodo è utile perché è più semplice mantenere un ambiente di sequenziazione pulito che è possibile riutilizzare con una configurazione aggiuntiva minima. Per altre informazioni sull'installazione di App-V Sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer.md).

2.  Copiare l'intero pacchetto di applicazione virtuale che contiene il file di Windows Installer che si vuole modificare nel computer in cui è in uso il sequencer.

3.  Per modificare il file di Windows Installer, aprire la console sequencer, selezionare **pacchetto**  /  **aperto**e quindi passare al percorso in cui è stato salvato il pacchetto di applicazione virtuale associato al file di Windows Installer.

4.  Per aggiungere o rimuovere sistemi operativi, selezionare la scheda **distribuzione** nella console Sequencer. Per specificare altri sistemi operativi che verranno associati al file di Windows Installer, selezionare il sistema operativo desiderato e quindi fare clic sulla freccia che punta al controllo elenco del sistema operativo **selezionato** .

    Per rimuovere un'associazione di sistema operativo, selezionare il sistema operativo che si vuole rimuovere e quindi fare clic sulla freccia che punta al controllo elenco sistema operativo **disponibile** .

5.  Per creare un nuovo Windows Installer che verrà associato al pacchetto di applicazione virtuale, selezionare **Genera pacchetto di Microsoft Windows Installer (MSI)**. In alternativa, è possibile selezionare **strumenti**per  /  **creare MSI**.

    **Nota**  Se si seleziona **strumenti** / **Crea MSI** per creare un nuovo file di Windows Installer, è possibile ignorare il **passaggio 6** di questa procedura.

     

6.  Per salvare il pacchetto di applicazione virtuale, **Package**selezionare  /  **Salva**pacchetto.

## Argomenti correlati


[Attività per Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)

 

 





