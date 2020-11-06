---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502168"
---
# <span data-ttu-id="79219-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="79219-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="79219-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79219-102">SYNOPSIS</span></span>
<span data-ttu-id="79219-103">Költségvetés eltávolítása előfizetésből vagy erőforráscsoportből</span><span class="sxs-lookup"><span data-stu-id="79219-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79219-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79219-104">SYNTAX</span></span>

### <span data-ttu-id="79219-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79219-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79219-106">Csővezeték</span><span class="sxs-lookup"><span data-stu-id="79219-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79219-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="79219-107">DESCRIPTION</span></span>
<span data-ttu-id="79219-108">Az Remove-AzureRmConsumptionBudget parancsmag egy előfizetésben vagy erőforráscsoportben távolítja el a költségvetést.</span><span class="sxs-lookup"><span data-stu-id="79219-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="79219-109">Példák</span><span class="sxs-lookup"><span data-stu-id="79219-109">EXAMPLES</span></span>

### <span data-ttu-id="79219-110">1. példa: költségvetés eltávolítása költségvetés-névvel az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="79219-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="79219-111">2. példa: költségvetés eltávolítása költségvetés-névvel az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="79219-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="79219-112">3. példa: költségvetés eltávolítása a csővezetékek között az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="79219-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="79219-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79219-113">PARAMETERS</span></span>

### <span data-ttu-id="79219-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79219-114">-DefaultProfile</span></span>
<span data-ttu-id="79219-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79219-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79219-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79219-116">-InputObject</span></span>
<span data-ttu-id="79219-117">Költségvetés objektum.</span><span class="sxs-lookup"><span data-stu-id="79219-117">Budget object.</span></span>

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

### <span data-ttu-id="79219-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79219-118">-Name</span></span>
<span data-ttu-id="79219-119">A költségvetés neve</span><span class="sxs-lookup"><span data-stu-id="79219-119">Name of a budget.</span></span>

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

### <span data-ttu-id="79219-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79219-120">-PassThru</span></span>
<span data-ttu-id="79219-121">A parancsmag igaz értéket ad eredményül, ha egy költségvetést sikeresen eltávolítottak.</span><span class="sxs-lookup"><span data-stu-id="79219-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="79219-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79219-122">-ResourceGroupName</span></span>
<span data-ttu-id="79219-123">Egy költségvetés erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="79219-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="79219-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79219-124">-Confirm</span></span>
<span data-ttu-id="79219-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79219-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79219-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79219-126">-WhatIf</span></span>
<span data-ttu-id="79219-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79219-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79219-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79219-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79219-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79219-129">CommonParameters</span></span>
<span data-ttu-id="79219-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79219-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79219-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79219-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79219-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79219-132">INPUTS</span></span>

### <span data-ttu-id="79219-133">Microsoft. Azure. commands. fogyasztás. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="79219-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="79219-134">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79219-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="79219-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79219-135">OUTPUTS</span></span>

### <span data-ttu-id="79219-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79219-136">System.Boolean</span></span>

## <span data-ttu-id="79219-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79219-137">NOTES</span></span>

## <span data-ttu-id="79219-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79219-138">RELATED LINKS</span></span>
