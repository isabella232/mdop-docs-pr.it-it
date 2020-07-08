---
title: Cercare e filtrare l'elenco di oggetti Criteri di gruppo
description: Cercare e filtrare l'elenco di oggetti Criteri di gruppo
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820265"
---
# Cercare e filtrare l'elenco di oggetti Criteri di gruppo


In Advanced Group Policy Management è possibile eseguire una ricerca nell'elenco degli oggetti Criteri di gruppo e dei relativi attributi per filtrare l'elenco dei GPO visualizzati. Ad esempio, puoi cercare gli oggetti Criteri di ricerca con un nome, uno stato o un commento specifico. È anche possibile cercare gli oggetti Criteri di gruppo modificati per l'ultima volta da un determinato amministratore dei criteri di raggruppamento o in una data specifica.

## Esecuzione di una ricerca complessa


È possibile eseguire una ricerca complessa usando il formato *attributo GPO 1: stringa di ricerca 1 attributo GPO 2: stringa di ricerca 2... stringhe di ricerca in tutte le colonne*. La ricerca non fa distinzione tra maiuscole e minuscole.

-   **Attributo GPO:** Qualsiasi intestazione di colonna nell'elenco di GPO in Advanced Group Policy Management diverso da **versione computer** o **versione utente**. Gli attributi GPO includono il nome del GPO, lo stato, l'utente che ha modificato di recente il GPO, la data e l'ora in cui l'oggetto Criteri di stato è stato modificato più di recente, commento, stato GPO e filtro WMI applicato all'oggetto Criteri di stato.

-   **Stringa di ricerca:** Testo per cui eseguire la ricerca nella colonna specificata. Se una stringa include spazi, è necessario racchiuderla tra virgolette.

-   **Stringhe di ricerca in tutte le colonne:** Testo per il quale eseguire la ricerca in tutte le colonne dell'elenco di GPO in Advanced Group Policy Management diverse dalla versione **computer** e **dall'utente**. Puoi includere più stringhe separate da spazi. Se una stringa include spazi, è necessario racchiuderla tra virgolette.

Ogni coppia di attributi GPO e stringa di ricerca e ogni stringa di ricerca di tutte le colonne vengono combinati usando un'operazione logica e. Il risultato è un elenco di tutti gli oggetti Criteri di gruppo per cui ogni attributo specificato include la stringa di ricerca specificata e per cui tutte le stringhe di ricerca di tutte le colonne vengono visualizzate in almeno una colonna. La ricerca restituisce eventuali corrispondenze parziali per le stringhe, in modo che sia possibile immettere parte di un nome di oggetto o di un nome utente e visualizzare un elenco di tutti i GPO che includono il testo nel nome.

Di seguito sono riportati alcuni esempi di ricerche:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrizione del risultato della ricerca</th>
<th align="left">Query di ricerca</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tutti i GPO con nomi che includono la <strong> sicurezza del testo </strong> e il <strong> Nord America </strong> .</p></td>
<td align="left"><p><strong>Nome: </strong><strong> </strong><strong> nome sicurezza: </strong> &quot; <strong> Nord America</strong>&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tutti i GPO estratti.</p></td>
<td align="left"><p><strong>stato: </strong> &quot; <strong> Estratto</strong>&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tutti i GPO modificati di recente dall'utente <strong> Administrator </strong> e modificati di recente nel mese precedente.</p></td>
<td align="left"><p><strong>modificato da: </strong><strong> </strong><strong> modifica data amministratore: </strong><strong> lastmonth</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Tutti i GPO in cui <strong> </strong> è incluso il firewall di Word nel commento più recente e in cui la parola <strong> sicurezza </strong> viene visualizzata in qualsiasi colonna.</p></td>
<td align="left"><p><strong>Commento: </strong><strong> </strong><strong> sicurezza firewall</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tutti i GPO che hanno lo stato di <strong> tutte le impostazioni disabilitate </strong> .</p></td>
<td align="left"><p><strong>stato GPO: </strong><strong> tutto</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Tutti i GPO a cui è applicato un filtro WMI denominato <strong> filtro WMI </strong> e che hanno lo stato delle <strong> impostazioni di configurazione utente disabilitate </strong> .</p></td>
<td align="left"><p><strong>filtro WMI: </strong> &quot; <strong> </strong> &quot; <strong> stato GPO filtro WMI: </strong><strong> utente</strong></p></td>
</tr>
</tbody>
</table>

 

## Specifica delle date


È possibile cercare i GPO modificati in una data specifica, in un momento specifico o durante un periodo di tempo usando gli stessi termini speciali disponibili durante la ricerca in Windows. Se si immette una data o un'ora specifica, è necessario usare il formato usato nella colonna **Cambia data** . Di seguito sono riportati alcuni esempi di ricerche della colonna **Cambia data** :

-   **modifica data:****10/10/2009**

-   **modifica data:****10/10/2009 9:00:00 AM**

-   **modifica data:****ThisWeek**

Quando si esegue una ricerca nella colonna **modifica data** , è possibile usare i termini speciali seguenti, che non fanno distinzione tra maiuscole e minuscole:

-   **Today**

-   **Ieri**

-   **ThisWeek**

-   **LastWeek**

-   **ThisMonth**

-   **LastMonth**

-   **TwoMonths**

-   **ThreeMonths**

-   **ThisYear**

-   **LastYear**

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere l'autorizzazione **contenuto elenco** per il dominio.

-   Per altre informazioni sugli attributi degli oggetti Criteri di ricerca, vedere [caratteristiche della scheda Sommario](contents-tab-features-agpm40.md).

### Riferimenti aggiuntivi

-   [Gestione avanzata Criteri di gruppo 4.0](advanced-group-policy-management-40.md)

 

 





