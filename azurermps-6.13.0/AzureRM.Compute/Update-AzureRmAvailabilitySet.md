---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499663"
---
# <span data-ttu-id="b40df-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b40df-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="b40df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b40df-102">SYNOPSIS</span></span>
<span data-ttu-id="b40df-103">Elérhetőségi készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="b40df-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b40df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b40df-104">SYNTAX</span></span>

### <span data-ttu-id="b40df-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="b40df-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b40df-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="b40df-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b40df-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b40df-107">DESCRIPTION</span></span>
<span data-ttu-id="b40df-108">Az **Update-AzureRmAvailabilitySet** parancsmag egy elérhetőségi készletet frissít.</span><span class="sxs-lookup"><span data-stu-id="b40df-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="b40df-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b40df-109">EXAMPLES</span></span>

### <span data-ttu-id="b40df-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b40df-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="b40df-111">Ez a parancs frissíti a "ResourceGroup01" nevű erőforráscsoport "AvSet01" nevű elérhetőségi készletét egy felügyelt elérhetőségi készletre.</span><span class="sxs-lookup"><span data-stu-id="b40df-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="b40df-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b40df-112">PARAMETERS</span></span>

### <span data-ttu-id="b40df-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b40df-113">-AsJob</span></span>
<span data-ttu-id="b40df-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b40df-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b40df-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b40df-115">-AvailabilitySet</span></span>
<span data-ttu-id="b40df-116">A frissítendő elérhetőségi készlet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b40df-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="b40df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40df-117">-DefaultProfile</span></span>
<span data-ttu-id="b40df-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b40df-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40df-119">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="b40df-119">-Managed</span></span>
<span data-ttu-id="b40df-120">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="b40df-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="b40df-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="b40df-121">-Sku</span></span>
<span data-ttu-id="b40df-122">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="b40df-122">The Name of Sku</span></span>

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

### <span data-ttu-id="b40df-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="b40df-123">-Tag</span></span>
<span data-ttu-id="b40df-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b40df-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="b40df-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b40df-125">-Confirm</span></span>
<span data-ttu-id="b40df-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b40df-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b40df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b40df-127">-WhatIf</span></span>
<span data-ttu-id="b40df-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b40df-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b40df-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b40df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b40df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40df-130">CommonParameters</span></span>
<span data-ttu-id="b40df-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b40df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40df-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b40df-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40df-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b40df-133">INPUTS</span></span>

### <span data-ttu-id="b40df-134">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b40df-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b40df-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b40df-135">OUTPUTS</span></span>

### <span data-ttu-id="b40df-136">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b40df-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b40df-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b40df-137">NOTES</span></span>

## <span data-ttu-id="b40df-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b40df-138">RELATED LINKS</span></span>
