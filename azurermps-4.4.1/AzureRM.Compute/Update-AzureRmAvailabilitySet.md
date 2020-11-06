---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505132"
---
# <span data-ttu-id="e1ca6-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e1ca6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ca6-103">Elérhetőségi készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="e1ca6-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ca6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1ca6-104">SYNTAX</span></span>

### <span data-ttu-id="e1ca6-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ca6-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ca6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1ca6-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ca6-108">Az **Update-AzureRmAvailabilitySet** parancsmag egy elérhetőségi készletet frissít.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="e1ca6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1ca6-109">EXAMPLES</span></span>

### <span data-ttu-id="e1ca6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1ca6-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="e1ca6-111">Ez a parancs frissíti a "ResourceGroup01" nevű erőforráscsoport "AvSet01" nevű elérhetőségi készletét egy felügyelt elérhetőségi készletre.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="e1ca6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1ca6-112">PARAMETERS</span></span>

### <span data-ttu-id="e1ca6-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-113">-AvailabilitySet</span></span>
<span data-ttu-id="e1ca6-114">A frissítendő elérhetőségi készlet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="e1ca6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ca6-115">-DefaultProfile</span></span>
<span data-ttu-id="e1ca6-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ca6-117">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="e1ca6-117">-Managed</span></span>
<span data-ttu-id="e1ca6-118">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-118">Managed Availability Set</span></span>

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

### <span data-ttu-id="e1ca6-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="e1ca6-119">-Sku</span></span>
<span data-ttu-id="e1ca6-120">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="e1ca6-120">The Name of Sku</span></span>

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

### <span data-ttu-id="e1ca6-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1ca6-121">-Confirm</span></span>
<span data-ttu-id="e1ca6-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ca6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ca6-123">-WhatIf</span></span>
<span data-ttu-id="e1ca6-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1ca6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1ca6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ca6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ca6-126">CommonParameters</span></span>
<span data-ttu-id="e1ca6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1ca6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ca6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ca6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ca6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ca6-129">INPUTS</span></span>

### <span data-ttu-id="e1ca6-130">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e1ca6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ca6-131">OUTPUTS</span></span>

### <span data-ttu-id="e1ca6-132">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1ca6-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e1ca6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1ca6-133">NOTES</span></span>

## <span data-ttu-id="e1ca6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1ca6-134">RELATED LINKS</span></span>

