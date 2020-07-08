---
title: Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0
description: Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826636"
---
# Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0


La distribuzione di Microsoft User Experience Virtualization (UE-V) richiede una posizione di archiviazione delle impostazioni in cui le impostazioni utente sono archiviate in un file di pacchetto di impostazioni. La posizione di archiviazione delle impostazioni può essere configurata in uno dei due modi seguenti:

-   **Directory Home di Active Directory** : se è definita una directory Home per l'utente in Active Directory, l'agente UE-V utilizzerà questa posizione per archiviare i pacchetti della posizione delle impostazioni. L'agente UE-V crea dinamicamente la cartella di archiviazione specifica dell'utente sotto la radice della Home Directory. L'agente usa solo la home directory di Active Directory se una posizione di archiviazione delle impostazioni non è definita.

-   **Creare una condivisione di archiviazione delle impostazioni** : la condivisione di archiviazione delle impostazioni è una condivisione di rete standard accessibile dagli utenti di UE-V.

## Distribuire una condivisione di archiviazione delle impostazioni di UE-V


Quando si crea la condivisione di archiviazione delle impostazioni, è consigliabile limitare l'accesso solo agli utenti che hanno bisogno di Access. Le autorizzazioni necessarie sono visualizzate nelle tabelle seguenti.

**Per distribuire la condivisione di rete UE-V**

1.  Creare un nuovo gruppo di sicurezza per gli utenti di UE-V.

2.  Creare una nuova cartella nel computer situato in posizione centrale in cui verranno archiviati i pacchetti di impostazioni di UE-V e quindi concedere agli utenti di UE-V le autorizzazioni di gruppo per la cartella. L'amministratore che supporta la versione UE-V dovrà disporre delle autorizzazioni per questa cartella condivisa.

3.  Impostare le seguenti autorizzazioni SMB (share-level) per la cartella della posizione di archiviazione dell'impostazione:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Account utente</strong></th>
    <th align="left"><strong>Autorizzazioni consigliate</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tutti</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Gruppo di sicurezza degli utenti di UE-V</p></td>
    <td align="left"><p>Controllo completo</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Impostare le autorizzazioni NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Account utente</strong></th>
    <th align="left"><strong>Autorizzazioni consigliate</strong></th>
    <th align="left"><strong>Cartella</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creatore/proprietario</p></td>
    <td align="left"><p>Controllo completo</p></td>
    <td align="left"><p>Solo sottocartelle e file</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Gruppo di sicurezza degli utenti di UE-V</p></td>
    <td align="left"><p>Cartella di elenco/dati letti, creare cartelle/accodare dati</p></td>
    <td align="left"><p>Solo questa cartella</p></td>
    </tr>
    </tbody>
    </table>

     

5.  Fare clic su **OK** per chiudere le finestre di dialogo.

Questa configurazione delle autorizzazioni consente agli utenti di creare cartelle per l'archiviazione delle impostazioni. L'agente UE-V crea e protegge una `settingspackage` cartella durante l'esecuzione nel contesto dell'utente. L'utente riceve il controllo completo nella `settingspackage` cartella. Altri utenti non ereditano l'accesso alla cartella. Non è necessario creare e proteggere singole directory utente, perché questa operazione verrà eseguita automaticamente dall'agente che viene eseguito nel contesto dell'utente.

**Nota**  La sicurezza aggiuntiva può essere configurata quando viene usato un server Windows per la condivisione di archiviazione delle impostazioni. L'opzione UE-V può essere configurata per verificare che il gruppo di amministratori locali o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni. Per abilitare la sicurezza aggiuntiva, completare le operazioni seguenti:

1.  Aggiungere una chiave del registro di sistema **reg \ _DWORD** denominata "RepositoryOwnerCheckEnabled" a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**

2.  Impostare il valore della chiave del registro di sistema su 1.

 

## Argomenti correlati


[Distribuzione di UE-V 1.0](deploying-ue-v-10.md)

[Configurazioni supportate per UE-V 1.0](supported-configurations-for-ue-v-10.md)

Distribuire lo spazio di archiviazione centrale per i modelli di impostazioni e le impostazioni di virtualizzazione dell'esperienza utente [installazione del generatore UE-V](installing-the-ue-v-generator.md)

[Distribuzione dell'agente di UE-V](deploying-the-ue-v-agent.md)

 

 





