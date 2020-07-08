---
title: Configurare le applicazioni e le estensioni delle applicazioni virtuali predefinite nel sistema di gestione
description: Come visualizzare e configurare applicazioni ed estensioni delle applicazioni virtuali predefinite tramite la console di gestione
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805926"
---
#   Configurare le applicazioni e le estensioni delle applicazioni virtuali predefinite nel sistema di gestione

Usare la procedura seguente per *visualizzare* e *configurare* le estensioni predefinite del pacchetto.

**Per visualizzare e configurare le estensioni delle applicazioni virtuali predefinite**

1.  Per visualizzare il pacchetto che si vuole configurare, aprire la console di gestione di App-V 5,1. Selezionare il pacchetto che si desidera configurare, fare clic con il pulsante destro del mouse sul nome del pacchetto e scegliere **modifica configurazione predefinita**.

2.  Per visualizzare le applicazioni contenute nel pacchetto specificato, nel riquadro **configurazione predefinita** fare clic su **applicazioni**. Per visualizzare i tasti di scelta rapida per il pacchetto, fare clic su **scelte rapide**. Per visualizzare le associazioni dei tipi di file per il pacchetto, fare clic su **tipi di file**.

3.  Per abilitare le estensioni dell'applicazione, selezionare **Abilita**.

    Per abilitare i tasti di scelta rapida, selezionare **attiva collegamenti**. Per aggiungere un nuovo collegamento per l'applicazione selezionata, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Aggiungi nuovo collegamento**. Per rimuovere un collegamento, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Rimuovi collegamento**. Per modificare un collegamento esistente, fare clic con il pulsante destro del mouse sull'applicazione e scegliere **Modifica collegamento**.

4.  Per visualizzare le altre estensioni dell'applicazione, fare clic su **Avanzate** e quindi su **Esporta configurazione**. Digitare un nome di file e fare clic su **Salva**. Puoi visualizzare tutte le estensioni dell'applicazione associate al pacchetto usando il file di configurazione.

5.  Per modificare altre estensioni dell'applicazione, modificare il file di configurazione e fare clic su **Importa e Sovrascrivi questa configurazione**. Selezionare il file modificato e fare clic su **Apri**. Nella finestra di dialogo fare clic su **Sovrascrivi** per completare il processo.

>**Nota** Se il caricamento non riesce e le dimensioni del file di configurazione sono superiori a 4 MB, sarà necessario aumentare le dimensioni massime dei file consentite dal server. Questa operazione può essere eseguita aggiungendo l'attributo maxRequestLength con un valore maggiore della dimensione del file di configurazione (in KB) all'elemento httpRuntime sulla linea 26 di `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .  
Ad esempio, la modifica in modo da `<httpRuntime targetFramework="4.5"/>` `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` aumentare la dimensione massima a 8MB


**Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





