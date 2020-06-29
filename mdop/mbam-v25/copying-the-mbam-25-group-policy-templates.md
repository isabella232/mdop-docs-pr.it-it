---
title: Copia dei modelli dei Criteri di gruppo di MBAM 2.5
description: Copia dei modelli dei Criteri di gruppo di MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825225"
---
# Copia dei modelli dei Criteri di gruppo di MBAM 2.5


Prima di distribuire l'installazione di MBAM client, è necessario scaricare i modelli di criteri di gruppo di MBAM, che contengono le impostazioni dei criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per crittografia unità BitLocker. Dopo aver scaricato i modelli, è possibile impostare le impostazioni di criteri di gruppo per l'implementazione in tutta l'organizzazione.

## Scaricare e distribuire i modelli di criteri di gruppo di MDOP


I modelli di criteri di gruppo di MDOP sono disponibili per il download in un file compresso autoestraente, raggruppato per tecnologia e versione.

**Come scaricare e distribuire i modelli di criteri di gruppo di MDOP**

1. Scaricare i modelli di criteri di gruppo di MDOP dai [modelli amministrativi di criteri di gruppo di Microsoft Desktop Optimization Pack](https://www.microsoft.com/download/details.aspx?id=55531).

2. Eseguire il file scaricato per estrarre le cartelle del modello.

   **Warning**  
   Non estrarre i modelli direttamente nella directory di distribuzione di criteri di gruppo. In questo file vengono raggruppate più tecnologie e versioni.



3. Nella cartella estratta individuare il file Technology-Version. admx. Alcune tecnologie MDOP hanno più set di oggetti Criteri di gruppo. Ad esempio, MBAM include le impostazioni di gestione di MBAM e le impostazioni utente di mbam.

4. Individuare il file con estensione adml appropriato per lingua-impostazioni cultura (ovvero, *en* per l'inglese-Stati Uniti).

5. Copiare i file con estensione ADMX e ADML in una cartella di definizione dei criteri. A seconda della posizione in cui vengono archiviati i modelli, è possibile configurare le impostazioni dei criteri di gruppo dal dispositivo locale o da qualsiasi computer del dominio.

   **File locali.** Per configurare le impostazioni dei criteri di gruppo dal dispositivo locale, copiare i file dei modelli nei percorsi seguenti:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo di file</th>
   <th align="left">Percorso del file</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Modello di criteri di gruppo (con estensione ADMX)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;PolicyDefinitions forte</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>File di lingua dei criteri di gruppo (con estensione adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;PolicyDefinitions forte</strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. Modificare le impostazioni dei criteri di gruppo usando la console Gestione criteri di gruppo o Advanced Group Policy Management per configurare le impostazioni dei criteri di gruppo per la tecnologia MDOP. Per altre informazioni, vedere [modificare le impostazioni dei criteri di gruppo di MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) .

   Per le descrizioni delle impostazioni dei criteri di gruppo, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).


## Argomenti correlati


[Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5](deploying-mbam-25-group-policy-objects.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






