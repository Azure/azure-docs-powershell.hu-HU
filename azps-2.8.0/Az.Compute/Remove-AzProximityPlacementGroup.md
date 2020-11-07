---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 2a3f4a6d386f37334908efde31332ed6137ecb74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667312"
---
# <span data-ttu-id="c35cc-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c35cc-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="c35cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c35cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c35cc-103">Törölje a közelségi hely erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c35cc-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="c35cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c35cc-104">SYNTAX</span></span>

### <span data-ttu-id="c35cc-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c35cc-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c35cc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c35cc-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c35cc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c35cc-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c35cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c35cc-108">DESCRIPTION</span></span>
<span data-ttu-id="c35cc-109">Ez a parancsmag a közelségi hely erőforrást fogja törölni.</span><span class="sxs-lookup"><span data-stu-id="c35cc-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="c35cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c35cc-110">EXAMPLES</span></span>

### <span data-ttu-id="c35cc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c35cc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="c35cc-112">Ez a parancs eltávolítja a megadott közelségi hely csoportját.</span><span class="sxs-lookup"><span data-stu-id="c35cc-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="c35cc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c35cc-113">PARAMETERS</span></span>

### <span data-ttu-id="c35cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c35cc-114">-AsJob</span></span>
<span data-ttu-id="c35cc-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c35cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c35cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35cc-116">-DefaultProfile</span></span>
<span data-ttu-id="c35cc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c35cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c35cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c35cc-118">-Force</span></span>
<span data-ttu-id="c35cc-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c35cc-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c35cc-120">-InputObject</span></span>
<span data-ttu-id="c35cc-121">A PS Proximity-elhelyezési csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="c35cc-121">The PS Proximity Placement Group Object</span></span>

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

### <span data-ttu-id="c35cc-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c35cc-122">-Name</span></span>
<span data-ttu-id="c35cc-123">A közelségi hely csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c35cc-123">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="c35cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="c35cc-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c35cc-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="c35cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c35cc-126">-ResourceId</span></span>
<span data-ttu-id="c35cc-127">A közelségi hely csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c35cc-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="c35cc-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c35cc-128">-Confirm</span></span>
<span data-ttu-id="c35cc-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c35cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c35cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c35cc-130">-WhatIf</span></span>
<span data-ttu-id="c35cc-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c35cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c35cc-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c35cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c35cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35cc-133">CommonParameters</span></span>
<span data-ttu-id="c35cc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c35cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35cc-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c35cc-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35cc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c35cc-136">INPUTS</span></span>

### <span data-ttu-id="c35cc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c35cc-137">System.String</span></span>

### <span data-ttu-id="c35cc-138">Microsoft. Azure. commands. számítási. Automation. models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c35cc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="c35cc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c35cc-139">OUTPUTS</span></span>

### <span data-ttu-id="c35cc-140">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c35cc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c35cc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c35cc-141">NOTES</span></span>

## <span data-ttu-id="c35cc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c35cc-142">RELATED LINKS</span></span>
