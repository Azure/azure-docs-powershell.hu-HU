---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466088"
---
# <span data-ttu-id="8efb5-101">Update-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="8efb5-101">Update-AzFunctionAppSetting</span></span>

## <span data-ttu-id="8efb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8efb5-102">SYNOPSIS</span></span>
<span data-ttu-id="8efb5-103">Alkalmazásbeállítások hozzáadása vagy frissítése egy függvényalkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="8efb5-103">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="8efb5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8efb5-104">SYNTAX</span></span>

### <span data-ttu-id="8efb5-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8efb5-105">ByName (Default)</span></span>
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8efb5-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="8efb5-106">ByObjectInput</span></span>
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8efb5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8efb5-107">DESCRIPTION</span></span>
<span data-ttu-id="8efb5-108">Alkalmazásbeállítások hozzáadása vagy frissítése egy függvényalkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="8efb5-108">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="8efb5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8efb5-109">EXAMPLES</span></span>

### <span data-ttu-id="8efb5-110">1. példa: Új appbeállítás hozzáadása egy függvényalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="8efb5-110">Example 1: Add a new app setting in a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

<span data-ttu-id="8efb5-111">Ez a parancs új appbeállítást ad hozzá egy függvényalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="8efb5-111">This command adds a new app setting in a function app.</span></span>

## <span data-ttu-id="8efb5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8efb5-112">PARAMETERS</span></span>

