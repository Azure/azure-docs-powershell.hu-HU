---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493189"
---
# <span data-ttu-id="9dd33-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9dd33-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="9dd33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dd33-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd33-103">Az Azure-ról származó elérhetőségi készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9dd33-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dd33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dd33-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dd33-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd33-106">A **Remove-AzureRmAvailabilitySet** parancsmag az Azure-ról származó elérhetőségi készletet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="9dd33-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="9dd33-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9dd33-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd33-108">Példa 1: elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9dd33-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9dd33-109">Ez a parancs eltávolítja a ResourceGroup11 nevű erőforráscsoport AvailablitySet03 nevű elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="9dd33-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9dd33-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dd33-110">PARAMETERS</span></span>

### <span data-ttu-id="9dd33-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9dd33-111">-Force</span></span>
<span data-ttu-id="9dd33-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9dd33-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd33-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dd33-113">-Name</span></span>
<span data-ttu-id="9dd33-114">Az elérhetőség beállítása név.</span><span class="sxs-lookup"><span data-stu-id="9dd33-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd33-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd33-115">-ResourceGroupName</span></span>
<span data-ttu-id="9dd33-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dd33-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd33-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9dd33-117">-Confirm</span></span>
<span data-ttu-id="9dd33-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9dd33-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd33-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd33-119">-WhatIf</span></span>
<span data-ttu-id="9dd33-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9dd33-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9dd33-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dd33-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd33-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd33-122">CommonParameters</span></span>
<span data-ttu-id="9dd33-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dd33-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd33-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd33-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd33-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dd33-125">INPUTS</span></span>

### <span data-ttu-id="9dd33-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9dd33-126">None</span></span>
<span data-ttu-id="9dd33-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9dd33-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9dd33-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dd33-128">OUTPUTS</span></span>

## <span data-ttu-id="9dd33-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dd33-129">NOTES</span></span>

## <span data-ttu-id="9dd33-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dd33-130">RELATED LINKS</span></span>

[<span data-ttu-id="9dd33-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9dd33-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="9dd33-132">Új – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9dd33-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


