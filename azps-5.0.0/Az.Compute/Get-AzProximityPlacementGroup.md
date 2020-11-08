---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194790"
---
# <span data-ttu-id="a7beb-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a7beb-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="a7beb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7beb-102">SYNOPSIS</span></span>
<span data-ttu-id="a7beb-103">Beolvashatja vagy listázhatja a Proximity-hely erőforrás (oka) t.</span><span class="sxs-lookup"><span data-stu-id="a7beb-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="a7beb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7beb-104">SYNTAX</span></span>

### <span data-ttu-id="a7beb-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7beb-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7beb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a7beb-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7beb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7beb-107">DESCRIPTION</span></span>
<span data-ttu-id="a7beb-108">Ez a parancsmag beolvassa vagy listázhatja a közelségi hely erőforrás (oka) t.</span><span class="sxs-lookup"><span data-stu-id="a7beb-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="a7beb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a7beb-109">EXAMPLES</span></span>

### <span data-ttu-id="a7beb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a7beb-110">Example 1</span></span>
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

<span data-ttu-id="a7beb-111">Ez a parancs a közelségi elhelyezés csoportba kerül</span><span class="sxs-lookup"><span data-stu-id="a7beb-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="a7beb-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a7beb-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="a7beb-113">Ebben a parancsban a megadott erőforráscsoport alatti közelségi elhelyezési csoportok jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="a7beb-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="a7beb-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="a7beb-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="a7beb-115">Ez a parancs az előfizetésben az összes Proximity-elhelyezési csoportot felsorolja.</span><span class="sxs-lookup"><span data-stu-id="a7beb-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="a7beb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7beb-116">PARAMETERS</span></span>

### <span data-ttu-id="a7beb-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="a7beb-117">-ColocationStatus</span></span>
<span data-ttu-id="a7beb-118">Egy erőforrás helybeli állapotát jeleníti meg a közelségi hely csoportban.</span><span class="sxs-lookup"><span data-stu-id="a7beb-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="a7beb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7beb-119">-DefaultProfile</span></span>
<span data-ttu-id="a7beb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7beb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7beb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7beb-121">-Name</span></span>
<span data-ttu-id="a7beb-122">A közelségi hely csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a7beb-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="a7beb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7beb-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7beb-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a7beb-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7beb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7beb-125">-ResourceId</span></span>
<span data-ttu-id="a7beb-126">A közelségi hely csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a7beb-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="a7beb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7beb-127">CommonParameters</span></span>
<span data-ttu-id="a7beb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7beb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7beb-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7beb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7beb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7beb-130">INPUTS</span></span>

### <span data-ttu-id="a7beb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a7beb-131">System.String</span></span>

## <span data-ttu-id="a7beb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7beb-132">OUTPUTS</span></span>

### <span data-ttu-id="a7beb-133">Microsoft. Azure. commands. számítási. Automation. models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a7beb-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="a7beb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7beb-134">NOTES</span></span>

## <span data-ttu-id="a7beb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7beb-135">RELATED LINKS</span></span>
