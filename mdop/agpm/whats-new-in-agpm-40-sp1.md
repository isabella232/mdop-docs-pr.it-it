---
title: Novità di Gestione avanzata Criteri di gruppo 4.0 SP1
description: Novità di Gestione avanzata Criteri di gruppo 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818155"
---
# Novità di Gestione avanzata Criteri di gruppo 4.0 SP1


Il contenuto "Novità" descrive i miglioramenti apportati e le configurazioni supportate per Microsoft Advanced Group Policy Management (Advanced criteri di gruppo) 4,0 SP1. Se c'è una differenza tra il contenuto e altre documentazioni della Advanced Group Policy Management, questo contenuto deve essere considerato attendibile e deve sostituire il contenuto incluso in questo prodotto.

## <a href="" id="what-s-new"></a>Novità


Advanced Group Policy Management 4,0 SP1 supporta i miglioramenti seguenti:

### Estensioni lato client nuove e modificate

Le estensioni lato client di criteri di gruppo (CSEs) sono state aggiunte o modificate per Advanced Group Policy per supportare nuovi criteri di gruppo in Windows 8 e Windows Server 2012. Questi criteri di gruppo consentono agli amministratori dei criteri di gruppo di gestire e tenere traccia delle impostazioni di criteri di gruppo specifiche di Windows 8 che cambiano tra due oggetti Criteri di gruppo o modelli. Puoi anche creare GPO personalizzati, con impostazioni specifiche di Windows 8 e configurare e salvare i GPO come modello. Per visualizzare il proprio CSEs, usare i report impostazioni e differenze disponibili nel client Advanced Group Policy Management di 4,0 SP1.

Le nuove estensioni lato client di criteri di gruppo modificate sono:

-   **Criteri di accesso centralizzato:** Consente agli amministratori di criteri di gruppo di specificare criteri di accesso centralizzati nei server dei criteri di gruppo, ad esempio file server. Criteri di accesso centralizzati è un criterio di autorizzazione specificato da un elemento GPO e applicato alle destinazioni dei criteri per facilitare l'accesso centralizzato e il controllo delle risorse. Questi criteri di accesso centralizzato devono essere configurati in un computer client di criteri di gruppo in Active Directory. Un criterio di gruppo distribuisce la conoscenza di un criterio di accesso centralizzato applicabile ai computer che devono imporlo.

-   **Modifiche ai criteri di risoluzione dei nomi:** Consente agli amministratori di criteri di gruppo di configurare le impostazioni per la sicurezza DNS e DirectAccess nei computer client DNS. Sono state aggiunte nuove schede per la configurazione delle impostazioni del server DNS generico e delle impostazioni di codifica.

-   **Modifiche alle preferenze di criteri di gruppo:** Aggiunge il supporto per la configurazione e la gestione delle impostazioni di Internet Explorer 10 aggiunte per Windows 8.

-   **Connessioni desktop e applicazioni remote:** Consente agli amministratori di criteri di gruppo di specificare l'URL di connessione predefinito usato per le connessioni desktop e dell'applicazione remota.

-   **Opzioni di avvio di Windows per andare:** Consente agli amministratori di criteri di gruppo di configurare se il computer verrà avviato in Windows per spostarsi se è connesso un dispositivo USB che contiene un'area di lavoro Windows to go.

-   **Opzioni di sospensione di Windows per andare:** Consente agli amministratori di criteri di gruppo di stabilire se un computer può usare lo stato di sospensione dell'ibernazione (S4) quando il computer viene avviato da un'area di lavoro di Windows to go.

### Feedback dei clienti e aggiornamento cumulativo

Advanced Group Policy Management 4,0 SP1 include un rollup di correzioni per risolvere i problemi riscontrati dopo la versione di Advanced Group Policy Management 4,0. Advanced Group Policy Management 4,0 SP1 contiene le correzioni più recenti fino a Microsoft Advanced gruppo criteri di gestione di 4,0 hotfix 1.

### Le impostazioni e i report differenze mostrano le nuove estensioni di criteri di gruppo

Le nuove estensioni di criteri di gruppo sono state aggiunte ai report impostazioni e differenze.

### Modifiche e supporto del programma di installazione

