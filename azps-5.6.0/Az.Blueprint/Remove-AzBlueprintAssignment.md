---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: f8a50a7e9686a3e40f517992e6c4de9912e8671b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925169"
---
# <span data-ttu-id="50d50-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="50d50-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="50d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d50-102">SYNOPSIS</span></span>
<span data-ttu-id="50d50-103">Tervrajz hozzárendelésének eltávolítása előfizetésből vagy felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="50d50-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="50d50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50d50-104">SYNTAX</span></span>

### <span data-ttu-id="50d50-105">BySubscriptionAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50d50-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d50-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="50d50-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d50-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="50d50-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50d50-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50d50-108">DESCRIPTION</span></span>
<span data-ttu-id="50d50-109">Távolítsa el az előfizetéshez hozzárendelt tervrajzot.</span><span class="sxs-lookup"><span data-stu-id="50d50-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="50d50-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50d50-110">EXAMPLES</span></span>

### <span data-ttu-id="50d50-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="50d50-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="50d50-112">Távolítsa el a névvel megadott tervrajz-hozzárendelést a megadott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="50d50-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="50d50-113">A parancsmag megerősítést kér a parancs végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="50d50-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="50d50-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50d50-114">PARAMETERS</span></span>

### <span data-ttu-id="50d50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d50-115">-DefaultProfile</span></span>
<span data-ttu-id="50d50-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50d50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50d50-117">-InputObject</span></span>
<span data-ttu-id="50d50-118">Blueprint assignment object.</span><span class="sxs-lookup"><span data-stu-id="50d50-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="50d50-119">-ManagementGroupId</span></span>
<span data-ttu-id="50d50-120">Annak a felügyeleti csoportnak az azonosítója, amelybe a Tervrajz feladatot mentette.</span><span class="sxs-lookup"><span data-stu-id="50d50-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50d50-121">-Name</span></span>
<span data-ttu-id="50d50-122">A terv feladatának neve.</span><span class="sxs-lookup"><span data-stu-id="50d50-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50d50-123">-PassThru</span></span>
<span data-ttu-id="50d50-124">Ha be van állítva, a parancsmag visszaadja az eltávolított Tervrajz hozzárendelést képviselő objektumot.</span><span class="sxs-lookup"><span data-stu-id="50d50-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="50d50-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="50d50-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50d50-126">-SubscriptionId</span></span>
<span data-ttu-id="50d50-127">Előfizetés azonosítója: A terv hozzárendelése telepítve van.</span><span class="sxs-lookup"><span data-stu-id="50d50-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50d50-128">-Confirm</span></span>
<span data-ttu-id="50d50-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50d50-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d50-130">-WhatIf</span></span>
<span data-ttu-id="50d50-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50d50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d50-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50d50-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d50-133">CommonParameters</span></span>
<span data-ttu-id="50d50-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d50-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50d50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d50-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50d50-136">INPUTS</span></span>

### <span data-ttu-id="50d50-137">System.String</span><span class="sxs-lookup"><span data-stu-id="50d50-137">System.String</span></span>

### <span data-ttu-id="50d50-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="50d50-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="50d50-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50d50-139">OUTPUTS</span></span>

### <span data-ttu-id="50d50-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="50d50-140">System.Object</span></span>
## <span data-ttu-id="50d50-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50d50-141">NOTES</span></span>

## <span data-ttu-id="50d50-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50d50-142">RELATED LINKS</span></span>
