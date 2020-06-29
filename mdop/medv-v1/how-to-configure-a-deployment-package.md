---
title: Come configurare un pacchetto di distribuzione
description: Come configurare un pacchetto di distribuzione
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825946"
---
# Come configurare un pacchetto di distribuzione


La procedura guidata per la creazione di pacchetti illustra come creare una cartella nel computer locale e trasferire tutti i file di installazione necessari alla singola cartella. Il contenuto della cartella può quindi essere spostato in più unità multimediali rimovibili per la distribuzione.

**Nota**  
Un singolo pacchetto non può contenere file di installazione per sistemi x86 e x64.



## Come creare un pacchetto di distribuzione


**Per creare un pacchetto di distribuzione**

1. Verificare nel modulo **Immagini** che è stata creata almeno un'immagine imballata locale.

2. Nel menu **strumenti** selezionare **creazione guidata pacchetti**.

3. Nella pagina di benvenuto della **creazione guidata pacchetti** fare clic su **Avanti**.

4. Nella pagina **immagine area di lavoro** selezionare la casella di controllo **Includi immagine nel pacchetto** per includere un'immagine nel pacchetto.

   Il campo **immagine** è abilitato.

   **Nota**  
   Un'immagine non è obbligatoria in un pacchetto MED-V. il pacchetto può essere creato senza un'immagine. In questo caso, l'immagine deve essere caricata nel server in modo che possa essere successivamente scaricata tramite la rete nel client oppure inserita in una cartella di pre-stage.



5. Fare clic sull'elenco **Immagini** per visualizzare tutte le immagini disponibili. Selezionare l'immagine da copiare nel pacchetto. Fare clic su **Aggiorna** per aggiornare l'elenco delle immagini disponibili.

6. Fai clic su **Avanti**.

7. Nella pagina **impostazioni di installazione di Med-v** selezionare il file di installazione di Med-v eseguendo una delle operazioni seguenti:

   -   Nel campo **file di installazione di MED-V** Digitare il percorso completo della directory in cui si trova il file di installazione.

   -   Fare clic su **...** per passare alla directory in cui si trova il file di installazione.

   **Nota**  
   Questo campo è obbligatorio e la procedura guidata non continuerà senza un nome di file valido.



8. Nel campo **Indirizzo server** Digitare il nome del server o l'indirizzo IP.

9. Nel campo **porta server** Digitare la porta del server.

10. Selezionare la casella di controllo **server accessibile tramite HTTPS** per richiedere una connessione HTTPS per la connessione al server.

11. Effettua una delle seguenti operazioni:

    -   Fare clic su **impostazioni di installazione predefinite**, quindi fare clic su **Avanti** per continuare e uscire dalle impostazioni predefinite.

    -   Fare clic su **impostazioni di installazione personalizzate**, quindi fare clic su **Avanti** per personalizzare le impostazioni di installazione.

        1.  Nella pagina **impostazioni personalizzate per l'installazione di Med-v** Digitare nel campo **cartella di installazione** il percorso della cartella in cui verranno installati i file MED-v nel computer host.

            **Nota**  
            È consigliabile usare le variabili nel percorso anziché nelle costanti, che possono variare da computer a computer.

            Ad esempio, USA *%ProgramFiles%\\MED-V* invece di *c:\\MED-V*.



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. Nella pagina **installazioni aggiuntive** selezionare la casella di controllo **Includi l'installazione del software di virtualizzazione** per includere l'installazione di Virtual PC nel pacchetto.

    Il campo **file di installazione** è abilitato. Digitare il percorso completo del file di installazione del software di virtualizzazione oppure fare clic su **...** per passare alla directory.

13. Selezionare la casella di controllo **Includi installazione di Virtual PC QFE** per includere l'installazione di Virtual PC Update nel pacchetto.

    Il campo **file di installazione** è abilitato. Digitare il percorso completo del file di installazione di Virtual PC Update oppure fare clic su **...** per passare alla directory.

14. Selezionare la casella di controllo **Includi l'installazione di Microsoft .NET framework 2,0** per includere l'installazione di Microsoft .net Framework 2,0 nel pacchetto.

    Il campo **file di installazione** è abilitato. Digitare il percorso completo del file di installazione di Microsoft .NET Framework 2,0 oppure fare clic su **...** per passare alla directory.

15. Fai clic su **Avanti**.

16. Nella pagina **finalizza** selezionare la posizione in cui deve essere salvato il pacchetto eseguendo una delle operazioni seguenti:

    -   Nel campo **destinazione pacchetto** Digitare il percorso completo della directory in cui deve essere salvato il pacchetto.

    -   Fare clic su **...** per passare alla directory in cui devono essere salvati i file di installazione.

    **Nota**  
    La creazione del pacchetto può richiedere più spazio rispetto alle dimensioni effettive del pacchetto. È quindi consigliabile creare il pacchetto sul disco rigido. Dopo aver creato il pacchetto, è possibile copiarlo nel dispositivo USB.



17. Nel campo **nome pacchetto** immettere un nome per il pacchetto.

18. Fare clic su **fine** per creare il pacchetto.

    Il pacchetto viene creato. Potrebbero essere necessarie diversi minuti.

    Dopo aver creato il pacchetto, viene visualizzato un messaggio che informa che è stato completato correttamente.

**Nota**  
Se sono stati salvati tutti i file localmente e non direttamente nel supporto rimovibile, assicurarsi di copiare solo il contenuto della cartella e non la cartella stessa nel supporto rimovibile.



**Nota**  
Il supporto rimovibile deve essere abbastanza grande in modo che il contenuto del pacchetto consumi un massimo di tre quarti della memoria del supporto rimovibile.



**Nota**  
Quando si crea il pacchetto, le dimensioni effettive del pacchetto potrebbero essere necessarie fino al completamento della compilazione.



## Argomenti correlati


[Creazione di un'immagine MED-V](creating-a-med-v-image.md)









