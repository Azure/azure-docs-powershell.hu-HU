---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184942"
---
# <span data-ttu-id="3ff37-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="3ff37-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="3ff37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ff37-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff37-103">Egy Function app-terv törlése.</span><span class="sxs-lookup"><span data-stu-id="3ff37-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="3ff37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ff37-104">SYNTAX</span></span>

### <span data-ttu-id="3ff37-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ff37-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ff37-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="3ff37-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ff37-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ff37-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff37-108">Egy Function app-terv törlése.</span><span class="sxs-lookup"><span data-stu-id="3ff37-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="3ff37-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3ff37-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff37-110">Példa 1: a Function app tervének beszerzése név alapján és törlése</span><span class="sxs-lookup"><span data-stu-id="3ff37-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="3ff37-111">Ez a parancs a Function app tervét név alapján kapja meg, és törli azt.</span><span class="sxs-lookup"><span data-stu-id="3ff37-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="3ff37-112">2. példa: a Function app tervének törlése név szerint.</span><span class="sxs-lookup"><span data-stu-id="3ff37-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="3ff37-113">Ez a parancs törli a Function app tervét név szerint.</span><span class="sxs-lookup"><span data-stu-id="3ff37-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="3ff37-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ff37-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff37-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff37-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ff37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff37-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3ff37-117">-Force</span></span>
<span data-ttu-id="3ff37-118">Kényszeríti a parancsmagot a Function app-csomag eltávolítására a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3ff37-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3ff37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff37-119">-InputObject</span></span>
<span data-ttu-id="3ff37-120">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3ff37-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ff37-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ff37-121">-Name</span></span>
<span data-ttu-id="3ff37-122">A függvény app neve.</span><span class="sxs-lookup"><span data-stu-id="3ff37-122">The name of function app.</span></span>

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

### <span data-ttu-id="3ff37-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ff37-123">-PassThru</span></span>
<span data-ttu-id="3ff37-124">Igaz érték visszaadása, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="3ff37-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="3ff37-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff37-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="3ff37-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ff37-126">-SubscriptionId</span></span>
<span data-ttu-id="3ff37-127">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ff37-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="3ff37-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ff37-128">-Confirm</span></span>
<span data-ttu-id="3ff37-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ff37-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff37-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff37-130">-WhatIf</span></span>
<span data-ttu-id="3ff37-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ff37-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff37-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ff37-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff37-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff37-133">CommonParameters</span></span>
<span data-ttu-id="3ff37-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ff37-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff37-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ff37-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff37-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff37-136">INPUTS</span></span>

### <span data-ttu-id="3ff37-137">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ff37-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="3ff37-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff37-138">OUTPUTS</span></span>

### <span data-ttu-id="3ff37-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ff37-139">System.Boolean</span></span>

## <span data-ttu-id="3ff37-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ff37-140">NOTES</span></span>

<span data-ttu-id="3ff37-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3ff37-141">ALIASES</span></span>

