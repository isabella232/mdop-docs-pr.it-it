---
title: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
description: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823765"
---
# Come ripristinare i computer locali usando l'immagine di ripristino di DaRT


Per recuperare un computer locale usando Microsoft Diagnostics and Recovery Toolset (DaRT) 7, è necessario essere fisicamente presenti nel computer dell'utente finale che sta riscontrando problemi che richiedono dardo. È anche possibile eseguire le freccette in remoto seguendo le istruzioni su [come recuperare i computer remoti usando l'immagine di ripristino DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

**Per recuperare un computer locale usando dardo**

1.  Man mano che il computer si avvia nell'immagine di ripristino DaRT, viene visualizzata la finestra di dialogo **netstart** . Viene chiesto se si desidera inizializzare i servizi di rete. Se si fa clic su **Sì**, si presuppone che in rete sia presente un server DHCP e si tenti di ottenere un indirizzo IP dal server. Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.

    Per ignorare il processo di inizializzazione della rete, fare clic su **No**.

2.  Dopo la finestra di dialogo di inizializzazione della rete, viene chiesto se si vuole rimappare le lettere dell'unità. Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione. Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online. Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.

3.  Dopo la finestra di dialogo rimappatura viene visualizzata la finestra di dialogo **Opzioni di ripristino del sistema** e viene chiesto di selezionare un layout di tastiera. Visualizza quindi la directory radice di sistema, il tipo di sistema operativo installato e le dimensioni della partizione. Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti. Verrà richiesto di inserire il supporto di installazione per il dispositivo e di selezionare il driver. Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.

    **Nota**  
    Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 7 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente.



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. Nella finestra **Opzioni ripristino sistema** fare clic su **strumenti di diagnostica e ripristino Microsoft**.

   Verrà visualizzata la finestra del **set di strumenti di diagnostica e ripristino** . È ora possibile eseguire tutti i singoli strumenti o procedure guidate inclusi quando è stata creata l'immagine di ripristino DaRT.

È possibile fare clic su **Guida** nella finestra del **set di strumenti di diagnostica e ripristino** per aprire il file della Guida client che fornisce istruzioni dettagliate e informazioni necessarie per eseguire i singoli strumenti DaRT. È anche possibile fare clic sulla **procedura guidata della soluzione** nella finestra del **set di strumenti di diagnostica e ripristino** per scegliere lo strumento migliore per la situazione, in base a una breve intervista fornita dalla procedura guidata.

Per informazioni generali su qualsiasi strumento DaRT, Vedi [Panoramica degli strumenti in dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

**Per eseguire dardo al prompt dei comandi**

1. Puoi eseguire freccetta al prompt dei comandi specificando il comando **netstart.exe** e usando uno dei parametri seguenti:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Parametro</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>-rete</p></td>
   <td align="left"><p>Inizializza i servizi di rete.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>-Rimontare</p></td>
   <td align="left"><p>Rimappa le lettere dell'unità.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>-prompt</p></td>
   <td align="left"><p>Visualizza i messaggi che chiedono all'utente finale di specificare se inizializzare la rete e rimappare le unità.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>La risposta dell'utente finale alle richieste esegue l'override degli switch-Network e-remount.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Puoi personalizzare il dardo in modo che un computer che si avvia in dardo apra automaticamente lo strumento di **connessione remota** usato per stabilire una connessione remota con l'help desk.

## Argomenti correlati


[Ripristino dei computer con DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









