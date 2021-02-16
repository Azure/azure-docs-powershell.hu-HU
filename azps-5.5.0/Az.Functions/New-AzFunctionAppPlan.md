---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163507"
---
# <span data-ttu-id="85058-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="85058-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="85058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85058-102">SYNOPSIS</span></span>
<span data-ttu-id="85058-103">Függvényalkalmazás-szolgáltatástervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85058-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="85058-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85058-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85058-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85058-105">DESCRIPTION</span></span>
<span data-ttu-id="85058-106">Függvényalkalmazás-szolgáltatástervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85058-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="85058-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85058-107">EXAMPLES</span></span>

### <span data-ttu-id="85058-108">1. példa: Windows prémium verziós appterv létrehozása Nyugat-Európában, legfeljebb 10 példányos kieső képességgel.</span><span class="sxs-lookup"><span data-stu-id="85058-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="85058-109">Ez a parancs egy Windows prémium verziós apptervet hoz létre Nyugat-Európában, legfeljebb 10 példányban.</span><span class="sxs-lookup"><span data-stu-id="85058-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="85058-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85058-110">PARAMETERS</span></span>

### <span data-ttu-id="85058-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85058-111">-AsJob</span></span>
<span data-ttu-id="85058-112">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="85058-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="85058-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85058-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-114">-Location</span><span class="sxs-lookup"><span data-stu-id="85058-114">-Location</span></span>
<span data-ttu-id="85058-115">A fogyasztási terv helye.</span><span class="sxs-lookup"><span data-stu-id="85058-115">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="85058-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="85058-117">Az appszolgáltatás-csomaghoz legfeljebb hány dolgozó lehet.</span><span class="sxs-lookup"><span data-stu-id="85058-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="85058-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="85058-119">Az appszolgáltatás-csomaghoz minimálisan szükséges számú dolgozó.</span><span class="sxs-lookup"><span data-stu-id="85058-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85058-120">-Name</span></span>
<span data-ttu-id="85058-121">Az appszolgáltatás-csomag neve.</span><span class="sxs-lookup"><span data-stu-id="85058-121">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85058-122">-NoWait</span></span>
<span data-ttu-id="85058-123">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="85058-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="85058-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85058-124">-ResourceGroupName</span></span>
<span data-ttu-id="85058-125">Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="85058-125">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="85058-126">-Sku</span></span>
<span data-ttu-id="85058-127">A csomag termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="85058-127">The plan sku.</span></span>
<span data-ttu-id="85058-128">Érvényes bemenetek: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="85058-128">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85058-129">-SubscriptionId</span></span>
<span data-ttu-id="85058-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="85058-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="85058-131">-Tag</span></span>
<span data-ttu-id="85058-132">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="85058-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="85058-133">-WorkerType</span></span>
<span data-ttu-id="85058-134">A terv dolgozótípusa.</span><span class="sxs-lookup"><span data-stu-id="85058-134">The worker type for the plan.</span></span>
<span data-ttu-id="85058-135">Érvényes bemenetek: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="85058-135">Valid inputs are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85058-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85058-136">-Confirm</span></span>
<span data-ttu-id="85058-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="85058-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85058-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85058-138">-WhatIf</span></span>
<span data-ttu-id="85058-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="85058-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85058-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85058-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85058-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85058-141">CommonParameters</span></span>
<span data-ttu-id="85058-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85058-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85058-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85058-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85058-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85058-144">INPUTS</span></span>

## <span data-ttu-id="85058-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85058-145">OUTPUTS</span></span>

### <span data-ttu-id="85058-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85058-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="85058-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85058-147">NOTES</span></span>

<span data-ttu-id="85058-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="85058-148">ALIASES</span></span>

## <span data-ttu-id="85058-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85058-149">RELATED LINKS</span></span>

