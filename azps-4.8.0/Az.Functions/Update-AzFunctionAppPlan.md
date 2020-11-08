---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94023977"
---
# <span data-ttu-id="802f2-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="802f2-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="802f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="802f2-102">SYNOPSIS</span></span>
<span data-ttu-id="802f2-103">A Function app szolgáltatási tervének frissítése</span><span class="sxs-lookup"><span data-stu-id="802f2-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="802f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="802f2-104">SYNTAX</span></span>

### <span data-ttu-id="802f2-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="802f2-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="802f2-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="802f2-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="802f2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="802f2-107">DESCRIPTION</span></span>
<span data-ttu-id="802f2-108">A Function app szolgáltatási tervének frissítése</span><span class="sxs-lookup"><span data-stu-id="802f2-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="802f2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="802f2-109">EXAMPLES</span></span>

### <span data-ttu-id="802f2-110">1. példa: az alkalmazás-szolgáltatási terv frissítése a EP2 SKU-ra a húsz legnagyobb dolgozóval.</span><span class="sxs-lookup"><span data-stu-id="802f2-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="802f2-111">Ez a parancs egy app-szolgáltatási csomagot frissít a EP2 SKU-ra húsz maximális munkással.</span><span class="sxs-lookup"><span data-stu-id="802f2-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="802f2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="802f2-112">PARAMETERS</span></span>

### <span data-ttu-id="802f2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="802f2-113">-AsJob</span></span>
<span data-ttu-id="802f2-114">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="802f2-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="802f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802f2-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="802f2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="802f2-116">-InputObject</span></span>
<span data-ttu-id="802f2-117">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="802f2-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="802f2-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="802f2-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="802f2-119">A munkavállalók maximális száma az alkalmazás-szolgáltatási tervben.</span><span class="sxs-lookup"><span data-stu-id="802f2-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="802f2-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="802f2-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="802f2-121">A munkavállalók minimális száma az alkalmazás-szolgáltatási tervben.</span><span class="sxs-lookup"><span data-stu-id="802f2-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="802f2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="802f2-122">-Name</span></span>
<span data-ttu-id="802f2-123">Az alkalmazás szolgáltatási tervének neve.</span><span class="sxs-lookup"><span data-stu-id="802f2-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="802f2-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="802f2-124">-NoWait</span></span>
<span data-ttu-id="802f2-125">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="802f2-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="802f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="802f2-127">Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="802f2-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="802f2-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="802f2-128">-Sku</span></span>
<span data-ttu-id="802f2-129">Az SKU-terv.</span><span class="sxs-lookup"><span data-stu-id="802f2-129">The plan sku.</span></span>
<span data-ttu-id="802f2-130">Érvényes bemenetek: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="802f2-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="802f2-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="802f2-131">-SubscriptionId</span></span>
<span data-ttu-id="802f2-132">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="802f2-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="802f2-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="802f2-133">-Tag</span></span>
<span data-ttu-id="802f2-134">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="802f2-134">Resource tags.</span></span>

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

### <span data-ttu-id="802f2-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="802f2-135">-Confirm</span></span>
<span data-ttu-id="802f2-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="802f2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="802f2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802f2-137">-WhatIf</span></span>
<span data-ttu-id="802f2-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="802f2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="802f2-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="802f2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="802f2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802f2-140">CommonParameters</span></span>
<span data-ttu-id="802f2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="802f2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802f2-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="802f2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802f2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="802f2-143">INPUTS</span></span>

### <span data-ttu-id="802f2-144">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="802f2-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="802f2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="802f2-145">OUTPUTS</span></span>

### <span data-ttu-id="802f2-146">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="802f2-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="802f2-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="802f2-147">NOTES</span></span>

<span data-ttu-id="802f2-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="802f2-148">ALIASES</span></span>

