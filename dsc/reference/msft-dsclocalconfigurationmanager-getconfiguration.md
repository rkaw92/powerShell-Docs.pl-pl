---
ms.date: 06/12/2017
keywords: DSC, powershell, konfiguracja, ustawienia
title: Metoda GetConfiguration klasy MSFT_DSCLocalConfigurationManager
ms.openlocfilehash: ae31ac30c152c96707b764ddaf00c924806afcfc
ms.sourcegitcommit: 00ff76d7d9414fe585c04740b739b9cf14d711e1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/14/2018
ms.locfileid: "53404886"
---
# <a name="getconfiguration-method-of-the-msftdsclocalconfigurationmanager-class"></a>Metoda GetConfiguration klasy MSFT_DSCLocalConfigurationManager

Wysyła dokument konfiguracji do zarządzanego węzła i używa **uzyskać** metoda przez agenta konfiguracji, aby zastosować konfigurację.

## <a name="syntax"></a>Składnia

```mof
uint32 GetConfiguration(
  [in]  uint8            configurationData[],
  [out] OMI_BaseResource configurations[]
);
```

## <a name="parameters"></a>Parametry

*configurationData* \[w\] Określa dane konfiguracji do wysłania.

*konfiguracje* \[się\] przy powrocie, zawiera wystąpienie osadzony w konfiguracji.

## <a name="return-value"></a>Wartość zwracana

Zwraca wartość zero w przypadku powodzenia; w przeciwnym razie zwraca kod błędu.

## <a name="remarks"></a>Uwagi

Jest to metoda statyczna.

## <a name="requirements"></a>Wymagania

**PLIK MOF:** DscCore.mof

**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration

## <a name="see-also"></a>Zobacz też

[**MSFT_DSCLocalConfigurationManager**](msft-dsclocalconfigurationmanager.md)