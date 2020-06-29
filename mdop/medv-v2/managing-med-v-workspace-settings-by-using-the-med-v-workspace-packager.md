---
title: Gestione delle impostazioni dell'area di lavoro MED-V con Packager nell'area di lavoro MED-V
description: Gestione delle impostazioni dell'area di lavoro MED-V con Packager nell'area di lavoro MED-V
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826125"
---
# Gestione delle impostazioni dell'area di lavoro MED-V con Packager nell'area di lavoro MED-V


Puoi usare Packager area di lavoro MED-V per gestire determinate impostazioni nell'area di lavoro MED-V.

**Per gestire le impostazioni in un'area di lavoro MED-V**

1. Per aprire **Packager area di lavoro MED-v**, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **Packager area di lavoro MED-v**.

2. Nel pannello principale di **Packager area di lavoro MED-V** fare clic su **Gestisci impostazioni**.

3. Nella finestra **Gestisci impostazioni** è possibile configurare le impostazioni dell'area di lavoro MED-V seguenti:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Avviare l'area di lavoro MED-V</strong></p></td>
   <td align="left"><p>Scegliere se avviare l'area di lavoro MED-V all'accesso dell'utente, al primo utilizzo o per consentire all'utente finale di decidere quando viene avviata l'area di lavoro MED-v.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>L'area di lavoro MED-V viene avviata in uno dei due modi seguenti: quando l'utente finale accede o quando esegue prima un'azione che richiede MED-V, ad esempio l'apertura di un'applicazione pubblicata o l'immissione di un URL che richiede il reindirizzamento.</p>
   <p>Puoi definire questa impostazione per l'utente finale o lasciare che l'utente finale controlli l'avvio di MED-V.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Se specifichi che l'utente finale decide, il comportamento predefinito che provano è che l'area di lavoro MED-V viene avviata quando si collegano. Possono modificare l'impostazione predefinita facendo clic con il pulsante destro del mouse sull'icona MED-V nell'area di notifica e selezionando <strong> impostazioni utente Med-v </strong> . Se si definisce questa impostazione per l'utente finale, non è possibile modificare il modo in cui viene avviato MED-V.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Reti</strong></p></td>
   <td align="left"><p>Selezionare <strong> condivisi </strong> o <strong> Bridged </strong> per l'impostazione di rete. Il valore predefinito è <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Condivisa </strong> - l'area di lavoro MED-V USA NAT (Network Address Translation) per condividere l'host&#39;s IP per il traffico in uscita.</p>
   <p><strong>Bridged </strong> - l'area di lavoro MED-V ha un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Credenziali dello Store</strong></p></td>
   <td align="left"><p>Scegliere se si desidera archiviare le credenziali dell'utente finale.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Il comportamento predefinito è che l'archiviazione delle credenziali è disabilitata in modo che l'utente finale debba essere autenticato ogni volta che accede.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Anche se la memorizzazione nella cache delle credenziali dell'utente finale offre la migliore esperienza utente, dovresti essere consapevole dei rischi.</p>
   <p>Le credenziali di dominio dell'utente finale sono archiviate in un formato reversibile in Gestione credenziali di Windows. Un utente malintenzionato può scrivere un programma che recupera la password e quindi accedere alle credenziali dell'utente. È possibile ridurre questo rischio solo disabilitando l'archiviazione delle credenziali degli utenti finali.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. Fare clic su **Salva con nome...** per salvare le impostazioni di configurazione aggiornate nella cartella specificata. MED-V crea un file del registro di sistema che contiene le impostazioni aggiornate. Distribuire il file del registro di sistema aggiornato usando criteri di gruppo. Per altre informazioni sull'uso dei criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V crea inoltre uno script di Windows PowerShell nella cartella specificata che è possibile usare per ricreare il file del registro di sistema aggiornato.

## Argomenti correlati


[Gestione delle impostazioni di configurazione dell'area di lavoro MED-V](managing-med-v-workspace-configuration-settings.md)

[Gestire le impostazioni dell'area di lavoro MED-V](manage-med-v-workspace-settings.md)









