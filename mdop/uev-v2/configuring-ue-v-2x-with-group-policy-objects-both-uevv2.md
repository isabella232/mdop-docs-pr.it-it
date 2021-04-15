---
title: Configurazione di UE-V 2.x con oggetti Criteri di gruppo
description: Configurazione di UE-V 2.x con oggetti Criteri di gruppo
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494061"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a>Configurazione di UE-V 2.x con oggetti Criteri di gruppo


Alcune impostazioni di Criteri di gruppo di Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 e 2.1 SP1 possono essere definite per i computer e altre impostazioni di Criteri di gruppo possono essere definite per gli utenti. Per informazioni su come installare i file ADMX di Criteri di gruppo UE-V, vedere [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).

Le impostazioni dei criteri seguenti possono essere configurate per UE-V.

**Impostazioni di Criteri di gruppo**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome dell'impostazione di Criteri di gruppo</th>
<th align="left">Target</th>
<th align="left">Descrizione dell'impostazione di Criteri di gruppo</th>
<th align="left">Opzioni di configurazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configure Sync, metodo</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Utilizzando questa impostazione di Criteri di gruppo, è possibile configurare se User Experience Virtualization (UE-V) usa la funzionalità del provider di sincronizzazione. Questa impostazione dei criteri consente inoltre di abilitare la visualizzazione di una notifica quando l'importazione delle impostazioni utente viene ritardata.</p></td>
<td align="left"><p>Abilitare questa impostazione per configurare l'agente UE-V in modo che non utilizzi il provider di sincronizzazione o che utilizzi il motore di sincronizzazione esterno.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Testo collegamento IT contatto</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo consente di specificare il testo del collegamento ipertestuale URL IT contatto nel Centro impostazioni società.</p></td>
<td align="left"><p>Se si abilita questa impostazione di Criteri di gruppo, nel Centro impostazioni società verrà visualizzato il testo specificato nel collegamento all'URL IT contatto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CONTATTA L'URL IT</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo consente di specificare l'URL per il collegamento IT Contatto nel Centro impostazioni società.</p></td>
<td align="left"><p>Se si abilita questa impostazione, il Centro impostazioni società collega il testo IT all'URL specificato. Il collegamento può essere di qualsiasi protocollo standard, ad esempio HTTP o mailto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notifica di primo utilizzo</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo abilita una notifica nell'area di notifica visualizzata quando ue-V</p>
<p>l'agente viene eseguito per la prima volta.</p></td>
<td align="left"><p>Il valore predefinito è abilitato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eseguire il ping del percorso di archiviazione delle impostazioni prima della sincronizzazione</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri consente alla configurazione del provider di sincronizzazione UE-V di eseguire il ping del percorso di archiviazione delle impostazioni prima di tentare di sincronizzare le impostazioni per verificare la connessione.</p></td>
<td align="left"><p>Abilita o disabilita questa impostazione di Criteri di gruppo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Soglia di avviso dimensioni pacchetto impostazioni</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo consente di configurare l'agente UE-V per segnalare quando le dimensioni del file di un pacchetto di impostazioni raggiungono una soglia definita.</p></td>
<td align="left"><p>Specificare la soglia preferita per le dimensioni dei pacchetti di impostazioni in kilobyte (KB).</p>
<p>Per impostazione predefinita, l'agente UE-V non ha una soglia per le dimensioni del file del pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Percorso di archiviazione delle impostazioni</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo consente di configurare la posizione in cui devono essere archiviate le impostazioni utente.</p></td>
<td align="left"><p>Immettere un percorso UNC (Universal Naming Convention) e variabili quali \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Percorso del catalogo dei modelli di impostazioni</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo consente di configurare la posizione in cui vengono archiviati i modelli di percorso delle impostazioni personalizzate. Questa impostazione dei criteri consente inoltre di configurare se il catalogo deve essere utilizzato per sostituire i modelli Microsoft predefiniti installati con l'agente UE-V.</p></td>
<td align="left"><p>Immettere un percorso UNC (Universal Naming Convention), ad esempio \Server\Condivisione Template o un percorso di cartella nel computer.</p>
<p>Selezionare la casella di controllo per sostituire i modelli Microsoft predefiniti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizzazione delle impostazioni su connessioni a consumo</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo definisce se UE-V sincronizza le impostazioni su connessioni a consumo.</p></td>
<td align="left"><p>Per impostazione predefinita, l'agente UE-V non sincronizza le impostazioni su una connessione a consumo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizzare le impostazioni su connessioni a consumo anche quando si esegue il roaming</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo definisce se UE-V sincronizza le impostazioni su connessioni a consumo esterne alla rete del provider principale, ad esempio quando la connessione dati è in modalità roaming.</p></td>
<td align="left"><p>Per impostazione predefinita, UE-V non sincronizza le impostazioni su una connessione a consumo quando è in modalità roaming.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Timeout sincronizzazione</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo configura il numero di millisecondi che il computer attende prima di un timeout quando recupera le impostazioni utente dalla posizione delle impostazioni remote. Se il percorso di archiviazione remota non è disponibile e l'utente non utilizza il provider di sincronizzazione, l'avvio dell'applicazione viene ritardato di questo numero di millisecondi.</p></td>
<td align="left"><p>Specificare il timeout di sincronizzazione preferito in millisecondi. Il valore predefinito è 2000 millisecondi.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizzare le impostazioni di Windows </p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo configura la sincronizzazione delle impostazioni di Windows.</p></td>
<td align="left"><p>Selezionare le impostazioni di Windows da sincronizzare tra i computer.</p>
<p>Per impostazione predefinita, i temi di Windows, le impostazioni del desktop e le impostazioni di Accessibilità sincronizzano le impostazioni tra i computer della stessa versione del sistema operativo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Icona Cassetto</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo abilita l'icona cassetto UE-V.</p></td>
<td align="left"><p>Il valore predefinito è abilitato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usare User Experience Virtualization (UE-V)</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo consente di abilitare o disabilitare UE-V.</p></td>
<td align="left"><p>Abilita o disabilita questa impostazione di Criteri di gruppo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurazione VDI</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri configura la sincronizzazione delle informazioni di rollback UE-V per i computer in esecuzione in un ambiente VDI in pool. Se questo criterio è abilitato, lo stato di rollback di UE-V viene copiato nel percorso di archiviazione delle impostazioni al logout e ripristinato all'accesso.</p></td>
<td align="left"><p>Abilita o disabilita questa impostazione di Criteri di gruppo.</p></td>
</tr>
</tbody>
</table>

 

