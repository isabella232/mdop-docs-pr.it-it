---
title: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
description: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: f679d522-49ab-429c-93d0-294c3f3e5639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1b5faa0eb9ac24b33c66f1d5262a050b92e11e52
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824306"
---
# Come ripristinare i computer locali usando l'immagine di ripristino di DaRT


Seguire queste istruzioni per recuperare un computer quando si è fisicamente presenti presso il computer dell'utente finale in cui si verificano problemi.

**Come recuperare un computer locale usando l'immagine di ripristino DaRT**

1.  Avviare il computer dell'utente finale usando l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

    Man mano che il computer si avvia nell'immagine di ripristino di DaRT 8,0, viene visualizzata la finestra di dialogo **netstart** .

2.  Quando viene chiesto se si vuole inizializzare i servizi di rete, selezionare una delle opzioni seguenti:

    **Sì** -si presuppone che sia presente un server DHCP nella rete e si tenti di ottenere un indirizzo IP dal server. Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.

    **No** -ignorare il processo di inizializzazione della rete.

3.  Indicare se si vuole riassociare le lettere dell'unità. Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione. Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online. Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.

4.  Nella finestra di dialogo **Opzioni ripristino** configurazione di sistema selezionare un layout di tastiera.

5.  Controllare la directory radice di sistema visualizzata, il tipo di sistema operativo installato e le dimensioni della partizione. Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti e quindi inserire il supporto di installazione per il dispositivo e selezionare il driver.

6.  Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.

    **Nota**  
    Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 8 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente.



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Nella finestra **Opzioni ripristino sistema** fare clic su **strumenti di diagnostica e ripristino Microsoft**.

   Verrà visualizzata la finestra del **set di strumenti di diagnostica e ripristino** . È ora possibile eseguire tutti i singoli strumenti o procedure guidate inclusi quando è stata creata l'immagine di ripristino DaRT.

È possibile fare clic su **Guida** nella finestra del **set di strumenti di diagnostica e ripristino** per aprire il file della Guida client che fornisce istruzioni dettagliate e informazioni necessarie per eseguire i singoli strumenti DaRT. È anche possibile fare clic sulla **procedura guidata della soluzione** nella finestra del **set di strumenti di diagnostica e ripristino** per scegliere lo strumento migliore per la situazione, in base a una breve intervista fornita dalla procedura guidata.

Per informazioni generali su qualsiasi strumento DaRT, Vedi [Panoramica degli strumenti in dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

**Come eseguire dardo al prompt dei comandi**

- Per eseguire dardo al prompt dei comandi, specificare il comando **netstart.exe** quindi usare uno dei parametri seguenti:

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong>Parametro</strong></p></td>
  <td align="left"><p><strong>Descrizione</strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-rete</p></td>
  <td align="left"><p>Inizializza i servizi di rete.</p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p>-Rimontare</p></td>
  <td align="left"><p>Rimappa le lettere dell'unità.</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-prompt</p></td>
  <td align="left"><p>Visualizza i messaggi che chiedono all'utente finale di specificare se inizializzare la rete e rimappare le unità.</p>
  <div class="alert">
  <strong>Warning</strong><br/><p>La risposta dell'utente finale alla richiesta sostituisce gli interruttori-network e-rimontare.</p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## Argomenti correlati


[Operazioni relative a DaRT 8.0](operations-for-dart-80-dart-8.md)

[Ripristino dei computer con DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)









