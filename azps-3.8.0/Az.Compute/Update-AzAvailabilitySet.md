---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014592"
---
# <span data-ttu-id="3273f-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3273f-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="3273f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3273f-102">SYNOPSIS</span></span>
<span data-ttu-id="3273f-103">Elérhetőségi készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="3273f-103">Updates an availability set.</span></span>

## <span data-ttu-id="3273f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3273f-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3273f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3273f-105">DESCRIPTION</span></span>
<span data-ttu-id="3273f-106">Az **Update-AzAvailabilitySet** parancsmag egy elérhetőségi készletet frissít.</span><span class="sxs-lookup"><span data-stu-id="3273f-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="3273f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3273f-107">EXAMPLES</span></span>

### <span data-ttu-id="3273f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3273f-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="3273f-109">Ez a parancs frissíti a "ResourceGroup01" nevű erőforráscsoport "AvSet01" nevű elérhetőségi készletét egy felügyelt elérhetőségi készletre.</span><span class="sxs-lookup"><span data-stu-id="3273f-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="3273f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3273f-110">PARAMETERS</span></span>

### <span data-ttu-id="3273f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3273f-111">-AsJob</span></span>
<span data-ttu-id="3273f-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="3273f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3273f-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3273f-113">-AvailabilitySet</span></span>
<span data-ttu-id="3273f-114">A frissítendő elérhetőségi készlet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3273f-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3273f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3273f-115">-DefaultProfile</span></span>
<span data-ttu-id="3273f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3273f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3273f-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3273f-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3273f-118">Annak a közelségi helynek az erőforrás-azonosítója, amellyel az elérhetőségi készlet használható.</span><span class="sxs-lookup"><span data-stu-id="3273f-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="3273f-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="3273f-119">-Sku</span></span>
<span data-ttu-id="3273f-120">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="3273f-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273f-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="3273f-121">-Tag</span></span>
<span data-ttu-id="3273f-122">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3273f-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="3273f-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3273f-123">-Confirm</span></span>
<span data-ttu-id="3273f-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3273f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3273f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3273f-125">-WhatIf</span></span>
<span data-ttu-id="3273f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3273f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3273f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3273f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3273f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3273f-128">CommonParameters</span></span>
<span data-ttu-id="3273f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3273f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3273f-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3273f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3273f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3273f-131">INPUTS</span></span>

### <span data-ttu-id="3273f-132">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3273f-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="3273f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3273f-133">OUTPUTS</span></span>

### <span data-ttu-id="3273f-134">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3273f-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="3273f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3273f-135">NOTES</span></span>

## <span data-ttu-id="3273f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3273f-136">RELATED LINKS</span></span>
