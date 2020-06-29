---
title: Amministrazione delle applicazioni virtuali App-V 5.0 usando la console di gestione
description: Amministrazione delle applicazioni virtuali App-V 5.0 usando la console di gestione
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806051"
---
# Amministrazione delle applicazioni virtuali App-V 5.0 usando la console di gestione


Usare il server di gestione di Microsoft Application Virtualization (App-V) 5,0 per gestire i pacchetti, i gruppi di connessioni e l'accesso ai pacchetti nell'ambiente. Il server pubblica le icone delle applicazioni, i collegamenti e le associazioni di tipi di file nei computer autorizzati che eseguono il client App-V 5,0. Uno o più server di gestione condividono in genere un archivio dati comune per le informazioni di configurazione e pacchetto.

Il server di gestione usa i gruppi di servizi di dominio Active Directory (AD DS) per gestire l'autorizzazione degli utenti e ha installato SQL Server per gestire il database e l'archivio dati.

Poiché i server di gestione applicano il flusso delle applicazioni agli utenti finali su richiesta, questi server sono ideali per le configurazioni di sistema con LAN affidabili e a larghezza di banda elevata. Il server di gestione è costituito dai componenti seguenti:

-   Server di gestione: usare il server di gestione per gestire i pacchetti e i gruppi di connessioni.

-   Server di pubblicazione: usare il server di pubblicazione per distribuire i pacchetti in computer che eseguono il client App-V 5,0.

-   Database di gestione: usare il database di gestione per gestire l'accesso al pacchetto e pubblicare la sincronizzazione del server con il server di gestione.

## Attività della console di gestione


Le attività più comuni che è possibile eseguire con la console di gestione di App-V 5,0 sono le seguenti:

-   [Come connettersi alla console di gestione](how-to-connect-to-the-management-console-beta.md)

-   [Come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [Come configurare l'accesso ai pacchetti tramite la console di gestione](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [Come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [Come eliminare un pacchetto nella console di gestione](how-to-delete-a-package-in-the-management-console-beta.md)

-   [Come aggiungere o rimuovere un amministratore tramite la console di gestione](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [Come trasferire l'accesso e le configurazioni a un'altra versione di un pacchetto con la console di gestione](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [Configurare le applicazioni e le estensioni delle applicazioni virtuali predefinite nel sistema di gestione](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

Gli elementi principali della console di gestione di App-V 5,0 sono i seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scheda console di gestione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Panoramica</p></td>
<td align="left"><p></p>
<ul>
<li><p><strong>App-V Sequencer </strong> - selezionare questa opzione per visualizzare informazioni generali sull'uso del sequencer App-v 5,0.</p></li>
<li><p><strong>Raccolta pacchetti applicazione </strong> : selezionare questa opzione per aprire la <strong> </strong> pagina pacchetti della console di gestione. Usare questa pagina per rivedere i pacchetti che sono stati aggiunti al server. È anche possibile gestire i gruppi di connessioni, nonché aggiungere o aggiornare i pacchetti.</p></li>
<li><p><strong>Server </strong> : selezionare questa opzione per aprire la <strong> </strong> pagina server della console di gestione. Usare questa pagina per esaminare l'elenco dei server registrati con l'infrastruttura dell'App-V 5,0.</p></li>
<li><p><strong>CLIENT </strong> : selezionare questa opzione per visualizzare informazioni generali sui client App-V 5,0.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda pacchetti</p></td>
<td align="left"><p>Usare la <strong> </strong> scheda pacchetti per aggiungere o aggiornare i pacchetti. È anche possibile gestire i gruppi di connessioni facendo clic su <strong> gruppi di connessioni </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scheda Server</p></td>
<td align="left"><p>Usare la <strong> </strong> scheda Server per registrare un nuovo server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda amministratori</p></td>
<td align="left"><p>Usare la <strong> </strong> scheda amministratori per registrare, aggiungere o rimuovere gli amministratori nell'ambiente App-V 5,0.</p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a>Altre risorse per questa implementazione di App-V 5,0


-   [Guida dell'amministratore di Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





