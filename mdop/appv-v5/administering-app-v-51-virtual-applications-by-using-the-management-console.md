---
title: Amministrazione delle applicazioni virtuali App-V 5.1 usando la console di gestione
description: Amministrazione delle applicazioni virtuali App-V 5.1 usando la console di gestione
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806046"
---
# Amministrazione delle applicazioni virtuali App-V 5.1 usando la console di gestione


Usare il server di gestione di Microsoft Application Virtualization (App-V) 5,1 per gestire i pacchetti, i gruppi di connessioni e l'accesso ai pacchetti nell'ambiente. Il server pubblica le icone delle applicazioni, i collegamenti e le associazioni di tipi di file nei computer autorizzati che eseguono il client App-V 5,1. Uno o più server di gestione condividono in genere un archivio dati comune per le informazioni di configurazione e pacchetto.

Il server di gestione usa i gruppi di servizi di dominio Active Directory (AD DS) per gestire l'autorizzazione degli utenti e ha installato SQL Server per gestire il database e l'archivio dati.

Poiché i server di gestione applicano il flusso delle applicazioni agli utenti finali su richiesta, questi server sono ideali per le configurazioni di sistema con LAN affidabili e a larghezza di banda elevata. Il server di gestione è costituito dai componenti seguenti:

-   Server di gestione: usare il server di gestione per gestire i pacchetti e i gruppi di connessioni.

-   Server di pubblicazione: usare il server di pubblicazione per distribuire i pacchetti in computer che eseguono il client App-V 5,1.

-   Database di gestione: usare il database di gestione per gestire l'accesso al pacchetto e pubblicare la sincronizzazione del server con il server di gestione.

## Attività della console di gestione


Le attività più comuni che è possibile eseguire con la console di gestione di App-V 5,1 sono le seguenti:

-   [Come connettersi alla console di gestione](how-to-connect-to-the-management-console-51.md)

-   [Come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [Come configurare l'accesso ai pacchetti tramite la console di gestione](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [Come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [Come eliminare un pacchetto nella console di gestione](how-to-delete-a-package-in-the-management-console-51.md)

-   [Come aggiungere o rimuovere un amministratore tramite la console di gestione](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [Come trasferire l'accesso e le configurazioni a un'altra versione di un pacchetto con la console di gestione](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [Come visualizzare e configurare applicazioni ed estensioni delle applicazioni virtuali predefinite tramite la console di gestione](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

Gli elementi principali della console di gestione di App-V 5,1 sono i seguenti:

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
<td align="left"><p>Scheda pacchetti</p></td>
<td align="left"><p>Usare la <strong> </strong> scheda pacchetti per aggiungere o aggiornare i pacchetti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda gruppi di connessioni</p></td>
<td align="left"><p>Usare la <strong> scheda gruppi </strong> di connessioni per gestire i gruppi di connessioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scheda Server</p></td>
<td align="left"><p>Usare la <strong> </strong> scheda Server per registrare un nuovo server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda amministratori</p></td>
<td align="left"><p>Usare la <strong> </strong> scheda amministratori per registrare, aggiungere o rimuovere gli amministratori nell'ambiente App-V 5,1.</p></td>
</tr>
</tbody>
</table>

 

**Importante**  JavaScript deve essere abilitato nel browser che apre la console di gestione Web.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>Altre risorse per questa implementazione di App-V 5,1


-   [Guida dell'amministratore di Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





