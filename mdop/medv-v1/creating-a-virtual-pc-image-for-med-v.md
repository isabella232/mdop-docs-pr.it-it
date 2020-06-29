---
title: Creazione di un'immagine Virtual PC per MED-V
description: Creazione di un'immagine Virtual PC per MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823665"
---
# Creazione di un'immagine Virtual PC per MED-V


Per creare un'immagine di un PC virtuale (VPC) per MED-V, è necessario eseguire le operazioni seguenti:

1.  [Creare un'immagine VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).

2.  [Installare il pacchetto di Workspace. msi MED-V nell'immagine VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).

3.  [Eseguire lo strumento di prerequisiti della macchina virtuale MED-V nell'immagine VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).

4.  [Configurare manualmente i prerequisiti della macchina virtuale nell'immagine VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).

5.  [Configurare Sysprep per le immagini MED-V](#bkmk-howtoconfiguresysprepformedvimages) (facoltativo).

6.  [Disattivare Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Creazione di un'immagine PC virtuale tramite Microsoft Virtual PC


Per creare un'immagine di Virtual PC con Microsoft Virtual PC, vedere la documentazione di Virtual PC.

Per ulteriori informazioni, vedere le pagine seguenti:

-   [Guida di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [Creare una macchina virtuale e installare un sistema operativo guest](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a>Come installare il pacchetto di area di lavoro MED-V. msi


Dopo aver creato l'immagine di Virtual PC, installare il pacchetto MED-V Workspace. msi nell'immagine.

**Per installare l'immagine dell'area di lavoro MED-V**

1.  Avviare la macchina virtuale e copiare il pacchetto Workspace. msi MED-V.

    Il pacchetto MSI di area di lavoro MED-V si chiama *MED-V\_workspace\_x.msi*, dove *x* è il numero di versione.

    Ad esempio, *MED-V\_workspace\_1.0.65.msi*.

2.  Fare doppio clic sul pacchetto Workspace. msi MED-V e seguire le istruzioni per l'installazione guidata.

    **Nota**  
    Quando viene rilasciata una nuova versione di MED-V e viene aggiornata un'immagine del PC virtuale esistente, disinstallare il pacchetto esistente di area di lavoro MED-V. msi, riavviare il computer e installare il nuovo pacchetto di Workspace. msi di MED-V.



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a>Come eseguire lo strumento prerequisiti macchina virtuale


Lo strumento dei prerequisiti della macchina virtuale (VM) è una procedura guidata che automatizza diversi dei prerequisiti.

**Nota**  
Anche se molti parametri sono configurabili nella procedura guidata, le proprietà necessarie per il corretto funzionamento di MED-V non sono configurabili.



**Per eseguire lo strumento prerequisiti macchina virtuale**

1.  Dopo aver installato il pacchetto di area di lavoro MED-V. msi, nel menu **Start** di Windows selezionare **tutti i programmi &gt; Med-v &gt; VM prerequisiti Tool**.

    **Nota**  
    L'utente che ha eseguito lo strumento prerequisiti della macchina virtuale deve avere diritti di amministratore locale e deve essere l'unico utente connesso.



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. Fai clic su **Avanti**.

3. Nella pagina **impostazioni di Windows** , dalle proprietà configurabili seguenti selezionare quelle da configurare:

   -   **Cancellare le informazioni sulla cronologia personale degli utenti**

   -   **Cancellare la directory Temp dei profili locali**

   -   **Disabilitare i suoni negli eventi di Windows seguenti: Start, Logon, disconnessione**

   **Nota**  
   Non abilitare Windows Page Saver in un criterio di gruppo.



4. Fai clic su **Avanti**.

5. Nella pagina **impostazioni di Internet Explorer** , dalle proprietà configurabili seguenti, selezionare quelle da configurare:

   -   **Non usare le caratteristiche di completamento automatico**

   -   **Disabilitare il riutilizzo di Windows per l'avvio dei collegamenti**

   -   **Cancellare la cronologia esplorazioni**

   -   **Abilitare l'esplorazione a schede in Internet Explorer 7**

6. Fai clic su **Avanti**.

7. Nella pagina **Servizi Windows** , dalle proprietà configurabili seguenti selezionare quelle da configurare:

   -   **Servizio Centro sicurezza**

   -   **Servizio Utilità di pianificazione**

   -   **Servizio Aggiornamenti automatici**

   -   **Servizio Ripristino configurazione di sistema**

   -   **Servizio di indicizzazione**

   -   **Configurazione wireless zero**

   -   **Compatibilità con il cambio rapido degli utenti**

8. Fai clic su **Avanti**.

9. Nella pagina **accesso automatico di Windows** eseguire le operazioni seguenti:

   1.  Selezionare la casella di controllo **Abilita accesso automatico di Windows** .

   2.  Assegnare un **nome utente** e una **password**.

10. Fare clic su **applica**e quindi, nella casella di conferma visualizzata, fare clic su **Sì**.

11. Nella pagina **Riepilogo** fare clic su **fine** per chiudere la procedura guidata

**Nota**  
Verificare che i criteri di gruppo non sovrascrivano le impostazioni obbligatorie impostate nello strumento prerequisiti.



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a>Come configurare i prerequisiti di installazione manuale della macchina virtuale MED-V


Diverse configurazioni non possono essere configurate tramite lo strumento prerequisiti macchina virtuale e devono essere eseguite manualmente.

-   Impostazioni della macchina virtuale

    È consigliabile configurare le impostazioni della macchina virtuale seguenti in Microsoft Virtual PC Console:

    -   Disabilitare le unità disco floppy.

    -   Disabilitare Undo-Disks (**Settings &gt; Undo-disks**).

    -   Verificare che l'immagine disponga di una sola CPU virtuale.

    -   Eliminare le interazioni tra la macchina virtuale e l'utente, in cui non sono correlate alle applicazioni pubblicate, ad esempio i messaggi che richiedono l'input dell'utente.

-   Impostazioni immagine

    Configurare le impostazioni manuali seguenti nell'immagine:

    1.  Nella finestra delle **proprietà delle opzioni risparmio energia** disattivare l'ibernazione e il sonno.

    2.  Applicare gli aggiornamenti di Windows più recenti.

    3.  Nella sezione **errore sistema** della finestra di dialogo **avvio e ripristino di Windows** deselezionare la casella di controllo **Riavvia automaticamente** .

    4.  Verificare che l'immagine usi una chiave di licenza di VLK.

-   Installazione delle aggiunte di VPC

    Nel menu **azione** selezionare **Installa o aggiorna aggiunte macchina virtuale**.

-   Configurazione della stampa

    È possibile configurare la stampa dall'area di lavoro MED-V in uno dei modi seguenti:

    -   Aggiungere una stampante alla macchina virtuale.

    -   Consentire la stampa con le stampanti configurate nel computer host.

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a>Come configurare Sysprep per le immagini di MED-V


In un'area di lavoro MED-V è possibile configurare Sysprep per l'assegnazione di ID di sicurezza univoco (SID), in particolare quando vengono eseguite più aree di lavoro MED-V in un singolo computer. Non è consigliabile usare Sysprep per partecipare a un dominio; USA invece l'azione di script Domain Join di MED-V come descritto in [come configurare le azioni di script](how-to-set-up-script-actions.md).

**Nota**  
Sysprep è l'utilità per la preparazione del sistema Microsoft per il sistema operativo Windows.



**Per configurare Sysprep in un'area di lavoro MED-V**

1.  Creare una directory nella radice dell'unità di sistema denominata *Sysprep*.

2.  Nel CD di installazione di Windows estrarre *deploy.cab* nella radice dell'unità di sistema oppure scaricare l'aggiornamento degli strumenti di distribuzione più recenti dal sito Web Microsoft.

    -   Per Windows 2000, vedere [aggiornamento degli strumenti di distribuzione per windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).

    -   Per Windows XP, vedere [aggiornamento degli strumenti di distribuzione per Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).

3.  Eseguire **Setup Manager** (setupmgr.exe).

4.  Seguire la configurazione guidata di Setup Manager.

Dopo aver configurato Sysprep e creato l'area di lavoro MED-V, è necessario eseguire Sysprep.

**Per eseguire Sysprep**

1.  Nella cartella Sysprep situata nella radice dell'unità di sistema eseguire lo strumento preparazione sistema (Sysprep.exe).

2.  Nella finestra di messaggio di avviso che viene visualizzata fare clic su **OK**.

3.  Nella finestra di dialogo **Proprietà Sysprep** selezionare la casella **di controllo non reimpostare il periodo di tolleranza per l'attivazione** e **usare la configurazione minima** .

4.  Fare clic su **Richiudi**.

5.  Se non si è soddisfatti delle informazioni elencate nella casella del messaggio di conferma che viene visualizzata, fare clic su **Annulla** e modificare le selezioni.

6.  Fare clic su **OK** per completare il processo di preparazione del sistema.

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a>Disattivazione di Microsoft Virtual PC


Dopo che tutti i componenti sono stati installati e configurati, chiudere Microsoft Virtual PC e selezionare **Disattiva**.

## Argomenti correlati


Creazione di un'immagine MED-V [come configurare le azioni di script](how-to-set-up-script-actions.md)









