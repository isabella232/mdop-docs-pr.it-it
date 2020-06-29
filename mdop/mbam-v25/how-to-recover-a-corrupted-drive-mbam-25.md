---
title: Come recuperare un'unità danneggiata
description: Come recuperare un'unità danneggiata
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822555"
---
# Come recuperare un'unità danneggiata


È possibile usare questa procedura con il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per recuperare un'unità danneggiata protetta da BitLocker. A questo scopo, verranno completate le attività descritte nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Dettagli e altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Creare un file di pacchetto chiave di ripristino accedendo all' <strong> area recupero unità </strong> del sito Web amministrazione e monitoraggio.</p></td>
<td align="left"><p>Per accedere all' <strong> area di ripristino dell'unità </strong> , è necessario essere assegnati al ruolo degli utenti di mbam helpdesk o al ruolo di utenti avanzati helpdesk di mbam. Quando sono stati creati, è possibile che siano stati assegnati nomi diversi a questi ruoli. Per altre informazioni, Vedi <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> pianificazione per i gruppi e gli account di MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copiare il file del pacchetto nel computer che contiene l'unità danneggiata.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usare il <code>repair-bde</code> comando per completare il processo di ripristino.</p></td>
<td align="left"><p>Per evitare una potenziale perdita di dati, è consigliabile rivedere il <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> comando Manage-bde prima di </a> usarlo.</p></td>
</tr>
</tbody>
</table>

 

**Per recuperare un'unità danneggiata**

1.  Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.

2.  Nel riquadro sinistro selezionare unità di **ripristino** per aprire la pagina **Recupera accesso a una unità crittografata** .

3.  Immettere il dominio di accesso e il nome utente di Windows dell'utente finale, il motivo per cui è stato sbloccato l'unità e l'ID password di ripristino dell'utente finale.

    **Nota**  Se si è un membro del gruppo di Access per utenti avanzati helpdesk, non è necessario immettere il nome di dominio o il nome utente dell'utente.

     

4.  Fai clic su **Invia**. Verrà visualizzata la chiave di ripristino.

5.  Fare clic su **Salva**e quindi selezionare **pacchetto chiave di ripristino**. Il pacchetto chiave di ripristino verrà creato nel computer.

6.  Copiare il pacchetto della chiave di ripristino nel computer in cui è presente l'unità danneggiata.

7.  Apri una finestra del prompt dei comandi con privilegi elevati. A tale scopo, fare clic sul pulsante **Start** e digitare `cmd` nella casella di testo **Cerca programmi e file** . Fare clic con il pulsante destro del mouse su **cmd.exe**e scegliere **Esegui come amministratore**.

8.  Al prompt dei comandi digitare quanto segue:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Nota**  Sostituire &lt; l' *unità fissa* &gt; con un'unità disco rigido disponibile che disponga di spazio libero uguale o maggiore rispetto ai dati nell'unità danneggiata. I dati dell'unità danneggiata vengono recuperati e spostati nell'unità disco rigido specificata.

     


## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





