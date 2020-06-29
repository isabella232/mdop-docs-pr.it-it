---
title: Monitoraggio delle distribuzioni nell'area di lavoro MED-V
description: Monitoraggio delle distribuzioni nell'area di lavoro MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827215"
---
# Monitoraggio delle distribuzioni nell'area di lavoro MED-V


La funzionalità di monitoraggio in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di eseguire query su singole aree di lavoro MED-V per determinare se la configurazione per la prima volta è riuscita in tutta l'organizzazione dopo la distribuzione delle aree di lavoro MED-V. Il monitoraggio dell'esito positivo della configurazione iniziale è importante perché MED-V non è in uno stato utilizzabile finché la configurazione iniziale non è stata completata correttamente.

Questa sezione fornisce informazioni e istruzioni per aiutarti a monitorare l'esito positivo o negativo della configurazione per la prima volta.

## Per monitorare le distribuzioni dell'area di lavoro MED-V


La funzionalità di monitoraggio è costituita da un provider di Strumentazione gestione Windows (WMI) in-process che è possibile eseguire una query usando la lingua di query WMI per individuare lo stato della configurazione iniziale per tutti gli utenti finali in un'area di lavoro MED-V.

Il provider WMI viene implementato tramite il Framework di estensione del provider WMI da Microsoft .NET Framework 3,5. Il provider WMI viene eseguito nel contesto di LocalService e archivia la prima volta lo stato di installazione in modo sicuro in \\ProgramData.

Il provider WMI viene implementato nello spazio dei nomi **root\\microsoft\\medv** e implementa la classe **FTS \ _Status**, che espone il metodo **SetFtsState**. MED-V usa **SetFtsState** per impostare lo stato di configurazione per la prima volta.

La classe contiene le proprietà seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Computer</strong></p></td>
<td align="left"><p><strong>Proprietà di sola lettura </strong> che contiene il nome della macchina virtuale Guest a cui è stato eseguito il provisioning per la prima volta. Questa chiave contiene il nome che l'ospite avrebbe avuto in caso di errore di configurazione per la prima volta.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>StatusCode</strong></p></td>
<td align="left"><p><strong></strong>Proprietà di sola lettura che contiene zero se la configurazione per la prima volta è riuscita. Qualsiasi altro valore restituito è uguale all'ID evento dell'errore registrato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Tempo</strong></p></td>
<td align="left"><p>Ora UTC che è stata completata la configurazione per la prima volta.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Utente</strong></p></td>
<td align="left"><p>L'utente per cui è stata eseguita la configurazione per la prima volta.</p></td>
</tr>
</tbody>
</table>

 

Il codice seguente mostra il file MOF (Managed Object Format) che definisce la classe **FTS \ _Status** .

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

Poiché la preoccupazione principale è molto probabile che le aree di lavoro MED-V per cui la configurazione per la prima volta non è stata completata correttamente, è possibile scrivere la query in modo che restituiscano solo quelli non riusciti per la prima volta, ad esempio:

``` syntax
Select * from FTS_Status where StatusCode != 0
```

In questo caso, la caratteristica di monitoraggio restituisce un elenco delle aree di lavoro MED-V che non sono state eseguite per la prima volta, che è possibile usare per eseguire le azioni appropriate per risolvere l'errore.

## Argomenti correlati


[Monitorare le aree di lavoro MED-V](monitor-med-v-workspaces.md)

[Come verificare le impostazioni della prima configurazione](how-to-verify-first-time-setup-settings.md)

 

 





