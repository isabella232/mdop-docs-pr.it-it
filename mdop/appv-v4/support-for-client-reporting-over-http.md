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
# Supporto per la creazione di report client su HTTP


La versione 4,6 del client App-V supporta ora l'uso delle comunicazioni HTTP quando si inviano i dati dei report client al server di pubblicazione. Questa funzionalità supporta gli scenari in cui un cliente ha implementato un server di pubblicazione HTTP (S) personalizzato configurato per raccogliere ed elaborare i dati del client.

Per altre informazioni sui server di pubblicazione HTTP, vedere <https://go.microsoft.com/fwlink/?LinkId=157426>

## Report client tramite HTTP


Il client avvia la raccolta dei dati quando riceve un attributo "REPORTING =" TRUE "" nel codice XML di risposta dell'aggiornamento della pubblicazione dal server di pubblicazione. Quando questo attributo viene ricevuto, il client invia tutti i dati accumulati al server di pubblicazione che ha inviato l'aggiornamento della pubblicazione. I dettagli di questo processo sono i seguenti:

-   Il client invia una richiesta GET HTTP al server di pubblicazione per un aggiornamento della pubblicazione. L'intestazione di questo messaggio contiene un'intestazione personalizzata "AppV-op: Refresh" che il server di pubblicazione HTTP (S) personalizzato usa per identificare il tipo di messaggio.

-   Il server di pubblicazione invia quindi l'XML di risposta dell'aggiornamento della pubblicazione che contiene un valore "REPORTING =" TRUE "".

-   Il client invia quindi una richiesta POST HTTP al server di pubblicazione insieme ai dati di report raccolti dopo l'aggiornamento precedente. L'intestazione di questo messaggio contiene un'intestazione personalizzata "AppV-op: report" che il server di pubblicazione HTTP (S) personalizzato usa per identificare il tipo di messaggio.

Lo schema seguente fornisce dettagli specifici del pacchetto e dei dati dell'applicazione inviati al server.

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

 

 





