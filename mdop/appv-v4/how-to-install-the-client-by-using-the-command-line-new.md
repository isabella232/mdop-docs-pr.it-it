---
title: Come installare il client usando la riga di comando
description: Come installare il client usando la riga di comando
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817325"
---
# Come installare il client usando la riga di comando


Gli argomenti di questa sezione includono procedure per installare il client Desktop Application Virtualization (App-V) o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal) usando setup.exe o setup.msi. Per eseguire il programma di installazione è necessario disporre dei diritti amministrativi.

Puoi usare i parametri facoltativi della riga di comando per applicare impostazioni di configurazione specifiche al client App-V durante l'installazione. Per altre informazioni sull'uso dei parametri, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md). Se sono state applicate le impostazioni del registro di sistema a un computer prima di distribuire un client, ad esempio tramite criteri di gruppo, queste impostazioni vengono mantenute e vengono applicati altri parametri della riga di comando. I valori dei parametri della riga di comando sostituiscono qualsiasi valore esistente per la stessa impostazione.

**Nota**  Quando si installa il client App-V da usare con una cache di sola lettura, ad esempio con un'implementazione del server VDI, è necessario impostare il parametro *AUTOLOADTARGET* su None per impedire al client di provare ad aggiornare le applicazioni quando la cache è di sola lettura.

 

Per altre informazioni sull'impostazione di questi valori di parametro dopo l'installazione, vedere [come configurare le impostazioni del registro di sistema client App-v usando la riga di comando](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) nella Guida alle operazioni di Application Virtualization (app-v).

**Nota**  Se un'impostazione di configurazione nel computer dell'utente dipende dal percorso di installazione del client, tenere presente che il client Application Virtualization (App-V) 4.5 copia i file di installazione in una cartella diversa rispetto alle versioni precedenti. Per impostazione predefinita, una nuova installazione del client App-V 4.5 copierà i file di installazione nella cartella cartella \\Programmi\\microsoft Application Virtualization Client. Se una versione precedente del client è già installata, l'esecuzione del programma di installazione client App-V 4,5 eseguirà un aggiornamento del client esistente usando la cartella di installazione esistente.

 

\ [Valore token modello \]

**Nota**  Per App-V versione 4.6 e successive, quando è installato App-V client, SFTLDR.DLL viene copiato nella directory Windows\\system32. Se l'App-V client è installata in un sistema a 64 bit, SFTLDR\_WOW64.DLL viene copiato nella directory Windows\\SysWOW64.

 

\ [Valore token modello \]

## In questa sezione


Gli argomenti seguenti descrivono come installare il client Desktop Application Virtualization (App-V) o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal) usando setup.exe o setup.msi.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[Come installare il client App-V con Setup.exe](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
Fornisce una procedura dettagliata per l'installazione del client App-V tramite il programma setup.exe.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[Come installare il client App-V con Setup.msi](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
Fornisce procedure dettagliate per l'installazione di qualsiasi software prerequisito e anche per il client App-V tramite il programma setup.msi.

## Argomenti correlati


[Parametri della riga di comando del programma di installazione di Application Virtualization Client](application-virtualization-client-installer-command-line-parameters.md)

[Come installare manualmente Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md)

[Come disinstallare il client App-V](how-to-uninstall-the-app-v-client.md)

 

 





