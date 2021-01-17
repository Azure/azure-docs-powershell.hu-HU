---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 1049c4b69f0d64c9b18063618ee09018fd224196
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469741"
---
# <span data-ttu-id="eb78a-101">Get-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="eb78a-101">Get-AzFunctionAppSetting</span></span>

## <span data-ttu-id="eb78a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb78a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb78a-103">Alkalmazásbeállításokat ad egy függvényalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="eb78a-103">Gets app settings for a function app.</span></span>

## <span data-ttu-id="eb78a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb78a-104">SYNTAX</span></span>

### <span data-ttu-id="eb78a-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb78a-105">ByName (Default)</span></span>
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eb78a-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="eb78a-106">ByObjectInput</span></span>
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="eb78a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb78a-107">DESCRIPTION</span></span>
<span data-ttu-id="eb78a-108">Alkalmazásbeállításokat ad egy függvényalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="eb78a-108">Gets app settings for a function app.</span></span>

## <span data-ttu-id="eb78a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb78a-109">EXAMPLES</span></span>

### <span data-ttu-id="eb78a-110">1. példa: A függvényalkalmazás appbeállításának lekérte.</span><span class="sxs-lookup"><span data-stu-id="eb78a-110">Example 1: Get the app settings of a function app.</span></span>
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="eb78a-111">Ez a parancs egy függvényalkalmazás appbeállítását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eb78a-111">This command gets the app settings of a function app.</span></span>

## <span data-ttu-id="eb78a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb78a-112">PARAMETERS</span></span>

### <span data-ttu-id="eb78a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb78a-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="eb78a-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb78a-114">-InputObject</span></span>
<span data-ttu-id="eb78a-115">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="eb78a-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb78a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eb78a-116">-Name</span></span>
<span data-ttu-id="eb78a-117">A függvényalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-117">Name of the function app.</span></span>

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

### <span data-ttu-id="eb78a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb78a-118">-ResourceGroupName</span></span>
<span data-ttu-id="eb78a-119">Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="eb78a-119">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="eb78a-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb78a-120">-SubscriptionId</span></span>
<span data-ttu-id="eb78a-121">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-121">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb78a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb78a-122">-Confirm</span></span>
<span data-ttu-id="eb78a-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eb78a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb78a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb78a-124">-WhatIf</span></span>
<span data-ttu-id="eb78a-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eb78a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb78a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb78a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb78a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb78a-127">CommonParameters</span></span>
<span data-ttu-id="eb78a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb78a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb78a-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb78a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb78a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb78a-130">INPUTS</span></span>

### <span data-ttu-id="eb78a-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="eb78a-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="eb78a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb78a-132">OUTPUTS</span></span>

### <span data-ttu-id="eb78a-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="eb78a-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="eb78a-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb78a-134">NOTES</span></span>

<span data-ttu-id="eb78a-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eb78a-135">ALIASES</span></span>

