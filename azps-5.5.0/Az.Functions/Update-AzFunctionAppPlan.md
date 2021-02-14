---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167514"
---
# <span data-ttu-id="d985a-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="d985a-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="d985a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d985a-102">SYNOPSIS</span></span>
<span data-ttu-id="d985a-103">Frissíti a függvényalkalmazások szolgáltatástervét.</span><span class="sxs-lookup"><span data-stu-id="d985a-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="d985a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d985a-104">SYNTAX</span></span>

### <span data-ttu-id="d985a-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d985a-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d985a-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="d985a-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d985a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d985a-107">DESCRIPTION</span></span>
<span data-ttu-id="d985a-108">Frissíti a függvényalkalmazások szolgáltatástervét.</span><span class="sxs-lookup"><span data-stu-id="d985a-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="d985a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d985a-109">EXAMPLES</span></span>

### <span data-ttu-id="d985a-110">1. példa: Egy appszolgáltatás-csomag frissítése EP2-termékváltozatra húsz legnagyobb dolgozóval.</span><span class="sxs-lookup"><span data-stu-id="d985a-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="d985a-111">Ez a parancs egy appszolgáltatás-tervet frissíti EP2-termékváltozatra, amely húsz legnagyobb dolgozót biztosít.</span><span class="sxs-lookup"><span data-stu-id="d985a-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="d985a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d985a-112">PARAMETERS</span></span>

### <span data-ttu-id="d985a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d985a-113">-AsJob</span></span>
<span data-ttu-id="d985a-114">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="d985a-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="d985a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d985a-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="d985a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d985a-116">-InputObject</span></span>
<span data-ttu-id="d985a-117">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="d985a-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d985a-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="d985a-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="d985a-119">Az appszolgáltatás-csomag dolgozóinak maximális száma.</span><span class="sxs-lookup"><span data-stu-id="d985a-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="d985a-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="d985a-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="d985a-121">Az appszolgáltatás-csomaghoz minimálisan szükséges számú dolgozó.</span><span class="sxs-lookup"><span data-stu-id="d985a-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="d985a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d985a-122">-Name</span></span>
<span data-ttu-id="d985a-123">Az appszolgáltatás-csomag neve.</span><span class="sxs-lookup"><span data-stu-id="d985a-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d985a-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d985a-124">-NoWait</span></span>
<span data-ttu-id="d985a-125">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="d985a-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d985a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d985a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d985a-127">Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="d985a-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d985a-128">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="d985a-128">-Sku</span></span>
<span data-ttu-id="d985a-129">A csomag termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="d985a-129">The plan sku.</span></span>
<span data-ttu-id="d985a-130">Érvényes bemenetek: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="d985a-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="d985a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d985a-131">-SubscriptionId</span></span>
<span data-ttu-id="d985a-132">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d985a-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d985a-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d985a-133">-Tag</span></span>
<span data-ttu-id="d985a-134">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="d985a-134">Resource tags.</span></span>

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

### <span data-ttu-id="d985a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d985a-135">-Confirm</span></span>
<span data-ttu-id="d985a-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d985a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d985a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d985a-137">-WhatIf</span></span>
<span data-ttu-id="d985a-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d985a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d985a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d985a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d985a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d985a-140">CommonParameters</span></span>
<span data-ttu-id="d985a-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d985a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d985a-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d985a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d985a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d985a-143">INPUTS</span></span>

### <span data-ttu-id="d985a-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d985a-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d985a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d985a-145">OUTPUTS</span></span>

### <span data-ttu-id="d985a-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d985a-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d985a-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d985a-147">NOTES</span></span>

<span data-ttu-id="d985a-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d985a-148">ALIASES</span></span>

