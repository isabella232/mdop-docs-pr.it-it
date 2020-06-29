---
title: Come installare il client App-V con Setup.exe
description: Come installare il client App-V con Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817336"
---
# Come installare il client App-V con Setup.exe


Questo argomento descrive come installare il client App-V usando il programma setup.exe. Quando si installa il client App-V usando il programma setup.exe, il installatore determina il software prerequisito necessario e lo installa automaticamente prima di installare il client.

**Per installare il client di virtualizzazione dell'applicazione usando Setup.exe**

1.  Verificare di avere effettuato l'accesso con un account che disponga dei diritti di amministratore nel computer.

2.  Aprire una finestra del prompt dei comandi e quindi cambiare la directory nella cartella che contiene i file di installazione. Quando si installa la versione 4.6 o una versione successiva del client App-V, è necessario usare il programma di installazione corretto per il sistema operativo del computer, 32 bit o 64 bit. L'installazione non riesce e verrà visualizzato un messaggio di errore se si usa il programma di installazione errato.

3.  Immettere la stringa di comando installa al prompt dei comandi. In alternativa, è possibile creare un file di comando ed eseguirlo dal prompt dei comandi. Puoi anche usare un linguaggio di scripting come VBScript o Windows PowerShell per eseguire il comando.

4.  Nell'esempio della riga di comando seguente viene illustrato il modo in cui setup.exe può essere usato con una serie di parametri facoltativi. Per altre informazioni su questi parametri, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).

    **"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" produzione System\\ "SWIPUBSVRTYPE = \ \"/secure\\ HTTP "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""**

    **Importante**  
    -   Le virgolette che compaiono nella sezione "**/v**" devono essere considerate caratteri speciali e immesse con un " **\\** ". Le virgolette sono obbligatorie solo quando il valore contiene uno spazio; Tuttavia, per coerenza, tutte le istanze nell'esempio precedente vengono visualizzate come virgolette.

    -   I **%** caratteri "" in "**% HOMEDRIVE%**" devono essere preceduti dal carattere di **^** escape "". In caso contrario, la shell dei comandi di Windows imposta il valore su quello dell'utente che sta eseguendo l'installazione.

    -   Gli switch di **InstallShield** **/s** e **/qn** sono necessari per creare un'installazione invisibile all'utente. L'opzione **/qn** deve seguire l'opzione **/v** , separata solo da un carattere di virgoletta senza spazi intermedi.

    -   La cartella specificata nel valore **SWIGLOBALDATA** deve esistere già.

     

5.  Al termine dell'installazione, è consigliabile eseguire un'analisi di Microsoft Update per verificare che siano installati gli aggiornamenti più recenti.

## Argomenti correlati


[Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





