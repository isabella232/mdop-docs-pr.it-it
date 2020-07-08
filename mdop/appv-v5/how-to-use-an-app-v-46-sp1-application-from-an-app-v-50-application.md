---
ms.reviewer: ''
title: Come usare un'applicazione App-V 4,6 da un'applicazione App-V 5,0
description: Come usare un'applicazione App-V 4,6 da un'applicazione App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805133"
---
# Come usare un'applicazione App-V 4,6 da un'applicazione App-V 5,0

*Nota:** App-V 4,6 è uscito dal supporto mainstream. La procedura seguente si applica a un pacchetto App-V 4,6 SP3.

Usare la procedura seguente per eseguire un'applicazione App-V 4.6 con le applicazioni App-V 5,0 in un client autonomo.

**Per eseguire applicazioni in un client autonomo**

1.  Selezionare due applicazioni nell'ambiente che possono essere aperte l'una dall'altra. Ad esempio, Microsoft Outlook e Adobe Acrobat Reader. È possibile accedere a un allegato di posta elettronica creato con Adobe Acrobat.

2.  Converti i pacchetti o crea un nuovo pacchetto per una delle applicazioni che usano il formato App-V 5,0. Per altre informazioni sulla conversione di pacchetti, vedere [come eseguire la migrazione di punti di estensione da un pacchetto App-v 4,6 a un pacchetto di App-v 5,0 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) o [come eseguire la migrazione di punti di estensione da un pacchetto app-v 4,6 a app-v 5,0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).

3.  Aggiungere e eseguire il provisioning del pacchetto usando la console di gestione di App-V 5,0. Per altre informazioni sull'aggiunta e il provisioning di pacchetti, vedere [come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [come configurare l'accesso ai pacchetti tramite la console di gestione](how-to-configure-access-to-packages-by-using-the-management-console-50.md).

4.  L'applicazione convertita viene ora eseguita tramite App-V 5,0 ed è possibile aprire un'applicazione dall'altra. Ad esempio, se hai convertito un pacchetto di Microsoft Office in un pacchetto di App-V 5,0 e Adobe Acrobat è ancora in corso come pacchetto App-V 4.6, puoi aprire un allegato di Adobe Acrobat Reader con Microsoft Outlook.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 








