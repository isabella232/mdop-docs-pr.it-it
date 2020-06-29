---
title: Come distribuire il server App-V 5.1
description: Come distribuire il server App-V 5.1
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805499"
---
# Come distribuire il server App-V 5.1


Usare la procedura seguente per installare il server Microsoft Application Virtualization (App-V) 5,1. Per informazioni sulla distribuzione del server App-V 5,1, vedere [informazioni su App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).

**Prima di iniziare:**

-   Verificare di aver installato il software prerequisito. Vedere [prerequisiti di App-V 5,1](app-v-51-prerequisites.md).

-   Esaminare la sezione server delle [considerazioni sulla sicurezza di App-V 5,1](app-v-51-security-considerations.md).

-   Specificare una porta in cui verranno ospitati tutti i componenti.

-   Aggiungere regole del firewall per consentire alle richieste in arrivo di accedere alle porte specificate.

-   Se si usano script SQL, invece di Windows Installer, per configurare il database di gestione o il database di report, è necessario eseguire gli script SQL prima di installare il server di gestione o il server di report. Informazioni [su come distribuire i database di App-V usando gli script SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).

**Per installare il server App-V 5,1**

1. Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo.

2. Avviare l'installazione del server App-V 5,1 facendo clic con il pulsante destro del mouse e eseguendo **appv\_server\_setup.exe** come amministratore e quindi fare clic su **Installa**.

3. Rivedere e accettare le condizioni di licenza e scegliere se abilitare gli aggiornamenti Microsoft.

4. Nella pagina **Selezione funzionalità** selezionare tutti i componenti seguenti.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Componente</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Server di gestione</p></td>
   <td align="left"><p>Offre funzionalità di gestione complessive per l'infrastruttura App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Database di gestione</p></td>
   <td align="left"><p>Facilita le predistribuzioni di database per la gestione di App-V.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Server di pubblicazione</p></td>
   <td align="left"><p>Offre funzionalità di hosting e flusso per le applicazioni virtuali.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Server di report</p></td>
   <td align="left"><p>Fornisce l'App-V 5,1 Reporting Services.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Database di report</p></td>
   <td align="left"><p>Facilita le predistribuzioni di database per i report di App-V.</p></td>
   </tr>
   </tbody>
   </table>

     

5. Nella pagina **posizione di installazione** accettare il percorso predefinito in cui verranno installati i componenti selezionati oppure modificare la posizione digitando un nuovo percorso nella riga del **percorso di installazione** .

6. Nella pagina iniziale **Crea nuovo database di gestione** configurare l' **istanza di Microsoft SQL Server** e il database del server di **gestione** selezionando l'opzione appropriata di seguito.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Metodo</th>
   <th align="left">Cosa è necessario fare</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Si usa un'istanza di Microsoft SQL Server personalizzata.</p></td>
   <td align="left"><p>Selezionare <strong> Usa l'istanza personalizzata </strong> e digitare il nome dell'istanza.</p>
   <p>Usare il formato <strong> InstanceName </strong> . Il percorso di installazione presupposto è il computer locale.</p>
   <p>Non supportato: nome di un server che usa <strong> l' </strong> &lt; istanza Strong di format servername &gt; </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Si usa un nome di database personalizzato.</p></td>
   <td align="left"><p>Selezionare <strong> configurazione personalizzata </strong> e digitare il nome del database.</p>
   <p>Il nome del database deve essere univoco oppure l'installazione avrà esito negativo.</p></td>
   </tr>
   </tbody>
   </table>

     

7. Nella pagina **Configura** accettare il valore predefinito **usare questo computer locale**.

   **Nota**  
   Se si sta installando il server di gestione e il database di gestione affiancati, alcune opzioni in questa pagina non sono disponibili. In questo caso, le opzioni appropriate sono selezionate per impostazione predefinita e non possono essere modificate.

     

