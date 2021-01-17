---
Module Name: Az.Blueprint
Module Guid: ef36c942-4a71-4e19-9450-05a35843deb6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.blueprint
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
ms.openlocfilehash: 1722032406a81253ebf580f79172be85aa23c55f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478086"
---
# <span data-ttu-id="3088d-101">Az.Blueprint modul</span><span class="sxs-lookup"><span data-stu-id="3088d-101">Az.Blueprint Module</span></span>
## <span data-ttu-id="3088d-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="3088d-102">Description</span></span>
<span data-ttu-id="3088d-103">A szakasz témakörei az Azure Resource Manager-keretrendszer Azure PowerShell-parancsmagokat tartalmaznak az Azure-tervrajzokhoz.</span><span class="sxs-lookup"><span data-stu-id="3088d-103">The topics in this section document the Azure PowerShell cmdlets for Azure Blueprints in the Azure Resource Manager framework.</span></span> <span data-ttu-id="3088d-104">A parancsmagok a Microsoft.Azure.PowerShell.Cmdlets.Blueprint névterében találhatóak.</span><span class="sxs-lookup"><span data-stu-id="3088d-104">The cmdlets exist in the Microsoft.Azure.PowerShell.Cmdlets.Blueprint namespace.</span></span>

## <span data-ttu-id="3088d-105">Az.Blueprint parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3088d-105">Az.Blueprint Cmdlets</span></span>
### [<span data-ttu-id="3088d-106">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="3088d-106">Export-AzBlueprintWithArtifact</span></span>](Export-AzBlueprintWithArtifact.md)
<span data-ttu-id="3088d-107">A megadott tervrajz-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="3088d-107">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

### [<span data-ttu-id="3088d-108">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3088d-108">Get-AzBlueprint</span></span>](Get-AzBlueprint.md)
<span data-ttu-id="3088d-109">Lekért egy vagy több tervrajzdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="3088d-109">Get one or more blueprint definitions.</span></span>

### [<span data-ttu-id="3088d-110">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="3088d-110">Get-AzBlueprintArtifact</span></span>](Get-AzBlueprintArtifact.md)
<span data-ttu-id="3088d-111">Az összetevők lekérése a tervrajz-definícióból</span><span class="sxs-lookup"><span data-stu-id="3088d-111">Retrieve artifacts from a blueprint definition.</span></span>

### [<span data-ttu-id="3088d-112">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3088d-112">Get-AzBlueprintAssignment</span></span>](Get-AzBlueprintAssignment.md)
<span data-ttu-id="3088d-113">Egy vagy több terv-feladat kiosztása.</span><span class="sxs-lookup"><span data-stu-id="3088d-113">Get one or more blueprint assignments.</span></span>

### [<span data-ttu-id="3088d-114">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="3088d-114">Import-AzBlueprintWithArtifact</span></span>](Import-AzBlueprintWithArtifact.md)
<span data-ttu-id="3088d-115">Egy tervrajzfájlT JSON formátumban importálhat egy tervrajzobjektumba, és a megadott előfizetés vagy felügyeleti csoporton belül mentheti.</span><span class="sxs-lookup"><span data-stu-id="3088d-115">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="3088d-116">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3088d-116">New-AzBlueprint</span></span>](New-AzBlueprint.md)
<span data-ttu-id="3088d-117">Hozzon létre egy új tervrajz-definíciót, és mentse azt a megadott előfizetésen vagy felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="3088d-117">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="3088d-118">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="3088d-118">New-AzBlueprintArtifact</span></span>](New-AzBlueprintArtifact.md)
<span data-ttu-id="3088d-119">Hozzon létre egy új tárgyat, és mentse a tervrajz definíciójában.</span><span class="sxs-lookup"><span data-stu-id="3088d-119">Create a new artifact and save it within a blueprint definition.</span></span>

### [<span data-ttu-id="3088d-120">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3088d-120">New-AzBlueprintAssignment</span></span>](New-AzBlueprintAssignment.md)
<span data-ttu-id="3088d-121">Tervrajzdefiníció hozzárendelése előfizetéshez vagy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="3088d-121">Assign a blueprint definition to a subscription or a management group.</span></span>

### [<span data-ttu-id="3088d-122">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3088d-122">Publish-AzBlueprint</span></span>](Publish-AzBlueprint.md)
<span data-ttu-id="3088d-123">Közzéteheti egy tervrajz új verzióját.</span><span class="sxs-lookup"><span data-stu-id="3088d-123">Publish a new version of a blueprint.</span></span>

### [<span data-ttu-id="3088d-124">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3088d-124">Remove-AzBlueprintAssignment</span></span>](Remove-AzBlueprintAssignment.md)
<span data-ttu-id="3088d-125">Tervrajz hozzárendelésének eltávolítása előfizetésből vagy felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="3088d-125">Remove a blueprint assignment from a subscription or a management group.</span></span>

### [<span data-ttu-id="3088d-126">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3088d-126">Set-AzBlueprint</span></span>](Set-AzBlueprint.md)
<span data-ttu-id="3088d-127">A tervrajz definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="3088d-127">Update a blueprint definition.</span></span>

### [<span data-ttu-id="3088d-128">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="3088d-128">Set-AzBlueprintArtifact</span></span>](Set-AzBlueprintArtifact.md)
<span data-ttu-id="3088d-129">Egy tervrajzdefinícióban frissítsen egy tárgyat.</span><span class="sxs-lookup"><span data-stu-id="3088d-129">Update an artifact in a blueprint definition.</span></span>

### [<span data-ttu-id="3088d-130">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3088d-130">Set-AzBlueprintAssignment</span></span>](Set-AzBlueprintAssignment.md)
<span data-ttu-id="3088d-131">Frissítheti a meglévő terv-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="3088d-131">Update an existing blueprint assignment.</span></span>

