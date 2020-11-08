---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195276"
---
# <span data-ttu-id="405e3-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="405e3-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="405e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="405e3-102">SYNOPSIS</span></span>
<span data-ttu-id="405e3-103">Költségvetés eltávolítása előfizetésből vagy erőforráscsoportből</span><span class="sxs-lookup"><span data-stu-id="405e3-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="405e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="405e3-104">SYNTAX</span></span>

### <span data-ttu-id="405e3-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="405e3-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405e3-106">Csővezeték</span><span class="sxs-lookup"><span data-stu-id="405e3-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="405e3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="405e3-107">DESCRIPTION</span></span>
<span data-ttu-id="405e3-108">Az Remove-AzConsumptionBudget parancsmag egy előfizetésben vagy erőforráscsoportben távolítja el a költségvetést.</span><span class="sxs-lookup"><span data-stu-id="405e3-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="405e3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="405e3-109">EXAMPLES</span></span>

### <span data-ttu-id="405e3-110">1. példa: költségvetés eltávolítása költségvetés-névvel az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="405e3-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="405e3-111">2. példa: költségvetés eltávolítása költségvetés-névvel az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="405e3-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="405e3-112">3. példa: költségvetés eltávolítása a csővezetékek között az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="405e3-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="405e3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="405e3-113">PARAMETERS</span></span>

### <span data-ttu-id="405e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405e3-114">-DefaultProfile</span></span>
<span data-ttu-id="405e3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="405e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="405e3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="405e3-116">-InputObject</span></span>
<span data-ttu-id="405e3-117">Költségvetés objektum.</span><span class="sxs-lookup"><span data-stu-id="405e3-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="405e3-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="405e3-118">-Name</span></span>
<span data-ttu-id="405e3-119">A költségvetés neve</span><span class="sxs-lookup"><span data-stu-id="405e3-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="405e3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="405e3-120">-PassThru</span></span>
<span data-ttu-id="405e3-121">A parancsmag igaz értéket ad eredményül, ha egy költségvetést sikeresen eltávolítottak.</span><span class="sxs-lookup"><span data-stu-id="405e3-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="405e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="405e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="405e3-123">Egy költségvetés erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="405e3-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="405e3-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="405e3-124">-Confirm</span></span>
<span data-ttu-id="405e3-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="405e3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="405e3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="405e3-126">-WhatIf</span></span>
<span data-ttu-id="405e3-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="405e3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="405e3-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="405e3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="405e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405e3-129">CommonParameters</span></span>
<span data-ttu-id="405e3-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="405e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405e3-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="405e3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405e3-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="405e3-132">INPUTS</span></span>

### <span data-ttu-id="405e3-133">Microsoft. Azure. commands. fogyasztás. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="405e3-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="405e3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="405e3-134">OUTPUTS</span></span>

### <span data-ttu-id="405e3-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="405e3-135">System.Boolean</span></span>

## <span data-ttu-id="405e3-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="405e3-136">NOTES</span></span>

## <span data-ttu-id="405e3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="405e3-137">RELATED LINKS</span></span>