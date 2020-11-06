---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492345"
---
# <span data-ttu-id="22469-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22469-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="22469-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22469-102">SYNOPSIS</span></span>
<span data-ttu-id="22469-103">Elérhetőségi készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="22469-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22469-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22469-104">SYNTAX</span></span>

### <span data-ttu-id="22469-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="22469-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22469-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="22469-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22469-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="22469-107">DESCRIPTION</span></span>
<span data-ttu-id="22469-108">Az **Update-AzureRmAvailabilitySet** parancsmag egy elérhetőségi készletet frissít.</span><span class="sxs-lookup"><span data-stu-id="22469-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="22469-109">Példák</span><span class="sxs-lookup"><span data-stu-id="22469-109">EXAMPLES</span></span>

### <span data-ttu-id="22469-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="22469-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="22469-111">Ez a parancs frissíti a "ResourceGroup01" nevű erőforráscsoport "AvSet01" nevű elérhetőségi készletét egy felügyelt elérhetőségi készletre.</span><span class="sxs-lookup"><span data-stu-id="22469-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="22469-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22469-112">PARAMETERS</span></span>

### <span data-ttu-id="22469-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22469-113">-AvailabilitySet</span></span>
<span data-ttu-id="22469-114">A frissítendő elérhetőségi készlet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22469-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22469-115">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="22469-115">-Managed</span></span>
<span data-ttu-id="22469-116">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="22469-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22469-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="22469-117">-Sku</span></span>
<span data-ttu-id="22469-118">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="22469-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22469-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22469-119">-Confirm</span></span>
<span data-ttu-id="22469-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22469-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22469-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22469-121">-WhatIf</span></span>
<span data-ttu-id="22469-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22469-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22469-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22469-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22469-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22469-124">CommonParameters</span></span>
<span data-ttu-id="22469-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22469-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22469-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22469-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22469-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22469-127">INPUTS</span></span>

### <span data-ttu-id="22469-128">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22469-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="22469-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22469-129">OUTPUTS</span></span>

### <span data-ttu-id="22469-130">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22469-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="22469-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22469-131">NOTES</span></span>

## <span data-ttu-id="22469-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22469-132">RELATED LINKS</span></span>

