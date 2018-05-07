---
title: ISymENCUnmanagedMethod::GetLineFromOffset-Methode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetLineFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetLineFromOffset
helpviewer_keywords:
- GetLineFromOffset method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetLineFromOffset method [.NET Framework debugging]
ms.assetid: cc09bad2-fb34-4d13-a521-6ec7b1a1d915
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 29990ad6a94f063577236bdbc84d02d4d2b4b2f9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="isymencunmanagedmethodgetlinefromoffset-method"></a>ISymENCUnmanagedMethod::GetLineFromOffset-Methode
Ruft die Zeileninformationen ein Offset zugeordnet. Wenn der Offset-Parameter (`dwOffset`) ein Sequenzpunkt ist diese Methode ruft die Zeileninformationen vorherigen Offset zugeordnet.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetLineFromOffset(  
     [in]  ULONG32   dwOffset,  
     [out] ULONG32*  pline,  
     [out] ULONG32*  pcolumn,  
     [out] ULONG32*  pendLine,  
     [out] ULONG32*  pendColumn,  
     [out] ULONG32*  pdwStartOffset);  
```  
  
#### <a name="parameters"></a>Parameter  
 `dwOffset`  
 [in] Ein `ULONG32` , der den Offset enthält.  
  
 `pline`  
 [out] Ein Zeiger auf eine `ULONG32` , empfängt die Zeile.  
  
 `pcolumn`  
 [out] Ein Zeiger auf eine `ULONG32` , empfängt die Spalte.  
  
 `pendLine`  
 [out] Ein Zeiger auf eine `ULONG32` , die die Endzeile empfängt.  
  
 `pendColumn`  
 [out] Ein Zeiger auf eine `ULONG32` , die die Endspalte empfängt.  
  
 `pdwStartOffset`  
 [out] Ein Zeiger auf eine `ULONG32` , die den zugeordneten Sequenzpunkt empfängt.  
  
## <a name="return-value"></a>Rückgabewert  
 S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Siehe auch  
 [ISymENCUnmanagedMethod-Schnittstelle](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
