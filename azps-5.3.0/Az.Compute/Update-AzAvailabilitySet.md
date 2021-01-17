---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480687"
---
# <span data-ttu-id="3b412-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3b412-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="3b412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b412-102">SYNOPSIS</span></span>
<span data-ttu-id="3b412-103">Frissíti az elérhetőségi készletet.</span><span class="sxs-lookup"><span data-stu-id="3b412-103">Updates an availability set.</span></span>

## <span data-ttu-id="3b412-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b412-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b412-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b412-105">DESCRIPTION</span></span>
<span data-ttu-id="3b412-106">Az **Update-AzAvailabilitySet** parancsmag frissíti az elérhetőségi készletet.</span><span class="sxs-lookup"><span data-stu-id="3b412-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="3b412-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b412-107">EXAMPLES</span></span>

### <span data-ttu-id="3b412-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3b412-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="3b412-109">Ez a parancs egy felügyelt rendelkezésre állási készletre frissíti az "AvSet01" nevű elérhetőségi készletet az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3b412-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="3b412-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b412-110">PARAMETERS</span></span>

### <span data-ttu-id="3b412-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b412-111">-AsJob</span></span>
<span data-ttu-id="3b412-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="3b412-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3b412-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3b412-113">-AvailabilitySet</span></span>
<span data-ttu-id="3b412-114">Megadja a frissíthető rendelkezésre állási halmaz-objektumot.</span><span class="sxs-lookup"><span data-stu-id="3b412-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="3b412-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b412-115">-DefaultProfile</span></span>
<span data-ttu-id="3b412-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b412-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b412-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3b412-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3b412-118">Az elérhetőségi készlethez használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3b412-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="3b412-119">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="3b412-119">-Sku</span></span>
<span data-ttu-id="3b412-120">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="3b412-120">The Name of Sku</span></span>

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

### <span data-ttu-id="3b412-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b412-121">-Tag</span></span>
<span data-ttu-id="3b412-122">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="3b412-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="3b412-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b412-123">-Confirm</span></span>
<span data-ttu-id="3b412-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3b412-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b412-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b412-125">-WhatIf</span></span>
<span data-ttu-id="3b412-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3b412-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b412-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b412-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b412-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b412-128">CommonParameters</span></span>
<span data-ttu-id="3b412-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b412-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b412-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b412-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b412-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b412-131">INPUTS</span></span>

### <span data-ttu-id="3b412-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3b412-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="3b412-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b412-133">OUTPUTS</span></span>

### <span data-ttu-id="3b412-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3b412-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="3b412-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b412-135">NOTES</span></span>

## <span data-ttu-id="3b412-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b412-136">RELATED LINKS</span></span>
