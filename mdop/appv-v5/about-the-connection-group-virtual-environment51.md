---
title: Informazioni sull'ambiente virtuale del gruppo di connessione
description: Informazioni sull'ambiente virtuale del gruppo di connessione
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806063"
---
# Informazioni sull'ambiente virtuale del gruppo di connessione


**In questo argomento:**

-   [Determinazione della priorità del pacchetto](#bkmk-pkg-priority-deter)

-   [Unione di percorsi di pacchetto identici in una directory virtuale in gruppi di connessioni](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a>Determinazione della priorità del pacchetto


L'ambiente virtuale e lo stato corrente sono associati al gruppo di connessioni, non ai singoli pacchetti. Se un pacchetto di App-V viene rimosso dal gruppo di connessioni, lo stato esistente come parte del gruppo di connessioni non verrà migrato con il pacchetto.

Se lo stesso pacchetto fa parte di due diversi gruppi di connessioni, è necessario indicare il gruppo di connessioni che deve essere usato da App-V. Ad esempio, potresti avere due pacchetti in un gruppo di connessioni che definiscono ognuno lo stesso valore DWORD del registro di sistema.

Il gruppo di connessioni usato si basa sull'ordine in cui un pacchetto viene visualizzato all'interno del documento XML di **AppConnectionGroup** :

-   Il primo pacchetto ha la precedenza più alta.

-   Il secondo pacchetto ha la seconda priorità più alta.

Si consideri la sezione di esempio seguente:

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

Supponiamo che lo stesso valore DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) sia definito nel primo e nel terzo pacchetto, ad esempio:

-   Pacchetto 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5

-   Pacchetto 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10

Poiché il pacchetto 1 viene visualizzato per primo, l'ambiente virtuale di AppConnectionGroup avrà il valore DWORD Single pari a 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5). Ciò significa che le applicazioni virtuali in Package 1, Package 2 e Package 3 vedranno tutti il valore 5 quando eseguono una query per HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.

Le altre risorse dell'ambiente virtuale vengono risolte allo stesso modo, ma il caso usuale è che le collisioni si verificano nel registro di sistema.

## <a href="" id="bkmk-merged-root-ve-exp"></a>Unione di percorsi di pacchetto identici in una directory virtuale in gruppi di connessioni


Se due o più pacchetti in un gruppo di connessioni contengono percorsi di directory identici, i percorsi vengono uniti in un'unica directory virtuale all'interno dell'ambiente virtuale del gruppo di connessioni. Questa unione di percorsi consente a un'applicazione in un pacchetto di accedere ai file che si trovano in un pacchetto diverso.

Quando si rimuove un pacchetto da un gruppo di connessioni, le applicazioni del pacchetto rimosso non sono più in grado di accedere ai file nei pacchetti rimanenti del gruppo di connessioni.

L'ordine in cui App-V cerca il nome di un file nel gruppo di connessioni viene specificato dall'ordine in cui i pacchetti App-V sono elencati nel file manifesto del gruppo di connessioni.

L'esempio seguente mostra l'ordine e la relazione di una ricerca di nomi di file in un gruppo di connessioni per il **pacchetto a** e il **pacchetto B**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pacchetto A</th>
<th align="left">Pacchetto B</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>C:\Windows\System32</p></td>
<td align="left"><p>C:\Windows\System32</p></td>
</tr>
<tr class="even">
<td align="left"><p>C:\AppTest</p></td>
<td align="left"><p>C:\AppTest</p></td>
</tr>
</tbody>
</table>

 

Nell'esempio precedente, quando un'applicazione virtualizzata cerca di trovare un file specifico, il pacchetto A viene prima cercato per un percorso di file corrispondente. Se non viene trovato un percorso corrispondente, viene eseguita la ricerca nel pacchetto B, usando le regole di mapping seguenti:

-   Se un file denominato **test.txt** esiste nella stessa gerarchia di cartelle virtuali in entrambi i pacchetti di applicazioni, viene usato il primo file corrispondente.

-   Se un file denominato **bar.txt** esiste nella gerarchia di cartelle virtuali di un pacchetto dell'applicazione, ma non nell'altra, viene usato il primo file corrispondente.






## Argomenti correlati


[Gestione dei gruppi di connessione](managing-connection-groups51.md)

 

 