8. Nella pagina iniziale **Crea nuovo database di report** configurare l' **istanza di Microsoft SQL Server** e il database del server di **Reporting** selezionando l'opzione appropriata di seguito.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Metodo</th>
   <th align="left">Cosa è necessario fare</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Si usa un'istanza di Microsoft SQL Server personalizzata.</p></td>
   <td align="left"><p>Selezionare <strong> Usa l'istanza personalizzata </strong> e digitare il nome dell'istanza.</p>
   <p>Usare il formato <strong> InstanceName </strong> . Il percorso di installazione presupposto è il computer locale.</p>
   <p>Non supportato: nome di un server che usa <strong> l' </strong> &lt; istanza Strong di format servername &gt; </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Si usa un nome di database personalizzato.</p></td>
   <td align="left"><p>Selezionare <strong> configurazione personalizzata </strong> e digitare il nome del database.</p>
   <p>Il nome del database deve essere univoco oppure l'installazione avrà esito negativo.</p></td>
   </tr>
   </tbody>
   </table>

     

9. Nella pagina **Configura** accettare il valore predefinito: **usare questo computer locale**.

   **Nota**  
   Se si sta installando il server di gestione e il database di gestione affiancati, alcune opzioni in questa pagina non sono disponibili. In questo caso, le opzioni appropriate sono selezionate per impostazione predefinita e non possono essere modificate.

     

10. Nella pagina **Configura** (Management Server Configuration) specificare quanto segue:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Elemento da configurare</th>
    <th align="left">Descrizione ed esempi</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Digitare il gruppo di annunci con autorizzazioni sufficienti per gestire l'ambiente App-V.</p></td>
    <td align="left"><p>Esempio: MyDomain\MyUser</p>
    <p>Dopo l'installazione, è possibile aggiungere altri utenti o gruppi tramite la console di gestione. Tuttavia, i gruppi di sicurezza globali e i gruppi di distribuzione di servizi di dominio Active Directory (AD DS) non sono supportati. <strong> </strong> Per eseguire questa azione è necessario usare il dominio locale o <strong> </strong> i gruppi universali.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nome sito Web </strong> : specificare il nome personalizzato che verrà usato per eseguire il servizio di pubblicazione.</p></td>
    <td align="left"><p>Se non si dispone di un nome personalizzato, non apportare alcuna modifica.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Binding della porta </strong> : specificare un numero di porta univoco che verrà usato da App-V.</p></td>
    <td align="left"><p>Esempio: <strong> 12345</strong></p>
    <p>Assicurarsi che la porta specificata non venga usata da un altro sito Web.</p></td>
    </tr>
    </tbody>
    </table>

     

11. Nella pagina **Configura** **Configurazione server di pubblicazione** specificare quanto segue:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Elemento da configurare</th>
    <th align="left">Descrizione ed esempi</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Specificare l'URL per il servizio di gestione.</p></td>
    <td align="left"><p>Esempio<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nome sito Web </strong> : specificare il nome personalizzato che verrà usato per eseguire il servizio di pubblicazione.</p></td>
    <td align="left"><p>Se non si dispone di un nome personalizzato, non apportare alcuna modifica.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Binding della porta </strong> : specificare un numero di porta univoco che verrà usato da App-V.</p></td>
    <td align="left"><p>Esempio: 54321</p>
    <p>Assicurarsi che la porta specificata non venga usata da un altro sito Web.</p></td>
    </tr>
    </tbody>
    </table>

     

12. Nella pagina **Reporting Server** specificare quanto segue:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Elemento da configurare</th>
    <th align="left">Descrizione ed esempi</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nome sito Web </strong> : specificare il nome personalizzato che verrà usato per eseguire il servizio di creazione di report.</p></td>
    <td align="left"><p>Se non si dispone di un nome personalizzato, non apportare alcuna modifica.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Binding della porta </strong> : specificare un numero di porta univoco che verrà usato da App-V.</p></td>
    <td align="left"><p>Esempio: 55555</p>
    <p>Assicurarsi che la porta specificata non venga usata da un altro sito Web.</p></td>
    </tr>
    </tbody>
    </table>

     

13. Per avviare l'installazione, fare clic su **Installa** nella pagina **pronto** e quindi fare clic su **Chiudi** nella pagina **finito** .

14. Per verificare che la configurazione sia stata completata correttamente, aprire un Web browser e digitare l'URL seguente:

    **http:// &lt; Nome computer del server di gestione &gt; : &lt; numero di porta del servizio di gestione &gt; /Console.html**.

    Esempio: **http://localhost:12345/console.html** . Se l'installazione è riuscita, viene visualizzata la console di gestione di App-V senza errori.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Distribuzione di App-V 5.1](deploying-app-v-51.md)

[Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[Come installare il server di pubblicazione in un computer remoto](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[Come distribuire il server App-V 5.1 con uno script](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





