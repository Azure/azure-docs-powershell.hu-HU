---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847621"
---
# <span data-ttu-id="79019-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="79019-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="79019-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79019-102">SYNOPSIS</span></span>
<span data-ttu-id="79019-103">Törölje a közelségi hely erőforrást.</span><span class="sxs-lookup"><span data-stu-id="79019-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="79019-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79019-104">SYNTAX</span></span>

### <span data-ttu-id="79019-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79019-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79019-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="79019-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79019-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="79019-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79019-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="79019-108">DESCRIPTION</span></span>
<span data-ttu-id="79019-109">Ez a parancsmag a közelségi hely erőforrást fogja törölni.</span><span class="sxs-lookup"><span data-stu-id="79019-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="79019-110">Példák</span><span class="sxs-lookup"><span data-stu-id="79019-110">EXAMPLES</span></span>

### <span data-ttu-id="79019-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="79019-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="79019-112">Ez a parancs eltávolítja a megadott közelségi hely csoportját.</span><span class="sxs-lookup"><span data-stu-id="79019-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="79019-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79019-113">PARAMETERS</span></span>

### <span data-ttu-id="79019-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79019-114">-AsJob</span></span>
<span data-ttu-id="79019-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="79019-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79019-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79019-116">-DefaultProfile</span></span>
<span data-ttu-id="79019-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79019-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79019-118">-Force</span><span class="sxs-lookup"><span data-stu-id="79019-118">-Force</span></span>
<span data-ttu-id="79019-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="79019-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79019-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79019-120">-InputObject</span></span>
<span data-ttu-id="79019-121">A PS Proximity-elhelyezési csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="79019-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79019-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79019-122">-Name</span></span>
<span data-ttu-id="79019-123">A közelségi hely csoport neve.</span><span class="sxs-lookup"><span data-stu-id="79019-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79019-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79019-124">-ResourceGroupName</span></span>
<span data-ttu-id="79019-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79019-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79019-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79019-126">-ResourceId</span></span>
<span data-ttu-id="79019-127">A közelségi hely csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="79019-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79019-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79019-128">-Confirm</span></span>
<span data-ttu-id="79019-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79019-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79019-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79019-130">-WhatIf</span></span>
<span data-ttu-id="79019-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79019-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79019-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79019-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79019-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79019-133">CommonParameters</span></span>
<span data-ttu-id="79019-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79019-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79019-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="79019-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79019-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79019-136">INPUTS</span></span>

### <span data-ttu-id="79019-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79019-137">System.String</span></span>

### <span data-ttu-id="79019-138">Microsoft. Azure. commands. számítási. Automation. models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="79019-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="79019-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79019-139">OUTPUTS</span></span>

### <span data-ttu-id="79019-140">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="79019-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="79019-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79019-141">NOTES</span></span>

## <span data-ttu-id="79019-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79019-142">RELATED LINKS</span></span>
