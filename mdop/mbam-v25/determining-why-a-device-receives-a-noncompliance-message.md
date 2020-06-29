---
title: Determinare il motivo per cui un dispositivo riceve un messaggio di non conformità
description: Determinare il motivo per cui un dispositivo riceve un messaggio di non conformità
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824575"
---
# Determinare il motivo per cui un dispositivo riceve un messaggio di non conformità


I codici di nonconformità seguenti sono forniti da WMI e descrivono i motivi per cui un determinato dispositivo viene segnalato da MBAM come non conforme.

Puoi usare il metodo preferito per visualizzare WMI. Se si usa PowerShell, eseguire `gwmi -class mbam_volume -Namespace root\microsoft\mbam` da un prompt di PowerShell e cercare ReasonsForNoncompliance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Codice di non conformità</th>
<th align="left">Motivo della mancata conformità</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>0</p></td>
<td align="left"><p>Non crittografare l'AES 256.</p></td>
</tr>
<tr class="even">
<td align="left"><p>1</p></td>
<td align="left"><p>MBAM Policy richiede che il volume sia crittografato, ma non lo è.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>I criteri di MBAM richiedono che il volume non venga crittografato, ma lo è.</p></td>
</tr>
<tr class="even">
<td align="left"><p>3</p></td>
<td align="left"><p>I criteri di MBAM richiedono che questo volume usi un Protector TPM, ma non lo fa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4</p></td>
<td align="left"><p>I criteri di MBAM richiedono che questo volume usi un TPM + PIN Protector, ma non lo fa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>5</p></td>
<td align="left"><p>I criteri di MBAM non consentono di segnalare i computer non TPM come conformi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>6</p></td>
<td align="left"><p>Il volume include un Protector TPM, ma il TPM non è visibile (viene avviato con il tasto recupera dopo la disattivazione del TPM nel BIOS?).</p></td>
</tr>
<tr class="even">
<td align="left"><p>7</p></td>
<td align="left"><p>I criteri di MBAM richiedono che questo volume usi una password Protector, ma non ne ha una.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>8</p></td>
<td align="left"><p>I criteri di MBAM richiedono che il volume non usi una password Protector, ma ne abbia una.</p></td>
</tr>
<tr class="even">
<td align="left"><p>9</p></td>
<td align="left"><p>I criteri di MBAM richiedono che questo volume usi un Protector di sblocco automatico, ma non ne ha una.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>10</p></td>
<td align="left"><p>I criteri di MBAM richiedono che questo volume non usi un Protector di sblocco automatico, ma ne ha una.</p></td>
</tr>
<tr class="even">
<td align="left"><p>11</p></td>
<td align="left"><p>Conflitto di criteri rilevato impedendo a MBAM di segnalare il volume come conforme.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>È necessario un volume di sistema per crittografare il volume del sistema operativo, ma non è presente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>13</p></td>
<td align="left"><p>La protezione viene sospesa per il volume.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>14</p></td>
<td align="left"><p>Autounlock non sicuro a meno che il volume del sistema operativo non sia crittografato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>15</p></td>
<td align="left"><p>I criteri richiedono una forza di codifica minima è XTS-AES-128 bit, la forza di Cypher effettiva è più debole.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>I criteri richiedono una forza di codifica minima è XTS-AES-256 bit, la forza di Cypher effettiva è più debole.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Documentazione tecnica per MBAM 2.5](technical-reference-for-mbam-25.md)

[Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





