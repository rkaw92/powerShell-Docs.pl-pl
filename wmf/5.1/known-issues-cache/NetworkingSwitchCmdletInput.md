---
ms.date: 06/12/2017
keywords: wmf,powershell,setup
ms.topic: conceptual
contributor: vaibch
title: Błąd polecenia cmdlet Menedżer przełącznika sieci
ms.openlocfilehash: a0f84c35974b6674faba4b0f19a28bd6e2490a96
ms.sourcegitcommit: 8b076ebde7ef971d7465bab834a3c2a32471ef6f
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/06/2018
ms.locfileid: "37893158"
---
# <a name="network-switch-manager-cmdlets-failure"></a>Błąd polecenia cmdlet Menedżer przełącznika sieci

Polecenia cmdlet Menedżer przełącznika sieci może służyć do zarządzania przełącznikami sieciowymi za pośrednictwem usługi WS-MANAGEMENT.
Kilka poleceń cmdlet tego modułu są w stanie akceptując wartości z potoków.
W programu WMF 5.1 (wersja zapoznawcza) polecenia cmdlet, które może akceptować wartości z potoku nie do wykonania, gdy wartości nie zostaną przekazane za pośrednictwem potoków.

Jeśli parametr "InputObject" nie jest używany, polecenia cmdlet powinny nadal wykonane bez błędów.

Poniżej przedstawiono listę poleceń cmdlet dotyczy tj tych poleceń cmdlet może akceptować wartość dla parametru "InputObject" z potoku.
Jeśli ta wartość nie zostanie przekazany z potoku wykonywania polecenia cmdlet nie powiedzie się.

- Wyłącz NetworkSwitchEthernetPort
- Włącz NetworkSwitchEthernetPort
- Usuń NetworkSwitchEthernetPortIPAddress
- Zestaw NetworkSwitchEthernetPortIPAddress
- Zestaw NetworkSwitchPortMode
- Zestaw NetworkSwitchPortProperty
- Wyłącz NetworkSwitchFeature
- Włącz NetworkSwitchFeature
- Usuń NetworkSwitchVlan
- Zestaw NetworkSwitchVlanProperty

## <a name="resolution"></a>Rozwiązanie

Dobrym rozwiązaniem, gdy wartość parametru InputObject są przekazywane do niego za pośrednictwem potoku pracy polecenia cmdlet. Kilka przykładów, które działają w przypadku powyższych poleceń cmdlet są:

- `Disable-NetworkSwitchEthernetPort`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Disable-NetworkSwitchEthernetPort -CimSession $cimSession
  ```

- `Enable-NetworkSwitchEthernetPort`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Enable-NetworkSwitchEthernetPort -CimSession $cimSession
  ```

- `Remove-NetworkSwitchEthernetPortIPAddress`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Remove-NetworkSwitchEthernetPortIPAddress -CimSession $cimSession
  ```

- `Set-NetworkSwitchEthernetPortIPAddress`

  ```powershell
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $ipAddress = "192.168.10.1"
  $subnetAddress = "255.255.255.0"
  $port | Set-NetworkSwitchEthernetPortIPAddress -IpAddress $ipAddress -SubnetAddress $subnetAddress -CimSession $cimSession
  ```

- `Set-NetworkSwitchPortProperty`

  ```powershell
  $portProperties = @{Caption = "New Caption"}
  $port = Get-CimInstance -Namespace root/interop -ClassName CIM_EthernetPort -CimSession $cimSession | Select-Object -First 1
  $port | Set-NetworkSwitchPortProperty -Property $portProperties -CimSession $cimSession
  ```

- `Disable-NetworkSwitchFeature`

  ```powershell
  $feature = Get-CimInstance -Namespace root/interop -ClassName MSFT_Feature -CimSession $cimSession | Select-Object -First 1
  $feature | Disable-NetworkSwitchFeature -CimSession $cimSession
  ```

- `Enable-NetworkSwitchFeature`

  ```powershell
  $feature = Get-CimInstance -Namespace root/interop -ClassName MSFT_Feature -CimSession $cimSession | Select-Object -First 1
  $feature | Enable-NetworkSwitchFeature -CimSession $cimSession
  ```

- `Set-NetworkSwitchVlanProperty`

  ```powershell
  $properties = @{Caption = "New Caption"}
  $vlan = Get-CimInstance -ClassName CIM_NetworkVlan -Namespace root/interop -CimSession $cimSession | Select-Object -First 1
  $vlan | Set-NetworkSwitchVlanProperty -Property $properties -CimSession $cimSession
  ```