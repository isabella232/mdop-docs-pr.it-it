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
# Come gestire il reindirizzamento URL con Packager nell'area di lavoro MED-V


È possibile usare Packager area di lavoro MED-V per gestire il reindirizzamento degli URL nell'area di lavoro MED-V.

**Per gestire il reindirizzamento degli indirizzi Web in un'area di lavoro MED-V**

1.  Per aprire **Packager area di lavoro MED-v**, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **Packager area di lavoro MED-v**.

2.  Nel pannello principale di **Packager area di lavoro MED-V** fare clic su **Gestisci reindirizzamento Web**.

3.  Nella finestra **Gestisci** il reindirizzamento Web è possibile digitare, incollare o importare un elenco degli URL reindirizzati a Internet Explorer nell'area di lavoro MED-V.

    **Nota**  
    Il reindirizzamento degli URL in MED-V supporta solo i protocolli HTTP e HTTPS. MED-V non offre il supporto per FTP o altri protocolli.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. Fare clic su **Salva con nome...** per salvare i file di reindirizzamento degli URL aggiornati nella cartella specificata. MED-V crea un file del registro di sistema contenente le informazioni aggiornate sul reindirizzamento degli URL. Distribuire la chiave del registro di sistema aggiornata usando criteri di gruppo. Per altre informazioni sull'uso dei criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V crea inoltre uno script di Windows PowerShell nella cartella specificata che è possibile usare per ricreare il pacchetto dell'area di lavoro MED-V aggiornata.

## Argomenti correlati


[Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[Gestire il reindirizzamento URL in MED-V](manage-med-v-url-redirection.md)









