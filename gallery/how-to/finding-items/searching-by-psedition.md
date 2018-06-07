---
ms.date: 06/12/2017
contributor: JKeithB
keywords: Galeria, programu powershell, polecenia cmdlet, psgallery
title: Elementy z niezgodne wersje programu PowerShell
ms.openlocfilehash: f661c2cd076acb9c11394ba0b752ebd154965ff4
ms.sourcegitcommit: 54534635eedacf531d8d6344019dc16a50b8b441
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/16/2018
---
# <a name="items-with-compatible-powershell-editions"></a><span data-ttu-id="71f86-103">Elementy z niezgodne wersje programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="71f86-103">Items with compatible PowerShell Editions</span></span>

<span data-ttu-id="71f86-104">Od wersji 5.1 program PowerShell jest dostępny w różnych wersjach, które charakteryzują się różnymi zestawami funkcji i zgodnością z różnymi platformami.</span><span class="sxs-lookup"><span data-stu-id="71f86-104">Starting with version 5.1, PowerShell is available in different editions which denote varying feature sets and platform compatibility.</span></span>

- <span data-ttu-id="71f86-105">**Wersja Desktop:** jest oparta na programie .NET Framework i zapewnia zgodność ze skryptami i modułami przeznaczonymi dla wersji programu PowerShell działających w pełnych wersjach systemu Windows, takich jak instalacja Podstawowe funkcje serwera i system Windows dla komputerów stacjonarnych.</span><span class="sxs-lookup"><span data-stu-id="71f86-105">**Desktop Edition:** Built on .NET Framework and provides compatibility with scripts and modules targeting versions of PowerShell running on full footprint editions of Windows such as Server Core and Windows Desktop.</span></span>
- <span data-ttu-id="71f86-106">**Wersja Core:** jest oparta na module .NET Core i zapewnia zgodność ze skryptami i modułami przeznaczonymi dla wersji programu PowerShell działających w ograniczonych wersjach systemu Windows, takich jak system Nano Server i Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="71f86-106">**Core Edition:** Built on .NET Core and provides compatibility with scripts and modules targeting versions of PowerShell running on reduced footprint editions of Windows such as Nano Server and Windows IoT.</span></span>

## <a name="powershell-gallery-extracts-supported-pseditions-metadata-and-allows-you-to-filters-the-items-compatible-for-specific-powershell-editions"></a><span data-ttu-id="71f86-107">Galerii programu PowerShell umożliwia wyodrębnianie metadanych PSEditions obsługiwane i pozwala filtrami elementy zgodny dla określonej wersji programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="71f86-107">PowerShell Gallery extracts supported PSEditions metadata and allows you to filters the items compatible for specific PowerShell Editions</span></span>

<span data-ttu-id="71f86-108">Jeśli element ma niezgodny PSEditions określony, zostaną wyświetlone jako część "Wersje programu PowerShell" na stronie wyświetlania elementu, a także w wynikach elementów.</span><span class="sxs-lookup"><span data-stu-id="71f86-108">If an item has compatible PSEditions specified, they will be listed as part of 'PowerShell Editions' in the item display page and also in items results.</span></span>

![Strona wyświetlania elementu z PSEditions](../../Images/ItemDisplayPageWithPSEditions.PNG)

## <a name="search-for-items-in-the-gallery-ui-which-works-on-powershellcore"></a><span data-ttu-id="71f86-110">Wyszukiwanie elementów w galerii interfejsu użytkownika, który działa na PowerShellCore</span><span class="sxs-lookup"><span data-stu-id="71f86-110">Search for items in the gallery UI which works on PowerShellCore</span></span>

<span data-ttu-id="71f86-111">Używaj tagów: "PSEdition_Desktop" i tagów: "PSEdition_Core" filtrami elementy galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71f86-111">Use Tags:"PSEdition_Desktop" and Tags:"PSEdition_Core" to filters the items on PowerShell Gallery.</span></span>

### <a name="use-tagspseditioncore-to-search-items-compatible-with-powershell-core-edition"></a><span data-ttu-id="71f86-112">Używaj tagów: "PSEdition_Core", aby wyszukać elementy zgodne z programu PowerShell w wersji podstawowej.</span><span class="sxs-lookup"><span data-stu-id="71f86-112">Use Tags:"PSEdition_Core" to search items compatible with PowerShell Core Edition.</span></span>

![Elementy zgodne z Core PSEdition wyniki wyszukiwania](../../Images/SearchResultsWithPSEditions.PNG)

### <a name="use-tagspseditiondesktop-to-search-items-compatible-with-powershell-desktop-edition"></a><span data-ttu-id="71f86-114">Używaj tagów: "PSEdition_Desktop", aby wyszukać elementy zgodne z wersji pulpitu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71f86-114">Use Tags:"PSEdition_Desktop" to search items compatible with PowerShell Desktop Edition.</span></span>

![Wyniki wyszukiwania dla elementów zgodne z PSEdition pulpitu](../../Images/SearchResultsWithPSEdition-Desktop.PNG)

## <a name="more-details-on-authoring-and-finding-the-items-with-compatible-powershell-editions"></a><span data-ttu-id="71f86-116">Więcej informacji na temat tworzenia i znajdowanie elementów z niezgodne wersje programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="71f86-116">More details on authoring and finding the items with compatible PowerShell Editions</span></span>

- [<span data-ttu-id="71f86-117">Moduły z elementami PSEdition</span><span class="sxs-lookup"><span data-stu-id="71f86-117">Modules with PSEditions</span></span>](../../concepts/module-psedition-support.md)
- [<span data-ttu-id="71f86-118">Skrypty z elementami PSEdition</span><span class="sxs-lookup"><span data-stu-id="71f86-118">Scripts with PSEditions</span></span>](../../concepts/script-psedition-support.md)