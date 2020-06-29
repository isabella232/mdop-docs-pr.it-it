---
title: Supporto per la creazione di report client su HTTP
description: Supporto per la creazione di report client su HTTP
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815286"
---
# <span data-ttu-id="6ed77-103">Supporto per la creazione di report client su HTTP</span><span class="sxs-lookup"><span data-stu-id="6ed77-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="6ed77-104">La versione 4,6 del client App-V supporta ora l'uso delle comunicazioni HTTP quando si inviano i dati dei report client al server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6ed77-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="6ed77-105">Questa funzionalità supporta gli scenari in cui un cliente ha implementato un server di pubblicazione HTTP (S) personalizzato configurato per raccogliere ed elaborare i dati del client.</span><span class="sxs-lookup"><span data-stu-id="6ed77-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="6ed77-106">Per altre informazioni sui server di pubblicazione HTTP, vedere</span><span class="sxs-lookup"><span data-stu-id="6ed77-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="6ed77-107">Report client tramite HTTP</span><span class="sxs-lookup"><span data-stu-id="6ed77-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="6ed77-108">Il client avvia la raccolta dei dati quando riceve un attributo "REPORTING =" TRUE "" nel codice XML di risposta dell'aggiornamento della pubblicazione dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6ed77-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="6ed77-109">Quando questo attributo viene ricevuto, il client invia tutti i dati accumulati al server di pubblicazione che ha inviato l'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6ed77-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="6ed77-110">I dettagli di questo processo sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ed77-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="6ed77-111">Il client invia una richiesta GET HTTP al server di pubblicazione per un aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6ed77-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="6ed77-112">L'intestazione di questo messaggio contiene un'intestazione personalizzata "AppV-op: Refresh" che il server di pubblicazione HTTP (S) personalizzato usa per identificare il tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="6ed77-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="6ed77-113">Il server di pubblicazione invia quindi l'XML di risposta dell'aggiornamento della pubblicazione che contiene un valore "REPORTING =" TRUE "".</span><span class="sxs-lookup"><span data-stu-id="6ed77-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="6ed77-114">Il client invia quindi una richiesta POST HTTP al server di pubblicazione insieme ai dati di report raccolti dopo l'aggiornamento precedente.</span><span class="sxs-lookup"><span data-stu-id="6ed77-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="6ed77-115">L'intestazione di questo messaggio contiene un'intestazione personalizzata "AppV-op: report" che il server di pubblicazione HTTP (S) personalizzato usa per identificare il tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="6ed77-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="6ed77-116">Lo schema seguente fornisce dettagli specifici del pacchetto e dei dati dell'applicazione inviati al server.</span><span class="sxs-lookup"><span data-stu-id="6ed77-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





