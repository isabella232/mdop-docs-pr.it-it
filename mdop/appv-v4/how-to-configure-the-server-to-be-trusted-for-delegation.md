---
title: Come configurare il server in modo che sia attendibile per la delega
description: Come configurare il server in modo che sia attendibile per la delega
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817746"
---
# Come configurare il server in modo che sia attendibile per la delega


Quando si installa il software Microsoft Application Virtualization (App-V) Management Server, è possibile scegliere di installarlo usando un'architettura di sistema distribuita. Se si installa la console, il servizio Web di gestione e il database in computer diversi, è necessario configurare il server Internet Information Services (IIS) come attendibile per la delega. Questa operazione è necessaria perché il servizio Web di gestione tenterà di connettersi all'archivio dati App-V usando le credenziali dell'amministratore di App-V che usa la console. Il server di database in cui è installato l'archivio dati non accetterà le credenziali dell'amministratore dal server IIS, a meno che il server IIS non sia configurato per essere considerato attendibile per la delega e quindi il servizio Web di gestione non sarà in grado di connettersi all'archivio dati di App-V.

**Nota**  Se si installa il software App-V Management Server in un singolo server e si inserisce l'archivio dati in un server distinto, è comunque necessario configurare il server in modo che sia attendibile per la delega anche se il servizio Web di gestione e la console di gestione si trovano nello stesso server. Questa situazione si verifica se è necessario connettersi al servizio Web di gestione nella console usando l'opzione **Usa credenziali alternative** .

 

Il tipo di delega che puoi usare dipende dal livello di funzionalità del dominio configurato nell'infrastruttura di servizi di dominio Active Directory (aggiunge). La tabella seguente elenca i tipi di delega che possono essere configurati per ogni livello di funzionalità del dominio per App-V. Istruzioni dettagliate seguire la tabella.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Livello di funzionalità del dominio</th>
<th align="left">Livelli di delega disponibili</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000 Native</p></td>
<td align="left"><ul>
<li><p>Nessuna delega (impostazione predefinita)</p></li>
<li><p>Delega senza vincoli</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</p></td>
<td align="left"><ul>
<li><p>Nessuna delega (impostazione predefinita)</p></li>
<li><p>Delega senza vincoli ¹</p></li>
<li><p>Delega vincolata (usare solo protocolli Kerberos)</p></li>
<li><p>Delega vincolata (usare qualsiasi protocollo di autenticazione) ¹</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

¹ non consigliato.

## Per configurare la delega senza vincoli quando il livello di funzionalità del dominio è Windows 2000 Native


Nel Domain controller per il dominio del server Web completare la procedura seguente.

****

1.  Fare clic su **Start**, **strumenti di amministrazione**e quindi su **utenti e computer di Active Directory**.

2.  Espandere Domain e quindi espandere la cartella computer.

3.  Nel riquadro destro fare clic con il pulsante destro del mouse sul nome del computer per il server Web e quindi scegliere **Proprietà**.

4.  Nella scheda **generale** verificare che la casella **di controllo attendibile computer per delega** sia selezionata.

5.  Fai clic su **OK**.

## Per configurare la delega senza vincoli quando il livello di funzionalità del dominio è Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2


Nel Domain controller per il dominio del server Web completare la procedura seguente.

****

1.  Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **utenti e computer di Active Directory**.

2.  Espandere Domain ed espandere la cartella computer.

3.  Nel riquadro destro fare clic con il pulsante destro del mouse sul nome del computer per il server Web, scegliere **Proprietà**e quindi fare clic sulla scheda **delega** .

4.  Fare clic per selezionare **Considera attendibile il computer per la delega a qualsiasi servizio (solo Kerberos)**.

5.  Fai clic su **OK**.

## Per configurare la delega vincolata quando il livello di funzionalità del dominio è Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2


Nel Domain controller per il dominio del server Web completare la procedura seguente.

****

1.  Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **utenti e computer di Active Directory**.

2.  Espandere Domain e quindi espandere la cartella computer.

3.  Nel riquadro destro fare clic con il pulsante destro del mouse sul nome del computer per il server Web, scegliere **Proprietà**e quindi fare clic sulla scheda **delega** .

4.  Fare clic per selezionare **Considera attendibile il computer solo per la delega per i servizi specificati**.

5.  Verificare che l'opzione **Usa solo Kerberos** sia selezionata e quindi fare clic su **OK**.

6.  Fare clic sul pulsante **Aggiungi** . Nella finestra di dialogo **Aggiungi servizi** fare clic su **utenti o computer**e quindi selezionare o digitare il nome di Microsoft SQL Server in cui è installato l'App-V Data Store e ricevere le credenziali degli utenti da IIS. Fai clic su **OK**.

7.  Nell'elenco **Servizi disponibili** selezionare il servizio MSSQLSvc che elenca il numero di porta in cui Microsoft SQL Server accetta connessioni per il database App-V (la porta predefinita è 1433). Fai clic su **OK**.

### Passaggi aggiuntivi per configurare IIS 7 per la delega vincolata

Se si esegue il servizio Web di gestione in un server IIS 7, è necessario completare la procedura seguente per impostare la variabile *useAppPoolCredentials* di IIS 7 su true.

1.  Aprire una finestra del prompt dei comandi con privilegi elevati. Per aprire una finestra del prompt dei comandi con privilegi elevati, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Accessori**, fare clic con il pulsante destro del mouse su prompt dei **comandi**e quindi scegliere **Esegui come amministratore**.

2.  Passare a%windir%\\system32\\inetsrv.

3.  Digitare **appcmd.exe set config-section: System. webServer/security/authentication/windowsAuthentication-useAppPoolCredentials: true**e quindi premere INVIO.

 

 





