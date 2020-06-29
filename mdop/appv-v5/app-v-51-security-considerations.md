---
title: Considerazioni sulla sicurezza relative ad App-V 5.1
description: Considerazioni sulla sicurezza relative ad App-V 5.1
author: dansimp
ms.assetid: 6bc6c1fc-f813-47d4-b763-06fd4faf6a72
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a5606b3e0ba5e6fb8c62f14e2ed8d93ea2cf134
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805973"
---
# Considerazioni sulla sicurezza relative ad App-V 5.1


Questo argomento contiene una breve panoramica degli account e dei gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft Application Virtualization (App-V) 5,1.

**Importante**  
App-V 5,1 non è un prodotto di sicurezza e non fornisce garanzie per un ambiente sicuro.



## La caratteristica PackageStoreAccessControl (PSAC) è deprecata


A partire da giugno 2014, la caratteristica PackageStoreAccessControl (PSAC) introdotta in Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) è stata deprecata sia in ambienti single-user che multiutente.

## Considerazioni generali sulla sicurezza


**Comprendere i rischi per la sicurezza.** Il rischio più grave per l'App-V 5,1 è che la sua funzionalità potrebbe essere dirottata da un utente non autorizzato che potrebbe quindi riconfigurare i dati chiave nei client App-V 5,1. La perdita della funzionalità App-V 5,1 per un breve periodo di tempo a causa di un attacco di tipo Denial of Service non avrebbe in genere un impatto catastrofico.

**Proteggere fisicamente i computer**. La sicurezza è incompleta senza sicurezza fisica. Chiunque abbia accesso fisico a un server App-V 5,1 potrebbe potenzialmente attaccare l'intera base client. Eventuali attacchi fisici potenziali devono essere considerati ad alto rischio e mitigati in modo appropriato. I server App-V 5,1 devono essere archiviati in una sala server fisicamente sicura con accesso controllato. Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.

**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**. Per essere sempre informati sugli aggiornamenti più recenti per i sistemi operativi, Microsoft SQL Server e App-V 5,1, iscriversi al servizio di notifica della sicurezza ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Usare password complesse o passare frasi**. Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di App-V 5,1 e App-V 5,1. Non usare mai password vuote. Per altre informazioni sui concetti relativi alle password, vedere il white paper "account password e criteri" su TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Account e gruppi in App-V 5,1


Una procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente. Aggiungi quindi gli account globali del dominio ai gruppi locali dell'App-V 5,1 necessari nei server App-V 5,1.

**Nota**  
Gli account di computer client App-V che devono connettersi al server di pubblicazione devono far parte del gruppo locale **utenti** del server di pubblicazione. Per impostazione predefinita, tutti i computer del dominio fanno parte del gruppo **utenti autorizzati** , che fa parte del gruppo **utenti** locali.



### <a href="" id="-------------app-v-5-1-server-security"></a> App-V 5,1 sicurezza del server

Nessun gruppo viene creato automaticamente durante l'installazione di App-V 5,1. È necessario creare i gruppi globali di servizi di dominio Active Directory seguenti per gestire le operazioni del server App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome gruppo</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gruppo di amministrazione di App-V Management</p></td>
<td align="left"><p>Usato per gestire il server di gestione di App-V 5,1. Questo gruppo viene creato durante l'installazione del server di gestione di App-V 5,1.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Non esiste alcun metodo per creare il gruppo usando la console di gestione dopo aver completato l'installazione.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Account del servizio di lettura/scrittura per database</p></td>
<td align="left"><p>Fornisce l'accesso in lettura/scrittura al database di gestione. Questo account deve essere creato durante l'installazione di database di gestione di App-V 5,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V Service Management installa l'account di amministratore</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa operazione è necessaria solo se il database di gestione viene installato separatamente dal servizio.</p>
</div>
<div>

</div></td>
<td align="left"><p>Fornisce l'accesso pubblico alla tabella della versione dello schema nel database di gestione. Questo account deve essere creato durante l'installazione di database di gestione di App-V 5,1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Reporting Service installare l'account di amministratore</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa operazione è necessaria solo se il database di report viene installato separatamente dal servizio.</p>
</div>
<div>

</div></td>
<td align="left"><p>Accesso pubblico alla tabella della versione dello schema nel database di report. Questo account deve essere creato durante l'installazione di un database di report App-V 5,1.</p></td>
</tr>
</tbody>
</table>



Prendere in considerazione le informazioni aggiuntive seguenti:

-   Accesso alle condivisioni del pacchetto: se una condivisione esiste nello stesso computer del server di gestione, il servizio di **rete** richiede l'accesso in lettura alla condivisione. Inoltre, ogni computer client App-V deve avere accesso in lettura alla condivisione del pacchetto.

    **Nota**  
    Nelle versioni precedenti di App-V la condivisione del pacchetto veniva definita condivisione di contenuto.



-   Registrazione dei server di pubblicazione con server di gestione-un server di pubblicazione deve essere registrato con il server di gestione. Ad esempio, deve essere aggiunto al database, in modo che gli account del computer del server di pubblicazione siano in grado di chiamare l'API del servizio di gestione.

### <a href="" id="-------------app-v-5-1-package-security"></a> Sicurezza del pacchetto App-V 5,1

La procedura seguente consente di pianificare come verificare che i pacchetti virtualizzati siano protetti.

-   Se un programma di installazione dell'applicazione applica un elenco di controllo di accesso (ACL, Access Control List) a un file o a una directory, l'ACL non viene mantenuta nel pacchetto. Quando il pacchetto viene distribuito, se il file o la directory viene modificata da un utente, erediterà l'ACL nell' **% USERPROFILE%** o erediterà l'ACL della directory del computer di destinazione. Il caso precedente si verifica se il file o la directory non esiste in una posizione di file system virtuale; quest'ultimo caso si verifica se il file o la directory esiste in una posizione di file system virtuale, ad esempio **% windir%**.

## <a href="" id="---------app-v-5-1-log-files"></a> File di log di App-V 5,1


Durante l'installazione di App-V 5,1, i file di log della configurazione vengono creati nella cartella **% Temp%** dell'utente che esegue l'installazione.






## Argomenti correlati


[Preparazione dell'ambiente per App-V 5.1](preparing-your-environment-for-app-v-51.md)









