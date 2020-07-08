---
title: Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione
description: Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805691"
---
# Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione


La distribuzione di pacchetti e gruppi di connessioni tramite il server di pubblicazione App-V 5,0 è utile perché offre una gestione a punti singoli e una elevata scalabilità.

Usare la procedura seguente per configurare il client App-V 5,0 per ricevere gli aggiornamenti dal server di pubblicazione.

**Nota**  Per le procedure seguenti, il server di gestione è stato installato in un computer denominato **MyMgmtSrv**e il server di pubblicazione è stato installato in un computer denominato **MyPubSrv**.

 

**Per configurare il client App-V 5,0 per ricevere gli aggiornamenti dal server di pubblicazione**

1.  Distribuire i server di gestione e pubblicazione di App-V 5,0 e aggiungere i pacchetti e i gruppi di connessioni necessari. Per altre informazioni sull'aggiunta di pacchetti e di gruppi di connessioni, vedere [come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [come creare un gruppo di connessioni](how-to-create-a-connection-group.md).

2.  Per aprire la console di gestione, fare clic sul collegamento seguente, aprire un browser e digitare quanto segue: http://MyMgmtSrv/AppvManagement/Console.html in un Web browser e importare, pubblicare e autorizzare tutti i pacchetti e i gruppi di connessioni che saranno necessari per un determinato set di utenti.

3.  Nel computer che esegue il client App-V 5,0 aprire un prompt dei comandi di PowerShell con privilegi elevati, eseguire il comando seguente:

    **Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing**

    Questo comando consente di configurare il server di pubblicazione specificato. Dovrebbe essere visualizzato l'output simile al seguente:

    ID: 1

    SetByGroupPolicy: false

    Nome: ABC

    URL: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: false

    GlobalRefreshOnLogon: false

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: giorno

    UserRefreshEnabled: vero

    UserRefreshOnLogon: vero

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: giorno

    ID restituito: in questo caso 1

4.  Nel computer che gestisce il client App-V 5,0 aprire un prompt dei comandi di PowerShell e digitare il comando seguente:

    **Sincronizzazione-AppvPublishingServer-ServerId 1**

    Il comando esegue una query sul server di pubblicazione per i pacchetti e i gruppi di connessioni che devono essere aggiunti o rimossi per questo particolare client in base ai diritti per i pacchetti e i gruppi di connessioni configurati nel server di gestione.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