**Nota**  
Inoltre, le impostazioni di Criteri di gruppo sono disponibili per molte applicazioni desktop e app di Windows. È possibile utilizzare queste impostazioni per abilitare o disabilitare la sincronizzazione delle impostazioni per applicazioni specifiche.

 

**Impostazioni di Criteri di gruppo per le app di Windows**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome dell'impostazione di Criteri di gruppo</th>
<th align="left">Target</th>
<th align="left">Descrizione dell'impostazione di Criteri di gruppo</th>
<th align="left">Opzioni di configurazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non sincronizzare le app di Windows</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo definisce se l'agente UE-V sincronizza le impostazioni per le app di Windows.</p></td>
<td align="left"><p>L'impostazione predefinita è la sincronizzazione delle app di Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Elenco app di Windows</p></td>
<td align="left"><p>Computer e utente</p></td>
<td align="left"><p>Questa impostazione elenca i nomi dei pacchetti di famiglia delle app di Windows e indica espressamente se UE-V sincronizza le impostazioni dell'app.</p></td>
<td align="left"><p>Puoi usare questa impostazione per specificare che le impostazioni di un'app non vengono mai sincronizzate da UE-V, anche se le impostazioni di tutte le altre app di Windows sono sincronizzate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizza app di Windows non in elenco</p></td>
<td align="left"><p>Computer e utente</p></td>
<td align="left"><p>Questa impostazione di Criteri di gruppo definisce il comportamento di sincronizzazione delle impostazioni predefinite dell'agente UE-V per le app di Windows che non sono esplicitamente elencate nell'elenco delle app di Windows.</p></td>
<td align="left"><p>Per impostazione predefinita, l'agente UE-V sincronizza solo le impostazioni delle app di Windows incluse nell'elenco delle app di Windows.</p></td>
</tr>
</tbody>
</table>

 

Per altre informazioni sulla sincronizzazione delle app di Windows, vedi [Elenco app di Windows.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

**Per configurare le impostazioni di Criteri di gruppo di destinazione del computer**

1.  Utilizzare console Gestione Criteri di gruppo (GPMC) o Gestione avanzata Criteri di gruppo (AGPM) nel computer che funge da controller di dominio per gestire le impostazioni di Criteri di gruppo per i computer UE-V. Passare a **Configurazione computer,** selezionare **Criteri,** **modelli**amministrativi, fare clic su Componenti di **Windows**e quindi selezionare Microsoft User **Experience Virtualization.**

2.  Selezionare l'impostazione di Criteri di gruppo da modificare.

**Per configurare le impostazioni di Criteri di gruppo mirate all'utente**

1.  Utilizzare la Console Gestione Criteri di gruppo (GPMC) o lo strumento Gestione avanzata Criteri di gruppo (AGPM) in Microsoft Desktop Optimization Pack (MDOP) nel computer controller di dominio per gestire le impostazioni di Criteri di gruppo per UE-V. Passare a **Configurazione utente,** selezionare **Criteri,** **modelli**amministrativi, fare clic su Componenti di **Windows**e quindi selezionare Microsoft User **Experience Virtualization.**

2.  Selezionare l'impostazione di Criteri di gruppo modificata.

L'agente UE-V usa il seguente ordine di precedenza per determinare la sincronizzazione.

**Ordine di precedenza per le impostazioni UE-V**

1.  Impostazioni di destinazione dell'utente gestite dalle impostazioni di Criteri di gruppo- Queste impostazioni di configurazione vengono archiviate nella chiave del Registro di sistema da Criteri di gruppo in `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Impostazioni di destinazione del computer gestite dalle impostazioni di Criteri di gruppo - Queste impostazioni di configurazione vengono archiviate nella chiave del Registro di sistema da Criteri di gruppo in `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Impostazioni di configurazione definite dall'utente corrente tramite Windows PowerShell o Strumentazione gestione Windows (WMI): queste impostazioni di configurazione vengono archiviate dall'agente UE-V in questo percorso del Registro di sistema: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Impostazioni di configurazione definite per il computer tramite Windows PowerShell o WMI. Queste impostazioni di configurazione vengono archiviate dall'agente UE-V in questo percorso del Registro di sistema: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **Hai un suggerimento per UE-V**? Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Hai un problema di UE-V?** Usa il [forum TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## <a name="related-topics"></a>Argomenti correlati


[Amministrazione di UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

[Gestire le configurazioni per UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
