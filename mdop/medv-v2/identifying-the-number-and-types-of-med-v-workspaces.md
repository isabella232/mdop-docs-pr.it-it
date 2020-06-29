---
title: Identificazione del numero e dei tipi di aree di lavoro MED-V
description: Identificazione del numero e dei tipi di aree di lavoro MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827265"
---
# Identificazione del numero e dei tipi di aree di lavoro MED-V


MED-V crea un ambiente virtuale per l'esecuzione di applicazioni che richiedono Windows XP o che richiedono una versione di Internet Explorer diversa dalla versione nel computer host. Questo ambiente virtuale è noto come area di lavoro MED-V.

A seconda dei requisiti di compatibilità delle applicazioni incontrati dall'organizzazione mentre si esegue la migrazione a Windows 7, solo determinati utenti o reparti potrebbero richiedere aree di lavoro MED-V. Quando si pianifica la distribuzione, è necessario determinare il numero di aree di lavoro MED-V necessarie nell'organizzazione. È inoltre necessario definire i requisiti di ogni area di lavoro MED-V.

## Identificare il numero e i tipi di aree di lavoro MED-V


Identificare i computer e i gruppi dell'organizzazione per i quali verranno create aree di lavoro MED-V. In genere, questi sono gli utenti che richiedono l'accesso alle applicazioni di cui non è possibile eseguire la migrazione in Windows 7. Identificare le applicazioni di cui non è possibile eseguire la migrazione e gli utenti che necessitano di un'area di lavoro MED-V per eseguire queste applicazioni.

Potresti anche avere indirizzi Intranet che non sono ancora stati ottimizzati per Windows 7. L'area di lavoro MED-V offre un browser Internet Explorer in cui gli utenti finali possono accedere meglio agli indirizzi Web non ancora pronti per la migrazione a Windows 7. Durante la preparazione e la pianificazione della distribuzione di MED-V, sarà necessario identificare e compilare un elenco degli indirizzi URL da reindirizzare da Internet Explorer nel computer host a Internet Explorer nell'area di lavoro MED-V.

Infine, è necessario valutare i requisiti di spazio su disco. La maggior parte delle aree di lavoro MED-V è di 2 gigabyte (GB) o più grande. Lo spazio disponibile su disco in un sistema può essere consumato rapidamente, a seconda del numero di utenti e della configurazione di MED-V. Inoltre, il metodo di distribuzione preferito della società può richiedere spazio aggiuntivo. In genere, è consigliabile liberare un minimo di 10 GB di spazio su disco per un'area di lavoro MED-V, ma questo è molto diverso, a seconda delle dimensioni dell'immagine.

### Calcolare i requisiti di spazio su disco per le aree di lavoro MED-V

Un'area di lavoro MED-V richiede memoria e spazio su disco dal computer host in cui è installato. Nell'host è necessario un minimo di 2 GB di spazio su disco. Lo spazio su disco è variabile e dipende dal numero di applicazioni e dai dati nell'area di lavoro MED-V di un utente.

È consigliabile un minimo di 10 GB di spazio su disco per MED-V. Questo importo consente l'utilizzo di un'area di lavoro di base di Windows XP e alcune applicazioni e il reindirizzamento Web installati di base. Offre anche spazio disponibile per l'unità di scambio host. In una configurazione di base, MED-V e una singola area di lavoro MED-V distribuita consumano fino a 6-8 GB. Se si includono molte applicazioni nell'area di lavoro MED-V o si hanno più utenti per computer, è possibile usare il calcolo seguente per determinare in modo più accurato lo spazio su disco richiesto dall'area di lavoro MED-V:

*VHD di base + (utente per computer x (differenza di disco + stato salvato))*

Per calcolare lo spazio su disco richiesto, determinare quanto segue:

-   **Dimensioni del VHD di base** : il disco rigido virtuale usato per creare l'area di lavoro MED-V.

    **Importante**  Non usare la dimensione del file con estensione MEDV per il calcolo perché il file con estensione MEDV è compresso.

     

-   **Utenti per computer** : Med-v crea un'area di lavoro MED-v per ogni utente in un computer; l'area di lavoro MED-V usa lo spazio su disco quando ogni utente accede e viene creata l'area di lavoro MED-V.

-   **Dimensioni del disco differenze** , usato per tenere traccia della differenza dal VHD di base. Questa dimensione varia man mano che si aggiungono applicazioni e aggiornamenti software al disco rigido virtuale. Viene creato un disco differenze per ogni utente MED-V quando avviano MED-V per la prima volta.

-   **Dimensioni del file di stato salvato** , usato per mantenere lo stato nella macchina virtuale. In genere, questo è solo un po' più grande della RAM allocata per la macchina virtuale. Ad esempio, 1 GB di RAM allocata crea un file di 1.081.000 KB.

L'esempio seguente mostra un calcolo basato su tre utenti di un'area di lavoro MED-V con un disco rigido virtuale di 2,6 GB:

*2.6 GB + (3 x (1.5 GB + 1GB)) = 10.1 GB*

**Nota**  Una procedura consigliata per MED-V consiste nel calcolare lo spazio richiesto usando una distribuzione di Lab per convalidare i requisiti.

 

### Individuare i file per determinare le dimensioni del file

Le posizioni seguenti contengono i file per il computer e le impostazioni utente:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo</th>
<th align="left">Posizione</th>
<th align="left">File</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>VHD di base</p></td>
<td align="left"><p>%ProgramData%\Microsoft\Medv\Workspace</p></td>
<td align="left"><p><em>InternalName </em> . vhd-Where <em> internalname </em> è il nome del disco rigido virtuale selezionato nel Packager area di lavoro MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Disco differenze</p></td>
<td align="left"><p>Macchine%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>Workspacename </em> . vhd</p></td>
</tr>
<tr class="odd">
<td align="left"><p>File di stato salvato</p></td>
<td align="left"><p>Macchine%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>Workspacename </em> . VSV</p></td>
</tr>
</tbody>
</table>

 

### Calcolare i requisiti di spazio su disco per le aree di lavoro MED-V condivise

Se si sta calcolando la distribuzione di un'area di lavoro MED-V condivisa in un singolo computer, il numero di utenti per computer nel calcolo è sempre "1" perché MED-V configura solo un singolo disco differenze per tutti gli utenti.

È possibile trovare il disco differenze e il file di stato salvato per le aree di lavoro MED-V condivise in%ProgramData%\\Microsoft\\Medv\\AllUsers.

## Argomenti correlati


[Definire e pianificare la distribuzione di MED-V](define-and-plan-your-med-v-deployment.md)

[Pianificazione di MED-V](planning-for-med-v.md)

 

 