<span data-ttu-id="d985a-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d985a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d985a-150">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d985a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d985a-151">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d985a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d985a-152">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="d985a-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="d985a-153">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d985a-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="d985a-154">`[Kind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="d985a-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="d985a-155">`[Tag <IResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="d985a-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d985a-156">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="d985a-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d985a-157">`[Capacity <Int32?>]`: Az erőforráshoz rendelt példányok aktuális száma.</span><span class="sxs-lookup"><span data-stu-id="d985a-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="d985a-158">`[FreeOfferExpirationTime <DateTime?>]`: A kiszolgálófarm ingyenes ajánlatának lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="d985a-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="d985a-159">`[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d985a-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="d985a-160">`[HyperV <Boolean?>]`: Ha a Hyper-V tároló app szolgáltatási <code>true</code> csomagja , <code>false</code> egyébként.</span><span class="sxs-lookup"><span data-stu-id="d985a-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d985a-161">`[IsSpot <Boolean?>]`: Ha <code>true</code> ez az appszolgáltatás-csomag rendelkezik direkt példányokkal.</span><span class="sxs-lookup"><span data-stu-id="d985a-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="d985a-162">`[IsXenon <Boolean?>]`: Elavult: Ha a Hyper-V tárolóalkalmazás szolgáltatási <code>true</code> csomagja , <code>false</code> egyébként.</span><span class="sxs-lookup"><span data-stu-id="d985a-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d985a-163">`[MaximumElasticWorkerCount <Int32?>]`: A RugalmasságiSkálaEnabled appszolgáltatás-csomaghoz engedélyezett összes dolgozó maximális száma</span><span class="sxs-lookup"><span data-stu-id="d985a-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="d985a-164">`[PerSiteScaling <Boolean?>]`: Ha az appszolgáltatás-csomaghoz rendelt appok egymástól függetlenül <code>true</code> skálázhatóak.</span><span class="sxs-lookup"><span data-stu-id="d985a-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="d985a-165">Ha az appszolgáltatás-csomaghoz rendelt appok a csomag összes példányához <code>false</code> méretre fognak méretezve.</span><span class="sxs-lookup"><span data-stu-id="d985a-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="d985a-166">`[Reserved <Boolean?>]`: Ha a Linux appszolgáltatásának <code>true</code> csomagja , <code>false</code> egyébként.</span><span class="sxs-lookup"><span data-stu-id="d985a-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d985a-167">`[SkuCapability <ICapability[]>]`: A termékváltozat képességei, például engedélyezve vannak a forgalomkezelők?</span><span class="sxs-lookup"><span data-stu-id="d985a-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="d985a-168">`[Name <String>]`: A termékváltozat-képesség neve.</span><span class="sxs-lookup"><span data-stu-id="d985a-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="d985a-169">`[Reason <String>]`: A termékváltozat-képesség oka.</span><span class="sxs-lookup"><span data-stu-id="d985a-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="d985a-170">`[Value <String>]`: A termékváltozat-képesség értéke.</span><span class="sxs-lookup"><span data-stu-id="d985a-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="d985a-171">`[SkuCapacityDefault <Int32?>]`: Az appszolgáltatás-csomag termékváltozatának alapértelmezett dolgozói száma.</span><span class="sxs-lookup"><span data-stu-id="d985a-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d985a-172">`[SkuCapacityMaximum <Int32?>]`: Az appszolgáltatás-csomag termékváltozatában dolgozók maximális száma.</span><span class="sxs-lookup"><span data-stu-id="d985a-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d985a-173">`[SkuCapacityMinimum <Int32?>]`: Az appszolgáltatás-csomaghoz minimálisan szükséges dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="d985a-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d985a-174">`[SkuCapacityScaleType <String>]`: Az appszolgáltatás-csomaghoz rendelkezésre álló méretarány-konfigurációk.</span><span class="sxs-lookup"><span data-stu-id="d985a-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="d985a-175">`[SkuFamily <String>]`: Az erőforrás-termékváltozat családi kódja.</span><span class="sxs-lookup"><span data-stu-id="d985a-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="d985a-176">`[SkuLocation <String[]>]`: A termékváltozat helye.</span><span class="sxs-lookup"><span data-stu-id="d985a-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="d985a-177">`[SkuName <String>]`: Az erőforrás-termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="d985a-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="d985a-178">`[SkuSize <String>]`: Az erőforrás-termékváltozat méretkierőszője.</span><span class="sxs-lookup"><span data-stu-id="d985a-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="d985a-179">`[SkuTier <String>]`: Az erőforrás-termékváltozat szolgáltatási rétege.</span><span class="sxs-lookup"><span data-stu-id="d985a-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="d985a-180">`[SpotExpirationTime <DateTime?>]`: A kiszolgálófarm lejáratának ideje.</span><span class="sxs-lookup"><span data-stu-id="d985a-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="d985a-181">Csak akkor érvényes, ha direkt kiszolgálófarmról van szükség.</span><span class="sxs-lookup"><span data-stu-id="d985a-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="d985a-182">`[TargetWorkerCount <Int32?>]`: A dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="d985a-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="d985a-183">`[TargetWorkerSizeId <Int32?>]`: A dolgozók méretazonosítójának méretezése.</span><span class="sxs-lookup"><span data-stu-id="d985a-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="d985a-184">`[WorkerTierName <String>]`: Az appszolgáltatás-csomaghoz hozzárendelt célmunkási szint.</span><span class="sxs-lookup"><span data-stu-id="d985a-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="d985a-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d985a-185">RELATED LINKS</span></span>

