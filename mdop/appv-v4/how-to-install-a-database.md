---
title: Come installare un database
description: Come installare un database
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817376"
---
# Come installare un database


Per installare un database per la distribuzione basata su server della virtualizzazione delle applicazioni, è possibile usare la procedura seguente se non è già disponibile un database. In genere, in un ambiente di produzione, ci si connette a un database esistente.

**Importante**  Per installare il database, è necessario usare un account di rete con le autorizzazioni appropriate. Se l'organizzazione richiede che solo gli amministratori di database siano autorizzati a creare e gestire gli aggiornamenti del database, gli script sono disponibili per consentire l'esecuzione di questa attività.

 

**Per installare un database**

1.  Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic su **Setup.exe**.

2.  Nella **pagina di benvenuto**fare clic su **Avanti**.

3.  Nella pagina **contratto di licenza** , per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**e fare clic su **Avanti**.

4.  Nella pagina **registrazione informazioni** specificare il **nome utente** e le informazioni sull' **organizzazione** e quindi fare clic su **Avanti**.

5.  Nella pagina **tipo di installazione** selezionare **personalizzato** e quindi fare clic su **Avanti**.

6.  Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema di virtualizzazione delle applicazioni eccetto **Application Virtualization Server**e quindi fare clic su **Avanti**.

    **Nota**  Se un componente è già installato nel computer, deselezionarlo nella schermata di **configurazione personalizzata** verrà disinstallato automaticamente.

     

7.  Nella pagina **server database** Digitare le password, assegnare un percorso di installazione, salvare le informazioni e fare clic su **Avanti**.

8.  Selezionare un nome per il database e quindi fare clic su **Avanti**.

    **Nota**  Se viene visualizzato il messaggio di errore 25109 quando si prova a completare questo passaggio, le autorizzazioni necessarie per l'installazione del database non sono impostate in modo errato. Per informazioni dettagliate sulla configurazione delle autorizzazioni SQL necessarie, vedere <https://go.microsoft.com/fwlink/?LinkId=132144> .

     

9.  Nella schermata del **server di directory** immettere un nome di dominio e le credenziali che i server di virtualizzazione dell'applicazione e il servizio Web di gestione utilizzeranno per accedere al controller di dominio, salvare queste informazioni e quindi fare clic su **Avanti**.

    **Nota**  L'installazione verrà predefinita per il dominio del computer corrente.

     

10. Nella pagina **gruppo amministratore** immettere il nome di un gruppo che avrà privilegi di amministratore, salvare queste informazioni e quindi fare clic su **Avanti**.

    **Nota**  È anche possibile immettere i primi caratteri del nome di un gruppo che avrà privilegi di amministratore, fare clic su **Avanti**e nella schermata **selezione gruppo di amministratori** Selezionare il gruppo nell'elenco risultante. Quindi Salva queste informazioni e fai clic su **Avanti**.

     

11. Nella pagina del **gruppo provider predefinito** immettere il nome completo di un gruppo che controllerà l'accesso alle applicazioni, salvare queste informazioni e quindi fare clic su **Avanti**.

    **Nota**  È anche possibile immettere i primi caratteri del nome di un gruppo che controlla l'accesso alle applicazioni, fare clic su **Avanti**e quindi selezionare il gruppo nell'elenco nella schermata **selezione gruppo provider predefinito** . Quindi Salva queste informazioni e fai clic su **Avanti**.

     

12. Nella pagina **installazione guidata completare** , per chiudere la procedura guidata, fare clic su **fine**.

    **Importante**  L'installazione può richiedere alcuni minuti per terminare. Un messaggio di stato lampeggerà sopra l'area di notifica desktop di Windows, indicando se l'installazione è riuscita.

     

## Argomenti correlati


[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)

 

 





