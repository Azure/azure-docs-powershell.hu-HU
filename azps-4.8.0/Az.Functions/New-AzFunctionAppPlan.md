---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182225"
---
# <span data-ttu-id="a29b1-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a29b1-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a29b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a29b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a29b1-103">Function app-szolgáltatási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a29b1-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="a29b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a29b1-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a29b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a29b1-105">DESCRIPTION</span></span>
<span data-ttu-id="a29b1-106">Function app-szolgáltatási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a29b1-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="a29b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a29b1-107">EXAMPLES</span></span>

### <span data-ttu-id="a29b1-108">1. példa: a Windows Premium app-csomag létrehozása Nyugat-Európában, kirobbant kapacitással legfeljebb 10 példányban.</span><span class="sxs-lookup"><span data-stu-id="a29b1-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="a29b1-109">Ez a parancs egy Windows Premium app-csomagot hoz létre Nyugat-Európában, kirobbant kapacitással legfeljebb 10 példányban.</span><span class="sxs-lookup"><span data-stu-id="a29b1-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="a29b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a29b1-110">PARAMETERS</span></span>

### <span data-ttu-id="a29b1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a29b1-111">-AsJob</span></span>
<span data-ttu-id="a29b1-112">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="a29b1-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="a29b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29b1-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="a29b1-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="a29b1-114">-Location</span></span>
<span data-ttu-id="a29b1-115">A fogyasztási terv helye.</span><span class="sxs-lookup"><span data-stu-id="a29b1-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="a29b1-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a29b1-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="a29b1-117">A munkavállalók maximális száma az alkalmazás-szolgáltatási tervben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="a29b1-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a29b1-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="a29b1-119">A munkavállalók minimális száma az alkalmazás-szolgáltatási tervben.</span><span class="sxs-lookup"><span data-stu-id="a29b1-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="a29b1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a29b1-120">-Name</span></span>
<span data-ttu-id="a29b1-121">Az alkalmazás szolgáltatási tervének neve.</span><span class="sxs-lookup"><span data-stu-id="a29b1-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="a29b1-122">-Várva</span><span class="sxs-lookup"><span data-stu-id="a29b1-122">-NoWait</span></span>
<span data-ttu-id="a29b1-123">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="a29b1-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a29b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="a29b1-125">Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="a29b1-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="a29b1-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="a29b1-126">-Sku</span></span>
<span data-ttu-id="a29b1-127">Az SKU-terv.</span><span class="sxs-lookup"><span data-stu-id="a29b1-127">The plan sku.</span></span>
<span data-ttu-id="a29b1-128">Érvényes bemenetek: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="a29b1-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="a29b1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a29b1-129">-SubscriptionId</span></span>
<span data-ttu-id="a29b1-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a29b1-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a29b1-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="a29b1-131">-Tag</span></span>
<span data-ttu-id="a29b1-132">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="a29b1-132">Resource tags.</span></span>

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

### <span data-ttu-id="a29b1-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="a29b1-133">-WorkerType</span></span>
<span data-ttu-id="a29b1-134">A terv munkatípusa.</span><span class="sxs-lookup"><span data-stu-id="a29b1-134">The worker type for the plan.</span></span>
<span data-ttu-id="a29b1-135">Az érvényes bemenetek a következők: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="a29b1-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="a29b1-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a29b1-136">-Confirm</span></span>
<span data-ttu-id="a29b1-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a29b1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a29b1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a29b1-138">-WhatIf</span></span>
<span data-ttu-id="a29b1-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a29b1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a29b1-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a29b1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a29b1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29b1-141">CommonParameters</span></span>
<span data-ttu-id="a29b1-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a29b1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29b1-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a29b1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29b1-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a29b1-144">INPUTS</span></span>

## <span data-ttu-id="a29b1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a29b1-145">OUTPUTS</span></span>

### <span data-ttu-id="a29b1-146">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a29b1-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a29b1-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a29b1-147">NOTES</span></span>

<span data-ttu-id="a29b1-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a29b1-148">ALIASES</span></span>

## <span data-ttu-id="a29b1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a29b1-149">RELATED LINKS</span></span>

