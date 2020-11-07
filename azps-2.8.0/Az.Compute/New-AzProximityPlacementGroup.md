---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: 88cdb68da94f84dc1af977ba5b12b5bfb4d73914
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667368"
---
# <span data-ttu-id="710da-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="710da-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="710da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="710da-102">SYNOPSIS</span></span>
<span data-ttu-id="710da-103">A közelségi hely létrehozása erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="710da-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="710da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="710da-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="710da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="710da-105">DESCRIPTION</span></span>
<span data-ttu-id="710da-106">Ezzel a parancsmaggal létrehozhatja a Proximity-csoport erőforrását.</span><span class="sxs-lookup"><span data-stu-id="710da-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="710da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="710da-107">EXAMPLES</span></span>

### <span data-ttu-id="710da-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="710da-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="710da-109">A parancs létrehoz egy Proximity-csoportot az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="710da-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="710da-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="710da-110">PARAMETERS</span></span>

### <span data-ttu-id="710da-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="710da-111">-AsJob</span></span>
<span data-ttu-id="710da-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="710da-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="710da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710da-113">-DefaultProfile</span></span>
<span data-ttu-id="710da-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="710da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="710da-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="710da-115">-Location</span></span>
<span data-ttu-id="710da-116">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="710da-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710da-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="710da-117">-Name</span></span>
<span data-ttu-id="710da-118">A közelségi hely csoport neve.</span><span class="sxs-lookup"><span data-stu-id="710da-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="710da-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="710da-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="710da-120">A közelségi hely csoport típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="710da-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="710da-121">A lehetséges értékek a következők: normál vagy Ultra</span><span class="sxs-lookup"><span data-stu-id="710da-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710da-122">-ResourceGroupName</span></span>
<span data-ttu-id="710da-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="710da-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="710da-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="710da-124">-Tag</span></span>
<span data-ttu-id="710da-125">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="710da-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710da-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="710da-126">-Confirm</span></span>
<span data-ttu-id="710da-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="710da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="710da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="710da-128">-WhatIf</span></span>
<span data-ttu-id="710da-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="710da-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="710da-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="710da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="710da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710da-131">CommonParameters</span></span>
<span data-ttu-id="710da-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="710da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710da-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="710da-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710da-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="710da-134">INPUTS</span></span>

### <span data-ttu-id="710da-135">System. String</span><span class="sxs-lookup"><span data-stu-id="710da-135">System.String</span></span>

## <span data-ttu-id="710da-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="710da-136">OUTPUTS</span></span>

### <span data-ttu-id="710da-137">Microsoft. Azure. commands. számítási. Automation. models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="710da-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="710da-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="710da-138">NOTES</span></span>

## <span data-ttu-id="710da-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="710da-139">RELATED LINKS</span></span>
