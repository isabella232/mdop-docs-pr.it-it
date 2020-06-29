---
title: Come modificare un file OSD usando un editor di testo
description: Come modificare un file OSD usando un editor di testo
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817445"
---
# Come modificare un file OSD usando un editor di testo


Usare la procedura seguente per modificare un file OSD (Open Software Descriptor) usando un editor di testo.

**Per modificare un file OSD usando un editor di testo**

1.  Aprire il file OSD usando qualsiasi editor di testo XML o ASCII, ad esempio Blocco note Microsoft.

    **Nota**  Prima di modificare il file OSD, leggere lo schema prescritto dal file XSD nella directory di installazione. Se non si riesce a seguire questo schema, è possibile che vengano introdotti errori che impediscono l'avvio di un'applicazione sequenziale.

     

2.  Modificare il file OSD usando l'editor di testo XML o ASCII di scelta, aderendo allo schema prescritto e alle linee guida seguenti:

    1.  Assicurati che gli elementi denominati siano annidati all'interno dell' &lt; &gt; elemento radice SOFTPKG.

    2.  Verificare che i nomi degli elementi siano in lettere maiuscole.

    3.  Tieni presente che i valori degli attributi sono maiuscole/minuscole.

    4.  Digitare con attenzione e osservare le specifiche XML.

## Argomenti correlati


[Informazioni sulla scheda OSD](about-the-osd-tab.md)

[Come modificare un File OSD](how-to-edit-an-osd-file.md)

[Elementi di file OSD](osd-file-elements.md)

 

 





