---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186097"
---
# <span data-ttu-id="ac5ab-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="ac5ab-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="ac5ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5ab-103">Tervrajz-hozzárendelés eltávolítása egy előfizetésből vagy egy felügyeleti csoportból</span><span class="sxs-lookup"><span data-stu-id="ac5ab-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="ac5ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac5ab-104">SYNTAX</span></span>

### <span data-ttu-id="ac5ab-105">BySubscriptionAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac5ab-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5ab-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="ac5ab-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5ab-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="ac5ab-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5ab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac5ab-108">DESCRIPTION</span></span>
<span data-ttu-id="ac5ab-109">Előfizetéshez rendelt tervrajz eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ac5ab-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="ac5ab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ac5ab-110">EXAMPLES</span></span>

### <span data-ttu-id="ac5ab-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac5ab-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="ac5ab-112">A megadott előfizetésből megadott név alapján megadott Blueprint-hozzárendelés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="ac5ab-113">A parancsmag a parancs végrehajtása előtt kérni fogja a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="ac5ab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac5ab-114">PARAMETERS</span></span>

### <span data-ttu-id="ac5ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5ab-115">-DefaultProfile</span></span>
<span data-ttu-id="ac5ab-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5ab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac5ab-117">-InputObject</span></span>
<span data-ttu-id="ac5ab-118">Terv hozzárendelés-objektuma.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="ac5ab-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ac5ab-119">-ManagementGroupId</span></span>
<span data-ttu-id="ac5ab-120">Annak a kezelési csoportnak az azonosítója, amelybe a Blueprint-hozzárendelést mentette.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="ac5ab-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac5ab-121">-Name</span></span>
<span data-ttu-id="ac5ab-122">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="ac5ab-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac5ab-123">-PassThru</span></span>
<span data-ttu-id="ac5ab-124">Ha be van állítva, a parancsmag egy olyan objektumot ad vissza, amely az eltávolított terv hozzárendelését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="ac5ab-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac5ab-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac5ab-126">-SubscriptionId</span></span>
<span data-ttu-id="ac5ab-127">Előfizetés azonosítója: a terv-hozzárendelés üzembe helyezése.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="ac5ab-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac5ab-128">-Confirm</span></span>
<span data-ttu-id="ac5ab-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5ab-130">-WhatIf</span></span>
<span data-ttu-id="ac5ab-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5ab-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5ab-133">CommonParameters</span></span>
<span data-ttu-id="ac5ab-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac5ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5ab-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac5ab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5ab-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac5ab-136">INPUTS</span></span>

### <span data-ttu-id="ac5ab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ac5ab-137">System.String</span></span>

### <span data-ttu-id="ac5ab-138">Microsoft. Azure. commands. Blueprint. models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="ac5ab-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="ac5ab-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac5ab-139">OUTPUTS</span></span>

### <span data-ttu-id="ac5ab-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ac5ab-140">System.Object</span></span>
## <span data-ttu-id="ac5ab-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac5ab-141">NOTES</span></span>

## <span data-ttu-id="ac5ab-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac5ab-142">RELATED LINKS</span></span>
