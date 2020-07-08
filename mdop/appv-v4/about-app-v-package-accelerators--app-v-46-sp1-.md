---
title: Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)
description: Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820095"
---
# Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)


Puoi usare gli acceleratori del pacchetto App-V per sequenziare automaticamente le applicazioni di grandi dimensioni e complesse. Inoltre, quando applichi un Acceleratore pacchetto App-V, non devi sempre installare manualmente un'applicazione per creare il pacchetto di applicazione virtuale.

**Nota**  In alcuni casi viene richiesto di installare un'applicazione localmente nel computer che esegue App-V Sequencer prima di poter usare l'Acceleratore pacchetto. Per installare un'applicazione, è necessario installare l'applicazione nella posizione predefinita dell'applicazione. Questa installazione non viene monitorata da App-V Sequencer. Quando viene creato l'Acceleratore pacchetto App-V, l'autore dell'acceleratore del pacchetto determina se installare un'applicazione localmente è obbligatorio.

 

App-V Sequencer estrae i file necessari dall'acceleratore del pacchetto App-V e dal supporto di installazione associato per creare un pacchetto virtuale senza dover monitorare l'installazione dell'applicazione.

**Importante**  Dichiarazione di non responsabilità: Microsoft Application Virtualization Sequencer non offre alcun diritto di licenza per l'applicazione software in uso per creare un Acceleratore pacchetto. È necessario rispettare tutte le condizioni di licenza per l'utente finale per tale applicazione. È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando Application Virtualization Sequencer.

 

Gli acceleratori del pacchetto App-V e i modelli di progetto sono diversi tra loro. Gli acceleratori pacchetto sono specifici dell'applicazione. I modelli di progetto consentono agli utenti di salvare le impostazioni di uso comune specifiche di un'organizzazione e di applicarle a più applicazioni. È anche possibile creare modelli di progetto al prompt dei comandi, mentre al contrario è necessario usare la console App-V Sequencer per creare acceleratori di pacchetti. Inoltre, la creazione di un pacchetto tramite un Acceleratore pacchetto e l'applicazione di un modello di progetto non è supportata.

## Condivisione di acceleratori pacchetto App-V


In questa sezione vengono fornite informazioni sulle procedure consigliate su come condividere gli acceleratori di pacchetto. Se si prevede di condividere gli acceleratori di pacchetto, le informazioni come i nomi di computer, le informazioni sugli account utente e le informazioni sulle applicazioni associate potrebbero essere incluse negli acceleratori del pacchetto. l'elenco seguente descrive i metodi da tenere in considerazione durante la creazione di acceleratori di pacchetti:

-   **Nome utente**. Quando si accede al computer in cui è in uso App-V Sequencer, è necessario usare un account utente generico, ad esempio l'account di **amministratore** predefinito per l'amministrazione del computer o del dominio. Non usare un account basato su un nome utente esistente.

-   **Nome computer**. Specificare un nome generale non Identificativo per il computer che ha eseguito il sequencer.

-   **URL del server**. Nella scheda **distribuzione** della console sequencer usare le impostazioni predefinite per le informazioni di configurazione dell'URL del server.

-   **Applicazioni**. Se non si vuole condividere l'elenco delle applicazioni installate nel computer che esegue il sequencer quando è stato creato l'acceleratore del pacchetto, è necessario eliminare il file **appv\_manifest.xml** . Questo file si trova nella directory radice del pacchetto del pacchetto di applicazione virtuale.

Dovresti anche rivedere le impostazioni o i file di configurazione associati al pacchetto di applicazione virtuale per assicurarti che le applicazioni non contengano informazioni personali.

## Protezione degli acceleratori del pacchetto App-V


Salva sempre gli acceleratori del pacchetto App-V e tutti i supporti di installazione associati in un percorso sicuro della rete per proteggere gli acceleratori del pacchetto App-V e i file di installazione da manomessi o danneggiati. Dato che gli acceleratori pacchetto possono anche contenere password e informazioni specifiche dell'utente, è necessario salvare gli acceleratori del pacchetto App-V in una posizione sicura ed è necessario firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'acceleratore del pacchetto. Per altre informazioni sulle firme digitali, vedere [linee guida per le procedure per la firma digitale per la sicurezza dei criteri comuni](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .

## Argomenti correlati


[Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[Come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (App-V 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