<span data-ttu-id="3ff37-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3ff37-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ff37-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3ff37-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ff37-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3ff37-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ff37-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="3ff37-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="3ff37-146">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="3ff37-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="3ff37-147">`[Kind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="3ff37-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="3ff37-148">`[Tag <IResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="3ff37-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="3ff37-149">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="3ff37-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3ff37-150">`[Capacity <Int32?>]`: Az erőforráshoz rendelt példányok aktuális száma.</span><span class="sxs-lookup"><span data-stu-id="3ff37-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="3ff37-151">`[FreeOfferExpirationTime <DateTime?>]`: A kiszolgálófarm ingyenes ajánlatának lejárati időpontja.</span><span class="sxs-lookup"><span data-stu-id="3ff37-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="3ff37-152">`[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ff37-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="3ff37-153">`[HyperV <Boolean?>]`: Ha a Hyper-V Container app Service csomagja <code>true</code> <code>false</code> másképpen van.</span><span class="sxs-lookup"><span data-stu-id="3ff37-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="3ff37-154">`[IsSpot <Boolean?>]`: Ha <code>true</code> Ez az alkalmazás-szolgáltatási terv a helyszíni példányokat is tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="3ff37-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="3ff37-155">`[IsXenon <Boolean?>]`: Elavult: Ha a Hyper-V Container app Service Plane ( <code>true</code> <code>false</code> egyéb).</span><span class="sxs-lookup"><span data-stu-id="3ff37-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="3ff37-156">`[MaximumElasticWorkerCount <Int32?>]`: A ElasticScaleEnabled-app szolgáltatási csomagjában engedélyezett teljes foglalkoztatottak maximális száma</span><span class="sxs-lookup"><span data-stu-id="3ff37-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="3ff37-157">`[PerSiteScaling <Boolean?>]`: Ha <code>true</code> az alkalmazás-szolgáltatási csomaghoz rendelt alkalmazások egymástól függetlenül is méretezhetők.</span><span class="sxs-lookup"><span data-stu-id="3ff37-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="3ff37-158">Ha <code>false</code> az alkalmazás-szolgáltatási csomaghoz rendelt alkalmazások átlépték a terv összes példányára.</span><span class="sxs-lookup"><span data-stu-id="3ff37-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="3ff37-159">`[Reserved <Boolean?>]`: Ha a Linux app Service Plan ( <code>true</code> <code>false</code> egyéb esetben)</span><span class="sxs-lookup"><span data-stu-id="3ff37-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="3ff37-160">`[SkuCapability <ICapability[]>]`: A SKU képességei, például a Traffic Manager engedélyezve van?</span><span class="sxs-lookup"><span data-stu-id="3ff37-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="3ff37-161">`[Name <String>]`: A SKU-kapacitás neve.</span><span class="sxs-lookup"><span data-stu-id="3ff37-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="3ff37-162">`[Reason <String>]`: A SKU-kapacitás oka.</span><span class="sxs-lookup"><span data-stu-id="3ff37-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="3ff37-163">`[Value <String>]`: A SKU tulajdonság értéke.</span><span class="sxs-lookup"><span data-stu-id="3ff37-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="3ff37-164">`[SkuCapacityDefault <Int32?>]`: A munkavállalók alapértelmezett száma az alkalmazás-szolgáltatási csomag SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="3ff37-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="3ff37-165">`[SkuCapacityMaximum <Int32?>]`: A munkavállalók maximális száma az alkalmazás-szolgáltatási csomag SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="3ff37-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="3ff37-166">`[SkuCapacityMinimum <Int32?>]`: Az alkalmazás-szolgáltatási csomag SKU-hoz szükséges dolgozók minimális száma.</span><span class="sxs-lookup"><span data-stu-id="3ff37-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="3ff37-167">`[SkuCapacityScaleType <String>]`: A rendelkezésre álló méretarány-konfigurációk egy app-szolgáltatási csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ff37-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="3ff37-168">`[SkuFamily <String>]`: Az erőforrás-SKU családi kódja.</span><span class="sxs-lookup"><span data-stu-id="3ff37-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="3ff37-169">`[SkuLocation <String[]>]`: A SKU helye.</span><span class="sxs-lookup"><span data-stu-id="3ff37-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="3ff37-170">`[SkuName <String>]`: Az erőforrás SKU neve.</span><span class="sxs-lookup"><span data-stu-id="3ff37-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="3ff37-171">`[SkuSize <String>]`: Az erőforrás-SKU méretének megadása</span><span class="sxs-lookup"><span data-stu-id="3ff37-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="3ff37-172">`[SkuTier <String>]`: Az erőforrás-SKU szolgáltatási rétege.</span><span class="sxs-lookup"><span data-stu-id="3ff37-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="3ff37-173">`[SpotExpirationTime <DateTime?>]`: A kiszolgálófarm elévülési ideje.</span><span class="sxs-lookup"><span data-stu-id="3ff37-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="3ff37-174">Csak akkor érvényes, ha az a hely kiszolgálófarm.</span><span class="sxs-lookup"><span data-stu-id="3ff37-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="3ff37-175">`[TargetWorkerCount <Int32?>]`: A munkavégzők számának méretezése.</span><span class="sxs-lookup"><span data-stu-id="3ff37-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="3ff37-176">`[TargetWorkerSizeId <Int32?>]`: A munkavégző méret-AZONOSÍTÓjának méretezése</span><span class="sxs-lookup"><span data-stu-id="3ff37-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="3ff37-177">`[WorkerTierName <String>]`: Az alkalmazás-szolgáltatási csomaghoz hozzárendelt célzott munkafolyamat-szint</span><span class="sxs-lookup"><span data-stu-id="3ff37-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="3ff37-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ff37-178">RELATED LINKS</span></span>

