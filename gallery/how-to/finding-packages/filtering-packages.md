---
ms.date: 06/12/2017
contributor: JKeithB
keywords: Galeria, programu powershell, polecenie cmdlet, galerii programu PowerShell
title: Filtrowanie wyników wyszukiwania
ms.openlocfilehash: 13270a310613a974e1588a9f56d443a936cfebb8
ms.sourcegitcommit: 98b7cfd8ad5718efa8e320526ca76c3cc4141d78
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/25/2018
ms.locfileid: "50004121"
---
# <a name="filtering-search-results"></a><span data-ttu-id="02a4a-103">Filtrowanie wyników wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="02a4a-103">Filtering search results</span></span>

<span data-ttu-id="02a4a-104">[Karcie pakiety](https://www.powershellgallery.com/packages) Wyświetla wszystkie dostępne pakiety w galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02a4a-104">The [Packages tab](https://www.powershellgallery.com/packages) displays all available packages in the PowerShell Gallery.</span></span>

<span data-ttu-id="02a4a-105">Istnieje kilka sposobów, aby filtrować, sortować i wyszukiwać pakiety.</span><span class="sxs-lookup"><span data-stu-id="02a4a-105">There are several ways to filter, sort, and search the packages.</span></span>
<span data-ttu-id="02a4a-106">Aby wyświetlić więcej szczegółów na temat danego pakietu, kliknij pakiet.</span><span class="sxs-lookup"><span data-stu-id="02a4a-106">To see more details about a particular package, click the package.</span></span>

## <a name="filter-by"></a><span data-ttu-id="02a4a-107">Filtruj według</span><span class="sxs-lookup"><span data-stu-id="02a4a-107">Filter By</span></span>

<span data-ttu-id="02a4a-108">Z listy rozwijanej w obszarze "Filtruj wg" umożliwia użytkownikom przefiltrować wyniki według:</span><span class="sxs-lookup"><span data-stu-id="02a4a-108">The drop-down under "Filter By" allows users to filter the results by:</span></span>
- <span data-ttu-id="02a4a-109">Uwzględnij wersję wstępną</span><span class="sxs-lookup"><span data-stu-id="02a4a-109">Include Prerelease</span></span>
- <span data-ttu-id="02a4a-110">Tylko wersja stabilna</span><span class="sxs-lookup"><span data-stu-id="02a4a-110">Stable Only</span></span>

<span data-ttu-id="02a4a-111">Aby uzyskać informacji na temat "Wersja wstępna" i "Stałe", zobacz [wersję wstępną Versioning dodane do modułu PowerShellGet oraz spełnione galerii programu PowerShell](https://blogs.msdn.microsoft.com/powershell/2017/12/05/prerelease-versioning-added-to-powershellget-and-powershell-gallery/) na blogu zespołu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02a4a-111">For information about "Prerelease" and "Stable", see [Prerelease Versioning Added to PowerShellGet and PowerShell Gallery](https://blogs.msdn.microsoft.com/powershell/2017/12/05/prerelease-versioning-added-to-powershellget-and-powershell-gallery/) in the PowerShell Team Blog.</span></span>

<span data-ttu-id="02a4a-112">Pola wyboru w obszarze listy rozwijanej Zezwalaj użytkownikom na przefiltrować wyniki według:</span><span class="sxs-lookup"><span data-stu-id="02a4a-112">The checkboxes under the drop-down allow users to filter the results by:</span></span>
- <span data-ttu-id="02a4a-113">Typy pakietów</span><span class="sxs-lookup"><span data-stu-id="02a4a-113">Package Types</span></span>
  - <span data-ttu-id="02a4a-114">Moduł</span><span class="sxs-lookup"><span data-stu-id="02a4a-114">Module</span></span>
  - <span data-ttu-id="02a4a-115">Skrypt</span><span class="sxs-lookup"><span data-stu-id="02a4a-115">Script</span></span>
- <span data-ttu-id="02a4a-116">Kategorie</span><span class="sxs-lookup"><span data-stu-id="02a4a-116">Categories</span></span>
  - <span data-ttu-id="02a4a-117">Polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="02a4a-117">Cmdlet</span></span>
  - <span data-ttu-id="02a4a-118">Zasób DSC</span><span class="sxs-lookup"><span data-stu-id="02a4a-118">DSC Resource</span></span>
  - <span data-ttu-id="02a4a-119">Funkcja</span><span class="sxs-lookup"><span data-stu-id="02a4a-119">Function</span></span>
  - <span data-ttu-id="02a4a-120">Możliwości roli</span><span class="sxs-lookup"><span data-stu-id="02a4a-120">Role Capability</span></span>
  - <span data-ttu-id="02a4a-121">Przepływ pracy</span><span class="sxs-lookup"><span data-stu-id="02a4a-121">Workflow</span></span>

<span data-ttu-id="02a4a-122">Aby zapoznać się tylko moduły w galerii programu PowerShell, zobacz moduł w typów pakietów.</span><span class="sxs-lookup"><span data-stu-id="02a4a-122">To see only modules in the PowerShell Gallery, check Module in the Package Types.</span></span>
<span data-ttu-id="02a4a-123">Podobnie Aby wyświetlić tylko skrypty w galerii programu PowerShell, Sprawdź skrypt w typów pakietów.</span><span class="sxs-lookup"><span data-stu-id="02a4a-123">Similarly, to see only scripts in the PowerShell Gallery, check Script in the Package Types.</span></span>

> [!NOTE]
> <span data-ttu-id="02a4a-124">Filtry są włącznie.</span><span class="sxs-lookup"><span data-stu-id="02a4a-124">Filters are inclusive.</span></span>
> <span data-ttu-id="02a4a-125">Przykład: Pakiet zawierający wersję poleceń cmdlet i funkcje będą wyświetlane, jeśli albo polecenia Cmdlet funkcji (i/lub) są sprawdzane.</span><span class="sxs-lookup"><span data-stu-id="02a4a-125">Example: A package containing both cmdlets and functions will appear if either Cmdlet or Function (or both) are checked.</span></span>
> <span data-ttu-id="02a4a-126">Jeśli nie zaznaczono żadnego z tych celów, nie pojawi się pakiet.</span><span class="sxs-lookup"><span data-stu-id="02a4a-126">If neither are selected, the package will not appear.</span></span>
> <span data-ttu-id="02a4a-127">Podobnie jeśli wszystkie kategorie są zaznaczone, tylko pakiety zawierające jeden z tych kategorii będą wyświetlane.</span><span class="sxs-lookup"><span data-stu-id="02a4a-127">Similarly, if all categories are selected, only packages containing one of those categories will appear.</span></span>
> <span data-ttu-id="02a4a-128">**Pakiety, które nie należą do żadnej z tych kategorii nie będą wyświetlane.**</span><span class="sxs-lookup"><span data-stu-id="02a4a-128">**Packages that do not belong to any of those categories will not appear.**</span></span>

## <a name="sort-by"></a><span data-ttu-id="02a4a-129">Sortuj według</span><span class="sxs-lookup"><span data-stu-id="02a4a-129">Sort By</span></span>

<span data-ttu-id="02a4a-130">Sortuj według listy rozwijanej umożliwia użytkownikom Sortuj wyniki według:</span><span class="sxs-lookup"><span data-stu-id="02a4a-130">The Sort By drop-down allows users to sort the results by:</span></span>
- <span data-ttu-id="02a4a-131">Popularność - popularność jest określana przez pobieranie liczby</span><span class="sxs-lookup"><span data-stu-id="02a4a-131">Popularity - Popularity is determined by Download Count</span></span>
- <span data-ttu-id="02a4a-132">A-Z - alfabetycznie według nazwy pakietu</span><span class="sxs-lookup"><span data-stu-id="02a4a-132">A-Z - Alphabetically by package name</span></span>
- <span data-ttu-id="02a4a-133">Ostatnie - pakiety są widoczne w kolejności daty opublikowania</span><span class="sxs-lookup"><span data-stu-id="02a4a-133">Recent - Packages appear in order of publish date</span></span>

## <a name="search-box"></a><span data-ttu-id="02a4a-134">Pole wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="02a4a-134">Search Box</span></span>

<span data-ttu-id="02a4a-135">Pole wyszukiwania umożliwia użytkownikom wyszukiwanie pakietów na słowa kluczowe.</span><span class="sxs-lookup"><span data-stu-id="02a4a-135">The Search Box allows users to search the packages on keywords.</span></span>
<span data-ttu-id="02a4a-136">Aby uzyskać więcej informacji, zobacz [składnia wyszukiwania w galerii](search-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="02a4a-136">For more information, see [Gallery Search Syntax](search-syntax.md).</span></span>