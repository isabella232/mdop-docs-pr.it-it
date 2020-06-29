---
title: Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita
description: Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826445"
---
# Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita


Per modificare le informazioni di reindirizzamento degli URL in un'area di lavoro MED-V distribuita, è consigliabile aggiornare il registro di sistema tramite criteri di gruppo. Anche se non è consigliabile, è anche possibile ricostruire e ridistribuire l'area di lavoro MED-V con le informazioni aggiornate sul reindirizzamento degli URL.

La chiave del registro di sistema si trova in genere in:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

Deve essere presente il valore multistringa seguente: `RedirectUrls`

I dati del valore per `RedirectUrls` sono un elenco di tutti gli URL specificati per il reindirizzamento quando è stato compilato il pacchetto dell'area di lavoro MED-v tramite **Packager area di lavoro MED-v**. Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).

È possibile aggiungere e rimuovere informazioni sul reindirizzamento degli URL eseguendo una delle attività seguenti:

-   [Modificare la chiave del registro di sistema di reindirizzamento URL e distribuire tramite criteri di gruppo](#bkmk-editreg)

-   [Modificare il file di testo del reindirizzamento degli URL e ricostruire l'area di lavoro MED-V](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**Per aggiornare le informazioni sul reindirizzamento degli URL tramite criteri di gruppo**

1.  Modificare il valore multistringa della chiave del registro di sistema denominato `RedirectUrls` . Questo valore si trova in genere in:

    Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

    Se si aggiungono URL alla chiave del registro di sistema, immetterli uno per riga, come richiesto quando si è compilato il pacchetto dell'area di lavoro MED-V. Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).

2.  Distribuire la chiave del registro di sistema aggiornata usando criteri di gruppo. Per altre informazioni sull'uso dei criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

**Nota**  Questo metodo per modificare le informazioni sul reindirizzamento degli URL è una procedura consigliata per MED-V.

 

<a href="" id="bkmk-edittext"></a>**Per ricompilare l'area di lavoro MED-V usando un file di testo URL aggiornato**

-   Un altro metodo per l'aggiunta e la rimozione di URL dall'elenco di reindirizzamento consiste nell'aggiornare il file di testo del reindirizzamento degli URL e quindi usarlo per creare una nuova area di lavoro MED-V. Puoi quindi ridistribuire l'area di lavoro MED-V come prima, usando il processo standard di distribuzione, ad esempio un sistema ESD.

    **Importante**  Non è consigliabile questo metodo per modificare le informazioni di reindirizzamento degli URL. Inoltre, ogni volta che si ridistribuisce l'area di lavoro MED-V nell'organizzazione, è necessario eseguire di nuovo la configurazione per la prima volta e tutti i dati salvati nella macchina virtuale andranno perduti.

     

## Argomenti correlati


[Come verificare il reindirizzamento URL](how-to-test-url-redirection.md)

[Gestione delle applicazioni distribuite in aree di lavoro MED-V](managing-applications-deployed-to-med-v-workspaces.md)

[Creare un pacchetto nell'area di lavoro MED-V](create-a-med-v-workspace-package.md)

 

 





