---
ms.date: 06/12/2017
keywords: DSC, powershell, konfiguracja, ustawienia
title: Zasób Serviceset DSC
ms.openlocfilehash: 5694c2abc5c0caf0098670b629af464b35125583
ms.sourcegitcommit: e04292a9c10de9a8391d529b7f7aa3753b362dbe
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/04/2019
ms.locfileid: "54048386"
---
# <a name="dsc-serviceset-resource"></a>Zasób Serviceset DSC

> Dotyczy: Program Windows PowerShell 4.0, Windows PowerShell 5.0

**ServiceSet** zasób w Windows PowerShell Desired State Configuration (DSC) zapewnia mechanizm zarządzania usługami na węzeł docelowy. Ten zasób jest [złożonego zasobów](../../../resources/authoringResourceComposite.md) wywołująca [usługi zasobów](serviceResource.md) każdą usług określonych w `Name` właściwości.

Korzystając z tego zasobu, gdy użytkownik chce skonfigurować wiele usług, aby ten sam stan.

## <a name="syntax"></a>Składnia

```
Service [string] #ResourceName
{
    Name = [string[]]
    [ StartupType = [string] { Automatic | Disabled | Manual }  ]
    [ BuiltInAccount = [string] { LocalService | LocalSystem | NetworkService }  ]
    [ State = [string] { Running | Stopped }  ]
    [ Ensure = [string] { Absent | Present }  ]
    [ Credential = [PSCredential] ]
    [ DependsOn = [string[]] ]

}
```

## <a name="properties"></a>Właściwości

|  Właściwość  |  Opis   |
|---|---|
| Nazwa| Określa nazwy usług. Należy pamiętać, że czasami to różni się od nazw wyświetlanych. Możesz uzyskać listę usług i ich bieżący stan z [Get-Service](https://technet.microsoft.com/library/hh849804.aspx) polecenia cmdlet.|
| StartupType| Wskazuje typ uruchomienia usługi. Wartości, które są dozwolone dla tej właściwości to: **Automatyczne**, **wyłączone**, i **ręczne**|
| BuiltInAccount| Wskazuje, że konto logowania do użycia dla usług. Wartości, które są dozwolone dla tej właściwości to: **Usługa lokalna**, **LocalSystem**, i **NetworkService**.|
| Stan| Wskazuje stan, który chcesz mieć pewność, czy usługi: **Zatrzymano** lub **systemem**.|
| Upewnij się| Wskazuje, czy usługi istnieje w systemie. Ustaw tę właściwość na **nieobecne** aby upewnić się, że usługi nie istnieją. Ustawienie **obecne** (wartość domyślna) zapewnia, że istnieją usługi docelowej.|
| Poświadczenie| Określa poświadczenia dla konta, które zostaną uruchomione zasób usługi. Ta właściwość i **BuiltinAccount** właściwości nie mogą być używane razem.|
| DependsOn| Wskazuje, że konfiguracji inny zasób, należy uruchomić przed ten zasób jest skonfigurowany. Na przykład, jeśli identyfikator konfiguracji zasobu skryptu Blok, który chcesz uruchomić najpierw jest *ResourceName* a jej typ jest *ResourceType*, składnia przy użyciu tej właściwości jest `DependsOn = "[ResourceType]ResourceName"`.|



## <a name="example"></a>Przykład

Następująca konfiguracja uruchamia usługi "Windows Audio" i "Usług pulpitu zdalnego".

```powershell
configuration ServiceSetTest
{
    Import-DscResource -ModuleName PSDesiredStateConfiguration
    Node localhost
    {

        ServiceSet ServiceSetExample
        {
            Name        = @("TermService", "Audiosrv")
            StartupType = "Manual"
            State       = "Running"
        }
    }
}
```