### <span data-ttu-id="8efb5-113">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="8efb5-113">-AppSetting</span></span>
<span data-ttu-id="8efb5-114">A kulcsokat és értékeket is tartalmazó hashtable leírja a függvényalkalmazásban hozzáadni vagy frissíteni szükséges alkalmazásbeállításokat.</span><span class="sxs-lookup"><span data-stu-id="8efb5-114">Hashtable with keys and values describe the app settings to be added or updated in the function app.</span></span>
<span data-ttu-id="8efb5-115">Például: @{"myappsetting"="123"}</span><span class="sxs-lookup"><span data-stu-id="8efb5-115">For example: @{"myappsetting"="123"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8efb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efb5-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="8efb5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8efb5-117">-Force</span></span>
<span data-ttu-id="8efb5-118">A parancsmagot kényszeríti a függvényalkalmazás beállításának frissítésére anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8efb5-118">Forces the cmdlet to update function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8efb5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8efb5-119">-InputObject</span></span>
<span data-ttu-id="8efb5-120">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="8efb5-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8efb5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8efb5-121">-Name</span></span>
<span data-ttu-id="8efb5-122">A függvényalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-122">Name of the function app.</span></span>

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

### <span data-ttu-id="8efb5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8efb5-123">-ResourceGroupName</span></span>
<span data-ttu-id="8efb5-124">Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="8efb5-124">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="8efb5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8efb5-125">-SubscriptionId</span></span>
<span data-ttu-id="8efb5-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-126">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="8efb5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8efb5-127">-Confirm</span></span>
<span data-ttu-id="8efb5-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8efb5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8efb5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8efb5-129">-WhatIf</span></span>
<span data-ttu-id="8efb5-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8efb5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8efb5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8efb5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8efb5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efb5-132">CommonParameters</span></span>
<span data-ttu-id="8efb5-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efb5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efb5-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8efb5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efb5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8efb5-135">INPUTS</span></span>

### <span data-ttu-id="8efb5-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="8efb5-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="8efb5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8efb5-137">OUTPUTS</span></span>

### <span data-ttu-id="8efb5-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="8efb5-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="8efb5-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8efb5-139">NOTES</span></span>

<span data-ttu-id="8efb5-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8efb5-140">ALIASES</span></span>

<span data-ttu-id="8efb5-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8efb5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8efb5-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8efb5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8efb5-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8efb5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8efb5-144">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="8efb5-144">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="8efb5-145">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8efb5-145">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="8efb5-146">`CloningInfoSourceWebAppId <String>`: ARM forrásalkalmazás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8efb5-146">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="8efb5-147">Az alkalmazáserőforrás-azonosító a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}, production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.</span><span class="sxs-lookup"><span data-stu-id="8efb5-147">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="8efb5-148">`[Kind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="8efb5-148">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="8efb5-149">`[Tag <IResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="8efb5-149">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8efb5-150">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="8efb5-150">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8efb5-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> az ügyfélkapcsolat engedélyezéséhez; a munkamenet-affinitás cookie-k küldésének megállítása, amelyek az ügyfélalkalmazások kérését ugyanannak a munkamenetnek a példányára <code>false</code> irányítják.</span><span class="sxs-lookup"><span data-stu-id="8efb5-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="8efb5-152">Az alapértelmezett érték <code>true</code> a .</span><span class="sxs-lookup"><span data-stu-id="8efb5-152">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="8efb5-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyfél tanúsítvány-hitelesítésének (TLS közös hitelesítés) engedélyezéséhez; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="8efb5-154">Az alapértelmezett érték <code>false</code> a .</span><span class="sxs-lookup"><span data-stu-id="8efb5-154">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="8efb5-155">`[ClientCertExclusionPath <String>]`: Ügyfél tanúsítványának hitelesítése vesszővel elválasztott kivétel elérési útjai</span><span class="sxs-lookup"><span data-stu-id="8efb5-155">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="8efb5-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazásbeállítási felülbírálások a klónozott appok esetén.</span><span class="sxs-lookup"><span data-stu-id="8efb5-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="8efb5-157">Ha meg van adva, ezek a beállítások felülbírálják a forrásalkalmazásból klónozott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="8efb5-157">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="8efb5-158">Ellenkező esetben a forrásalkalmazás alkalmazásbeállítása megmarad.</span><span class="sxs-lookup"><span data-stu-id="8efb5-158">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="8efb5-159">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="8efb5-159">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8efb5-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> az egyéni állomásnevek klónozása a forrásalkalmazásból, ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="8efb5-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrásalkalmazásból a forrásvezérlők klónozása; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="8efb5-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> konfigurálhatja a terheléselosztást a forrás- és célalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="8efb5-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="8efb5-163">`[CloningInfoCorrelationId <String>]`: A cloning művelet korrelációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-163">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="8efb5-164">Ez az azonosító több cloning műveletet hoz létre ugyanannak a pillanatfelvételnek a végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="8efb5-164">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="8efb5-165">`[CloningInfoHostingEnvironment <String>]`: App szolgáltatási környezet.</span><span class="sxs-lookup"><span data-stu-id="8efb5-165">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="8efb5-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a célalkalmazás felülírása; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="8efb5-167">`[CloningInfoSourceWebAppLocation <String>]`: A forrásalkalmazás helye, pl. Nyugat-Usa vagy Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="8efb5-167">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="8efb5-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM a Traffic Manager-profil erőforrás-azonosítóját, ha létezik ilyen.</span><span class="sxs-lookup"><span data-stu-id="8efb5-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="8efb5-169">A Traffic Manager erőforrás-azonosítója a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="8efb5-169">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="8efb5-170">`[CloningInfoTrafficManagerProfileName <String>]`: A létrehozni szükséges Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="8efb5-171">Erre csak akkor van szükség, ha a Traffic Manager-profil még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="8efb5-171">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="8efb5-172">`[Config <ISiteConfig>]`: Az app konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="8efb5-172">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="8efb5-173">`IsPushEnabled <Boolean>`: Jelölőt kap vagy állít be, amely jelzi, hogy a leküldéses végpont engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="8efb5-173">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="8efb5-174">`[ActionMinProcessExecutionTime <String>]`: A művelet végrehajtása előtt a folyamat minimálisan szükséges ideje</span><span class="sxs-lookup"><span data-stu-id="8efb5-174">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="8efb5-175">`[ActionType <AutoHealActionType?>]`: Előre meghatározott teendő.</span><span class="sxs-lookup"><span data-stu-id="8efb5-175">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="8efb5-176">`[AlwaysOn <Boolean?>]`: <code>true</code> ha a Mindig be van kapcsolva, egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-176">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-177">`[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.</span><span class="sxs-lookup"><span data-stu-id="8efb5-177">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="8efb5-178">`[ApiManagementConfigId <String>]`: APIM-Api azonosító.</span><span class="sxs-lookup"><span data-stu-id="8efb5-178">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="8efb5-179">`[AppCommandLine <String>]`: Elindítandó alkalmazás parancssora.</span><span class="sxs-lookup"><span data-stu-id="8efb5-179">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="8efb5-180">`[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.</span><span class="sxs-lookup"><span data-stu-id="8efb5-180">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="8efb5-181">`[Name <String>]`: Párnév.</span><span class="sxs-lookup"><span data-stu-id="8efb5-181">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="8efb5-182">`[Value <String>]`: Érték párosítása.</span><span class="sxs-lookup"><span data-stu-id="8efb5-182">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="8efb5-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> ha az Automatikus lejátszás funkció be van kapcsolva; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-184">`[AutoSwapSlotName <String>]`: Az automatikus cserehely neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-184">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="8efb5-185">`[ConnectionString <IConnStringInfo[]>]`: Kapcsolati karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="8efb5-185">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="8efb5-186">`[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.</span><span class="sxs-lookup"><span data-stu-id="8efb5-186">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="8efb5-187">`[Name <String>]`: A kapcsolati karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-187">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="8efb5-188">`[Type <ConnectionStringType?>]`: Az adatbázis típusa.</span><span class="sxs-lookup"><span data-stu-id="8efb5-188">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="8efb5-189">`[CorAllowedOrigin <String[]>]`: Beállítja vagy beállítja azon forráslistát, amely lehetővé teszi a több forrásból való hívásokat (például: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="8efb5-189">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="8efb5-190">Az összes engedélyezése a "\*" szóra van állítva.</span><span class="sxs-lookup"><span data-stu-id="8efb5-190">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="8efb5-191">`[CorSupportCredentials <Boolean?>]`: Beállítja vagy beállítja, hogy engedélyezettek-e a hitelesítő adatokkal megadott CORS-kérések.</span><span class="sxs-lookup"><span data-stu-id="8efb5-191">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="8efb5-192">További         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         részleteket itt talál.</span><span class="sxs-lookup"><span data-stu-id="8efb5-192">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="8efb5-193">`[CustomActionExe <String>]`: Futtatható végrehajtható fájl.</span><span class="sxs-lookup"><span data-stu-id="8efb5-193">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="8efb5-194">`[CustomActionParameter <String>]`: A végrehajtható fájl paraméterei.</span><span class="sxs-lookup"><span data-stu-id="8efb5-194">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="8efb5-195">`[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.</span><span class="sxs-lookup"><span data-stu-id="8efb5-195">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="8efb5-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ha a részletes hibanaplózás engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-197">`[DocumentRoot <String>]`: Dokumentumgyök.</span><span class="sxs-lookup"><span data-stu-id="8efb5-197">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="8efb5-198">`[DynamicTagsJson <String>]`: Egy olyan JSON-karakterláncot kap vagy állít be, amely a leküldéses regisztrációs végponton található felhasználói igények alapján kiértékelésre kerül a dinamikus címkék listáját tartalmazó JSON-karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="8efb5-198">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="8efb5-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: A felfutási szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="8efb5-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="8efb5-200">`[ActionHostName <String>]`: Annak a tárolóhelynek a állomásneve, amelybe a forgalmat átirányítja a rendszer, ha úgy dönt.</span><span class="sxs-lookup"><span data-stu-id="8efb5-200">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="8efb5-201">Például:</span><span class="sxs-lookup"><span data-stu-id="8efb5-201">E.g.</span></span> <span data-ttu-id="8efb5-202">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="8efb5-202">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="8efb5-203">`[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmus is meg lehet adni a TiPCallback webhelybővítményben, amely URL-címet is meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="8efb5-203">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="8efb5-204">Lásd a TiPCallback webhelybővítményét az állványhoz és a szerződésekhez.</span><span class="sxs-lookup"><span data-stu-id="8efb5-204">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="8efb5-205"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="8efb5-205">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="8efb5-206">`[ChangeIntervalInMinute <Int32?>]`: Az ReroutePercentage átértékelhető intervallumát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="8efb5-206">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="8efb5-207">`[ChangeStep <Double?>]`: Automatikus felfutás esetén ezt a lépést kell hozzáadni/eltávolítani, amíg el nem éri a <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> vagy         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-207">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="8efb5-208">A webhely metrikákat a .\nCustom döntési algoritmusban megadott N percenként ellenőrzi a <code>ChangeIntervalInMinutes</code> TiPCallback webhelybővítmény, amely az URL-címet meg lehet <code>ChangeDecisionCallbackUrl</code> adni.</span><span class="sxs-lookup"><span data-stu-id="8efb5-208">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="8efb5-209">`[MaxReroutePercentage <Double?>]`: Azt a felső határot adja meg, amely alatt a ReroutePercentage meg fog maradni.</span><span class="sxs-lookup"><span data-stu-id="8efb5-209">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="8efb5-210">`[MinReroutePercentage <Double?>]`: Azt az alsó határértéket adja meg, amely fölött az ReroutePercentage meg fog maradni.</span><span class="sxs-lookup"><span data-stu-id="8efb5-210">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="8efb5-211">`[Name <String>]`: Az útválasztási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-211">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="8efb5-212">Az ajánlott név a kísérlet során a forgalmat tároló tárolóhelyre mutat.</span><span class="sxs-lookup"><span data-stu-id="8efb5-212">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="8efb5-213">`[ReroutePercentage <Double?>]`: Azon forgalom százalékos aránya, amelyre a rendszer átirányítja <code>ActionHostName</code> a forgalmat.</span><span class="sxs-lookup"><span data-stu-id="8efb5-213">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="8efb5-214">`[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás állapota</span><span class="sxs-lookup"><span data-stu-id="8efb5-214">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="8efb5-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span><span class="sxs-lookup"><span data-stu-id="8efb5-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="8efb5-216">`[Argument <String>]`: A parancsprogram-processzornak át kell adandó parancssori argumentumokat.</span><span class="sxs-lookup"><span data-stu-id="8efb5-216">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="8efb5-217">`[Extension <String>]`: Az ilyen kiterjesztésű kérelmeket a megadott FastCGI alkalmazással kezeljük.</span><span class="sxs-lookup"><span data-stu-id="8efb5-217">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="8efb5-218">`[ScriptProcessor <String>]`: A FastCGI alkalmazás abszolút elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8efb5-218">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="8efb5-219">`[HealthCheckPath <String>]`: Állapot-ellenőrzés útvonala</span><span class="sxs-lookup"><span data-stu-id="8efb5-219">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="8efb5-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfigurál egy webhelyet, amely engedélyezi az ügyfeleknek a http2.0-s kapcsolaton keresztüli csatlakozást</span><span class="sxs-lookup"><span data-stu-id="8efb5-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="8efb5-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> ha a HTTP-naplózás engedélyezve van; egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: A fő IP-biztonsági korlátozásai.</span><span class="sxs-lookup"><span data-stu-id="8efb5-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="8efb5-223">`[Action <String>]`: Hozzáférés engedélyezése vagy elutasítása ehhez az IP-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="8efb5-223">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="8efb5-224">`[Description <String>]`: IP-korlátozási szabály leírása.</span><span class="sxs-lookup"><span data-stu-id="8efb5-224">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="8efb5-225">`[IPAddress <String>]`: Az IP-cím, amelyre a biztonsági korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="8efb5-225">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="8efb5-226">Ez lehet csak ipv4-cím (kötelező AlhálózatiMaszk tulajdonság) vagy CIDR-cím, például ipv4/mask (leading bit match).</span><span class="sxs-lookup"><span data-stu-id="8efb5-226">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="8efb5-227">CIDR esetén az Alhálózatimaszk tulajdonságot nem kell megadni.</span><span class="sxs-lookup"><span data-stu-id="8efb5-227">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="8efb5-228">`[Name <String>]`: IP-korlátozási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-228">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="8efb5-229">`[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="8efb5-229">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="8efb5-230">`[SubnetMask <String>]`: Az IP-címek tartományának alhálózati maszkja, amelyekre a korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="8efb5-230">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="8efb5-231">`[SubnetTrafficTag <Int32?>]`: (belső) Alhálózati adatforgalom címkéje</span><span class="sxs-lookup"><span data-stu-id="8efb5-231">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="8efb5-232">`[Tag <IPFilterTag?>]`: Meghatározza, hogy mire fogja használni ezt az IP-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="8efb5-232">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="8efb5-233">Ez a proxyk IP-szűrésének támogatását támogatja.</span><span class="sxs-lookup"><span data-stu-id="8efb5-233">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="8efb5-234">`[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8efb5-234">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="8efb5-235">`[VnetTrafficTag <Int32?>]`: (belső) Vnet-adatforgalom címkéje</span><span class="sxs-lookup"><span data-stu-id="8efb5-235">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="8efb5-236">`[JavaContainer <String>]`: Java tároló.</span><span class="sxs-lookup"><span data-stu-id="8efb5-236">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="8efb5-237">`[JavaContainerVersion <String>]`: Java-tároló verziója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-237">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="8efb5-238">`[JavaVersion <String>]`: Java verzió.</span><span class="sxs-lookup"><span data-stu-id="8efb5-238">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="8efb5-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximális lemezméret-használat MB-ban.</span><span class="sxs-lookup"><span data-stu-id="8efb5-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="8efb5-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximális memóriahasználat MB-ban.</span><span class="sxs-lookup"><span data-stu-id="8efb5-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="8efb5-241">`[LimitMaxPercentageCpu <Double?>]`: Maximális engedélyezett processzorhasználati százalékérték.</span><span class="sxs-lookup"><span data-stu-id="8efb5-241">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="8efb5-242">`[LinuxFxVersion <String>]`: Linux app keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="8efb5-242">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="8efb5-243">`[LoadBalancing <SiteLoadBalancing?>]`: Webhely terheléselosztása.</span><span class="sxs-lookup"><span data-stu-id="8efb5-243">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="8efb5-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók címtárméretkorlátja.</span><span class="sxs-lookup"><span data-stu-id="8efb5-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="8efb5-246">`[MachineKeyDecryption <String>]`: A visszafejtési algoritmus.</span><span class="sxs-lookup"><span data-stu-id="8efb5-246">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="8efb5-247">`[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.</span><span class="sxs-lookup"><span data-stu-id="8efb5-247">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="8efb5-248">`[MachineKeyValidation <String>]`: Gépkulcs érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="8efb5-248">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="8efb5-249">`[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.</span><span class="sxs-lookup"><span data-stu-id="8efb5-249">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="8efb5-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt folyamat mód.</span><span class="sxs-lookup"><span data-stu-id="8efb5-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="8efb5-251">`[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás identitásazonosítója</span><span class="sxs-lookup"><span data-stu-id="8efb5-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="8efb5-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Az SSL-kérelmekhez minimálisan szükséges TLS-verzió konfigurálása</span><span class="sxs-lookup"><span data-stu-id="8efb5-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="8efb5-253">`[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-253">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="8efb5-254">`[NodeVersion <String>]`: A Node.js.</span><span class="sxs-lookup"><span data-stu-id="8efb5-254">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="8efb5-255">`[NumberOfWorker <Int32?>]`: Dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="8efb5-255">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="8efb5-256">`[PhpVersion <String>]`: A PHP verziója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-256">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="8efb5-257">`[PowerShellVersion <String>]`: A PowerShell verziója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-257">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="8efb5-258">`[PreWarmedInstanceCount <Int32?>]`: Awarmed példányok száma.</span><span class="sxs-lookup"><span data-stu-id="8efb5-258">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="8efb5-259">Ez a beállítás csak a fogyasztási és rugalmas csomagokra vonatkozik</span><span class="sxs-lookup"><span data-stu-id="8efb5-259">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="8efb5-260">`[PublishingUsername <String>]`: Közzétételi felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="8efb5-260">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="8efb5-261">`[PushKind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="8efb5-261">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="8efb5-262">`[PythonVersion <String>]`: A Python verziója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-262">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="8efb5-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> ha a távoli hibakeresés engedélyezve van; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-264">`[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.</span><span class="sxs-lookup"><span data-stu-id="8efb5-264">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="8efb5-265">`[RequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="8efb5-265">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="8efb5-266">`[RequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="8efb5-266">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="8efb5-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> ha a kéréskövetés engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-268">`[RequestTracingExpirationTime <DateTime?>]`: A lejárati idő nyomon követésének kérése.</span><span class="sxs-lookup"><span data-stu-id="8efb5-268">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="8efb5-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: AZ SCM IP-biztonsági korlátozásai.</span><span class="sxs-lookup"><span data-stu-id="8efb5-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="8efb5-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-biztonsági korlátozások az scm fő használatára.</span><span class="sxs-lookup"><span data-stu-id="8efb5-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="8efb5-271">`[ScmType <ScmType?>]`: SCM típus.</span><span class="sxs-lookup"><span data-stu-id="8efb5-271">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="8efb5-272">`[SlowRequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="8efb5-272">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="8efb5-273">`[SlowRequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="8efb5-273">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="8efb5-274">`[SlowRequestTimeTaken <String>]`: A szükséges idő.</span><span class="sxs-lookup"><span data-stu-id="8efb5-274">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="8efb5-275">`[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használható címkék listáját tartalmazó JSON-karakterláncot állít be vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="8efb5-275">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="8efb5-276">`[TagsRequiringAuth <String>]`: A leküldéses regisztrációs végponton felhasználói hitelesítést igénylő címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="8efb5-276">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="8efb5-277">A címkék alfanumerikus karakterekből állhatnak, és a következő karakterekből állhatnak: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="8efb5-277">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="8efb5-278">Az érvényesítést a PushRequestHandlerben kell elvégezni.</span><span class="sxs-lookup"><span data-stu-id="8efb5-278">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="8efb5-279">`[TracingOption <String>]`: Nyomkövetési beállítások.</span><span class="sxs-lookup"><span data-stu-id="8efb5-279">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="8efb5-280">`[TriggerPrivateBytesInKb <Int32?>]`: Egy magánjellegű bájton alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="8efb5-280">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="8efb5-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Egy állapotkódon alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="8efb5-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="8efb5-282">`[Count <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="8efb5-282">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="8efb5-283">`[Status <Int32?>]`: HTTP-állapotkód.</span><span class="sxs-lookup"><span data-stu-id="8efb5-283">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="8efb5-284">`[SubStatus <Int32?>]`: Alállapot kérése.</span><span class="sxs-lookup"><span data-stu-id="8efb5-284">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="8efb5-285">`[TimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="8efb5-285">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="8efb5-286">`[Win32Status <Int32?>]`: Win32 hibakód.</span><span class="sxs-lookup"><span data-stu-id="8efb5-286">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="8efb5-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> a 32 bites munkavégző folyamathoz; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.</span><span class="sxs-lookup"><span data-stu-id="8efb5-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="8efb5-289">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="8efb5-289">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="8efb5-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> ha az előbetöltés engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="8efb5-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak virtuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="8efb5-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="8efb5-292">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="8efb5-292">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="8efb5-293">`[VirtualPath <String>]`: Virtuális alkalmazás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8efb5-293">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="8efb5-294">`[VirtualPath <String>]`: Virtuális elérési út.</span><span class="sxs-lookup"><span data-stu-id="8efb5-294">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="8efb5-295">`[VnetName <String>]`: Virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="8efb5-295">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="8efb5-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> ha a WebSocket engedélyezve van, egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="8efb5-297">`[WindowsFxVersion <String>]`: Xenon app keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="8efb5-297">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="8efb5-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás identitásazonosítója</span><span class="sxs-lookup"><span data-stu-id="8efb5-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="8efb5-299">`[ContainerSize <Int32?>]`: A függvénytároló mérete.</span><span class="sxs-lookup"><span data-stu-id="8efb5-299">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="8efb5-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximális napi memóriaidő-kvóta (csak dinamikus alkalmazások esetén alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="8efb5-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="8efb5-301">`[Enabled <Boolean?>]`: <code>true</code> ha az alkalmazás engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-301">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="8efb5-302">Ennek az értéknek a hamis értékre állításával letiltja az appot (offline állapotba vált).</span><span class="sxs-lookup"><span data-stu-id="8efb5-302">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="8efb5-303">`[HostNameSslState <IHostNameSslState[]>]`: Az SSL-állomásnevek SSL-államai az alkalmazás állomásnevéhez szükséges SSL-kötések kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="8efb5-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="8efb5-304">`[HostType <HostType?>]`: Azt jelzi, hogy az állomásnév normál vagy tárházi állomásnév-e.</span><span class="sxs-lookup"><span data-stu-id="8efb5-304">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="8efb5-305">`[Name <String>]`: Állomásnév.</span><span class="sxs-lookup"><span data-stu-id="8efb5-305">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="8efb5-306">`[SslState <SslState?>]`: SSL-típus.</span><span class="sxs-lookup"><span data-stu-id="8efb5-306">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="8efb5-307">`[Thumbprint <String>]`: SSL-tanúsítvány thumbprint.</span><span class="sxs-lookup"><span data-stu-id="8efb5-307">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="8efb5-308">`[ToUpdate <Boolean?>]`: A meglévő <code>true</code> állomásnév frissítésére van beállítva.</span><span class="sxs-lookup"><span data-stu-id="8efb5-308">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="8efb5-309">`[VirtualIP <String>]`: Az IP-alapú SSL engedélyezése esetén az állomásnévhez hozzárendelt virtuális IP-cím.</span><span class="sxs-lookup"><span data-stu-id="8efb5-309">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="8efb5-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> az app nyilvános állomásnevének letiltásához; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="8efb5-311">Ha <code>true</code> az app csak API-kezelési folyamaton keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="8efb5-311">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="8efb5-312">`[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8efb5-312">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="8efb5-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: úgy konfigurál egy webhelyet, hogy csak a https-kérelmeket fogadja el.</span><span class="sxs-lookup"><span data-stu-id="8efb5-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="8efb5-314">A http-kérelmek problémáinak átirányítása</span><span class="sxs-lookup"><span data-stu-id="8efb5-314">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="8efb5-315">`[HyperV <Boolean?>]`: Hyper-V védőfal.</span><span class="sxs-lookup"><span data-stu-id="8efb5-315">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="8efb5-316">`[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="8efb5-316">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="8efb5-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által hozzárendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="8efb5-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="8efb5-318">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="8efb5-318">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="8efb5-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="8efb5-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8efb5-320">`[IsXenon <Boolean?>]`: Elavult: Hyper-V védőfal.</span><span class="sxs-lookup"><span data-stu-id="8efb5-320">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="8efb5-321">`[RedundancyMode <RedundancyMode?>]`: Webhely redundancia üzemmódja</span><span class="sxs-lookup"><span data-stu-id="8efb5-321">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="8efb5-322">`[Reserved <Boolean?>]`: <code>true</code> ha foglalt; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-322">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="8efb5-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> leállítja az SCM (KUDU) webhelyet az alkalmazás leállításakor; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="8efb5-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="8efb5-324">Az alapértelmezett érték <code>false</code> a .</span><span class="sxs-lookup"><span data-stu-id="8efb5-324">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="8efb5-325">`[ServerFarmId <String>]`: A társított App Service-csomag erőforrás-azonosítója, formátuma: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="8efb5-325">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="8efb5-326">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8efb5-326">RELATED LINKS</span></span>

