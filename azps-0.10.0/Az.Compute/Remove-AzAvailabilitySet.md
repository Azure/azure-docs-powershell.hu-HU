---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844434"
---
# <span data-ttu-id="e4192-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e4192-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="e4192-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4192-102">SYNOPSIS</span></span>
<span data-ttu-id="e4192-103">Az Azure-ról származó elérhetőségi készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e4192-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="e4192-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4192-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4192-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4192-105">DESCRIPTION</span></span>
<span data-ttu-id="e4192-106">A **Remove-AzAvailabilitySet** parancsmag az Azure-ról származó elérhetőségi készletet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="e4192-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="e4192-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4192-107">EXAMPLES</span></span>

### <span data-ttu-id="e4192-108">Példa 1: elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e4192-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e4192-109">Ez a parancs eltávolítja a ResourceGroup11 nevű erőforráscsoport AvailablitySet03 nevű elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="e4192-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e4192-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4192-110">PARAMETERS</span></span>

### <span data-ttu-id="e4192-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4192-111">-AsJob</span></span>
<span data-ttu-id="e4192-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e4192-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e4192-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4192-113">-DefaultProfile</span></span>
<span data-ttu-id="e4192-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4192-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4192-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4192-115">-Force</span></span>
<span data-ttu-id="e4192-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e4192-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4192-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4192-117">-Name</span></span>
<span data-ttu-id="e4192-118">Az elérhetőség beállítása név.</span><span class="sxs-lookup"><span data-stu-id="e4192-118">The availability set name.</span></span>

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

### <span data-ttu-id="e4192-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4192-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4192-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4192-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e4192-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4192-121">-Confirm</span></span>
<span data-ttu-id="e4192-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4192-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4192-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4192-123">-WhatIf</span></span>
<span data-ttu-id="e4192-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4192-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e4192-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4192-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4192-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4192-126">CommonParameters</span></span>
<span data-ttu-id="e4192-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4192-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4192-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4192-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4192-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4192-129">INPUTS</span></span>

### <span data-ttu-id="e4192-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4192-130">None</span></span>
<span data-ttu-id="e4192-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e4192-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4192-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4192-132">OUTPUTS</span></span>

### <span data-ttu-id="e4192-133">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4192-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e4192-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4192-134">NOTES</span></span>

## <span data-ttu-id="e4192-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4192-135">RELATED LINKS</span></span>

[<span data-ttu-id="e4192-136">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e4192-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e4192-137">Új – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e4192-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


