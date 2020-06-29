---
title: Opzioni della riga di comando per i file di installazione MED-V
description: Opzioni della riga di comando per i file di installazione MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826466"
---
# Opzioni della riga di comando per i file di installazione MED-V


Quando si installa o si disinstalla Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, è possibile eseguire i file di installazione al prompt dei comandi. Questa sezione descrive diverse opzioni che è possibile specificare quando si installa o si disinstalla MED-V al prompt dei comandi.

### Argomenti della riga di comando

Puoi usare gli argomenti della riga di comando seguenti insieme ai rispettivi file di installazione di MED-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File di installazione</th>
<th align="left">Argomento</th>
<th align="left">Valori accettati</th>
<th align="left">Tipo</th>
<th align="left">Descrizione</th>
<th align="left">Default</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Agente host</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;percorso di installazione&gt;</p></td>
<td align="left"><p>Installazione</p></td>
<td align="left"><p>Modificare la directory installata</p></td>
<td align="left"><p>L'installazione passa a Programmi\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Packager area di lavoro MED-V</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;percorso di installazione&gt;</p></td>
<td align="left"><p>Installazione</p></td>
<td align="left"><p>Modificare la directory installata</p></td>
<td align="left"><p>L'installazione passa a Programmi\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Area di lavoro MED-V</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;percorso di installazione&gt;</p></td>
<td align="left"><p>Installazione</p></td>
<td align="left"><p>Modificare la directory installata</p></td>
<td align="left"><p>L'installazione passa a ProgramData\Microsoft\Medv\Workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Area di lavoro MED-V</p></td>
<td align="left"><p>SOVRASCRIVERE VHD</p></td>
<td align="left"><p>0 o 1</p></td>
<td align="left"><p>Installazione</p></td>
<td align="left"><p>Errore di installazione se il VHD esiste (0) o sovrascrive il VHD esistente (1).</p></td>
<td align="left"><p>La sovrascrittura non si verifica e l'installazione non riesce se esiste già un disco rigido virtuale (VHD).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Area di lavoro MED-V</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0 o 1</p></td>
<td align="left"><p>Installazione</p></td>
<td align="left"><p>Avviare (0) o non avviare (1) MED-V dopo l'installazione dell'area di lavoro MED-V.</p></td>
<td align="left"><p>Se l'area di lavoro MED-V è stata installata con l'interfaccia utente, una casella di controllo nella <strong> </strong> pagina fine controlla se avviare MED-v.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Area di lavoro MED-V</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0 o 1</p></td>
<td align="left"><p>Disinstallazione</p></td>
<td align="left"><p>Mantieni (0) o Elimina (1) VHD creati da MED-V</p></td>
<td align="left"><p>Nessun VHD viene eliminato.</p></td>
</tr>
</tbody>
</table>

 

### Esempi di argomenti della riga di comando

Nell'esempio seguente viene installata l'area di lavoro MED-V creata dal Packager area di lavoro MED-V. Il file di installazione crea un file di log nella directory Temp ed esegue il file di installazione in modalità non interattiva, ma non avvia il completamento dell'agente host MED-V. Il file di installazione sovrascrive qualsiasi VHD lasciato da un'installazione precedente con lo stesso nome.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

Nell'esempio seguente viene disinstallata l'area di lavoro MED-V installata in precedenza. Il file di installazione crea un file di log nella directory Temp ed esegue il file di installazione in modalità non interattiva. Il file di installazione Elimina i file di disco rigido virtuali rimanenti dal file System.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## Argomenti correlati


[Distribuire i componenti MED-V](deploy-the-med-v-components.md)

[Documentazione tecnica su MED-V](technical-reference-for-med-v.md)

 

 





