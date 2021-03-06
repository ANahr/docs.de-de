---
title: Benutzerdefiniertes Element für "SingleTagSectionHandler"
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName
helpviewer_keywords:
- custom element
ms.assetid: e62056c6-b351-40eb-afc0-cc13fc44e45e
author: guardrex
ms.author: mairaw
ms.openlocfilehash: 07bc0d9560546f4946d34413697fb0adcf84c58d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
ms.locfileid: "32743276"
---
# <a name="custom-element-for-singletagsectionhandler"></a>Benutzerdefiniertes Element für "SingleTagSectionHandler"

Definiert die Einstellungen in eine benutzerdefinierte Konfigurationsabschnitt, der von definiert wird ein <section> Element- und verwendet die <xref:System.Configuration.SingleTagSectionHandler> Klasse.

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;*\<sectionName>*

## <a name="syntax"></a>Syntax

```xml
<sectionName key="value" key2="value2" ... />
```

## <a name="attributes"></a>Attribute

Attribute und Attributwerte werden vom Benutzer definiert sind.

## <a name="parent-element"></a>Übergeordnetes Element

|     | Beschreibung |
| --- | ----------- |
| [**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) | Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei. |

## <a name="child-elements"></a>Untergeordnete Elemente

Keiner

## <a name="remarks"></a>Hinweise

Die  **\<SectionName >** Element ist ein benutzerdefiniertes Element definiert, indem Sie eine [  **\<Abschnitt >** ](~/docs/framework/configure-apps/file-schema/section-element.md) -Tag in die [  **\<ConfigSections >** ](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) Element. Gibt das Konfigurationssystem ein <xref:System.Collections.IDictionary> Objekt beim Aufrufen von <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.

## <a name="example"></a>Beispiel

Das folgende Beispiel deklariert ein benutzerdefiniertes Element aufgerufen  **\<SampleSection >** enthält Einstellungen, die durch Lesen der <xref:System.Configuration.SingleTagSectionHandler> Klasse:

```xml
<configuration>
  <configSections>
    <section name="sampleSection" 
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a>Konfigurationsdatei

Dieses Element kann in der Anwendungskonfigurationsdatei Computerkonfigurationsdatei verwendet werden (*"Machine.config"*), und *"Web.config"* Dateien, die nicht auf Anwendungsebene Verzeichnis sind.

## <a name="see-also"></a>Siehe auch

[Konfigurationsdateischema für .NET Framework](~/docs/framework/configure-apps/file-schema/index.md)
