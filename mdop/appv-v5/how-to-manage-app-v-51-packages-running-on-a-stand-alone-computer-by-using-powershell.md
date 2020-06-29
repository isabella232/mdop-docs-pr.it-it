---
title: Come gestire i pacchetti App-V 5.1 in esecuzione in un computer autonomo con PowerShell
description: Come gestire i pacchetti App-V 5.1 in esecuzione in un computer autonomo con PowerShell
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805337"
---
# Come gestire i pacchetti App-V 5.1 in esecuzione in un computer autonomo con PowerShell


Le sezioni seguenti spiegano come eseguire varie attività di gestione in un computer client autonomo usando PowerShell:

-   [Per restituire un elenco di pacchetti](#bkmk-return-pkgs-standalone-posh)

-   [Per aggiungere un pacchetto](#bkmk-add-pkgs-standalone-posh)

-   [Per pubblicare un pacchetto](#bkmk-pub-pkg-standalone-posh)

-   [Per pubblicare un pacchetto in un utente specifico](#bkmk-pub-pkg-a-user-standalone-posh)

-   [Per aggiungere e pubblicare un pacchetto](#bkmk-add-pub-pkg-standalone-posh)

-   [Per annullare la pubblicazione di un pacchetto esistente](#bkmk-unpub-pkg-standalone-posh)

-   [Per annullare la pubblicazione di un pacchetto per un utente specifico](#bkmk-unpub-pkg-specfc-use)

-   [Per rimuovere un pacchetto esistente](#bkmk-remove-pkg-standalone-posh)

-   [Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti](#bkmk-admins-pub-pkgs)

-   [Informazioni sui pacchetti in sospeso (UserPending e GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>Per restituire un elenco di pacchetti


Usare le informazioni seguenti per restituire un elenco di pacchetti aventi diritto a un utente specifico:

**Cmdlet**: Get-AppvClientPackage

**Parametri**:-name-version-PackageID-VersionId

**Esempio**: Get-AppvClientPackage-Name "ContosoApplication"-versione 2

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>Per aggiungere un pacchetto


Usare le informazioni seguenti per aggiungere un pacchetto a un computer.

**Importante**  Questo esempio aggiunge solo un pacchetto. Il pacchetto non viene pubblicato nell'utente o nel computer.

 

**Cmdlet**: Add-AppvClientPackage

**Esempio**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>Per pubblicare un pacchetto


Usare le informazioni seguenti per pubblicare un pacchetto aggiunto a un utente specifico o a livello globale a qualsiasi utente nel computer.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo di pubblicazione</th>
<th align="left">Cmdlet ed esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Pubblicazione per l'utente</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publish-AppvClientPackage</p>
<p><strong>Esempio </strong> : Publish-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pubblicazione globale</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publish-AppvClientPackage</p>
<p><strong>Esempio </strong> : Publish-AppvClientPackage "ContosoApplication"-Global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>Per pubblicare un pacchetto in un utente specifico


**Nota**  Per usare questo parametro è necessario usare il pacchetto hotfix 5 o versioni successive di App-V 5,0 SP2.

 

Un amministratore può pubblicare un pacchetto in un utente specifico specificando il parametro facoltativa- **UserSID** con il cmdlet **Publish-AppvClientPackage** , dove **-UserSID** rappresenta l'identificatore di sicurezza (SID) dell'utente finale.

Per usare questo parametro:

-   Puoi eseguire questo cmdlet dalla sessione utente o amministratore.

-   Per usare il parametro è necessario avere effettuato l'accesso con le credenziali amministrative.

-   L'utente finale deve essere connesso.

-   Devi specificare l'identificatore di sicurezza (SID) dell'utente finale.

**Cmdlet**: Publish-AppvClientPackage

**Esempio**: Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>Per aggiungere e pubblicare un pacchetto


Usare le informazioni seguenti per aggiungere un pacchetto a un computer e pubblicarlo per l'utente.

**Cmdlet**: Add-AppvClientPackage

**Esempio**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publish-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>Per annullare la pubblicazione di un pacchetto esistente


Usare le informazioni seguenti per annullare la pubblicazione di un pacchetto autorizzato a un utente, ma non rimuovere il pacchetto dal computer.

**Cmdlet**: annullamento della pubblicazione-AppvClientPackage

**Esempio**: Unpublish-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>Per annullare la pubblicazione di un pacchetto per un utente specifico


**Nota**  Per usare questo parametro è necessario usare il pacchetto hotfix 5 o versioni successive di App-V 5,0 SP2.

 

Un amministratore può annullare la pubblicazione di un pacchetto per un utente specifico usando il parametro facoltativo **-UserSID** con il cmdlet **Unpublish-AppvClientPackage** , dove **-UserSID** rappresenta l'identificatore di sicurezza (SID) dell'utente finale.

Per usare questo parametro:

-   Puoi eseguire questo cmdlet dalla sessione utente o amministratore.

-   Per usare il parametro è necessario avere effettuato l'accesso con le credenziali amministrative.

-   L'utente finale deve essere connesso.

-   Devi specificare l'identificatore di sicurezza (SID) dell'utente finale.

**Cmdlet**: annullamento della pubblicazione-AppvClientPackage

**Esempio**: Unpublish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>Per rimuovere un pacchetto esistente


Usare le informazioni seguenti per rimuovere un pacchetto dal computer.

**Cmdlet**: Remove-AppvClientPackage

**Esempio**: Remove-AppvClientPackage "ContosoApplication"

**Nota**  I cmdlet App-V sono stati assegnati alle variabili per gli esempi precedenti solo per motivi di chiarezza; l'assegnazione non è un requisito. La maggior parte dei cmdlet può essere combinata come visualizzata in [per aggiungere e pubblicare un pacchetto](#bkmk-add-pub-pkg-standalone-posh). Per un'esercitazione dettagliata, vedere [App-V 5,0 client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti


**Nota** 
 **Questa funzionalità è supportata a partire da App-V 5,0 SP3.**

 

Usa il cmdlet e il parametro seguenti per consentire solo agli amministratori (non agli utenti finali) di pubblicare o annullare la pubblicazione di pacchetti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cmdlet</strong></p></td>
<td align="left"><p>Set-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Parametro</strong></p></td>
<td align="left"><p>-RequirePublishAsAdmin</p>
<p>Valori dei parametri:</p>
<ul>
<li><p>0-falso</p></li>
<li><p>1-vero</p></li>
</ul>
<p><strong>Esempio: </strong> : set-AppvClientConfiguration-RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Per usare la console di gestione di App-V per impostare questa configurazione, vedere [come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-51.md).

## <a href="" id="bkmk-understd-pend-pkgs"></a>Informazioni sui pacchetti in sospeso (UserPending e GlobalPending)


A **partire da App-V 5,0 SP2**: se si esegue un cmdlet di PowerShell che influisce su un pacchetto attualmente in uso, l'attività che si sta provando a eseguire viene inserita in uno stato in sospeso. Se ad esempio si prova a pubblicare un pacchetto quando si usa un'applicazione in tale pacchetto e quindi si esegue **Get-AppvClientPackage**, lo stato in sospeso verrà visualizzato nell'output del cmdlet come indicato di seguito:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento di output cmdlet</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>UserPending</p></td>
<td align="left"><p>Indica se il pacchetto elencato ha un'attività in sospeso che viene applicata all'utente:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>Indica se il pacchetto elencato ha un'attività in sospeso applicata globalmente al computer:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

L'attività in sospeso verrà eseguita in un secondo momento, in base alle regole seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di attività</th>
<th align="left">Regola applicabile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività basata su utenti, ad esempio, pubblicazione di un pacchetto in un utente</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita dopo la disattivazione dell'utente e quindi il log di nuovo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basata su base globale, ad esempio, che consente a un gruppo di connessioni a livello globale</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</p></td>
</tr>
</tbody>
</table>

 

Per altre informazioni sulle attività in sospeso, vedere [informazioni su App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).

**Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

[Amministrazione di App-V 5.1 con PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





