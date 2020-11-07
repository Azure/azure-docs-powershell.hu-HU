---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842442"
---
# <span data-ttu-id="376eb-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="376eb-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="376eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="376eb-102">SYNOPSIS</span></span>
<span data-ttu-id="376eb-103">Elérhetőségi készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="376eb-103">Updates an availability set.</span></span>

## <span data-ttu-id="376eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="376eb-104">SYNTAX</span></span>

### <span data-ttu-id="376eb-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="376eb-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376eb-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="376eb-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376eb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="376eb-107">DESCRIPTION</span></span>
<span data-ttu-id="376eb-108">Az **Update-AzAvailabilitySet** parancsmag egy elérhetőségi készletet frissít.</span><span class="sxs-lookup"><span data-stu-id="376eb-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="376eb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="376eb-109">EXAMPLES</span></span>

### <span data-ttu-id="376eb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="376eb-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="376eb-111">Ez a parancs frissíti a "ResourceGroup01" nevű erőforráscsoport "AvSet01" nevű elérhetőségi készletét egy felügyelt elérhetőségi készletre.</span><span class="sxs-lookup"><span data-stu-id="376eb-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="376eb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="376eb-112">PARAMETERS</span></span>

### <span data-ttu-id="376eb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="376eb-113">-AsJob</span></span>
<span data-ttu-id="376eb-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="376eb-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376eb-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="376eb-115">-AvailabilitySet</span></span>
<span data-ttu-id="376eb-116">A frissítendő elérhetőségi készlet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="376eb-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="376eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376eb-117">-DefaultProfile</span></span>
<span data-ttu-id="376eb-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="376eb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376eb-119">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="376eb-119">-Managed</span></span>
<span data-ttu-id="376eb-120">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="376eb-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="376eb-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="376eb-121">-Sku</span></span>
<span data-ttu-id="376eb-122">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="376eb-122">The Name of Sku</span></span>

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

### <span data-ttu-id="376eb-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="376eb-123">-Confirm</span></span>
<span data-ttu-id="376eb-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="376eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376eb-125">-WhatIf</span></span>
<span data-ttu-id="376eb-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="376eb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="376eb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="376eb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376eb-128">CommonParameters</span></span>
<span data-ttu-id="376eb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="376eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376eb-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376eb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376eb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="376eb-131">INPUTS</span></span>

### <span data-ttu-id="376eb-132">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="376eb-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="376eb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="376eb-133">OUTPUTS</span></span>

### <span data-ttu-id="376eb-134">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="376eb-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="376eb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="376eb-135">NOTES</span></span>

## <span data-ttu-id="376eb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="376eb-136">RELATED LINKS</span></span>

