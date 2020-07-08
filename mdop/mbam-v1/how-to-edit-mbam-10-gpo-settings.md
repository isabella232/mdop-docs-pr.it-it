---
title: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0
description: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824285"
---
# Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0


Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker, è prima di tutto necessario determinare i criteri di gruppo che verranno usati nell'implementazione dell'amministrazione e del monitoraggio di Microsoft BitLocker. Per altre informazioni sui vari criteri disponibili, vedere [pianificazione per i requisiti dei criteri di gruppo di MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Dopo aver determinato i criteri che si intende usare, è necessario modificare uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri di MBAM.

I passaggi seguenti descrivono come configurare le impostazioni di base degli oggetti Criteri di gruppo (GPO) consigliate per consentire a MBAM di gestire la crittografia BitLocker per i computer client dell'organizzazione.

**Per modificare le impostazioni del GPO client MBAM**

1.  In un computer in cui è installato il modello di criteri di gruppo di MBAM verificare che i servizi MBAM siano abilitati.

2.  Usare la console Gestione criteri di gruppo (GPMC. msc) o il prodotto MDOP Advanced Group Policy Management per queste azioni: selezionare **Configurazione computer**, scegliere **criteri**, **modelli amministrativi**, selezionare **componenti di Windows**e quindi fare clic su **MDOP mbam (Gestione BitLocker)**.

3.  Modificare le impostazioni degli oggetti Criteri di gruppo necessarie per abilitare i servizi client di MBAM nei computer client. Per ogni criterio nella tabella seguente selezionare **gruppo criteri**, fare clic sul **criterio**e quindi configurare l' **impostazione**.

    Gruppo criteri

    Criterio

    Impostazione

    Gestione dei client

    Configurare i servizi MBAM

    Abilitata. Impostare l' **endpoint del servizio hardware e ripristino di mbam** e **selezionare informazioni di ripristino di BitLocker da archiviare**.

    Impostare l' **endpoint del servizio di conformità mbam** e **immettere la frequenza del rapporto di stato in (minuti)**.

    Consentire il controllo della compatibilità hardware

    Disabilitato. Questo criterio è abilitato per impostazione predefinita, ma non è necessario per un'implementazione di MBAM di base.

    Unità del sistema operativo

    Impostazioni di crittografia unità del sistema operativo

    Abilitata. Impostare **Seleziona protezione per l'unità del sistema operativo**. Questo è necessario per salvare i dati dell'unità del sistema operativo nel server di ripristino di MBAM Key.

    Unità rimovibile

    Controllare l'uso di BitLocker su unità rimovibili

    Abilitata. Questo è necessario se MBAM Salva i dati di unità rimovibili nel server di ripristino di chiave di MBAM.

    Unità fissa

    Controllare l'uso di BitLocker su unità fisse

    Abilitata. Questo è necessario se MBAM salverà i dati fissi delle unità nel server di ripristino di chiave di MBAM.

    Impostare **scegliere il modo in cui le unità protette da BitLocker possono essere recuperate** e **consentire l'agente di recupero dati**.



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Argomenti correlati


[Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0](deploying-mbam-10-group-policy-objects.md)









