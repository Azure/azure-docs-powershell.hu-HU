---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469737"
---
# <span data-ttu-id="38170-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="38170-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="38170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38170-102">SYNOPSIS</span></span>
<span data-ttu-id="38170-103">Függvényalkalmazás-terv törlése.</span><span class="sxs-lookup"><span data-stu-id="38170-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="38170-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38170-104">SYNTAX</span></span>

### <span data-ttu-id="38170-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38170-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38170-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="38170-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38170-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38170-107">DESCRIPTION</span></span>
<span data-ttu-id="38170-108">Függvényalkalmazás-terv törlése.</span><span class="sxs-lookup"><span data-stu-id="38170-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="38170-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38170-109">EXAMPLES</span></span>

### <span data-ttu-id="38170-110">1. példa: Függvényalkalmazásterv lekért név szerint, és törlése.</span><span class="sxs-lookup"><span data-stu-id="38170-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="38170-111">Ez a parancs név szerint lekért egy függvényalkalmazástervet, és törli azt.</span><span class="sxs-lookup"><span data-stu-id="38170-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="38170-112">2. példa: Függvényalkalmazás tervének törlése név szerint.</span><span class="sxs-lookup"><span data-stu-id="38170-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="38170-113">Ez a parancs név szerint töröl egy függvényalkalmazástervet.</span><span class="sxs-lookup"><span data-stu-id="38170-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="38170-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38170-114">PARAMETERS</span></span>

### <span data-ttu-id="38170-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38170-115">-DefaultProfile</span></span>
<span data-ttu-id="38170-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38170-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38170-117">-Force</span><span class="sxs-lookup"><span data-stu-id="38170-117">-Force</span></span>
<span data-ttu-id="38170-118">Kényszeríti a parancsmagot, hogy a függvényalkalmazás-tervet jóváhagyás kérése nélkül távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="38170-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="38170-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38170-119">-InputObject</span></span>
<span data-ttu-id="38170-120">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="38170-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38170-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38170-121">-Name</span></span>
<span data-ttu-id="38170-122">A függvényalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="38170-122">The name of function app.</span></span>

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

### <span data-ttu-id="38170-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38170-123">-PassThru</span></span>
<span data-ttu-id="38170-124">Eredménye igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="38170-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="38170-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38170-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="38170-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38170-126">-SubscriptionId</span></span>
<span data-ttu-id="38170-127">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38170-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="38170-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38170-128">-Confirm</span></span>
<span data-ttu-id="38170-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="38170-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38170-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38170-130">-WhatIf</span></span>
<span data-ttu-id="38170-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="38170-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38170-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38170-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38170-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38170-133">CommonParameters</span></span>
<span data-ttu-id="38170-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38170-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38170-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38170-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38170-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38170-136">INPUTS</span></span>

### <span data-ttu-id="38170-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="38170-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="38170-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38170-138">OUTPUTS</span></span>

### <span data-ttu-id="38170-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38170-139">System.Boolean</span></span>

## <span data-ttu-id="38170-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38170-140">NOTES</span></span>

<span data-ttu-id="38170-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="38170-141">ALIASES</span></span>

