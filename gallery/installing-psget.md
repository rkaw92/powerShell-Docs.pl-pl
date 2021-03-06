---
ms.date: 06/12/2017
contributor: manikb
keywords: Galeria, programu powershell, polecenie cmdlet, psget
title: Instalowanie menedżera pakietów PowerShellGet
ms.openlocfilehash: 5c51cb1c7ea2538cc5f8503ce6c5d80edda70e15
ms.sourcegitcommit: 98b7cfd8ad5718efa8e320526ca76c3cc4141d78
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/25/2018
ms.locfileid: "50002227"
---
# <a name="installing-powershellget"></a>Instalowanie menedżera pakietów PowerShellGet

## <a name="powershellget-is-an-in-box-module-in-the-following-releases"></a>Moduł PowerShellGet jest moduł skrzynkach odbiorczych w następujących wersjach

- [Windows 10](https://www.microsoft.com/windows) lub nowszej
- [System Windows Server 2016](/windows-server/windows-server) lub nowszej
- [Windows Management Framework (WMF) 5.0](https://www.microsoft.com/download/details.aspx?id=50395) lub nowszej
- [Program PowerShell 6](https://github.com/PowerShell/PowerShell/releases)

## <a name="get-powershellget-module-for-powershell-versions-30-and-40"></a>Uzyskiwanie modułu PowerShellGet w przypadku programu PowerShell w wersji 3.0 i 4.0

- [Funkcja PackageManagement MSI](https://www.microsoft.com/download/details.aspx?id=51451)

## <a name="get-the-latest-version-from-powershell-gallery"></a>Pobierz najnowszą wersję z galerii programu PowerShell

- Przed zaktualizowaniem modułu PowerShellGet, należy zawsze instalować najnowszego dostawcę Nuget. Aby to zrobić, uruchom następujące polecenie w sesji programu PowerShell z podwyższonym poziomem uprawnień.

  ```powershell
  Install-PackageProvider Nuget –Force
  Exit
  ```

### <a name="for-systems-with-powershell-50-or-newer-you-can-install-the-latest-powershellget"></a>Dla systemów z programu PowerShell w wersji 5.0 (lub nowsza) można zainstalować najnowszy moduł PowerShellGet

- Aby to zrobić w systemie Windows 10, Windows Server 2016, każdy system WMF 5.0 lub 5.1 zainstalowane lub dowolnego systemu przy użyciu programu PowerShell 6 Uruchom następujące polecenia w sesji programu PowerShell z podwyższonym poziomem uprawnień.

  ```powershell
  Install-Module –Name PowerShellGet –Force
  Exit
  ```

- Użyj `Update-Module` można pobrać nowsze wersje.

  ```powershell
  Update-Module -Name PowerShellGet
  Exit
  ```

### <a name="for-systems-running-powershell-3-or-powershell-4-that-have-installed-the-packagemanagement-msihttpswwwmicrosoftcomdownloaddetailsaspxid51451"></a>Dla komputerów z systemami program PowerShell 3 lub 4 programu PowerShell, który został zainstalowany [MSI funkcji PackageManagement](https://www.microsoft.com/download/details.aspx?id=51451)

- Użyć poniższego polecenia cmdlet PowerShellGet sesję programu PowerShell z podwyższonym poziomem uprawnień do zapisania modułów do katalogu lokalnego

  ```powershell
  Save-Module PowerShellGet -Path C:\LocalFolder
  Exit
  ```

- Upewnij się, modułu PowerShellGet oraz spełnione PackageManagment modułów nie są ładowane w żadnych innych procesów.
- Usuń zawartość `$env:ProgramFiles\WindowsPowerShell\Modules\PowerShellGet\` i `$env:ProgramFiles\WindowsPowerShell\Modules\PackageManagement\` folderów.
- Ponownie otwórz konsolę PS z podwyższonym poziomem uprawnień, a następnie uruchom następujące polecenia.

  ```powershell
  Copy-Item "C:\LocalFolder\PowerShellGet\*" "$env:ProgramFiles\WindowsPowerShell\Modules\PowerShellGet\" -Recurse -Force
  Copy-Item "C:\LocalFolder\PackageManagement\*" "$env:ProgramFiles\WindowsPowerShell\Modules\PackageManagement\" -Recurse -Force
  ```
