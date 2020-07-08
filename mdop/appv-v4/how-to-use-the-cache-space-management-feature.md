---
title: Come usare la funzionalità di gestione dello spazio della cache
description: Come usare la funzionalità di gestione dello spazio della cache
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816406"
---
# Come usare la funzionalità di gestione dello spazio della cache


La funzionalità di gestione dello spazio della cache di FileSystem usa un algoritmo LRU (least used) ed è abilitato per impostazione predefinita. Se lo spazio necessario per un nuovo pacchetto supererà lo spazio disponibile nella cache, il client di Application Virtualization (App-V) utilizzerà questa caratteristica per determinare i pacchetti esistenti che possono essere eliminati dalla cache per creare spazio per il nuovo pacchetto. Il client elimina il pacchetto con la data di accesso ultimo meno recente, se è precedente al valore specificato nel valore del registro di sistema MinPkgAge. L'uso della funzionalità di gestione dello spazio della cache di FileSystem può anche evitare problemi di spazio nella cache Bassi.

Se necessario, viene eliminato più di un pacchetto. I pacchetti bloccati non vengono eliminati.

**Nota**  Per assicurarti che la cache disponga di spazio sufficiente per tutti i pacchetti che potrebbero essere distribuiti, usa l'impostazione **USA soglia di spazio libero su disco** quando configuri il client in modo che la cache possa crescere in base alle esigenze. In alternativa, determinare in anticipo la quantità di spazio su disco necessaria per la cache di App-V e, al momento dell'installazione, impostare le dimensioni della cache di conseguenza.

 

La caratteristica di gestione dello spazio della cache è controllata dal valore del registro di sistema UnloadLeastRecentlyUsed. Il valore 1 Abilita la caratteristica e il valore 0 (zero) lo Disabilita.

**Per abilitare o disabilitare la funzionalità di gestione dello spazio della cache**

-   Imposta il valore del registro di sistema seguente su 1 per abilitare l'algoritmo LRU. Impostarla su 0 (zero) per disabilitare la caratteristica.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed

**Per controllare i pacchetti che possono essere eliminati**

-   Per determinare quando il pacchetto può essere selezionato per la disattivazione, imposta il valore del registro di sistema seguente per uguagliare il numero minimo di giorni che vuoi trascorrere dopo l'ultimo accesso al pacchetto. I pacchetti che sono stati usati più di recente non vengono eliminati.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge

    **Attenzione**  Il valore massimo per questa chiave del registro di sistema è 0x00011111. I valori più grandi impediscono il corretto funzionamento della funzionalità di gestione dello spazio della cache.

     

## Argomenti correlati


[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





