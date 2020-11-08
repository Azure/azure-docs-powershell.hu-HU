---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018122"
---
# <span data-ttu-id="91a9c-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91a9c-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="91a9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="91a9c-103">Az Azure-ról származó elérhetőségi készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="91a9c-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="91a9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91a9c-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91a9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="91a9c-106">A **Remove-AzAvailabilitySet** parancsmag az Azure-ról származó elérhetőségi készletet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="91a9c-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="91a9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="91a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="91a9c-108">Példa 1: elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="91a9c-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="91a9c-109">Ez a parancs eltávolítja a ResourceGroup11 nevű erőforráscsoport AvailabilitySet03 nevű elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="91a9c-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="91a9c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="91a9c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91a9c-111">-AsJob</span></span>
<span data-ttu-id="91a9c-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="91a9c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="91a9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a9c-113">-DefaultProfile</span></span>
<span data-ttu-id="91a9c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91a9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91a9c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="91a9c-115">-Force</span></span>
<span data-ttu-id="91a9c-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="91a9c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a9c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91a9c-117">-Name</span></span>
<span data-ttu-id="91a9c-118">Az elérhetőség beállítása név.</span><span class="sxs-lookup"><span data-stu-id="91a9c-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="91a9c-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a9c-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a9c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91a9c-121">-Confirm</span></span>
<span data-ttu-id="91a9c-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91a9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a9c-123">-WhatIf</span></span>
<span data-ttu-id="91a9c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91a9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91a9c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91a9c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a9c-126">CommonParameters</span></span>
<span data-ttu-id="91a9c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91a9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a9c-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91a9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a9c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a9c-129">INPUTS</span></span>

### <span data-ttu-id="91a9c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="91a9c-130">System.String</span></span>

## <span data-ttu-id="91a9c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a9c-131">OUTPUTS</span></span>

### <span data-ttu-id="91a9c-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="91a9c-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="91a9c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91a9c-133">NOTES</span></span>

## <span data-ttu-id="91a9c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91a9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="91a9c-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91a9c-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="91a9c-136">Új – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91a9c-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