<span data-ttu-id="eb78a-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="eb78a-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb78a-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="eb78a-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb78a-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb78a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb78a-139">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="eb78a-139">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="eb78a-140">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eb78a-140">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="eb78a-141">`CloningInfoSourceWebAppId <String>`: ARM forrásalkalmazás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="eb78a-141">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="eb78a-142">Az alkalmazáserőforrás-azonosító a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}, production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.</span><span class="sxs-lookup"><span data-stu-id="eb78a-142">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="eb78a-143">`[Kind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="eb78a-143">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="eb78a-144">`[Tag <IResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="eb78a-144">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="eb78a-145">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="eb78a-145">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="eb78a-146">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> az ügyfélkapcsolat engedélyezéséhez; a munkamenet-affinitás cookie-k küldésének megállítása, amelyek az ügyfélalkalmazások kérését ugyanannak a munkamenetnek a példányára <code>false</code> irányítják.</span><span class="sxs-lookup"><span data-stu-id="eb78a-146">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="eb78a-147">Az alapértelmezett érték <code>true</code> a .</span><span class="sxs-lookup"><span data-stu-id="eb78a-147">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="eb78a-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyfél tanúsítvány-hitelesítésének (TLS közös hitelesítés) engedélyezéséhez; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="eb78a-149">Az alapértelmezett érték <code>false</code> a .</span><span class="sxs-lookup"><span data-stu-id="eb78a-149">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="eb78a-150">`[ClientCertExclusionPath <String>]`: Ügyfél tanúsítványának hitelesítése vesszővel elválasztott kivétel elérési útjai</span><span class="sxs-lookup"><span data-stu-id="eb78a-150">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="eb78a-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazásbeállítási felülbírálások a klónozott appok esetén.</span><span class="sxs-lookup"><span data-stu-id="eb78a-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="eb78a-152">Ha meg van adva, ezek a beállítások felülbírálják a forrásalkalmazásból klónozott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="eb78a-152">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="eb78a-153">Ellenkező esetben a forrásalkalmazás alkalmazásbeállítása megmarad.</span><span class="sxs-lookup"><span data-stu-id="eb78a-153">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="eb78a-154">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="eb78a-154">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="eb78a-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> az egyéni állomásnevek klónozása a forrásalkalmazásból, ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="eb78a-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrásalkalmazásból a forrásvezérlők klónozása; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="eb78a-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> konfigurálhatja a terheléselosztást a forrás- és célalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="eb78a-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="eb78a-158">`[CloningInfoCorrelationId <String>]`: A cloning művelet korrelációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-158">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="eb78a-159">Ez az azonosító több cloning műveletet hoz létre ugyanannak a pillanatfelvételnek a végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="eb78a-159">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="eb78a-160">`[CloningInfoHostingEnvironment <String>]`: App szolgáltatási környezet.</span><span class="sxs-lookup"><span data-stu-id="eb78a-160">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="eb78a-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a célalkalmazás felülírása; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="eb78a-162">`[CloningInfoSourceWebAppLocation <String>]`: A forrásalkalmazás helye, pl. Nyugat-Usa vagy Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="eb78a-162">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="eb78a-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM a Traffic Manager-profil erőforrás-azonosítóját, ha létezik ilyen.</span><span class="sxs-lookup"><span data-stu-id="eb78a-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="eb78a-164">A Traffic Manager erőforrás-azonosítója a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="eb78a-164">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="eb78a-165">`[CloningInfoTrafficManagerProfileName <String>]`: A létrehozni szükséges Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-165">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="eb78a-166">Erre csak akkor van szükség, ha a Traffic Manager-profil még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="eb78a-166">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="eb78a-167">`[Config <ISiteConfig>]`: Az app konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="eb78a-167">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="eb78a-168">`IsPushEnabled <Boolean>`: Jelölőt kap vagy állít be, amely jelzi, hogy a leküldéses végpont engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="eb78a-168">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="eb78a-169">`[ActionMinProcessExecutionTime <String>]`: A művelet végrehajtása előtt a folyamat minimálisan szükséges ideje</span><span class="sxs-lookup"><span data-stu-id="eb78a-169">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="eb78a-170">`[ActionType <AutoHealActionType?>]`: Előre meghatározott teendő.</span><span class="sxs-lookup"><span data-stu-id="eb78a-170">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="eb78a-171">`[AlwaysOn <Boolean?>]`: <code>true</code> ha a Mindig be van kapcsolva, egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-171">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-172">`[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.</span><span class="sxs-lookup"><span data-stu-id="eb78a-172">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="eb78a-173">`[ApiManagementConfigId <String>]`: APIM-Api azonosító.</span><span class="sxs-lookup"><span data-stu-id="eb78a-173">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="eb78a-174">`[AppCommandLine <String>]`: Elindítandó alkalmazás parancssora.</span><span class="sxs-lookup"><span data-stu-id="eb78a-174">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="eb78a-175">`[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.</span><span class="sxs-lookup"><span data-stu-id="eb78a-175">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="eb78a-176">`[Name <String>]`: Párnév.</span><span class="sxs-lookup"><span data-stu-id="eb78a-176">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="eb78a-177">`[Value <String>]`: Érték párosítása.</span><span class="sxs-lookup"><span data-stu-id="eb78a-177">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="eb78a-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> ha az Automatikus lejátszás funkció be van kapcsolva; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-179">`[AutoSwapSlotName <String>]`: Az automatikus cserehely neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-179">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="eb78a-180">`[ConnectionString <IConnStringInfo[]>]`: Kapcsolati karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="eb78a-180">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="eb78a-181">`[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.</span><span class="sxs-lookup"><span data-stu-id="eb78a-181">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="eb78a-182">`[Name <String>]`: A kapcsolati karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-182">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="eb78a-183">`[Type <ConnectionStringType?>]`: Az adatbázis típusa.</span><span class="sxs-lookup"><span data-stu-id="eb78a-183">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="eb78a-184">`[CorAllowedOrigin <String[]>]`: Beállítja vagy beállítja azon forráslistát, amely lehetővé teszi a több forrásból való hívásokat (például: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="eb78a-184">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="eb78a-185">Az összes engedélyezése a "\*" szóra van állítva.</span><span class="sxs-lookup"><span data-stu-id="eb78a-185">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="eb78a-186">`[CorSupportCredentials <Boolean?>]`: Beállítja vagy beállítja, hogy engedélyezettek-e a hitelesítő adatokkal megadott CORS-kérések.</span><span class="sxs-lookup"><span data-stu-id="eb78a-186">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="eb78a-187">További         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         részleteket itt talál.</span><span class="sxs-lookup"><span data-stu-id="eb78a-187">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="eb78a-188">`[CustomActionExe <String>]`: Futtatható végrehajtható fájl.</span><span class="sxs-lookup"><span data-stu-id="eb78a-188">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="eb78a-189">`[CustomActionParameter <String>]`: A végrehajtható fájl paraméterei.</span><span class="sxs-lookup"><span data-stu-id="eb78a-189">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="eb78a-190">`[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.</span><span class="sxs-lookup"><span data-stu-id="eb78a-190">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="eb78a-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ha a részletes hibanaplózás engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-192">`[DocumentRoot <String>]`: Dokumentumgyök.</span><span class="sxs-lookup"><span data-stu-id="eb78a-192">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="eb78a-193">`[DynamicTagsJson <String>]`: Egy olyan JSON-karakterláncot kap vagy állít be, amely a leküldéses regisztrációs végponton található felhasználói igények alapján kiértékelésre kerül a dinamikus címkék listáját tartalmazó JSON-karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="eb78a-193">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="eb78a-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: A felfutási szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="eb78a-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="eb78a-195">`[ActionHostName <String>]`: Annak a tárolóhelynek a állomásneve, amelybe a forgalmat átirányítja a rendszer, ha úgy dönt.</span><span class="sxs-lookup"><span data-stu-id="eb78a-195">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="eb78a-196">Például:</span><span class="sxs-lookup"><span data-stu-id="eb78a-196">E.g.</span></span> <span data-ttu-id="eb78a-197">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="eb78a-197">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="eb78a-198">`[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmus is meg lehet adni a TiPCallback webhelybővítményben, amely URL-címet is meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="eb78a-198">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="eb78a-199">Lásd a TiPCallback webhelybővítményét az állványhoz és a szerződésekhez.</span><span class="sxs-lookup"><span data-stu-id="eb78a-199">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="eb78a-200"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="eb78a-200">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="eb78a-201">`[ChangeIntervalInMinute <Int32?>]`: Az ReroutePercentage átértékelhető intervallumát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="eb78a-201">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="eb78a-202">`[ChangeStep <Double?>]`: Automatikus felfutás esetén ezt a lépést kell hozzáadni/eltávolítani, amíg el nem éri a <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> vagy         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-202">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="eb78a-203">A webhely metrikákat a .\nCustom döntési algoritmusban megadott N percenként ellenőrzi a <code>ChangeIntervalInMinutes</code> TiPCallback webhelybővítmény, amely az URL-címet meg lehet <code>ChangeDecisionCallbackUrl</code> adni.</span><span class="sxs-lookup"><span data-stu-id="eb78a-203">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="eb78a-204">`[MaxReroutePercentage <Double?>]`: Azt a felső határot adja meg, amely alatt a ReroutePercentage meg fog maradni.</span><span class="sxs-lookup"><span data-stu-id="eb78a-204">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="eb78a-205">`[MinReroutePercentage <Double?>]`: Azt az alsó határértéket adja meg, amely fölött az ReroutePercentage meg fog maradni.</span><span class="sxs-lookup"><span data-stu-id="eb78a-205">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="eb78a-206">`[Name <String>]`: Az útválasztási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-206">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="eb78a-207">Az ajánlott név a kísérlet során a forgalmat tároló tárolóhelyre mutat.</span><span class="sxs-lookup"><span data-stu-id="eb78a-207">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="eb78a-208">`[ReroutePercentage <Double?>]`: Azon forgalom százalékos aránya, amelyre a rendszer átirányítja <code>ActionHostName</code> a forgalmat.</span><span class="sxs-lookup"><span data-stu-id="eb78a-208">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="eb78a-209">`[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás állapota</span><span class="sxs-lookup"><span data-stu-id="eb78a-209">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="eb78a-210">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span><span class="sxs-lookup"><span data-stu-id="eb78a-210">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="eb78a-211">`[Argument <String>]`: A parancsprogram-processzornak át kell adandó parancssori argumentumokat.</span><span class="sxs-lookup"><span data-stu-id="eb78a-211">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="eb78a-212">`[Extension <String>]`: Az ilyen kiterjesztésű kérelmeket a megadott FastCGI alkalmazással kezeljük.</span><span class="sxs-lookup"><span data-stu-id="eb78a-212">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="eb78a-213">`[ScriptProcessor <String>]`: A FastCGI alkalmazás abszolút elérési útja.</span><span class="sxs-lookup"><span data-stu-id="eb78a-213">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="eb78a-214">`[HealthCheckPath <String>]`: Állapot-ellenőrzés útvonala</span><span class="sxs-lookup"><span data-stu-id="eb78a-214">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="eb78a-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfigurál egy webhelyet, amely engedélyezi az ügyfeleknek a http2.0-s kapcsolaton keresztüli csatlakozást</span><span class="sxs-lookup"><span data-stu-id="eb78a-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="eb78a-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> ha a HTTP-naplózás engedélyezve van; egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: A fő IP-biztonsági korlátozásai.</span><span class="sxs-lookup"><span data-stu-id="eb78a-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="eb78a-218">`[Action <String>]`: Hozzáférés engedélyezése vagy elutasítása ehhez az IP-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="eb78a-218">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="eb78a-219">`[Description <String>]`: IP-korlátozási szabály leírása.</span><span class="sxs-lookup"><span data-stu-id="eb78a-219">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="eb78a-220">`[IPAddress <String>]`: Az IP-cím, amelyre a biztonsági korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="eb78a-220">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="eb78a-221">Ez lehet csak ipv4-cím (kötelező AlhálózatiMaszk tulajdonság) vagy CIDR-cím, például ipv4/mask (leading bit match).</span><span class="sxs-lookup"><span data-stu-id="eb78a-221">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="eb78a-222">CIDR esetén az Alhálózatimaszk tulajdonságot nem kell megadni.</span><span class="sxs-lookup"><span data-stu-id="eb78a-222">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="eb78a-223">`[Name <String>]`: IP-korlátozási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-223">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="eb78a-224">`[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="eb78a-224">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="eb78a-225">`[SubnetMask <String>]`: Az IP-címek tartományának alhálózati maszkja, amelyekre a korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="eb78a-225">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="eb78a-226">`[SubnetTrafficTag <Int32?>]`: (belső) Alhálózati adatforgalom címkéje</span><span class="sxs-lookup"><span data-stu-id="eb78a-226">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="eb78a-227">`[Tag <IPFilterTag?>]`: Meghatározza, hogy mire fogja használni ezt az IP-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="eb78a-227">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="eb78a-228">Ez a proxyk IP-szűrésének támogatását támogatja.</span><span class="sxs-lookup"><span data-stu-id="eb78a-228">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="eb78a-229">`[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="eb78a-229">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="eb78a-230">`[VnetTrafficTag <Int32?>]`: (belső) Vnet-adatforgalom címkéje</span><span class="sxs-lookup"><span data-stu-id="eb78a-230">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="eb78a-231">`[JavaContainer <String>]`: Java tároló.</span><span class="sxs-lookup"><span data-stu-id="eb78a-231">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="eb78a-232">`[JavaContainerVersion <String>]`: Java-tároló verziója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-232">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="eb78a-233">`[JavaVersion <String>]`: Java verzió.</span><span class="sxs-lookup"><span data-stu-id="eb78a-233">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="eb78a-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximális lemezméret-használat MB-ban.</span><span class="sxs-lookup"><span data-stu-id="eb78a-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="eb78a-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximális memóriahasználat MB-ban.</span><span class="sxs-lookup"><span data-stu-id="eb78a-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="eb78a-236">`[LimitMaxPercentageCpu <Double?>]`: Maximális engedélyezett processzorhasználati százalékérték.</span><span class="sxs-lookup"><span data-stu-id="eb78a-236">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="eb78a-237">`[LinuxFxVersion <String>]`: Linux app keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="eb78a-237">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="eb78a-238">`[LoadBalancing <SiteLoadBalancing?>]`: Webhely terheléselosztása.</span><span class="sxs-lookup"><span data-stu-id="eb78a-238">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="eb78a-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók címtárméretkorlátja.</span><span class="sxs-lookup"><span data-stu-id="eb78a-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="eb78a-241">`[MachineKeyDecryption <String>]`: A visszafejtési algoritmus.</span><span class="sxs-lookup"><span data-stu-id="eb78a-241">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="eb78a-242">`[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.</span><span class="sxs-lookup"><span data-stu-id="eb78a-242">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="eb78a-243">`[MachineKeyValidation <String>]`: Gépkulcs érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="eb78a-243">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="eb78a-244">`[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.</span><span class="sxs-lookup"><span data-stu-id="eb78a-244">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="eb78a-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt folyamat mód.</span><span class="sxs-lookup"><span data-stu-id="eb78a-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="eb78a-246">`[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás identitásazonosítója</span><span class="sxs-lookup"><span data-stu-id="eb78a-246">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="eb78a-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Az SSL-kérelmekhez minimálisan szükséges TLS-verzió konfigurálása</span><span class="sxs-lookup"><span data-stu-id="eb78a-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="eb78a-248">`[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-248">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="eb78a-249">`[NodeVersion <String>]`: A Node.js.</span><span class="sxs-lookup"><span data-stu-id="eb78a-249">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="eb78a-250">`[NumberOfWorker <Int32?>]`: Dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="eb78a-250">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="eb78a-251">`[PhpVersion <String>]`: A PHP verziója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-251">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="eb78a-252">`[PowerShellVersion <String>]`: A PowerShell verziója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-252">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="eb78a-253">`[PreWarmedInstanceCount <Int32?>]`: Awarmed példányok száma.</span><span class="sxs-lookup"><span data-stu-id="eb78a-253">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="eb78a-254">Ez a beállítás csak a fogyasztási és rugalmas csomagokra vonatkozik</span><span class="sxs-lookup"><span data-stu-id="eb78a-254">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="eb78a-255">`[PublishingUsername <String>]`: Közzétételi felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="eb78a-255">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="eb78a-256">`[PushKind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="eb78a-256">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="eb78a-257">`[PythonVersion <String>]`: A Python verziója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-257">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="eb78a-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> ha a távoli hibakeresés engedélyezve van; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-259">`[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.</span><span class="sxs-lookup"><span data-stu-id="eb78a-259">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="eb78a-260">`[RequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="eb78a-260">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="eb78a-261">`[RequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="eb78a-261">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="eb78a-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> ha a kéréskövetés engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-263">`[RequestTracingExpirationTime <DateTime?>]`: A lejárati idő nyomon követésének kérése.</span><span class="sxs-lookup"><span data-stu-id="eb78a-263">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="eb78a-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: AZ SCM IP-biztonsági korlátozásai.</span><span class="sxs-lookup"><span data-stu-id="eb78a-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="eb78a-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-biztonsági korlátozások az scm fő használatára.</span><span class="sxs-lookup"><span data-stu-id="eb78a-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="eb78a-266">`[ScmType <ScmType?>]`: SCM típus.</span><span class="sxs-lookup"><span data-stu-id="eb78a-266">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="eb78a-267">`[SlowRequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="eb78a-267">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="eb78a-268">`[SlowRequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="eb78a-268">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="eb78a-269">`[SlowRequestTimeTaken <String>]`: A szükséges idő.</span><span class="sxs-lookup"><span data-stu-id="eb78a-269">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="eb78a-270">`[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használható címkék listáját tartalmazó JSON-karakterláncot állít be vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="eb78a-270">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="eb78a-271">`[TagsRequiringAuth <String>]`: A leküldéses regisztrációs végponton felhasználói hitelesítést igénylő címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="eb78a-271">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="eb78a-272">A címkék alfanumerikus karakterekből állhatnak, és a következő karakterekből állhatnak: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="eb78a-272">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="eb78a-273">Az érvényesítést a PushRequestHandlerben kell elvégezni.</span><span class="sxs-lookup"><span data-stu-id="eb78a-273">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="eb78a-274">`[TracingOption <String>]`: Nyomkövetési beállítások.</span><span class="sxs-lookup"><span data-stu-id="eb78a-274">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="eb78a-275">`[TriggerPrivateBytesInKb <Int32?>]`: Egy magánjellegű bájton alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="eb78a-275">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="eb78a-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Egy állapotkódon alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="eb78a-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="eb78a-277">`[Count <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="eb78a-277">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="eb78a-278">`[Status <Int32?>]`: HTTP-állapotkód.</span><span class="sxs-lookup"><span data-stu-id="eb78a-278">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="eb78a-279">`[SubStatus <Int32?>]`: Alállapot kérése.</span><span class="sxs-lookup"><span data-stu-id="eb78a-279">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="eb78a-280">`[TimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="eb78a-280">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="eb78a-281">`[Win32Status <Int32?>]`: Win32 hibakód.</span><span class="sxs-lookup"><span data-stu-id="eb78a-281">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="eb78a-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> a 32 bites munkavégző folyamathoz; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.</span><span class="sxs-lookup"><span data-stu-id="eb78a-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="eb78a-284">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="eb78a-284">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="eb78a-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> ha az előbetöltés engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="eb78a-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak virtuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="eb78a-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="eb78a-287">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="eb78a-287">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="eb78a-288">`[VirtualPath <String>]`: Virtuális alkalmazás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="eb78a-288">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="eb78a-289">`[VirtualPath <String>]`: Virtuális elérési út.</span><span class="sxs-lookup"><span data-stu-id="eb78a-289">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="eb78a-290">`[VnetName <String>]`: Virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="eb78a-290">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="eb78a-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> ha a WebSocket engedélyezve van, egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="eb78a-292">`[WindowsFxVersion <String>]`: Xenon app keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="eb78a-292">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="eb78a-293">`[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás identitásazonosítója</span><span class="sxs-lookup"><span data-stu-id="eb78a-293">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="eb78a-294">`[ContainerSize <Int32?>]`: A függvénytároló mérete.</span><span class="sxs-lookup"><span data-stu-id="eb78a-294">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="eb78a-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximális napi memóriaidő-kvóta (csak dinamikus alkalmazások esetén alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="eb78a-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="eb78a-296">`[Enabled <Boolean?>]`: <code>true</code> ha az alkalmazás engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-296">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="eb78a-297">Ennek az értéknek a hamis értékre állításával letiltja az appot (offline állapotba vált).</span><span class="sxs-lookup"><span data-stu-id="eb78a-297">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="eb78a-298">`[HostNameSslState <IHostNameSslState[]>]`: Az SSL-állomásnevek SSL-államai az alkalmazás állomásnevéhez szükséges SSL-kötések kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="eb78a-298">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="eb78a-299">`[HostType <HostType?>]`: Azt jelzi, hogy az állomásnév normál vagy tárházi állomásnév-e.</span><span class="sxs-lookup"><span data-stu-id="eb78a-299">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="eb78a-300">`[Name <String>]`: Állomásnév.</span><span class="sxs-lookup"><span data-stu-id="eb78a-300">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="eb78a-301">`[SslState <SslState?>]`: SSL-típus.</span><span class="sxs-lookup"><span data-stu-id="eb78a-301">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="eb78a-302">`[Thumbprint <String>]`: SSL-tanúsítvány thumbprint.</span><span class="sxs-lookup"><span data-stu-id="eb78a-302">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="eb78a-303">`[ToUpdate <Boolean?>]`: A meglévő <code>true</code> állomásnév frissítésére van beállítva.</span><span class="sxs-lookup"><span data-stu-id="eb78a-303">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="eb78a-304">`[VirtualIP <String>]`: Az IP-alapú SSL engedélyezése esetén az állomásnévhez hozzárendelt virtuális IP-cím.</span><span class="sxs-lookup"><span data-stu-id="eb78a-304">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="eb78a-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> az app nyilvános állomásnevének letiltásához; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="eb78a-306">Ha <code>true</code> az app csak API-kezelési folyamaton keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="eb78a-306">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="eb78a-307">`[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb78a-307">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="eb78a-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: úgy konfigurál egy webhelyet, hogy csak a https-kérelmeket fogadja el.</span><span class="sxs-lookup"><span data-stu-id="eb78a-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="eb78a-309">A http-kérelmek problémáinak átirányítása</span><span class="sxs-lookup"><span data-stu-id="eb78a-309">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="eb78a-310">`[HyperV <Boolean?>]`: Hyper-V védőfal.</span><span class="sxs-lookup"><span data-stu-id="eb78a-310">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="eb78a-311">`[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="eb78a-311">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="eb78a-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által hozzárendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="eb78a-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="eb78a-313">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="eb78a-313">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="eb78a-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="eb78a-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="eb78a-315">`[IsXenon <Boolean?>]`: Elavult: Hyper-V védőfal.</span><span class="sxs-lookup"><span data-stu-id="eb78a-315">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="eb78a-316">`[RedundancyMode <RedundancyMode?>]`: Webhely redundancia üzemmódja</span><span class="sxs-lookup"><span data-stu-id="eb78a-316">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="eb78a-317">`[Reserved <Boolean?>]`: <code>true</code> ha foglalt; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-317">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="eb78a-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> leállítja az SCM (KUDU) webhelyet az alkalmazás leállításakor; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="eb78a-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="eb78a-319">Az alapértelmezett érték <code>false</code> a .</span><span class="sxs-lookup"><span data-stu-id="eb78a-319">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="eb78a-320">`[ServerFarmId <String>]`: A társított App Service-csomag erőforrás-azonosítója, formátuma: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="eb78a-320">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="eb78a-321">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb78a-321">RELATED LINKS</span></span>

