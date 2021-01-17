---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481007"
---
# <span data-ttu-id="f9577-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="f9577-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="f9577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9577-102">SYNOPSIS</span></span>
<span data-ttu-id="f9577-103">Költségvetés eltávolítása előfizetésből vagy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="f9577-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f9577-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9577-104">SYNTAX</span></span>

### <span data-ttu-id="f9577-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9577-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9577-106">Pipázás</span><span class="sxs-lookup"><span data-stu-id="f9577-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9577-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9577-107">DESCRIPTION</span></span>
<span data-ttu-id="f9577-108">A Remove-AzConsumptionBudget parancsmag eltávolítja a költségvetést egy előfizetésből vagy egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="f9577-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f9577-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9577-109">EXAMPLES</span></span>

### <span data-ttu-id="f9577-110">1. példa: Költségvetés eltávolítása előfizetési szinten egy költségvetésnévvel</span><span class="sxs-lookup"><span data-stu-id="f9577-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="f9577-111">2. példa: Költségvetés eltávolítása egy költségvetésnévvel az erőforráscsoport szintjén</span><span class="sxs-lookup"><span data-stu-id="f9577-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="f9577-112">3. példa: Költségvetés eltávolítása a pipázáson keresztül előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="f9577-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="f9577-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9577-113">PARAMETERS</span></span>

### <span data-ttu-id="f9577-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9577-114">-DefaultProfile</span></span>
<span data-ttu-id="f9577-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9577-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9577-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9577-116">-InputObject</span></span>
<span data-ttu-id="f9577-117">Budget objektum.</span><span class="sxs-lookup"><span data-stu-id="f9577-117">Budget object.</span></span>

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

### <span data-ttu-id="f9577-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f9577-118">-Name</span></span>
<span data-ttu-id="f9577-119">A költségvetés neve.</span><span class="sxs-lookup"><span data-stu-id="f9577-119">Name of a budget.</span></span>

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

### <span data-ttu-id="f9577-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9577-120">-PassThru</span></span>
<span data-ttu-id="f9577-121">A parancsmag igaz értéket ad vissza, ha a költségvetés eltávolítása sikerült.</span><span class="sxs-lookup"><span data-stu-id="f9577-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="f9577-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9577-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9577-123">Költségvetés erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="f9577-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="f9577-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9577-124">-Confirm</span></span>
<span data-ttu-id="f9577-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9577-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9577-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9577-126">-WhatIf</span></span>
<span data-ttu-id="f9577-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9577-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9577-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9577-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9577-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9577-129">CommonParameters</span></span>
<span data-ttu-id="f9577-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9577-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9577-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9577-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9577-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9577-132">INPUTS</span></span>

### <span data-ttu-id="f9577-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="f9577-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="f9577-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9577-134">OUTPUTS</span></span>

### <span data-ttu-id="f9577-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9577-135">System.Boolean</span></span>

## <span data-ttu-id="f9577-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9577-136">NOTES</span></span>

## <span data-ttu-id="f9577-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9577-137">RELATED LINKS</span></span>
