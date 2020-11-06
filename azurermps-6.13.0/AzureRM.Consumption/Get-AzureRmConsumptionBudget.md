---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
ms.openlocfilehash: 7793dfe2f5d83e0975a5a8c200d19b48d8c4d9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494096"
---
# <span data-ttu-id="e5de9-101">Get-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="e5de9-101">Get-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="e5de9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5de9-102">SYNOPSIS</span></span>
<span data-ttu-id="e5de9-103">A költségvetések listájának beszerzése előfizetésben vagy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="e5de9-103">Get a list of budgets in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5de9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5de9-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5de9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5de9-105">DESCRIPTION</span></span>
<span data-ttu-id="e5de9-106">A Get-AzureRmConsumptionBudget parancsmag egy előfizetésben vagy egy erőforráscsoport listájában kapja meg a költségvetéseket.</span><span class="sxs-lookup"><span data-stu-id="e5de9-106">The Get-AzureRmConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="e5de9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5de9-107">EXAMPLES</span></span>

### <span data-ttu-id="e5de9-108">1. példa: a költségvetések listájának beszerzése az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="e5de9-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="e5de9-109">2. példa: a költségvetések listájának beszerzése az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="e5de9-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="e5de9-110">3. példa: költségvetés beszerzése a költségvetés nevével az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="e5de9-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="e5de9-111">Példa 4: költségvetés beszerzése a költségvetés nevével az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="e5de9-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="e5de9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5de9-112">PARAMETERS</span></span>

### <span data-ttu-id="e5de9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5de9-113">-DefaultProfile</span></span>
<span data-ttu-id="e5de9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5de9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5de9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5de9-115">-Name</span></span>
<span data-ttu-id="e5de9-116">A költségvetés neve</span><span class="sxs-lookup"><span data-stu-id="e5de9-116">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5de9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5de9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5de9-118">Egy költségvetés erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="e5de9-118">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5de9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5de9-119">CommonParameters</span></span>
<span data-ttu-id="e5de9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5de9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5de9-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5de9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5de9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5de9-122">INPUTS</span></span>

### <span data-ttu-id="e5de9-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5de9-123">None</span></span>

## <span data-ttu-id="e5de9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5de9-124">OUTPUTS</span></span>

### <span data-ttu-id="e5de9-125">Microsoft. Azure. commands. fogyasztás. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="e5de9-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="e5de9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5de9-126">NOTES</span></span>

## <span data-ttu-id="e5de9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5de9-127">RELATED LINKS</span></span>
