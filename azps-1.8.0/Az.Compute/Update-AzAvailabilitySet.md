---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836610"
---
# <span data-ttu-id="aba06-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aba06-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="aba06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aba06-102">SYNOPSIS</span></span>
<span data-ttu-id="aba06-103">Elérhetőségi készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="aba06-103">Updates an availability set.</span></span>

## <span data-ttu-id="aba06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aba06-104">SYNTAX</span></span>

### <span data-ttu-id="aba06-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="aba06-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba06-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="aba06-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba06-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aba06-107">DESCRIPTION</span></span>
<span data-ttu-id="aba06-108">Az **Update-AzAvailabilitySet** parancsmag egy elérhetőségi készletet frissít.</span><span class="sxs-lookup"><span data-stu-id="aba06-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="aba06-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aba06-109">EXAMPLES</span></span>

### <span data-ttu-id="aba06-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aba06-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="aba06-111">Ez a parancs frissíti a "ResourceGroup01" nevű erőforráscsoport "AvSet01" nevű elérhetőségi készletét egy felügyelt elérhetőségi készletre.</span><span class="sxs-lookup"><span data-stu-id="aba06-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="aba06-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aba06-112">PARAMETERS</span></span>

### <span data-ttu-id="aba06-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aba06-113">-AsJob</span></span>
<span data-ttu-id="aba06-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="aba06-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aba06-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aba06-115">-AvailabilitySet</span></span>
<span data-ttu-id="aba06-116">A frissítendő elérhetőségi készlet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aba06-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="aba06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba06-117">-DefaultProfile</span></span>
<span data-ttu-id="aba06-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aba06-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aba06-119">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="aba06-119">-Managed</span></span>
<span data-ttu-id="aba06-120">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="aba06-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba06-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="aba06-121">-Sku</span></span>
<span data-ttu-id="aba06-122">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="aba06-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba06-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="aba06-123">-Tag</span></span>
<span data-ttu-id="aba06-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="aba06-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="aba06-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aba06-125">-Confirm</span></span>
<span data-ttu-id="aba06-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aba06-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba06-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba06-127">-WhatIf</span></span>
<span data-ttu-id="aba06-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aba06-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aba06-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aba06-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba06-130">CommonParameters</span></span>
<span data-ttu-id="aba06-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aba06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba06-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba06-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba06-133">INPUTS</span></span>

### <span data-ttu-id="aba06-134">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aba06-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="aba06-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba06-135">OUTPUTS</span></span>

### <span data-ttu-id="aba06-136">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aba06-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="aba06-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aba06-137">NOTES</span></span>

## <span data-ttu-id="aba06-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aba06-138">RELATED LINKS</span></span>
