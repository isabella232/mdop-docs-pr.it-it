---
title: Configurazione di UE-V con oggetti Criteri di gruppo
description: Configurazione di UE-V con oggetti Criteri di gruppo
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826696"
---
# Configurazione di UE-V con oggetti Criteri di gruppo


Alcune impostazioni di criteri di gruppo di Microsoft User Experience Virtualization (UE-V) possono essere definite per i computer e altre possono essere definite per gli utenti. Le impostazioni dei criteri di configurazione dell'agente UE-V possono essere definite per i computer o gli utenti. Per informazioni su come installare i file ADMX di criteri di gruppo UE-V, vedere [installare i modelli ADMX di criteri di gruppo UE-v](installing-the-ue-v-group-policy-admx-templates.md).

Le impostazioni dei criteri seguenti possono essere configurate per UE-V:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nome impostazione criterio</strong></p></td>
<td align="left"><p><strong>Target</strong></p></td>
<td align="left"><p><strong>Descrizione delle impostazioni dei criteri</strong></p></td>
<td align="left"><p><strong>Opzioni di configurazione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Usare la virtualizzazione dell'esperienza utente (UE-V)</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri consente di abilitare o disabilitare la virtualizzazione dell'esperienza utente (UE-V).</p></td>
<td align="left"><p>Abilitare o disabilitare questa impostazione per i criteri.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Percorso di archiviazione delle impostazioni</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri Configura la posizione in cui verranno archiviate le impostazioni utente.</p></td>
<td align="left"><p>Specificare un percorso UNC (Universal Naming Convention) e variabili come \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Percorso catalogo di modelli di impostazioni</p></td>
<td align="left"><p>Solo computer</p></td>
<td align="left"><p>Questa impostazione dei criteri Configura dove sono archiviati i modelli di posizione delle impostazioni personalizzate. Questa impostazione dei criteri Configura anche se il catalogo verrà usato per sostituire i modelli Microsoft predefiniti installati con l'agente UE-V.</p></td>
<td align="left"><p>Specificare un percorso UNC (Universal Naming Convention), ad esempio \Server\TemplateShare, o un percorso di cartella nel computer.</p>
<p></p>
<p>Selezionare la casella di controllo per sostituire i modelli Microsoft predefiniti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non usare file offline</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri consente di configurare se UE-V utilizzerà la funzionalità file offline di Windows. Questa impostazione dei criteri consente inoltre di abilitare la notifica quando l'importazione delle impostazioni utente viene ritardata.</p></td>
<td align="left"><p>Per configurare l'agente UE-V per non usare i file offline, abilitare questa impostazione.</p>
<p></p>
<p>Specificare se le notifiche devono essere fornite quando l'importazione delle impostazioni è ritardata.</p>
<p></p>
<p>Specificare l'intervallo di tempo in secondi da attendere prima che venga visualizzata la notifica.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Timeout della sincronizzazione</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione del criterio Configura il numero di millisecondi di attesa prima di un timeout durante il recupero delle impostazioni utente dalla posizione di impostazioni remote. Se la posizione di archiviazione remota non è disponibile, l'avvio dell'applicazione viene ritardato di molti millisecondi.</p></td>
<td align="left"><p>Specificare il timeout di sincronizzazione preferito in millisecondi. Il valore predefinito di 2000 millisecondi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Soglia di avviso dimensione pacchetto</p></td>
<td align="left"><p>Computer e utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri consente di configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</p></td>
<td align="left"><p>Specificata la soglia preferita per le dimensioni del pacchetto di impostazioni in kilobyte.</p>
<p>Per impostazione predefinita, l'agente UE-V non ha una soglia di dimensione del file del pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostazioni dell'applicazione roaming</p></td>
<td align="left"><p>Solo utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri Configura il roaming delle impostazioni utente delle applicazioni.</p></td>
<td align="left"><p>Selezionare le impostazioni di Windows che andranno in roaming tra i computer.</p>
<p>Per impostazione predefinita, le impostazioni utente delle applicazioni con il modello di impostazioni fornito da UE-V sono in roaming tra i computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni di Windows in roaming</p></td>
<td align="left"><p>Solo utenti</p></td>
<td align="left"><p>Questa impostazione dei criteri Configura il roaming delle impostazioni di Windows.</p></td>
<td align="left"><p>Selezionare le applicazioni che andranno in roaming tra i computer.</p>
<p>Per impostazione predefinita, i temi di Windows vengono spostati tra i computer della stessa versione del sistema operativo. Le impostazioni desktop di Windows e le impostazioni di accesso facilitato non sono in roaming.</p></td>
</tr>
</tbody>
</table>

 

**Per configurare i criteri di destinazione del computer**

1.  Usare la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo nel computer controller di dominio che gestisce i criteri di gruppo per i computer UE-V. Passare alla **configurazione del computer**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.

2.  Selezionare l'impostazione del criterio da modificare.

**Per configurare i criteri di destinazione dell'utente**

1.  Usare la console di gestione di criteri di gruppo o lo strumento Advanced Group Policy Management in Microsoft Desktop Optimization Pack (MDOP) nel computer controller di dominio che gestisce i criteri di gruppo per UE-V. Passare alla **Configurazione utente**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.

2.  Selezionare l'impostazione dei criteri modificata.

L'agente UE-V usa l'ordine di precedenza seguente per determinare la sincronizzazione.

**Ordine di precedenza per le impostazioni UE-V**

1.  Impostazioni di destinazione utente gestite da criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Impostazioni di destinazione del computer gestite da criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Impostazioni di configurazione definite dall'utente corrente tramite PowerShell o WMI-queste impostazioni di configurazione sono archiviate dall'agente UE-V in questo percorso del registro di sistema: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Impostazioni di configurazione definite per il computer con PowerShell o WMI. Queste impostazioni di configurazione sono archiviate dall'agente UE-V in `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .

## Argomenti correlati


[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





