---
title: Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo
description: Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824425"
---
# Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo


Alcune impostazioni di criteri di gruppo di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 possono essere definite per i computer e le altre impostazioni di criteri di gruppo possono essere definite per gli utenti. Per informazioni su come installare i file ADMX di criteri di gruppo UE-V, vedere [installare i modelli ADMX di criteri di gruppo UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).

Le impostazioni dei criteri seguenti possono essere configurate per la versione UE-V.

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
<th align="left">Nome dell'impostazione di criteri di gruppo</th>
<th align="left">Target</th>
<th align="left">Descrizione dell'impostazione di criteri di gruppo</th>
<th align="left">Opzioni di configurazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Contattare il testo del collegamento</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo specifica il testo del collegamento ipertestuale contatto URL nel centro impostazioni società.</p></td>
<td align="left"><p>Se si abilita questa impostazione di criteri di gruppo, il centro impostazioni società Visualizza il testo specificato nel collegamento all'URL del contatto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL contatti</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo specifica l'URL del collegamento contatto IT nel centro impostazioni società.</p></td>
<td align="left"><p>Se si abilita questa impostazione, il centro impostazioni società Contatta i collegamenti di testo all'URL specificato. Il collegamento può essere di qualsiasi protocollo standard, ad esempio HTTP o mailto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non usare il provider di sincronizzazione</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Usando questa impostazione di criteri di gruppo, è possibile specificare se la funzionalità provider di sincronizzazione viene usata da UE-V. Questa impostazione dei criteri consente inoltre di attivare la notifica quando l'importazione delle impostazioni utente viene ritardata.</p></td>
<td align="left"><p>Abilitare questa impostazione per configurare l'agente UE-V per non usare il provider di sincronizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notifica primo utilizzo</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo Abilita una notifica nell'area di notifica visualizzata quando l'UE-V</p>
<p>l'agente viene eseguito per la prima volta.</p></td>
<td align="left"><p>Il valore predefinito è Enabled.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni di Windows roaming</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo configura la sincronizzazione delle impostazioni di Windows.</p></td>
<td align="left"><p>Selezionare le impostazioni di Windows da sincronizzare tra i computer.</p>
<p>Per impostazione predefinita, i temi di Windows, le impostazioni desktop e le impostazioni di accesso facilitato sincronizzano le impostazioni tra i computer della stessa versione del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Soglia di avviso dimensioni pacchetto impostazioni</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo consente di configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</p></td>
<td align="left"><p>Specificare la soglia preferita per le dimensioni del pacchetto di impostazioni in kilobyte (KB).</p>
<p>Per impostazione predefinita, l'agente UE-V non ha una soglia di dimensione del file del pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Percorso di archiviazione delle impostazioni</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo configura la posizione in cui devono essere archiviate le impostazioni utente.</p></td>
<td align="left"><p>Immettere un percorso UNC (Universal Naming Convention) e variabili come \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Percorso catalogo di modelli di impostazioni</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo Configura dove sono archiviati i modelli di posizione delle impostazioni personalizzate. Questa impostazione dei criteri Configura anche se il catalogo deve essere usato per sostituire i modelli Microsoft predefiniti installati con l'agente UE-V.</p></td>
<td align="left"><p>Immettere un percorso UNC (Universal Naming Convention), ad esempio \Server\TemplateShare, o una posizione di cartella nel computer.</p>
<p>Selezionare la casella di controllo per sostituire i modelli Microsoft predefiniti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni di sincronizzazione tramite connessioni a consumo</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo definisce se l'opzione UE-V sincronizza le impostazioni tramite connessioni a consumo.</p></td>
<td align="left"><p>Per impostazione predefinita, l'agente UE-V non sincronizza le impostazioni tramite una connessione a consumo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizzare le impostazioni tramite connessioni a consumo anche in roaming</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo definisce se l'opzione UE-V sincronizza le impostazioni tramite connessioni a consumo all'esterno della rete del provider Home, ad esempio quando la connessione dati è in modalità roaming.</p></td>
<td align="left"><p>Per impostazione predefinita, l'opzione UE-V non sincronizza le impostazioni tramite una connessione a consumo quando è in modalità roaming.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Timeout della sincronizzazione</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo Configura il numero di millisecondi che il computer attende prima di un timeout quando recupera le impostazioni utente dalla posizione di impostazioni remote. Se la posizione di archiviazione remota non è disponibile e l'utente non usa il provider di sincronizzazione, l'avvio dell'applicazione viene ritardato di molti millisecondi.</p></td>
<td align="left"><p>Specificare il timeout di sincronizzazione preferito in millisecondi. Il valore predefinito è 2000 millisecondi.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Icona del vassoio</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo consente l'icona della barra multifunzione di virtualizzazione (UE-V) dell'esperienza utente.</p></td>
<td align="left"><p>Il valore predefinito è Enabled.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usare la virtualizzazione dell'esperienza utente (UE-V)</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo consente di abilitare o disabilitare la virtualizzazione dell'esperienza utente (UE-V).</p></td>
<td align="left"><p>Abilitare o disabilitare questa impostazione di criteri di gruppo.</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Inoltre, le impostazioni dei criteri di gruppo sono disponibili per molte applicazioni desktop e app di Windows. Puoi usare queste impostazioni per abilitare o disabilitare la sincronizzazione delle impostazioni per applicazioni specifiche.

 

