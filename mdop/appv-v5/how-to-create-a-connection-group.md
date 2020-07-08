---
title: Come creare un gruppo di connessione
description: Come creare un gruppo di connessione
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805655"
---
# Come creare un gruppo di connessione


Seguire questa procedura per creare un gruppo di connessioni usando la console di gestione di App-V. Per usare PowerShell per creare gruppi di connessioni, vedere [come gestire i gruppi di connessioni in un computer autonomo usando PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).

Quando si inseriscono i pacchetti in un gruppo di connessioni, i percorsi radice del pacchetto vengono uniti. Se si rimuovono i pacchetti, solo i pacchetti rimanenti manterranno la radice unita.

**Per creare un gruppo di connessioni**

1.  Nella console di gestione di App-V 5,0 selezionare **pacchetti**.

2.  Selezionare **gruppi di connessioni** per visualizzare la raccolta gruppi di connessioni.

3.  Selezionare **Aggiungi gruppo di connessioni** per creare un nuovo gruppo di connessioni.

4.  Nel riquadro **nuovo gruppo di connessioni** Digitare una descrizione per il gruppo.

5.  Fare clic su **modifica** nel riquadro **pacchetti connessi** per aggiungere una nuova applicazione al gruppo di connessioni.

6.  Nell' **intero riquadro Raccolta pacchetti** selezionare l'applicazione da aggiungere e fare clic sulla freccia per aggiungere l'applicazione.

    Per rimuovere un'applicazione, selezionare l'applicazione da rimuovere nel riquadro **pacchetti in** e fare clic sulla freccia.

    Per riassegnare le priorità alle applicazioni nel gruppo di connessioni, usare le frecce nel riquadro **pacchetti in** .

    **Importante**  Per impostazione predefinita, le configurazioni di accesso ai servizi di dominio Active Directory associate a un'applicazione specifica non vengono aggiunte al gruppo di connessioni. Per trasferire la configurazione di Access in Active Directory, selezionare **Aggiungi accesso a un pacchetto all'accesso al gruppo**, che si trova nel riquadro **pacchetti in** .

     

7.  Dopo aver aggiunto tutte le applicazioni e aver configurato l'accesso a Active Directory, fare clic su **applica**.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

[Gestione dei gruppi di connessione](managing-connection-groups.md)

 

 





