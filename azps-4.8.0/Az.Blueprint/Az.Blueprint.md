---
Module Name: Az.Blueprint
Module Guid: ef36c942-4a71-4e19-9450-05a35843deb6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.blueprint
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
ms.openlocfilehash: 1722032406a81253ebf580f79172be85aa23c55f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024194"
---
# <span data-ttu-id="d2fc5-101">Az. Blueprint modul</span><span class="sxs-lookup"><span data-stu-id="d2fc5-101">Az.Blueprint Module</span></span>
## <span data-ttu-id="d2fc5-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2fc5-102">Description</span></span>
<span data-ttu-id="d2fc5-103">A szakasz témakörei az Azure PowerShell-parancsmagokat az Azure Resource Manager keretrendszerben az Azure-tervezetekhez című témakörben dokumentálják.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-103">The topics in this section document the Azure PowerShell cmdlets for Azure Blueprints in the Azure Resource Manager framework.</span></span> <span data-ttu-id="d2fc5-104">A parancsmagok a Microsoft. Azure. PowerShell. parancsmagok. terv névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-104">The cmdlets exist in the Microsoft.Azure.PowerShell.Cmdlets.Blueprint namespace.</span></span>

## <span data-ttu-id="d2fc5-105">Az. Blueprint parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d2fc5-105">Az.Blueprint Cmdlets</span></span>
### [<span data-ttu-id="d2fc5-106">Exportálás – AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="d2fc5-106">Export-AzBlueprintWithArtifact</span></span>](Export-AzBlueprintWithArtifact.md)
<span data-ttu-id="d2fc5-107">A megadott terv-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-107">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

### [<span data-ttu-id="d2fc5-108">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d2fc5-108">Get-AzBlueprint</span></span>](Get-AzBlueprint.md)
<span data-ttu-id="d2fc5-109">Szerezzen be egy vagy több tervrajz meghatározását.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-109">Get one or more blueprint definitions.</span></span>

### [<span data-ttu-id="d2fc5-110">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="d2fc5-110">Get-AzBlueprintArtifact</span></span>](Get-AzBlueprintArtifact.md)
<span data-ttu-id="d2fc5-111">A tervrajz-definícióból származó leletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="d2fc5-111">Retrieve artifacts from a blueprint definition.</span></span>

### [<span data-ttu-id="d2fc5-112">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d2fc5-112">Get-AzBlueprintAssignment</span></span>](Get-AzBlueprintAssignment.md)
<span data-ttu-id="d2fc5-113">Szerezzen be egy vagy több feladatot a tervekhez.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-113">Get one or more blueprint assignments.</span></span>

### [<span data-ttu-id="d2fc5-114">Importálás – AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="d2fc5-114">Import-AzBlueprintWithArtifact</span></span>](Import-AzBlueprintWithArtifact.md)
<span data-ttu-id="d2fc5-115">A Blueprint-fájlt JSON formátumban importálhatja a Blueprint objektumba, és mentheti azt a megadott előfizetés vagy kezelési csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-115">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="d2fc5-116">Új – AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d2fc5-116">New-AzBlueprint</span></span>](New-AzBlueprint.md)
<span data-ttu-id="d2fc5-117">Hozzon létre egy új tervrajz-definíciót, és mentse azt a megadott előfizetés vagy kezelési csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-117">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="d2fc5-118">Új – AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="d2fc5-118">New-AzBlueprintArtifact</span></span>](New-AzBlueprintArtifact.md)
<span data-ttu-id="d2fc5-119">Hozzon létre egy új tárgyat, és mentse azt egy tervrajz-definíción belül.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-119">Create a new artifact and save it within a blueprint definition.</span></span>

### [<span data-ttu-id="d2fc5-120">Új – AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d2fc5-120">New-AzBlueprintAssignment</span></span>](New-AzBlueprintAssignment.md)
<span data-ttu-id="d2fc5-121">Tervrajz-definíció hozzárendelése előfizetéshez vagy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="d2fc5-121">Assign a blueprint definition to a subscription or a management group.</span></span>

### [<span data-ttu-id="d2fc5-122">Közzététel – AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d2fc5-122">Publish-AzBlueprint</span></span>](Publish-AzBlueprint.md)
<span data-ttu-id="d2fc5-123">A tervezet új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="d2fc5-123">Publish a new version of a blueprint.</span></span>

### [<span data-ttu-id="d2fc5-124">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d2fc5-124">Remove-AzBlueprintAssignment</span></span>](Remove-AzBlueprintAssignment.md)
<span data-ttu-id="d2fc5-125">Tervrajz-hozzárendelés eltávolítása egy előfizetésből vagy egy felügyeleti csoportból</span><span class="sxs-lookup"><span data-stu-id="d2fc5-125">Remove a blueprint assignment from a subscription or a management group.</span></span>

### [<span data-ttu-id="d2fc5-126">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d2fc5-126">Set-AzBlueprint</span></span>](Set-AzBlueprint.md)
<span data-ttu-id="d2fc5-127">A tervrajzok definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d2fc5-127">Update a blueprint definition.</span></span>

### [<span data-ttu-id="d2fc5-128">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="d2fc5-128">Set-AzBlueprintArtifact</span></span>](Set-AzBlueprintArtifact.md)
<span data-ttu-id="d2fc5-129">A tervrajz definíciójában lévő tárgy frissítése</span><span class="sxs-lookup"><span data-stu-id="d2fc5-129">Update an artifact in a blueprint definition.</span></span>

### [<span data-ttu-id="d2fc5-130">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d2fc5-130">Set-AzBlueprintAssignment</span></span>](Set-AzBlueprintAssignment.md)
<span data-ttu-id="d2fc5-131">Meglévő tervrajz-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="d2fc5-131">Update an existing blueprint assignment.</span></span>

