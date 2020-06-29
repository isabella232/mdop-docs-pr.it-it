---
title: Come gestire il reindirizzamento URL con Packager nell'area di lavoro MED-V
description: Come gestire il reindirizzamento URL con Packager nell'area di lavoro MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824816"
---
# <span data-ttu-id="07922-103">Come gestire il reindirizzamento URL con Packager nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="07922-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="07922-104">È possibile usare Packager area di lavoro MED-V per gestire il reindirizzamento degli URL nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="07922-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="07922-105">Per gestire il reindirizzamento degli indirizzi Web in un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="07922-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="07922-106">Per aprire **Packager area di lavoro MED-v**, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="07922-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="07922-107">Nel pannello principale di **Packager area di lavoro MED-V** fare clic su **Gestisci reindirizzamento Web**.</span><span class="sxs-lookup"><span data-stu-id="07922-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="07922-108">Nella finestra **Gestisci** il reindirizzamento Web è possibile digitare, incollare o importare un elenco degli URL reindirizzati a Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="07922-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="07922-109">Nota</span><span class="sxs-lookup"><span data-stu-id="07922-109">Note</span></span>**  
    <span data-ttu-id="07922-110">Il reindirizzamento degli URL in MED-V supporta solo i protocolli HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="07922-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="07922-111">MED-V non offre il supporto per FTP o altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="07922-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="07922-112">Fare clic su **Salva con nome...**</span><span class="sxs-lookup"><span data-stu-id="07922-112">Click **Save as…**</span></span> <span data-ttu-id="07922-113">per salvare i file di reindirizzamento degli URL aggiornati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="07922-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="07922-114">MED-V crea un file del registro di sistema contenente le informazioni aggiornate sul reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="07922-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="07922-115">Distribuire la chiave del registro di sistema aggiornata usando criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="07922-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="07922-116">Per altre informazioni sull'uso dei criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="07922-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="07922-117">MED-V crea inoltre uno script di Windows PowerShell nella cartella specificata che è possibile usare per ricreare il pacchetto dell'area di lavoro MED-V aggiornata.</span><span class="sxs-lookup"><span data-stu-id="07922-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="07922-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07922-118">Related topics</span></span>


[<span data-ttu-id="07922-119">Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita</span><span class="sxs-lookup"><span data-stu-id="07922-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="07922-120">Gestire il reindirizzamento URL in MED-V</span><span class="sxs-lookup"><span data-stu-id="07922-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)









