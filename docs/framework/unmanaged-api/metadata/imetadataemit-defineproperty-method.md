---
title: IMetaDataEmit::DefineProperty-Methode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineProperty
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5c250a577f2ccdbbfefb35225b880c0e4317db36
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448106"
---
# <a name="imetadataemitdefineproperty-method"></a>IMetaDataEmit::DefineProperty-Methode
Erstellt eine Eigenschaftsdefinition für den angegebenen Typ mit dem angegebenen `get` und `set` Methodenaccessoren und ruft ein Token auf, Eigenschaftsdefinition ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT DefineProperty (   
    [in]  mdTypeDef          td,   
    [in]  LPCWSTR            szProperty,   
    [in]  DWORD              dwPropFlags,   
    [in]  PCCOR_SIGNATURE    pvSig,   
    [in]  ULONG              cbSig,   
    [in]  DWORD              dwCPlusTypeFlag,   
    [in]  void const         *pValue,   
    [in]  ULONG              cchValue,   
    [in]  mdMethodDef        mdSetter,   
    [in]  mdMethodDef        mdGetter,   
    [in]  mdMethodDef        rmdOtherMethods[],   
    [out] mdProperty         *pmdProp   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `td`  
 [in] Das Token für die Klasse oder Schnittstelle, die auf dem die Eigenschaft definiert wird.  
  
 `szProperty`  
 [in] Der Name der Eigenschaft.  
  
 `dwPropFlags`  
 [in] Die Eigenschaftenflags.  
  
 `pvSig`  
 [in] Die Signatur der Eigenschaft.  
  
 `cbSig`  
 [in] Die Anzahl der Bytes im `pvSig`.  
  
 `dwCPlusTypeFlag`  
 [in] Der Typ des Standardwerts für die Eigenschaft.  
  
 `pValue`  
 [in] Der Standardwert für die Eigenschaft.  
  
 `cchValue`  
 [in] Die Anzahl von (Unicode-) Zeichen `pValue`.  
  
 `mdSetter`  
 [in] Die Methode, die den Wert der Eigenschaft festlegt.  
  
 `mdGetter`  
 [in] Die Methode, die den Eigenschaftswert abruft.  
  
 `rmdOtherMethods[]`  
 [in] Ein Array von anderen Methoden, die der Eigenschaft zugeordnet werden soll. Beenden Sie das Array mit einem `mdTokenNil`.  
  
 `pmdProp`  
 [out] Die `mdProperty` Token zugewiesen.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** Cor.h  
  
 **Bibliothek:** als Ressource in MSCorEE.dll verwendet  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 [IMetaDataEmit-Schnittstelle](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2-Schnittstelle](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