Le modifiche e il supporto per il programma di installazione di Advanced Group Policy Management 4,0 SP1 sono:

-   Se si installa Advanced Group Policy Manager 4,0 SP1 in Windows 8 o Windows Server 2012, il programma di installazione di Advanced Group Policy Management verifica che sia installato il software prerequisito richiesto (console di gestione dei criteri di gruppo e .NET 3,5 Framework). Se questi prerequisiti non sono installati, l'installazione di Advanced Group Policy Management 4,0 SP1 è bloccata.

-   Quando si installa Advanced Group Policy 4,0 Management SP1, l'attivazione di WCF, l'attivazione non HTTP e il servizio di attivazione processo Windows vengono abilitati automaticamente.

-   Nei sistemi operativi client Windows Vista, Windows 7 e Windows 8 scaricare la versione appropriata di Remote System Administration Toolkit per il sistema operativo prima di installare Advanced Group Policy Management SP1 4,0.

-   È supportata la compatibilità con le versioni precedenti dei sistemi operativi supportati meno recenti.

### Possibilità di eseguire l'aggiornamento o l'aggiornamento a Advanced Group Policy Management 4,0 SP1 senza immettere di nuovo i parametri di configurazione

È possibile aggiornare il client o il server Advanced Group Policy Management a Advanced Group Policy Management 4,0 SP1 solo da Advanced Group Policy 4,0 Management senza che venga chiesto di immettere di nuovo i parametri di configurazione, definiti "Smart Upgrade", come illustrato nella tabella seguente. Se si esegue l'aggiornamento a Advanced Group Policy Management 4,0 SP1 da altre versioni di Advanced Group Policy Management, come illustrato nella tabella, è necessario usare l'"aggiornamento classico", che richiede di immettere di nuovo i parametri di configurazione. Poiché ogni versione di Advanced Group Policy Management è associata a un sistema operativo specifico, vedere [scelta della versione di Advanced Group Policy Management da installare](https://go.microsoft.com/fwlink/?LinkId=254350)e assicurarsi di aggiornare il sistema operativo in modo appropriato prima di eseguire l'aggiornamento.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versione Advanced Group Policy Management da cui è possibile eseguire l'aggiornamento</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
</tr>
</tbody>
</table>

 

## Configurazioni supportate


Advanced Group Policy Management supporta le configurazioni nella tabella seguente. Anche se Advanced Group Policy Management supporta configurazioni miste, è consigliabile eseguire il client e il server Advanced Group Policy Management nella stessa famiglia di sistemi operativi, ad esempio Windows 8 con Windows Server 2012, Windows 7 con Windows Server 2008 R2 e così via.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurazioni supportate per il server Advanced Group Policy Management 4,0</strong></p></td>
<td align="left"><p><strong>Configurazioni supportate per il client Advanced Group Policy Management 4,0</strong></p></td>
<td align="left"><p><strong>Supporto per Advanced Group Policy Management 4,0</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 o Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 o Windows 7</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 o Windows 7 o Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows Server 2008 R2 o Windows 7 o Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 o Windows 7 o Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server 2008 R2 o Windows 7 o Windows 8</p></td>
</tr>
</tbody>
</table>

 

## Prerequisiti per l'installazione di Advanced Group Policy Management 4,0 SP1


La tabella seguente descrive il comportamento in Windows 8 del client e dei programmi di installazione di Advanced Group Policy Management 4,0 SP1 quando non è presente .NET 3,5 o la console di gestione di criteri di gruppo negli strumenti di amministrazione del server remoto.

**Client Advanced Group Policy Management 4,0 SP1**

**Advanced Group Policy Management Server 4,0 SP1**

**Sistema operativo**

**.NET**

**Strumenti di amministrazione remota del server**

**.NET**

**Strumenti di amministrazione remota del server**

**Windows 8**

Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.

Se GPMC non è abilitato o non è installato nel sistema, il programma di installazione blocca le installazioni.

Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.

Se GPMC non è abilitato o non è installato nel sistema, il programma di installazione blocca le installazioni.

**Windows Server 2012**

Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.

Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.

Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.

Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.

 

## Argomenti correlati


[Gestione avanzata Criteri di gruppo](index.md)

[Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





