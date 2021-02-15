---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166714"
---
# <span data-ttu-id="98594-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="98594-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="98594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98594-102">SYNOPSIS</span></span>
<span data-ttu-id="98594-103">Lekérte a költségvetések listáját előfizetésben vagy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="98594-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="98594-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98594-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="98594-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98594-105">DESCRIPTION</span></span>
<span data-ttu-id="98594-106">A Get-AzConsumptionBudget parancsmag lekérte a költségvetések listáját előfizetésben vagy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="98594-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="98594-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98594-107">EXAMPLES</span></span>

### <span data-ttu-id="98594-108">1. példa: Költségvetések listájának lekérte előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="98594-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
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

### <span data-ttu-id="98594-109">2. példa: Költségvetések listájának lekérte az erőforráscsoport szintjén</span><span class="sxs-lookup"><span data-stu-id="98594-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
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

### <span data-ttu-id="98594-110">3. példa: Költségvetés lekérte a költségvetés nevét előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="98594-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
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

### <span data-ttu-id="98594-111">4. példa: Költségvetés lekérte a költségvetés nevét az erőforráscsoport szintjén</span><span class="sxs-lookup"><span data-stu-id="98594-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
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

## <span data-ttu-id="98594-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98594-112">PARAMETERS</span></span>

### <span data-ttu-id="98594-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98594-113">-DefaultProfile</span></span>
<span data-ttu-id="98594-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98594-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98594-115">-Name</span><span class="sxs-lookup"><span data-stu-id="98594-115">-Name</span></span>
<span data-ttu-id="98594-116">A költségvetés neve.</span><span class="sxs-lookup"><span data-stu-id="98594-116">Name of a budget.</span></span>

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

### <span data-ttu-id="98594-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98594-117">-ResourceGroupName</span></span>
<span data-ttu-id="98594-118">Költségvetés erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="98594-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="98594-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98594-119">CommonParameters</span></span>
<span data-ttu-id="98594-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98594-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98594-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98594-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98594-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98594-122">INPUTS</span></span>

### <span data-ttu-id="98594-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="98594-123">None</span></span>

## <span data-ttu-id="98594-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98594-124">OUTPUTS</span></span>

### <span data-ttu-id="98594-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="98594-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="98594-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98594-126">NOTES</span></span>

## <span data-ttu-id="98594-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98594-127">RELATED LINKS</span></span>
