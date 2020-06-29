---
title: Come configurare un utente o un gruppo di dominio
description: Come configurare un utente o un gruppo di dominio
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827196"
---
# Come configurare un utente o un gruppo di dominio


Le impostazioni di distribuzione consentono di controllare gli utenti o i gruppi che possono accedere all'area di lavoro MED-V, nonché per quanto tempo può essere utilizzata l'area di lavoro MED-V e se può essere usata offline. È anche possibile configurare altre regole per controllare l'accesso tra l'area di lavoro MED-V e l'host.

Tutte le autorizzazioni dell'area di lavoro MED-V sono configurate nel modulo **criteri** nella scheda **distribuzione** .

Per consentire agli utenti di usare l'area di lavoro MED-V, è necessario prima di tutto aggiungere utenti o gruppi di dominio alle autorizzazioni dell'area di lavoro MED-V. Puoi quindi impostare le autorizzazioni per ogni utente o gruppo.

## Come aggiungere un utente o un gruppo di dominio


**Per aggiungere un utente o un gruppo di dominio**

1.  Nella finestra **utenti/gruppi** fare clic su **Aggiungi.**

2.  Nella finestra di dialogo **Immetti nomi utente o di gruppo** selezionare utenti o gruppi di dominio eseguendo una delle operazioni seguenti:

    -   Nel campo **Immetti nomi utente o gruppo** Digitare un utente o un gruppo esistente nel dominio o come utente o gruppo locale nel computer. Quindi fare clic su **Controlla nomi** per risolverlo con il nome completo esistente.

    -   Fare clic su **trova** per aprire la finestra di dialogo standard **Seleziona utenti o gruppi** . Quindi Seleziona utenti o gruppi di dominio.

3.  Fai clic su **OK**.

    Gli utenti o i gruppi di dominio vengono aggiunti.

    **Nota**  
    Gli utenti provenienti da domini attendibili devono essere aggiunti manualmente.



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## Come rimuovere un utente o un gruppo di dominio


**Per rimuovere un utente o un gruppo di dominio**

1.  Nella finestra **utenti/gruppi** selezionare un utente o un gruppo.

2.  Fare clic su **Rimuovi**.

    L'utente o il gruppo viene eliminato.

## Come impostare le autorizzazioni per un utente o un gruppo


**Per impostare le autorizzazioni per un utente o un gruppo**

1.  Fare clic sull'utente o sul gruppo per cui si stanno impostando le autorizzazioni.

2.  Configurare le proprietà dell'area di lavoro MED-V come descritto nella tabella seguente.

3.  Nel menu **criteri** selezionare **commit**.

**Proprietà di distribuzione dell'area di lavoro**

Descrizione *generale* della proprietà

Abilitare l'area di lavoro per l' &lt; utente o il gruppo&gt;

Selezionare questa casella di controllo per abilitare l'area di lavoro MED-V per l'utente o il gruppo.

L'area di lavoro scade in questa data

Selezionare questa casella di controllo per assegnare una data di scadenza per il set di autorizzazioni per l'utente o il gruppo.

Quando l'opzione è selezionata, la casella Data è abilitata. Impostare la data e le autorizzazioni scadono alla fine della data specificata.

Il lavoro offline è limitato a

Selezionare questa casella di controllo per assegnare un periodo di tempo in cui il criterio deve essere aggiornato per l'utente o il gruppo. Quando l'opzione è selezionata, la casella periodo di tempo è abilitata. Impostare il numero di giorni o ore e alla fine del periodo di tempo specificato l'utente o il gruppo non sarà in grado di connettersi se il criterio non viene aggiornato.

Opzioni di eliminazione dell'area di lavoro

Fare clic per impostare le opzioni di eliminazione dell'area di lavoro MED-V. Per altre informazioni, vedere [come impostare le opzioni di eliminazione dell'area di lavoro MED-V](how-to-set-med-v-workspace-deletion-options.md).

*Trasferimento dati*

Supporto degli Appunti tra host e area di lavoro

Selezionare questa casella di controllo per abilitare la copia e l'incollatura tra l'host e l'area di lavoro MED-V.

Supporto del trasferimento di file tra l'host e l'area di lavoro

Selezionare questa casella di controllo per consentire il trasferimento di file tra l'area di lavoro host e MED-V. Nella casella **trasferimento file** selezionare una delle opzioni seguenti:

-   **Entrambi**: Abilita il trasferimento di file tra l'host e l'area di lavoro MED-V.

-   **Host to Workspace**: consente di trasferire file dall'host all'area di lavoro MED-V.

-   **Area di lavoro da ospitare**: consente di trasferire file dall'area di lavoro MED-V all'host.

**Nota**  
Se un utente senza autorizzazioni tenta di trasferire i file, verrà visualizzata una finestra che chiede di immettere le credenziali di un utente con le autorizzazioni necessarie per eseguire il trasferimento di file.



**Importante**  
Per supportare il trasferimento di file in Windows XP SP3, è necessario disabilitare la sincronizzazione dei file offline modificando il registro di sistema nel modo seguente:

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



Avanzate

Fare clic per impostare le opzioni avanzate per il trasferimento di file. Per altre informazioni, vedere [come impostare le opzioni avanzate per il trasferimento di file](how-to-set-advanced-file-transfer-options.md).

*Controllo dispositivo*

Abilitare la stampa alle stampanti connesse all'host

Selezionare questa casella di controllo per consentire agli utenti di stampare dall'area di lavoro MED-V tramite la stampante host.

**Nota**  
La stampa viene eseguita dalle stampanti definite nell'host.



Abilitare l'accesso a CD/DVD

Selezionare questa casella di controllo per consentire l'accesso a un'unità CD o DVD da questa area di lavoro MED-V.



**Più appartenenze**

1.  Se l'utente fa parte di un gruppo e le autorizzazioni vengono applicate all'utente e al gruppo in cui fanno parte, vengono applicate tutte le autorizzazioni.

2.  Se l'utente è un membro di due gruppi diversi, vengono applicate le autorizzazioni meno restrittive.

## Argomenti correlati


[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Come impostare le opzioni di eliminazione nell'area di lavoro MED-V](how-to-set-med-v-workspace-deletion-options.md)

[Come impostare le opzioni avanzate per il trasferimento dei file](how-to-set-advanced-file-transfer-options.md)