**Impostazioni dei criteri di gruppo delle app di Windows**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome dell'impostazione di criteri di gruppo</th>
<th align="left">Target</th>
<th align="left">Descrizione dell'impostazione di criteri di gruppo</th>
<th align="left">Opzioni di configurazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non sincronizzare le app di Windows</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo definisce se l'agente UE-V sincronizza le impostazioni per le app di Windows.</p></td>
<td align="left"><p>Il valore predefinito è la sincronizzazione delle app di Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Elenco delle app di Windows</p></td>
<td align="left"><p>Computer e utente</p></td>
<td align="left"><p>Questa impostazione elenca i nomi dei pacchetti familiari delle app di Windows e dichiara espressamente se l'opzione UE-V sincronizza le impostazioni dell'app.</p></td>
<td align="left"><p>Puoi usare questa impostazione per specificare che le impostazioni di un'app non vengono mai sincronizzate da UE-V, anche se le impostazioni di tutte le altre app di Windows sono sincronizzate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizzare le app di Windows non in elenco</p></td>
<td align="left"><p>Computer e utente</p></td>
<td align="left"><p>Questa impostazione di criteri di gruppo definisce il comportamento di sincronizzazione delle impostazioni predefinite dell'agente UE-V per le app di Windows che non sono elencate esplicitamente nell'elenco delle app di Windows.</p></td>
<td align="left"><p>Per impostazione predefinita, l'agente UE-V Sincronizza solo le impostazioni delle app di Windows incluse nell'elenco delle app di Windows.</p></td>
</tr>
</tbody>
</table>

 

Per altre informazioni sulla sincronizzazione delle app di Windows, Vedi [elenco delle app di Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**Per configurare le impostazioni di criteri di gruppo mirate al computer**

1.  Usare la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo nel computer che funge da controller di dominio per gestire le impostazioni dei criteri di gruppo per i computer UE-V. Passare alla **configurazione del computer**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.

2.  Selezionare l'impostazione di criteri di gruppo da modificare.

**Per configurare le impostazioni di criteri di gruppo mirate dall'utente**

1.  Usare la console di gestione di criteri di gruppo o lo strumento Advanced Group Policy Management in Microsoft Desktop Optimization Pack (MDOP) nel computer del controller di dominio per gestire le impostazioni dei criteri di gruppo per UE-V. Passare alla **Configurazione utente**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.

2.  Selezionare l'impostazione di criteri di gruppo modificata.

L'agente UE-V usa l'ordine di precedenza seguente per determinare la sincronizzazione.

**Ordine di precedenza per le impostazioni UE-V**

1.  Impostazioni di destinazione utente gestite da impostazioni di criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Impostazioni di destinazione del computer gestite da impostazioni di criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Impostazioni di configurazione definite dall'utente corrente tramite Windows PowerShell o Strumentazione gestione Windows (WMI)-queste impostazioni di configurazione sono archiviate dall'agente UE-V in questo percorso del registro di sistema: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Impostazioni di configurazione definite per il computer tramite Windows PowerShell o WMI. Queste impostazioni di configurazione sono archiviate dall'agente UE-V in questo percorso del registro di sistema: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **Hai un suggerimento per l'UE-V**? Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **È stato ottenuto un problema UE-V**? Utilizzare il [forum TechNet di UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Argomenti correlati


[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Gestire le configurazioni per UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





