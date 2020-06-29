---
title: Informazioni sull'ambiente virtuale del gruppo di connessione
description: Informazioni sull'ambiente virtuale del gruppo di connessione
author: dansimp
ms.assetid: 535fa640-cbd9-425e-8437-94650a70c264
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bd93c9e7acbf7bbf3f9da506d5d95b8df09e1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806081"
---
# <span data-ttu-id="6afe6-103">Informazioni sull'ambiente virtuale del gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="6afe6-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="6afe6-104">In questo argomento:</span><span class="sxs-lookup"><span data-stu-id="6afe6-104">In this topic:</span></span>**

-   [<span data-ttu-id="6afe6-105">Determinazione della priorità del pacchetto</span><span class="sxs-lookup"><span data-stu-id="6afe6-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="6afe6-106">Unione di percorsi di pacchetto identici in una directory virtuale in gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6afe6-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="6afe6-107">Determinazione della priorità del pacchetto</span><span class="sxs-lookup"><span data-stu-id="6afe6-107">How package priority is determined</span></span>


<span data-ttu-id="6afe6-108">L'ambiente virtuale e lo stato corrente sono associati al gruppo di connessioni, non ai singoli pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6afe6-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="6afe6-109">Se un pacchetto di App-V viene rimosso dal gruppo di connessioni, lo stato esistente come parte del gruppo di connessioni non verrà migrato con il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6afe6-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="6afe6-110">Se lo stesso pacchetto fa parte di due diversi gruppi di connessioni, è necessario indicare il gruppo di connessioni che deve essere usato da App-V.</span><span class="sxs-lookup"><span data-stu-id="6afe6-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="6afe6-111">Ad esempio, potresti avere due pacchetti in un gruppo di connessioni che definiscono ognuno lo stesso valore DWORD del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6afe6-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="6afe6-112">Il gruppo di connessioni usato si basa sull'ordine in cui un pacchetto viene visualizzato all'interno del documento XML di **AppConnectionGroup** :</span><span class="sxs-lookup"><span data-stu-id="6afe6-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="6afe6-113">Il primo pacchetto ha la precedenza più alta.</span><span class="sxs-lookup"><span data-stu-id="6afe6-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="6afe6-114">Il secondo pacchetto ha la seconda priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="6afe6-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="6afe6-115">Si consideri la sezione di esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6afe6-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="6afe6-116">Supponiamo che lo stesso valore DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) sia definito nel primo e nel terzo pacchetto, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6afe6-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="6afe6-117">Pacchetto 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="6afe6-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="6afe6-118">Pacchetto 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="6afe6-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="6afe6-119">Poiché il pacchetto 1 viene visualizzato per primo, l'ambiente virtuale di AppConnectionGroup avrà il valore DWORD Single pari a 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5).</span><span class="sxs-lookup"><span data-stu-id="6afe6-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="6afe6-120">Ciò significa che le applicazioni virtuali in Package 1, Package 2 e Package 3 vedranno tutti il valore 5 quando eseguono una query per HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="6afe6-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="6afe6-121">Le altre risorse dell'ambiente virtuale vengono risolte allo stesso modo, ma il caso usuale è che le collisioni si verificano nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6afe6-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="6afe6-122">Unione di percorsi di pacchetto identici in una directory virtuale in gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6afe6-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="6afe6-123">Se due o più pacchetti in un gruppo di connessioni contengono percorsi di directory identici, i percorsi vengono uniti in un'unica directory virtuale all'interno dell'ambiente virtuale del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6afe6-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="6afe6-124">Questa unione di percorsi consente a un'applicazione in un pacchetto di accedere ai file che si trovano in un pacchetto diverso.</span><span class="sxs-lookup"><span data-stu-id="6afe6-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="6afe6-125">Quando si rimuove un pacchetto da un gruppo di connessioni, le applicazioni del pacchetto rimosso non sono più in grado di accedere ai file nei pacchetti rimanenti del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6afe6-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="6afe6-126">L'ordine in cui App-V cerca il nome di un file nel gruppo di connessioni viene specificato dall'ordine in cui i pacchetti App-V sono elencati nel file manifesto del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6afe6-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="6afe6-127">L'esempio seguente mostra l'ordine e la relazione di una ricerca di nomi di file in un gruppo di connessioni per il **pacchetto a** e il **pacchetto B**.</span><span class="sxs-lookup"><span data-stu-id="6afe6-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6afe6-128">Pacchetto A</span><span class="sxs-lookup"><span data-stu-id="6afe6-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="6afe6-129">Pacchetto B</span><span class="sxs-lookup"><span data-stu-id="6afe6-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6afe6-130">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="6afe6-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="6afe6-131">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="6afe6-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6afe6-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="6afe6-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="6afe6-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="6afe6-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6afe6-134">Nell'esempio precedente, quando un'applicazione virtualizzata cerca di trovare un file specifico, il pacchetto A viene prima cercato per un percorso di file corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6afe6-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="6afe6-135">Se non viene trovato un percorso corrispondente, viene eseguita la ricerca nel pacchetto B, usando le regole di mapping seguenti:</span><span class="sxs-lookup"><span data-stu-id="6afe6-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="6afe6-136">Se un file denominato **test.txt** esiste nella stessa gerarchia di cartelle virtuali in entrambi i pacchetti di applicazioni, viene usato il primo file corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6afe6-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="6afe6-137">Se un file denominato **bar.txt** esiste nella gerarchia di cartelle virtuali di un pacchetto dell'applicazione, ma non nell'altra, viene usato il primo file corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6afe6-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="6afe6-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6afe6-138">Related topics</span></span>


[<span data-ttu-id="6afe6-139">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="6afe6-139">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





