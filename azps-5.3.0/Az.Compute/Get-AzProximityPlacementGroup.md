---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477830"
---
# <span data-ttu-id="1c334-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1c334-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="1c334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c334-102">SYNOPSIS</span></span>
<span data-ttu-id="1c334-103">Közelítési elhelyezési csoporterőforrás(ak) be- vagy listába való be- vagy listába hozása</span><span class="sxs-lookup"><span data-stu-id="1c334-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="1c334-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c334-104">SYNTAX</span></span>

### <span data-ttu-id="1c334-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c334-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c334-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1c334-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c334-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c334-107">DESCRIPTION</span></span>
<span data-ttu-id="1c334-108">Ez a parancsmag be fogja szerezni vagy listába sorolja a Közelség elhelyezési csoport erőforrás(ak)t.</span><span class="sxs-lookup"><span data-stu-id="1c334-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="1c334-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c334-109">EXAMPLES</span></span>

### <span data-ttu-id="1c334-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="1c334-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="1c334-111">Ez a parancs a közelség elhelyezési csoportját kapja</span><span class="sxs-lookup"><span data-stu-id="1c334-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="1c334-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1c334-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="1c334-113">Ez a parancs felsorolja az adott erőforráscsoporton belül az összes közeli elhelyezési csoportot.</span><span class="sxs-lookup"><span data-stu-id="1c334-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="1c334-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="1c334-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="1c334-115">Ez a parancs felsorolja az előfizetéshez közeli elhelyezési csoportokat.</span><span class="sxs-lookup"><span data-stu-id="1c334-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="1c334-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c334-116">PARAMETERS</span></span>

### <span data-ttu-id="1c334-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="1c334-117">-ColocationStatus</span></span>
<span data-ttu-id="1c334-118">Egy erőforrás áthelyezési állapotát jeleníti meg a közelítési elhelyezési csoportban.</span><span class="sxs-lookup"><span data-stu-id="1c334-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c334-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c334-119">-DefaultProfile</span></span>
<span data-ttu-id="1c334-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c334-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c334-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c334-121">-Name</span></span>
<span data-ttu-id="1c334-122">A közelítési elhelyezési csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c334-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1c334-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c334-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c334-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c334-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1c334-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c334-125">-ResourceId</span></span>
<span data-ttu-id="1c334-126">A közelítés elhelyezési csoportjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c334-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="1c334-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c334-127">CommonParameters</span></span>
<span data-ttu-id="1c334-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c334-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c334-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c334-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c334-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c334-130">INPUTS</span></span>

### <span data-ttu-id="1c334-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1c334-131">System.String</span></span>

## <span data-ttu-id="1c334-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c334-132">OUTPUTS</span></span>

### <span data-ttu-id="1c334-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1c334-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="1c334-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c334-134">NOTES</span></span>

## <span data-ttu-id="1c334-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c334-135">RELATED LINKS</span></span>