<span data-ttu-id="38170-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="38170-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38170-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="38170-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38170-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38170-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38170-145">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="38170-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="38170-146">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="38170-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="38170-147">`[Kind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="38170-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="38170-148">`[Tag <IResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="38170-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="38170-149">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="38170-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="38170-150">`[Capacity <Int32?>]`: Az erőforráshoz rendelt példányok aktuális száma.</span><span class="sxs-lookup"><span data-stu-id="38170-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="38170-151">`[FreeOfferExpirationTime <DateTime?>]`: A kiszolgálófarm ingyenes ajánlatának lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="38170-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="38170-152">`[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38170-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="38170-153">`[HyperV <Boolean?>]`: Ha a Hyper-V tároló appszolgáltatás-csomagja <code>true</code> , <code>false</code> egyébként.</span><span class="sxs-lookup"><span data-stu-id="38170-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="38170-154">`[IsSpot <Boolean?>]`: Ha <code>true</code> ez az appszolgáltatás-csomag rendelkezik direkt példányokkal.</span><span class="sxs-lookup"><span data-stu-id="38170-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="38170-155">`[IsXenon <Boolean?>]`: Elavult: Ha a Hyper-V tárolóalkalmazás szolgáltatási <code>true</code> csomagja , <code>false</code> egyébként.</span><span class="sxs-lookup"><span data-stu-id="38170-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="38170-156">`[MaximumElasticWorkerCount <Int32?>]`: A RugalmasságiSkálaEnabled appszolgáltatás-csomaghoz engedélyezett összes dolgozó maximális száma</span><span class="sxs-lookup"><span data-stu-id="38170-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="38170-157">`[PerSiteScaling <Boolean?>]`: Ha az appszolgáltatás-csomaghoz rendelt appok egymástól függetlenül <code>true</code> skálázhatóak.</span><span class="sxs-lookup"><span data-stu-id="38170-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="38170-158">Ha az appszolgáltatás-csomaghoz rendelt appok a csomag összes példányához <code>false</code> méretre fognak méretezve.</span><span class="sxs-lookup"><span data-stu-id="38170-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="38170-159">`[Reserved <Boolean?>]`: Ha a Linux appszolgáltatás-csomagja <code>true</code> , <code>false</code> egyébként.</span><span class="sxs-lookup"><span data-stu-id="38170-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="38170-160">`[SkuCapability <ICapability[]>]`: A termékváltozat képességei, például engedélyezve van a forgalomkezelő?</span><span class="sxs-lookup"><span data-stu-id="38170-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="38170-161">`[Name <String>]`: A termékváltozat-képesség neve.</span><span class="sxs-lookup"><span data-stu-id="38170-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="38170-162">`[Reason <String>]`: A termékváltozat-képesség oka.</span><span class="sxs-lookup"><span data-stu-id="38170-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="38170-163">`[Value <String>]`: A termékváltozat-képesség értéke.</span><span class="sxs-lookup"><span data-stu-id="38170-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="38170-164">`[SkuCapacityDefault <Int32?>]`: Az appszolgáltatás-csomaghoz az alapértelmezett dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="38170-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="38170-165">`[SkuCapacityMaximum <Int32?>]`: Az appszolgáltatás-csomag termékváltozatában dolgozók maximális száma.</span><span class="sxs-lookup"><span data-stu-id="38170-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="38170-166">`[SkuCapacityMinimum <Int32?>]`: Az appszolgáltatás-csomaghoz minimálisan szükséges dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="38170-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="38170-167">`[SkuCapacityScaleType <String>]`: Az appszolgáltatás-csomaghoz rendelkezésre álló méretarány-konfigurációk.</span><span class="sxs-lookup"><span data-stu-id="38170-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="38170-168">`[SkuFamily <String>]`: Az erőforrás-termékváltozat családi kódja.</span><span class="sxs-lookup"><span data-stu-id="38170-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="38170-169">`[SkuLocation <String[]>]`: A termékváltozat helye.</span><span class="sxs-lookup"><span data-stu-id="38170-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="38170-170">`[SkuName <String>]`: Az erőforrás-termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="38170-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="38170-171">`[SkuSize <String>]`: Az erőforrás-termékváltozat méretkierőszője.</span><span class="sxs-lookup"><span data-stu-id="38170-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="38170-172">`[SkuTier <String>]`: Az erőforrás-termékváltozat szolgáltatási rétege.</span><span class="sxs-lookup"><span data-stu-id="38170-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="38170-173">`[SpotExpirationTime <DateTime?>]`: A kiszolgálófarm lejáratának ideje.</span><span class="sxs-lookup"><span data-stu-id="38170-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="38170-174">Csak akkor érvényes, ha direkt kiszolgálófarmról van szükség.</span><span class="sxs-lookup"><span data-stu-id="38170-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="38170-175">`[TargetWorkerCount <Int32?>]`: A dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="38170-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="38170-176">`[TargetWorkerSizeId <Int32?>]`: A dolgozók méretazonosítójának méretezése.</span><span class="sxs-lookup"><span data-stu-id="38170-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="38170-177">`[WorkerTierName <String>]`: Az appszolgáltatás-csomaghoz hozzárendelt célmunkási szint.</span><span class="sxs-lookup"><span data-stu-id="38170-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="38170-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38170-178">RELATED LINKS</span></span>