<span data-ttu-id="802f2-149">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="802f2-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="802f2-150">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="802f2-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="802f2-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="802f2-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="802f2-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="802f2-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="802f2-153">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="802f2-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="802f2-154">`[Kind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="802f2-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="802f2-155">`[Tag <IResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="802f2-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="802f2-156">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="802f2-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="802f2-157">`[Capacity <Int32?>]`: Az erőforráshoz rendelt példányok aktuális száma.</span><span class="sxs-lookup"><span data-stu-id="802f2-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="802f2-158">`[FreeOfferExpirationTime <DateTime?>]`: A kiszolgálófarm ingyenes ajánlatának lejárati időpontja.</span><span class="sxs-lookup"><span data-stu-id="802f2-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="802f2-159">`[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="802f2-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="802f2-160">`[HyperV <Boolean?>]`: Ha a Hyper-V Container app Service csomagja <code>true</code> <code>false</code> másképpen van.</span><span class="sxs-lookup"><span data-stu-id="802f2-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="802f2-161">`[IsSpot <Boolean?>]`: Ha <code>true</code> Ez az alkalmazás-szolgáltatási terv a helyszíni példányokat is tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="802f2-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="802f2-162">`[IsXenon <Boolean?>]`: Elavult: Ha a Hyper-V Container app Service Plane ( <code>true</code> <code>false</code> egyéb).</span><span class="sxs-lookup"><span data-stu-id="802f2-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="802f2-163">`[MaximumElasticWorkerCount <Int32?>]`: A ElasticScaleEnabled-app szolgáltatási csomagjában engedélyezett teljes foglalkoztatottak maximális száma</span><span class="sxs-lookup"><span data-stu-id="802f2-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="802f2-164">`[PerSiteScaling <Boolean?>]`: Ha <code>true</code> az alkalmazás-szolgáltatási csomaghoz rendelt alkalmazások egymástól függetlenül is méretezhetők.</span><span class="sxs-lookup"><span data-stu-id="802f2-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="802f2-165">Ha <code>false</code> az alkalmazás-szolgáltatási csomaghoz rendelt alkalmazások átlépték a terv összes példányára.</span><span class="sxs-lookup"><span data-stu-id="802f2-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="802f2-166">`[Reserved <Boolean?>]`: Ha a Linux app Service Plan ( <code>true</code> <code>false</code> egyéb esetben)</span><span class="sxs-lookup"><span data-stu-id="802f2-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="802f2-167">`[SkuCapability <ICapability[]>]`: A SKU képességei, például a Traffic Manager engedélyezve van?</span><span class="sxs-lookup"><span data-stu-id="802f2-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="802f2-168">`[Name <String>]`: A SKU-kapacitás neve.</span><span class="sxs-lookup"><span data-stu-id="802f2-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="802f2-169">`[Reason <String>]`: A SKU-kapacitás oka.</span><span class="sxs-lookup"><span data-stu-id="802f2-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="802f2-170">`[Value <String>]`: A SKU tulajdonság értéke.</span><span class="sxs-lookup"><span data-stu-id="802f2-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="802f2-171">`[SkuCapacityDefault <Int32?>]`: A munkavállalók alapértelmezett száma az alkalmazás-szolgáltatási csomag SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="802f2-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="802f2-172">`[SkuCapacityMaximum <Int32?>]`: A munkavállalók maximális száma az alkalmazás-szolgáltatási csomag SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="802f2-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="802f2-173">`[SkuCapacityMinimum <Int32?>]`: Az alkalmazás-szolgáltatási csomag SKU-hoz szükséges dolgozók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="802f2-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="802f2-174">`[SkuCapacityScaleType <String>]`: A rendelkezésre álló méretarány-konfigurációk egy app-szolgáltatási csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="802f2-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="802f2-175">`[SkuFamily <String>]`: Az erőforrás-SKU családi kódja.</span><span class="sxs-lookup"><span data-stu-id="802f2-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="802f2-176">`[SkuLocation <String[]>]`: A SKU helye.</span><span class="sxs-lookup"><span data-stu-id="802f2-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="802f2-177">`[SkuName <String>]`: Az erőforrás SKU neve.</span><span class="sxs-lookup"><span data-stu-id="802f2-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="802f2-178">`[SkuSize <String>]`: Az erőforrás-SKU méretének megadása</span><span class="sxs-lookup"><span data-stu-id="802f2-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="802f2-179">`[SkuTier <String>]`: Az erőforrás-SKU szolgáltatási rétege.</span><span class="sxs-lookup"><span data-stu-id="802f2-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="802f2-180">`[SpotExpirationTime <DateTime?>]`: A kiszolgálófarm elévülési ideje.</span><span class="sxs-lookup"><span data-stu-id="802f2-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="802f2-181">Csak akkor érvényes, ha az a hely kiszolgálófarm.</span><span class="sxs-lookup"><span data-stu-id="802f2-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="802f2-182">`[TargetWorkerCount <Int32?>]`: A munkavégzők számának méretezése.</span><span class="sxs-lookup"><span data-stu-id="802f2-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="802f2-183">`[TargetWorkerSizeId <Int32?>]`: A munkavégző méret-AZONOSÍTÓjának méretezése</span><span class="sxs-lookup"><span data-stu-id="802f2-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="802f2-184">`[WorkerTierName <String>]`: Az alkalmazás-szolgáltatási csomaghoz hozzárendelt célzott munkafolyamat-szint</span><span class="sxs-lookup"><span data-stu-id="802f2-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="802f2-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="802f2-185">RELATED LINKS</span></span>

