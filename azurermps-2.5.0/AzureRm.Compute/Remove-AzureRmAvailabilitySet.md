---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850093"
---
# <span data-ttu-id="a6520-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a6520-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="a6520-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6520-102">SYNOPSIS</span></span>
<span data-ttu-id="a6520-103">Az Azure-ról származó elérhetőségi készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a6520-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6520-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6520-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6520-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6520-105">DESCRIPTION</span></span>
<span data-ttu-id="a6520-106">A **Remove-AzureRmAvailabilitySet** parancsmag az Azure-ról származó elérhetőségi készletet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="a6520-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="a6520-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6520-107">EXAMPLES</span></span>

### <span data-ttu-id="a6520-108">Példa 1: elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a6520-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a6520-109">Ez a parancs eltávolítja a ResourceGroup11 nevű erőforráscsoport AvailablitySet03 nevű elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="a6520-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a6520-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6520-110">PARAMETERS</span></span>

### <span data-ttu-id="a6520-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6520-111">-AsJob</span></span>
<span data-ttu-id="a6520-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a6520-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6520-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6520-113">-DefaultProfile</span></span>
<span data-ttu-id="a6520-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6520-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6520-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6520-115">-Force</span></span>
<span data-ttu-id="a6520-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a6520-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a6520-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6520-117">-Name</span></span>
<span data-ttu-id="a6520-118">Az elérhetőség beállítása név.</span><span class="sxs-lookup"><span data-stu-id="a6520-118">The availability set name.</span></span>

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

### <span data-ttu-id="a6520-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6520-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6520-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6520-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a6520-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6520-121">-Confirm</span></span>
<span data-ttu-id="a6520-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6520-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6520-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6520-123">-WhatIf</span></span>
<span data-ttu-id="a6520-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6520-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a6520-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6520-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6520-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6520-126">CommonParameters</span></span>
<span data-ttu-id="a6520-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6520-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6520-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6520-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6520-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6520-129">INPUTS</span></span>

### <span data-ttu-id="a6520-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="a6520-130">None</span></span>
<span data-ttu-id="a6520-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a6520-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6520-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6520-132">OUTPUTS</span></span>

### <span data-ttu-id="a6520-133">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a6520-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a6520-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6520-134">NOTES</span></span>

## <span data-ttu-id="a6520-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6520-135">RELATED LINKS</span></span>

[<span data-ttu-id="a6520-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a6520-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="a6520-137">Új – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a6520-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


