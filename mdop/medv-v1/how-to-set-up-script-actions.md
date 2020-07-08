---
title: Come configurare le azioni script
description: Come configurare le azioni script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804191"
---
# Come configurare le azioni script


L'Editor azioni script consente all'amministratore di creare azioni da eseguire durante la configurazione dell'area di lavoro MED-V, nonché di definire l'ordine in cui vengono eseguite.

Di seguito è riportato un elenco di azioni che possono essere aggiunte allo script di configurazione del dominio:

-   **Riavvia Windows**: riavvia Windows.

-   **Join Domain**: se si partecipa a un dominio, includere questa azione e configurare il nome utente, la password, il nome di dominio completo, il nome di dominio NetBIOS e l'unità organizzativa (facoltativo).

-   **Verificare la connettività**: configurare un server a cui connettersi e verificare che l'area di lavoro MED-V sia in grado di connettersi a una risorsa di rete, ad esempio il server di dominio.

-   **Riga di comando**: configurare uno script nell'area di lavoro MED-V e immettere una riga di comando che includa il percorso dello script e gli argomenti dello script.

-   **Rinomina computer**: rinominare il computer della macchina virtuale in base alle impostazioni definite.

-   **Disabilitare l'accesso automatico**: disabilitare l'accesso automatico di Windows. Questa azione deve essere aggiunta alla fine degli script che aggiungono il computer al dominio.

## <a href="" id="how-to-set-up-script-actions-"></a>Come configurare le azioni script


**Per configurare le azioni di script**

1.  Nella scheda **configurazione VM** fare clic su **Editor script**.

2.  Nella finestra di dialogo **azioni script** fare clic su **Aggiungi**e quindi nel sottomenu fare clic sulle azioni desiderate.

3.  Configurare le azioni come descritto nelle tabelle seguenti.

    **Nota** 
     **Rinominare il computer** è configurato nella scheda **Impostazioni VM** . Per altre informazioni, vedere [come configurare le proprietà del modello di nome computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. Impostare l'ordine delle azioni selezionando un'azione e facendo clic **su in alto o in** **basso**.

5. Fai clic su **OK**.

**Nota**  
Durante l'esecuzione dello script di join Domain, perché lo script funzioni, l'utente che ha eseguito l'accesso alla macchina virtuale dell'area di lavoro MED-V deve avere diritti di amministratore locale.



**Nota**  
Durante l'esecuzione dello script di accesso automatico disabilitato, è consigliabile disabilitare l'account Guest locale usato per l'accesso automatico dopo il completamento della configurazione iniziale.



### <a href="" id="bkmk-joindomainproperties"></a>

**Unire le proprietà del dominio**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Credenziali da usare quando si unisce la VM al dominio</p></td>
<td align="left"><p>Selezionare una delle credenziali seguenti da usare quando si unisce la VM al dominio:</p>
<ul>
<li><p><strong>Usare le credenziali di MED-V </strong> : le credenziali dell'utente finale.</p></li>
<li><p><strong>Utilizzare le credenziali seguenti </strong> : le credenziali specificate; immettere un nome utente e una password nei campi corrispondenti.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Le credenziali immesse sono visibili a tutti gli utenti dell'area di lavoro MED-V. Non è consigliabile specificare le credenziali di amministratore di dominio.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Dominio per l'aggiunta</p></td>
<td align="left"><p>Seleziona una delle opzioni seguenti:</p>
<ul>
<li><p><strong>Usare il nome di dominio usato per avviare l'area </strong> di lavoro: partecipare al dominio immesso dall'utente finale quando si accede al client MED-V.</p>
<p>Per definire il mapping da NetBIOS a nomi di dominio completi, fare clic su <strong> tabella di mapping del dominio globale </strong> . Nella tabella di mapping del dominio globale fare clic su <strong> Aggiungi </strong> , immettere un <strong> nome di dominio NetBIOS </strong> e un nome di dominio completo e <strong> </strong> fare clic su <strong> OK </strong> .</p></li>
<li><p><strong>Usare il nome di dominio seguente </strong> : partecipare al dominio specificato; immettere un nome di dominio e un nome di dominio NetBIOS nei campi corrispondenti.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unità organizzativa</p></td>
<td align="left"><p>Un'unità organizzativa (OU) può essere specificata per partecipare al computer a una specifica UO. Il formato deve seguire un nome distinto dell'UO: OU = &lt; unità organizzativa &gt; , &lt; controller &gt; di dominio (ad esempio ou = QATest, DC = il, DC = MED-V, DC = com).</p>
<div class="alert">
<strong>Warning</strong><br/><p>È supportata solo un'unità organizzativa a livello singolo, come illustrato nell'esempio precedente.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**Controllare le proprietà di connettività**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Indirizzo IP</p></td>
<td align="left"><p>Indirizzo IP del server a cui si sta verificando la connessione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Port</p></td>
<td align="left"><p>La porta del server a cui si sta verificando la connessione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Timeout</p></td>
<td align="left"><p>Numero di secondi di attesa di una risposta prima del timeout.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**Proprietà della riga di comando**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Path</p></td>
<td align="left"><p>Il percorso della riga di comando.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Argomenti</p></td>
<td align="left"><p>Argomenti della riga di comando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Attendere l'uscita</p></td>
<td align="left"><p>Selezionare la casella di controllo per attendere un ritorno prima di continuare con le azioni di script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Errore non riuscito</p></td>
<td align="left"><p>Selezionare questa casella di controllo se il valore restituito è tutt'altro che quello specificato.</p>
<p>Immettere il valore che indicherà il comando come operazione riuscita.</p>
<p>Impostazione predefinita: <strong> 0</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eseguire una sola volta</p></td>
<td align="left"><p>Selezionare questa casella di controllo per eseguire la riga di comando una sola volta. Se lo script non riesce o viene annullato, il comando non verrà eseguito di nuovo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Questa riga di comando causa il riavvio di Windows nell'area di lavoro</p></td>
<td align="left"><p>Selezionare questa casella di controllo se la riga di comando causa un riavvio dopo il completamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consenti interazione</p></td>
<td align="left"><p>Selezionare questa casella di controllo se il comando richiede l'interazione dell'utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Messaggio di stato</p></td>
<td align="left"><p>Messaggio da visualizzare all'utente durante l'esecuzione del comando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Messaggio di errore</p></td>
<td align="left"><p>Messaggio da visualizzare all'utente se il comando non riesce.</p></td>
</tr>
</tbody>
</table>

 

Quando si configura l'azione della riga di comando, è possibile usare diverse variabili come definito nella tabella seguente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Valore</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>%MEDVUser%</p></td>
<td align="left"><p>Nome utente autenticato.</p></td>
<td align="left"><p>Nome utente autenticato di MED-V. Il nome utente e la password possono essere usati nello script di configurazione della VM di join Domain.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%MEDVPassword%</p></td>
<td align="left"><p>Una password autenticata.</p></td>
<td align="left"><p>Password autenticata di MED-V. Il nome utente e la password possono essere usati nello script di configurazione della VM di join Domain.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>%MEDVDomain%</p></td>
<td align="left"><p>Dominio configurato.</p></td>
<td align="left"><p>Il dominio configurato nell'autenticazione MED-V. Può essere usato nello script di configurazione della VM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%DesiredMachineName%</p></td>
<td align="left"><p>Nome computer.</p></td>
<td align="left"><p>Il nome del computer univoco configurato nell'applicazione di gestione. Può essere usato nello script di configurazione della VM.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Come configurare la macchina virtuale per un'area di lavoro MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Come configurare le proprietà dei modelli di nome dei computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





