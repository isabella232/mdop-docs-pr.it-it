---
title: Informazioni sulle licenze dell'applicazione
description: Informazioni sulle licenze dell'applicazione
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820096"
---
# Informazioni sulle licenze dell'applicazione


È possibile gestire le licenze applicative direttamente dalla console di gestione del server Application Virtualization.

## Tipi di licenza


Il sistema di virtualizzazione delle applicazioni di System Center supporta attualmente i seguenti tipi di licenza:

-   **Licenza illimitata**: consente l'accesso all'applicazione in base a qualsiasi numero di utenti simultanei. Questo metodo di gestione delle licenze è appropriato quando si vuole associare una licenza a livello aziendale a un'applicazione.

-   **Licenza simultanea**: consente di definire il numero massimo di utenti simultanei autorizzati a usare l'applicazione.

-   **Licenza denominata**: consente di assegnare una licenza a un singolo utente. Una licenza denominata può essere usata per garantire che un determinato utente sia sempre in grado di eseguire l'applicazione.

Puoi combinare licenze simultanee e denominate per la stessa applicazione.

La gestione delle licenze è disabilitata per impostazione predefinita, ma è possibile abilitarla dalla scheda **Pipeline provider** della finestra di dialogo **Proprietà provider** . Per informazioni dettagliate sull'abilitazione e la disabilitazione delle licenze, vedere [come configurare o disabilitare le licenze](how-to-set-up-or-disable-application-licensing.md)per le applicazioni.

## Criteri per i provider


I criteri per il provider sono stati sviluppati per il modello ASP (Application Service Provider). In questo modello una singola app ASP può ospitare un singolo sistema di virtualizzazione delle applicazioni per più client, in cui ogni client deve rimanere isolato. I client potrebbero avere requisiti radicalmente diversi, ad esempio un client potrebbe richiedere l'autenticazione, mentre un altro non lo fa. Puoi usare i criteri del provider per associare le autorizzazioni ai client in modo che solo gli utenti approvati possano accedere a ogni applicazione virtuale o pacchetto di applicazione virtuale.

Per il cliente aziendale, è possibile usare questa funzionalità quando si hanno requisiti di licenza severi per una o più applicazioni. In questa situazione, il componente licenza è disabilitato nella scheda **Pipeline provider** della finestra di dialogo **Proprietà provider** .

La scheda **Pipeline provider** include anche le caselle di controllo per abilitare l'autenticazione, l'autorizzazione (**applicare le impostazioni di autorizzazione di accesso**) e la misurazione (**informazioni sull'utilizzo dei log**). Se la tua configurazione ha requisiti speciali, puoi scrivere i tuoi componenti della pipeline e aggiungerli al sistema facendo clic sul pulsante **Avanzate** .

## Autorità account


L'autorità account è il dominio in cui è installato l'Application Virtualization Server. Man mano che si procede con l'installazione del server, viene chiesto di specificare un nome di dominio; il dominio in cui è installato il computer viene rilevato e usato per impostazione predefinita. Quando gli utenti tentano di accedere al sistema, vengono richieste le credenziali prima di poter accedere a tale dominio.

Il sistema di virtualizzazione delle applicazioni supporta più domini. Se si stabilisce una relazione di trust tra domini, è possibile concedere l'accesso alle applicazioni ai gruppi di utenti in altri domini. Gli utenti devono fornire le credenziali riconosciute da ogni dominio.

Nella console di gestione di Application Virtualization Server è possibile modificare il dominio principale (autorità account) e le credenziali usate per accedervi.

## Autenticazione


L'autenticazione è il meccanismo usato per confermare l'identità di un utente. Qualsiasi utente con un nome utente e una password riconosciuti ha accesso.

Nel sistema di virtualizzazione dell'applicazione è possibile abilitare o disabilitare l'autenticazione tramite una casella di controllo nella scheda **Pipeline provider** . Per impostazione predefinita, l'autenticazione di Windows è abilitata.

## Autorizzazione


L'autorizzazione è il processo usato per confermare l'identità di un utente. Dopo aver confermato l'identità dell'utente, il sistema determina se l'utente ha concesso l'accesso al sistema e alle applicazioni a cui l'utente ha concesso l'accesso. La console di gestione di Application Virtualization Server include una casella di controllo **Applica impostazioni di autorizzazione di accesso** nella scheda **pipeline del provider** per abilitare o disabilitare l'autorizzazione.

Nel sistema di virtualizzazione dell'applicazione, l'accesso viene concesso solo a un gruppo di utenti, non a un singolo utente.

## Argomenti correlati


[Come gestire le licenze dell'applicazione in Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Come configurare o disabilitare le licenze dell'applicazione](how-to-set-up-or-disable-application-licensing.md)

[Server Management Console: Nodo Criteri dei provider](server-management-console-provider-policies-node.md)

 

 





