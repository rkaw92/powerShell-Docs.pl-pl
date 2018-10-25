# <a name="microsoft-open-source-code-of-conduct"></a><span data-ttu-id="8ddcc-101">Kodeks postępowania firmy Microsoft dla oprogramowania typu open source</span><span class="sxs-lookup"><span data-stu-id="8ddcc-101">Microsoft Open Source Code of Conduct</span></span>

<span data-ttu-id="8ddcc-102">W tym projekcie jest używany [Kodeks postępowania firmy Microsoft dla oprogramowania typu open source](https://opensource.microsoft.com/codeofconduct/).</span><span class="sxs-lookup"><span data-stu-id="8ddcc-102">This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="8ddcc-103">Aby uzyskać więcej informacji, zobacz [Kodeks postępowania — Często zadawane pytania](https://opensource.microsoft.com/codeofconduct/faq/) lub napisz wiadomość e-mail na adres [opencode@microsoft.com](mailto:opencode@microsoft.com) z dodatkowymi pytaniami lub komentarzami.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-103">For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.</span></span>

<span data-ttu-id="8ddcc-104">[![Status kompilacji:](https://ci.appveyor.com/api/projects/status/onshefxnc4g4pv87/branch/staging?svg=true)](https://ci.appveyor.com/project/PowerShell/powershell-docs/branch/staging)</span><span class="sxs-lookup"><span data-stu-id="8ddcc-104">[![Build status](https://ci.appveyor.com/api/projects/status/onshefxnc4g4pv87/branch/staging?svg=true)](https://ci.appveyor.com/project/PowerShell/powershell-docs/branch/staging)</span></span>

## <a name="powershell-documentation"></a><span data-ttu-id="8ddcc-105">Dokumentacja programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ddcc-105">PowerShell Documentation</span></span>

<span data-ttu-id="8ddcc-106">Witamy w repozytorium dokumentów programu PowerShell, mieszkalnictwo oficjalnej dokumentacji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-106">Welcome to the PowerShell-Docs repository, housing the official PowerShell documentation.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="8ddcc-107">Struktura repozytorium</span><span class="sxs-lookup"><span data-stu-id="8ddcc-107">Repository Structure</span></span>

<span data-ttu-id="8ddcc-108">Następujące foldery najwyższego poziomu, w tym repozytorium zawiera między zestawami dokumentów, które są publikowane w [Microsoft Docs](https://docs.microsoft.com/powershell).</span><span class="sxs-lookup"><span data-stu-id="8ddcc-108">Each of the following top-level folders in this repo contain a DocSet that is published to [Microsoft Docs](https://docs.microsoft.com/powershell).</span></span>

- <span data-ttu-id="8ddcc-109">[/Developer/](https://docs.microsoft.com/powershell/developer/) to miejsce, w którym został przyszłych w dokumentacji zestawu SDK programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ddcc-109">[/developer/](https://docs.microsoft.com/powershell/developer/) is the future home of the PowerShell SDK documentation</span></span>
  - <span data-ttu-id="8ddcc-110">Jesteśmy w trakcie migracji tej zawartości z witryny MSDN</span><span class="sxs-lookup"><span data-stu-id="8ddcc-110">We are in the process of migrating this content from MSDN</span></span>
- <span data-ttu-id="8ddcc-111">[/DSC/](https://docs.microsoft.com/powershell/dsc/) dotyczy funkcji Desired State Configuration</span><span class="sxs-lookup"><span data-stu-id="8ddcc-111">[/dsc/](https://docs.microsoft.com/powershell/dsc/) is for the Desired State Configuration feature</span></span>
- <span data-ttu-id="8ddcc-112">[/Gallery/](https://docs.microsoft.com/powershell/gallery) dotyczy [galerii programu PowerShell](https://www.powershellgallery.com/)</span><span class="sxs-lookup"><span data-stu-id="8ddcc-112">[/gallery/](https://docs.microsoft.com/powershell/gallery) is for the [PowerShell Gallery](https://www.powershellgallery.com/)</span></span>
- <span data-ttu-id="8ddcc-113">[/jea/](https://docs.microsoft.com/powershell/jea/) dotyczy funkcji Just Enough Administration</span><span class="sxs-lookup"><span data-stu-id="8ddcc-113">[/jea/](https://docs.microsoft.com/powershell/jea/) is for the Just Enough Administration feature</span></span>
- <span data-ttu-id="8ddcc-114">[/Reference/](https://docs.microsoft.com/powershell/scripting/) jest przeznaczony dla tematów pojęciowych programu PowerShell i odwołania do modułu w wersjach 3.0, 4.0, 5.0, 5.1 i 6.0</span><span class="sxs-lookup"><span data-stu-id="8ddcc-114">[/reference/](https://docs.microsoft.com/powershell/scripting/) is for PowerShell conceptual topics and module reference across versions 3.0, 4.0, 5.0, 5.1, and 6.0</span></span>
  - <span data-ttu-id="8ddcc-115">Ta zawartość jest również źródło zawartości pomocy, pobierane przez `Get-Help` polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ddcc-115">This content is also the source of help content retrieved by the `Get-Help` cmdlet</span></span>
- <span data-ttu-id="8ddcc-116">[/WMF](https://docs.microsoft.com/powershell/wmf/readme) zawiera informacje o wersji dla Windows Management Framework, pakiet używane do rozpowszechniania nowe wersje programu PowerShell do poprzednich wersji systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-116">[/wmf](https://docs.microsoft.com/powershell/wmf/readme) contains release notes for the Windows Management Framework, the package used to distribute new versions of PowerShell to previous versions of Windows.</span></span>

## <a name="contributing"></a><span data-ttu-id="8ddcc-117">Współtworzenie</span><span class="sxs-lookup"><span data-stu-id="8ddcc-117">Contributing</span></span>

<span data-ttu-id="8ddcc-118">Firma Microsoft aktywnie scalanie wkład w repozytorium za pomocą [żądania ściągnięcia](https://help.github.com/articles/using-pull-requests/) do *przemieszczania* gałęzi.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-118">We actively merge contributions into this repository via [pull request](https://help.github.com/articles/using-pull-requests/) into the *staging* branch.</span></span>
<span data-ttu-id="8ddcc-119">Należy pamiętać, że zanim prześlesz żądanie ściągnięcia należy [podpisania umowy licencyjnej udziału](https://cla.microsoft.com/) aby upewnić się, że community jest bezpłatne korzystanie z materiałów przesłanych.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-119">Please note that before you submit a pull request you must [sign a Contribution License Agreement](https://cla.microsoft.com/) to ensure that the community is free to use your submissions.</span></span>

<span data-ttu-id="8ddcc-120">Aby uzyskać więcej informacji na temat przekazywania, przeczytaj nasze [przewodnika dla współautorów](CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="8ddcc-120">For more information on contributing, read our [contributor's guide](CONTRIBUTING.md).</span></span>
<span data-ttu-id="8ddcc-121">Przewodnik współautora zawiera szczegółowe informacje dotyczące sposobu współtworzenia dokumentacji, sugerowane narzędzi i stylu i formatowania wymagania.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-121">The contributor's guide contains detail information about how to contribute documentation, suggested tools, and style and formatting requirements.</span></span>
<span data-ttu-id="8ddcc-122">Użyj szablonów problemu i żądania ściągnięcia do zapewnienia dokumentacji spójny między wersjami.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-122">Please use the Issue and Pull Request templates to help keep documentation consistent across versions.</span></span>

## <a name="licenses"></a><span data-ttu-id="8ddcc-123">Licencje</span><span class="sxs-lookup"><span data-stu-id="8ddcc-123">Licenses</span></span>

<span data-ttu-id="8ddcc-124">Istnieją dwa pliki licencji dla tego projektu.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-124">There are two license files for this project.</span></span>
<span data-ttu-id="8ddcc-125">Licencja MIT dotyczy kod zawarty w tym repozytorium.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-125">The MIT License applies to the code contained in this repo.</span></span>
<span data-ttu-id="8ddcc-126">Licencja Creative Commons ma zastosowanie do dokumentacji.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-126">The Creative Commons license applies to the documentation.</span></span>