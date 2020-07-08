---
title: Pianificazione delle applicazioni da sincronizzare con UE-V 1.0
description: Pianificazione delle applicazioni da sincronizzare con UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804210"
---
# Pianificazione delle applicazioni da sincronizzare con UE-V 1.0


Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate da UE-V. UE-V include un set di modelli di posizione predefiniti per le impostazioni e consente inoltre agli amministratori di creare modelli di posizione personalizzati per le applicazioni di terze parti o line-of-business usate nell'organizzazione.

In qualità di amministratore, quando si considerano le applicazioni da includere nella soluzione UE-V, valutare quali impostazioni possono essere personalizzate dagli utenti e come e dove l'applicazione archivia le proprie impostazioni. Non tutte le applicazioni hanno impostazioni che possono essere personalizzate o che sono personalizzate in routine dagli utenti. Inoltre, non tutte le impostazioni delle applicazioni possono spostarsi in modo sicuro in più computer o ambienti. Sincronizzare le impostazioni che soddisfano i criteri seguenti:

-   Impostazioni archiviate in percorsi accessibili dall'utente. Ad esempio, non sincronizzare le impostazioni archiviate nella sezione system32 o outside HKCU del registro di sistema.

-   Impostazioni non specifiche per il computer specifico. Ad esempio, Escludi configurazioni di rete o hardware.

-   Impostazioni che è possibile sincronizzare tra computer senza rischio di dati danneggiati. Ad esempio, non usare le impostazioni archiviate in un file di database.

## Modelli di posizione delle impostazioni inclusi in UE-V


**Modelli di posizione delle impostazioni dell'applicazione UE-V**

Il software di installazione dell'agente UE-V installa l'agente e registra un gruppo predefinito di modelli di posizione delle impostazioni per le applicazioni Microsoft comuni. Questi modelli di posizione delle impostazioni acquisiscono i valori delle impostazioni per le applicazioni seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria applicazione</strong></th>
<th align="left"><strong>Descrizione</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applicazioni di Microsoft Office 2010</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opzioni del browser (Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10)</p></td>
<td align="left"><p>Preferiti, Home page, schede e barre degli strumenti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Accessori per Windows</p></td>
<td align="left"><p>Calcolatrice, blocco note, WordPad.</p></td>
</tr>
</tbody>
</table>

 

Le impostazioni dell'applicazione vengono applicate all'applicazione quando l'applicazione viene avviata. Vengono salvati quando l'applicazione viene chiusa.

**Modelli di posizione delle impostazioni di Windows UE-V**

Esperienza utente la virtualizzazione include i modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per le impostazioni di Windows seguenti:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">impostazioni di Windows</th>
<th align="left">Descrizione</th>
<th align="left">Applicare il</th>
<th align="left">Stato predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sfondo del desktop</p></td>
<td align="left"><p>Sfondo del desktop attualmente attivo.</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota.</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accessibilità</p></td>
<td align="left"><p>Impostazioni di accessibilità e input, lente di ingrandimento, Assistente vocale e tastiera su schermo.</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota.</p></td>
<td align="left"><p>Disabilitato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni desktop</p></td>
<td align="left"><p>Menu Start e impostazioni della barra delle applicazioni, Opzioni cartella, icone desktop predefinite, clock aggiuntivi e impostazioni area geografica e lingua.</p></td>
<td align="left"><p>Solo accesso.</p></td>
<td align="left"><p>Disabilitato</p></td>
</tr>
</tbody>
</table>

 

Lo sfondo del desktop di Windows e le impostazioni di accessibilità vengono applicati quando l'utente effettua l'accesso, quando il computer viene sbloccato o dopo la connessione remota a un altro computer. L'agente Salva queste impostazioni quando l'utente si disconnette, quando il computer è bloccato o quando una connessione remota è disconnessa. Per impostazione predefinita, le impostazioni in background di Windows desktop sono in roaming tra i computer della stessa versione del sistema operativo.

Il desktop di Windows e le impostazioni di accesso facilitato vengono applicati all'accesso prima che il desktop venga presentato all'utente. Per ottimizzare l'esperienza di accesso, queste impostazioni non sono in roaming per impostazione predefinita. Le impostazioni desktop e di accesso facilitato possono essere abilitate tramite criteri di gruppo, PowerShell e WMI.

UE-V non supporta il roaming delle impostazioni tra sistemi operativi con lingue diverse. La sincronizzazione tra l'inglese e il tedesco, ad esempio, non è supportata. La lingua di tutti i computer a cui è necessario eseguire il roaming delle impostazioni utente in UE-V deve corrispondere.

**Nota**  Se si modificano i modelli di posizione delle impostazioni forniti da Microsoft, la virtualizzazione dell'esperienza utente potrebbe non funzionare correttamente per l'applicazione designata o per il gruppo impostazioni di Windows.

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a>Impedire la configurazione delle impostazioni utente non intenzionale


L'esperienza utente verifica la virtualizzazione delle nuove informazioni sulle impostazioni utente e Scarica le informazioni di conseguenza da una posizione di archiviazione delle impostazioni. Applica quindi le impostazioni al computer locale nei casi seguenti:

-   Ogni volta che viene avviata un'applicazione con un modello UE-V registrato.

-   Quando un utente accede al proprio computer.

-   Quando un utente sblocca il computer.

-   Quando viene effettuata una connessione a un computer desktop remoto in cui è installata la versione UE-V.

Se UE-V è installato nel computer A e nel computer B e le impostazioni desiderate per l'applicazione si trovano nel computer A, il computer A deve aprire e chiudere prima l'applicazione. Se un'applicazione viene aperta e chiusa prima del computer B, le impostazioni dell'applicazione nel computer A verranno configurate in modo che siano le stesse delle impostazioni dell'applicazione nel computer B.

Questo scenario si applica anche alle impostazioni di Windows. Se le impostazioni di Windows nel computer B devono essere le stesse delle impostazioni di Windows nel computer A, l'utente deve innanzitutto accedere al computer e disconnessione.

Se le impostazioni utente desiderate vengono applicate nell'ordine errato, possono essere recuperate eseguendo un'operazione di ripristino per l'applicazione specifica o la configurazione di Windows nel computer in cui sono state sovrascritte le impostazioni. Per altre informazioni, vedere [ripristino delle impostazioni di applicazione e Windows sincronizzate con UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).

## Modelli di posizione delle impostazioni UE-V personalizzati


Puoi creare modelli di posizione delle impostazioni personalizzati usando il generatore UE-V. Dopo aver creato e testato un modello di posizione delle impostazioni personalizzato in un ambiente di test, è possibile distribuire i modelli di posizione delle impostazioni ai computer nell'organizzazione. I modelli di posizione delle impostazioni personalizzate devono essere distribuiti con un'infrastruttura di distribuzione esistente, ad esempio il metodo ESD (Enterprise Software Distribution), con le preferenze o configurando un catalogo di modelli di impostazioni UE-V. I modelli distribuiti con ESD o criteri di gruppo devono essere registrati usando WMI o PowerShell di UE-V. Per altre informazioni sui modelli di posizione delle impostazioni personalizzate, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

Per informazioni sull'eventuale sincronizzazione di un'applicazione line-of-business, vedere [elenco di controllo per la valutazione delle applicazioni line-of-business per UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).

## Argomenti correlati


[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

[Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Distribuzione di UE-V 1.0](deploying-ue-v-10.md)

 

 





