---
title: Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)
description: Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826916"
---
# Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)


Puoi gestire le impostazioni delle caratteristiche di alcune tecnologie MDOP (Microsoft Desktop Optimization Pack), ad esempio App-V, UE-V o MBAM, usando i modelli di criteri di gruppo, i file con estensione ADMX e adml. I modelli di criteri di gruppo di MDOP sono disponibili per il download in un file compresso autoestraente, raggruppato per tecnologia e versione.

## Modelli di criteri di gruppo di MDOP

**Come scaricare e distribuire i modelli di criteri di gruppo di MDOP**

1. Scaricare i [modelli di criteri di gruppo](https://www.microsoft.com/download/details.aspx?id=55531) più recenti di MDOP 

2. Espandere il file CAB scaricato eseguendo `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Warning**  
   Non estrarre i modelli direttamente nella directory di distribuzione di criteri di gruppo. In questo file vengono raggruppate più tecnologie e versioni.

3. Nella cartella estratta individuare il file Technology-Version. admx. Alcune tecnologie MDOP hanno più set di oggetti Criteri di gruppo. Ad esempio, MBAM include le impostazioni di gestione di MBAM e le impostazioni utente di mbam.

4. Individuare il file con estensione adml appropriato per lingua-impostazioni cultura (ovvero *en-US* per l'inglese-Stati Uniti).

5. Copiare i file con estensione ADMX e ADML in una cartella di definizione dei criteri. A seconda della posizione in cui vengono archiviati i modelli, è possibile configurare le impostazioni dei criteri di gruppo dal dispositivo locale o da qualsiasi computer del dominio.

   - **File locali:** Per configurare le impostazioni dei criteri di gruppo dal dispositivo locale, copiare i file dei modelli nei percorsi seguenti:

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

   - **Archivio centrale di dominio:** Per abilitare la configurazione delle impostazioni dei criteri di gruppo da un amministratore di criteri di gruppo da qualsiasi computer del dominio, copiare i file nelle posizioni seguenti del controller di dominio:

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
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;sysvol\domain\policies\PolicyDefinitions forte</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>File di lingua dei criteri di gruppo (con estensione adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;Strong &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>Ad esempio, il file specifico della lingua ADML in inglese USA verrà archiviato in%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
   </tr>
   </tbody>
   </table>

6. Modificare le impostazioni dei criteri di gruppo usando la console Gestione criteri di gruppo o Advanced Group Policy Management per configurare le impostazioni dei criteri di gruppo per la tecnologia MDOP.

### Criteri di gruppo di MDOP per tecnologia

Per altre informazioni sui criteri di gruppo di MDOP supportati, vedere la documentazione specifica relativa alla tecnologia.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tecnologia MDOP</th>
<th align="left">Bundle di versioni</th>
<th align="left">Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Application Virtualization (App-V)</strong></p></td>
<td align="left"><p>App-V 5,0 e App-V 5,0 Service Pack</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">Come modificare la configurazione del client App-V 5.0 usando il modello ADMX e Criteri di gruppo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>User Experience Virtualization (UE-V)</strong></p></td>
<td align="left"><p>UE-V 2,0 e UE-V 2,1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1,0 incluso 1,0 SP1</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">Configurazione di UE-V con oggetti Criteri di gruppo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Microsoft BitLocker Administration and Monitoring (MBAM)</strong></p></td>
<td align="left"><p>MBAM 2,5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2,0 incluso 2,0 SP1</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1,0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0</a></p></td>
</tr>
</tbody>
</table>

 

 

 





