---
title: QualifierSet_BeginEnumeration-Funktion (Referenz zur nicht verwalteten API)
description: Die Funktion QualifierSet_BeginEnumeration setzt einen Enumerator der Qualifizierer eines Objekts zurück.
ms.date: 11/06/2017
api_name:
- QualifierSet_BeginEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_BeginEnumeration
helpviewer_keywords:
- QualifierSet_BeginEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d20701237501834c611c4e498c39597cf275176
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2018
ms.locfileid: "43518685"
---
# <a name="qualifiersetbeginenumeration-function"></a>QualifierSet_BeginEnumeration-Funktion
Setzt einen Enumerator der Qualifizierer eines Objekts auf den Anfang der Enumeration zurück.  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT QualifierSet_BeginEnumeration (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LONG                 lFlags
); 
```  

## <a name="parameters"></a>Parameter

`vFunc`   
[in] Dieser Parameter wird nicht verwendet.

`ptr`   
[in] Ein Zeiger auf ein [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) Instanz.

`lFlags`   
[in] Eine bitweise Kombination der Flags oder Werte, die in beschriebenen der ["Hinweise"](#remarks) Abschnitt, der angibt, die Qualifizierer in der Enumeration einschließen.

## <a name="return-value"></a>Rückgabewert

Die folgenden Werte, die von dieser Funktion zurückgegebenen werden definiert, der *WbemCli.h* Header-Datei, und Sie können definieren sie als Konstanten in Ihrem Code:

|Konstante  |Wert  |Beschreibung  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Die `lFlags` -Parameter ist ungültig. |
|`WBEM_E_UNEXPECTED` | 0x8004101d | Einen zweiten Aufruf von `QualifierSet_BeginEnumeration` wurde ohne einen zwischenzeitlichen Aufruf versucht [ `QualifierSet_EndEnumeration` ](qualifierset-endenumeration.md). |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Es ist nicht genügend Arbeitsspeicher zur Verfügung, um eine neue Enumeration beginnen. |
|`WBEM_S_NO_ERROR` | 0 | Der Funktionsaufruf war erfolgreich.  |
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt einen Aufruf der [IWbemQualifierSet::BeginEnumeration](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration) Methode.

Zum Aufzählen aller die Qualifizierer für ein Objekt muss vor dem ersten Aufruf dieser Methode aufgerufen werden [QualifierSet_Next](qualifierset-next.md). Die Reihenfolge, in der aufgelisteten Qualifizierer, ist garantiert Invarianten für eine angegebene Enumeration.

Die Flags, die als übergeben werden können die `lEnumFlags` Argument definiert werden, der *WbemCli.h* Header-Datei, und Sie können definieren sie als Konstanten in Ihrem Code.   

|Konstante  |Wert  |Beschreibung  |
|---------|---------|---------|
|  | 0 | Die Namen aller Qualifizierer zurück |
| `WBEM_FLAG_LOCAL_ONLY` | 0x10 | Nur die Namen der Qualifizierer an die current-Eigenschaft oder das Objekt bestimmte zurück. <br/> Für eine Eigenschaft: nur der Qualifizierer der Eigenschaft (einschließlich Außerkraftsetzungen) bestimmte zurückgeben und nicht diese Qualifizierer aus der Klassendefinition weitergegeben. <br/> Für eine Instanz: nur instanzspezifischen Qualifizierer Namen zurückgeben. <br/> Für eine Klasse: nur die Qualifizierer, die abgeleitete Klasse Beiong bestimmte zurück.
|`WBEM_FLAG_PROPAGATED_ONLY` | 0x20 | Rückgabe, nur die Namen der Qualifizierer weitergegeben aus einem anderen Objekt. <br/> Für eine Eigenschaft: Rückgabe, nur die Qualifizierer weitergegeben für diese Eigenschaft aus der Klassendefinition und nicht die von der Eigenschaft selbst. <br/> Für eine Instanz: zurück, die nur diese Qualifizierer weitergegeben werden, aus der Klassendefinition. <br/> Für eine Klasse: zurück, die nur für die Qualifizierer Namen, die von der übergeordneten Klassen geerbt. |

## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** WMINet_Utils.idl  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Siehe auch  
[WMI und Leistungsindikatoren (Referenz zur nicht verwalteten API)](index.md)
