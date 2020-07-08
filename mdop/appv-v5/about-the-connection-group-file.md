---
title: Informazioni sul file del gruppo di connessione
description: Informazioni sul file del gruppo di connessione
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806099"
---
# Informazioni sul file del gruppo di connessione


**In questo argomento:**

-   [Scopo e posizione del file del gruppo di connessioni](#bkmk-cg-purpose-loc)

-   [Struttura del file XML del gruppo di connessioni](#bkmk-define-cg-5-0sp3)

-   [Configurazione della priorità dei pacchetti in un gruppo di connessioni](#bkmk-config-pkg-priority-incg)

-   [Configurazioni di connessione dell'applicazione virtuale supportate](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>Scopo e posizione del file del gruppo di connessioni


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Scopo del gruppo di connessioni</p></td>
<td align="left"><p>Un gruppo di connessioni è una funzionalità App-V che consente di raggruppare i pacchetti per creare un ambiente virtuale in cui le applicazioni in questi pacchetti possono interagire tra loro.</p>
<p>Esempio: si vogliono usare i plug-in con Microsoft Office. È possibile creare un pacchetto che contiene i plug-in e creare un altro pacchetto che contiene Office e quindi aggiungere entrambi i pacchetti a un gruppo di connessioni per consentire a Office di usare questi plug-in.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Funzionamento del file del gruppo di connessioni</p></td>
<td align="left"><p>Quando si applica un file del gruppo di connessioni di Application Virtualization 5,0, i pacchetti enumerati nel file verranno combinati in fase di esecuzione in un unico ambiente virtuale. Usare il file del gruppo di connessioni 5,0 di Microsoft Application Virtualization (App-V) per configurare i gruppi di connessioni di Application Virtualization 5,0 esistenti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Percorso file di esempio</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>Struttura del file XML del gruppo di connessioni


**In questa sezione:**

-   [Parametri che definiscono il gruppo di connessioni](#bkmk-params-define-cg)

-   [Parametri che definiscono i pacchetti nel gruppo di connessioni](#bkmk-params-define-pkgs-incg)

-   [File XML del gruppo di connessioni di esempio App-V 5,0 SP3](#bkmk-50sp3-exp-cg-xml)

-   [App-V 5,0 tramite l'App-V 5,0 SP2 esempio di file XML del gruppo di connessioni](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>Parametri che definiscono il gruppo di connessioni

La tabella seguente descrive i parametri nel file XML che definiscono il gruppo di connessioni stesso, non i pacchetti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome schema</p></td>
<td align="left"><p>Nome dello schema.</p>
<p><strong>Applicabile a partire da App-V 5,0 SP3 </strong> : se si vogliono usare le nuove funzionalità "pacchetti facoltativi" e "Usa qualsiasi versione" descritte in questa tabella, è necessario specificare lo schema seguente nel file XML:</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>Identificatore GUID univoco per il gruppo di connessioni. Lo stato del gruppo di connessioni è associato a questo identificatore. Specificare questo identificatore solo quando si crea il gruppo di connessioni.</p>
<p>È possibile creare un nuovo GUID digitando: <strong>[Guid]::NewGuid()</strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificatore GUID versione per questa versione del gruppo di connessioni.</p>
<p>Quando si aggiorna un gruppo di connessioni, ad esempio aggiungendo o aggiornando un nuovo pacchetto, è necessario aggiornare il GUID della versione per riflettere la nuova versione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>Visualizzare il nome del gruppo di connessioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Priority</p></td>
<td align="left"><p>Campo Priority facoltativo per il gruppo di connessioni.</p>
<p><strong>"0" </strong> - indica la priorità più alta.</p>
<p>Se è necessaria una priorità, ma non è stata configurata, il pacchetto non riuscirà perché non è possibile determinare il gruppo di connessioni corretto da usare.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>Parametri che definiscono i pacchetti nel gruppo di connessioni

Nella &lt; sezione pacchetti &gt; del file XML del gruppo di connessioni è possibile elencare i pacchetti di membri nel gruppo di connessioni specificando l'identificatore univoco del pacchetto e l'identificatore di versione di ogni pacchetto, come descritto nella tabella seguente. Il primo pacchetto nell'elenco ha la precedenza più alta.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageId</p></td>
<td align="left"><p>Identificatore GUID univoco per il pacchetto. Questo GUID non cambia quando vengono pubblicate versioni più recenti del pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificatore GUID univoco per la versione del pacchetto.</p>
<p><strong>Applicabile a partire da App-V 5,0 SP3 </strong> : se specifichi <strong> "*" </strong> per la versione del pacchetto, il GUID della versione più recente del pacchetto disponibile viene inserito in modo dinamico.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IsOptional</p></td>
<td align="left"><p><strong>Applicabile a partire da App-V 5,0 SP3 </strong> : parametro che consente di rendere facoltativo un pacchetto all'interno del gruppo di connessioni. Le voci valide sono:</p>
<ul>
<li><p><strong>"true" </strong> : il pacchetto è facoltativo nel gruppo di connessioni</p></li>
<li><p><strong>"false" </strong> : il pacchetto è obbligatorio nel gruppo di connessioni</p></li>
</ul>
<p>Informazioni <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)"> su come usare i pacchetti facoltativi nei gruppi di connessioni </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>File XML del gruppo di connessioni di esempio App-V 5,0 SP3

Il file XML del gruppo di connessioni di esempio seguente mostra esempi di campi nelle tabelle precedenti ed evidenzia gli elementi nuovi per App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>App-V 5,0 tramite l'App-V 5,0 SP2 esempio di file XML del gruppo di connessioni

Il file XML del gruppo di connessioni di esempio seguente si applica a App-V 5,0 tramite App-V 5,0 SP2. Mostra alcuni esempi dei campi della tabella precedente, ma esclude le modifiche descritte in precedenza per App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>Configurazione della priorità dei pacchetti in un gruppo di connessioni


La precedenza del pacchetto viene configurata con l'ordine di elenco dei pacchetti. Il primo pacchetto nel documento ha la precedenza più alta. I pacchetti successivi nell'elenco hanno priorità decrescente.

La precedenza del pacchetto è la risoluzione per eventuali collisioni di risorse inevitabili durante l'inizializzazione dell'ambiente virtuale. Se ad esempio due pacchetti che si aprono nello stesso ambiente virtuale definiscono lo stesso valore DWORD del registro di sistema, il pacchetto con la precedenza più alta determina il valore impostato.

È possibile usare il file del gruppo di connessioni per configurare ogni gruppo di connessioni usando i metodi seguenti:

-   Specificare le priorità di runtime per i gruppi di connessioni.

    **Nota**  La priorità è obbligatoria solo se il pacchetto è associato a più di un gruppo di connessioni.

     

-   Specificare la precedenza del pacchetto nel gruppo di connessioni.

Il campo priorità è obbligatorio quando un'applicazione virtuale in uso viene avviata da una richiesta di applicazione nativa, ad esempio Esplora risorse di Microsoft Windows. Il client App-V usa la priorità per determinare l'ambiente virtuale del gruppo di connessioni in cui deve essere eseguita l'applicazione. Questa situazione si verifica se un'applicazione virtuale fa parte di più gruppi di connessioni.

Se un'applicazione virtuale viene aperta con un'altra applicazione virtuale, verrà usato l'ambiente virtuale dell'applicazione virtuale originale. Il campo priorità non viene usato in questo caso.

**Esempio:**

L'applicazione virtuale Microsoft Outlook è in uso nell'ambiente virtuale **XYZ**. Quando si apre un documento di Microsoft Word allegato, viene aperta una versione virtualizzata di Microsoft Word nell'ambiente virtuale **XYZ**, indipendentemente dai gruppi di connessioni associati o dalle priorità di runtime virtualizzati di Microsoft Word.

## <a href="" id="bkmk-va-conn-configs"></a>Configurazioni di connessione dell'applicazione virtuale supportate


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configurazione</th>
<th align="left">Scenario di esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Un. file exe e plug-in (dll)</p></td>
<td align="left"><ul>
<li><p>Si vuole distribuire Microsoft Office a tutti gli utenti, ma distribuire un plug-in di Microsoft Excel solo a un sottoinsieme di utenti.</p></li>
<li><p>Abilitare il gruppo di connessioni per gli utenti appropriati.</p></li>
<li><p>Aggiornare ogni pacchetto singolarmente, come richiesto.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Un. file exe e un'applicazione middleware</p></td>
<td align="left"><ul>
<li><p>L'applicazione richiede un'applicazione middleware o diverse applicazioni che dipendono dalla stessa versione di runtime di middleware.</p></li>
<li><p>Tutti i computer che richiedono una o più applicazioni ricevono i gruppi di connessioni con l'applicazione e il runtime dell'applicazione middleware.</p></li>
<li><p>Puoi facoltativamente combinare più applicazioni middleware in un singolo gruppo di connessioni.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Esempio</th>
<th align="left">Descrizione dell'esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gruppo connessione applicazione virtuale per la divisione finanziaria</p></td>
<td align="left"><ul>
<li><p>Applicazione middleware 1</p></li>
<li><p>Applicazione middleware 2</p></li>
<li><p>Applicazione middleware 3</p></li>
<li><p>Middleware Application runtime</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Gruppo connessione applicazione virtuale per la divisione HR</p></td>
<td align="left"><ul>
<li><p>Applicazione middleware 5</p></li>
<li><p>Applicazione middleware 6</p></li>
<li><p>Middleware Application runtime</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Un. file exe e file exe</p></td>
<td align="left"><p>Si ha un'applicazione che si basa su un'altra applicazione e si vuole evitare che i pacchetti vengano separati per l'efficienza operativa, le restrizioni delle licenze o le sequenze temporali di implementazione.</p>
<p><strong>Esempio:</strong></p>
<p>Se si distribuisce Microsoft Lync 2010, è possibile usare tre pacchetti:</p>
<ul>
<li><p>Microsoft Office2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>È possibile gestire la distribuzione usando i gruppi di connessioni seguenti:</p>
<ul>
<li><p>Microsoft Office2010 e Microsoft Communicator2007</p></li>
<li><p>Microsoft Office2010 e Microsoft Lync2010</p></li>
</ul>
<p>Al termine della distribuzione, è possibile creare un singolo nuovo pacchetto Microsoft Office2010 + Microsoft Lync2010 oppure conservarlo e mantenerlo come pacchetti separati e distribuirlo usando un gruppo di connessioni.</p></td>
</tr>
</tbody>
</table>

 






## Argomenti correlati


[Gestione dei gruppi di connessione](managing-connection-groups.md)

 

 





