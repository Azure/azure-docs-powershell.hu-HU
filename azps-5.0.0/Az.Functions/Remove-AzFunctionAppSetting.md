---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185416"
---
# <span data-ttu-id="310d2-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="310d2-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="310d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="310d2-102">SYNOPSIS</span></span>
<span data-ttu-id="310d2-103">Az app-beállítások eltávolítása egy függvény alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="310d2-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="310d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="310d2-104">SYNTAX</span></span>

### <span data-ttu-id="310d2-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="310d2-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="310d2-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="310d2-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="310d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="310d2-107">DESCRIPTION</span></span>
<span data-ttu-id="310d2-108">Az app-beállítások eltávolítása egy függvény alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="310d2-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="310d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="310d2-109">EXAMPLES</span></span>

### <span data-ttu-id="310d2-110">1. példa: az app-beállítások eltávolítása egy függvény alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="310d2-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="310d2-111">Ez a parancs eltávolítja az App beállításait egy függvény alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="310d2-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="310d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="310d2-112">PARAMETERS</span></span>

### <span data-ttu-id="310d2-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="310d2-113">-AppSettingName</span></span>
<span data-ttu-id="310d2-114">A Function App alkalmazásból eltávolítandó Function app-beállítások listája.</span><span class="sxs-lookup"><span data-stu-id="310d2-114">List of function app settings to be removed from the function app.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310d2-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="310d2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="310d2-116">-Force</span></span>
<span data-ttu-id="310d2-117">Kényszeríti a parancsmagot a Function app beállítás eltávolítására a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="310d2-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="310d2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="310d2-118">-InputObject</span></span>
<span data-ttu-id="310d2-119">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="310d2-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="310d2-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="310d2-120">-Name</span></span>
<span data-ttu-id="310d2-121">A függvény app neve.</span><span class="sxs-lookup"><span data-stu-id="310d2-121">Name of the function app.</span></span>

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

### <span data-ttu-id="310d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="310d2-123">Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="310d2-123">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="310d2-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="310d2-124">-SubscriptionId</span></span>
<span data-ttu-id="310d2-125">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="310d2-125">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="310d2-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="310d2-126">-Confirm</span></span>
<span data-ttu-id="310d2-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="310d2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310d2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310d2-128">-WhatIf</span></span>
<span data-ttu-id="310d2-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="310d2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310d2-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="310d2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310d2-131">CommonParameters</span></span>
<span data-ttu-id="310d2-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="310d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310d2-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="310d2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310d2-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="310d2-134">INPUTS</span></span>

### <span data-ttu-id="310d2-135">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="310d2-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="310d2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="310d2-136">OUTPUTS</span></span>

### <span data-ttu-id="310d2-137">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="310d2-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="310d2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="310d2-138">NOTES</span></span>

<span data-ttu-id="310d2-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="310d2-139">ALIASES</span></span>

<span data-ttu-id="310d2-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="310d2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="310d2-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="310d2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="310d2-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="310d2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="310d2-143">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="310d2-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="310d2-144">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="310d2-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="310d2-145">`CloningInfoSourceWebAppId <String>`: A forrás app ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="310d2-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="310d2-146">Az App-erőforrás-azonosító a gyártási résidők és a/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} más bővítőhelyekhez való/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}.</span><span class="sxs-lookup"><span data-stu-id="310d2-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="310d2-147">`[Kind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="310d2-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="310d2-148">`[Tag <IResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="310d2-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="310d2-149">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="310d2-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="310d2-150">`[ClientAffinityEnabled <Boolean?>]`: az <code>true</code> ügyfél-affinitás engedélyezéséhez: a <code>false</code> munkamenet-affinitást tartalmazó cookie-k küldésének leállítása, amely az ügyfélalkalmazás ugyanazon példányra irányuló kérelme.</span><span class="sxs-lookup"><span data-stu-id="310d2-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="310d2-151">Alapértelmezés: <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="310d2-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyféltanúsítvány-alapú hitelesítés engedélyezéséhez (TLS-alapú kölcsönös hitelesítés); egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="310d2-153">Alapértelmezés: <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="310d2-154">`[ClientCertExclusionPath <String>]`: ügyféltanúsítvány-alapú hitelesítés vesszővel elválasztott kizárási útvonalak</span><span class="sxs-lookup"><span data-stu-id="310d2-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="310d2-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazás beállításai felülbírálják a klónozott alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="310d2-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="310d2-156">Ha meg van adva, ezek a beállítások felülbírálják a forrás alkalmazásból klónozott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="310d2-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="310d2-157">Egyéb esetben a Source App alkalmazás beállításai megőrződnek.</span><span class="sxs-lookup"><span data-stu-id="310d2-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="310d2-158">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="310d2-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="310d2-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Egyéni állomásnevek klónozása a Source app-ból; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="310d2-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrás-irányítás klónozása forrás alkalmazásból; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="310d2-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> a forrás-és a rendeltetési app terheléselosztásának beállítása.</span><span class="sxs-lookup"><span data-stu-id="310d2-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="310d2-162">`[CloningInfoCorrelationId <String>]`: A klónozási művelet korrelációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="310d2-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="310d2-163">Ez az azonosító több klónozási műveletet köt össze, hogy ugyanazt a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="310d2-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="310d2-164">`[CloningInfoHostingEnvironment <String>]`: Alkalmazás-szolgáltatási környezet.</span><span class="sxs-lookup"><span data-stu-id="310d2-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="310d2-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a cél-app felülírása; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="310d2-166">`[CloningInfoSourceWebAppLocation <String>]`: A Source app: Nyugat-amerikai vagy észak-európai verzió helye</span><span class="sxs-lookup"><span data-stu-id="310d2-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="310d2-167">`[CloningInfoTrafficManagerProfileId <String>]`: A használni kívánt forgalomirányító-profil ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="310d2-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="310d2-168">A Traffic Manager erőforrás-AZONOSÍTÓja az űrlap/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="310d2-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="310d2-169">`[CloningInfoTrafficManagerProfileName <String>]`: A létrehozandó Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="310d2-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="310d2-170">Erre csak akkor van szükség, ha a Traffic Manager profilja még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="310d2-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="310d2-171">`[Config <ISiteConfig>]`: Az alkalmazás konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="310d2-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="310d2-172">`IsPushEnabled <Boolean>`: Megadhatja vagy beállíthatja, hogy a leküldéses végpont engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="310d2-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="310d2-173">`[ActionMinProcessExecutionTime <String>]`: A folyamat végrehajtásának minimális ideje a művelet megkezdése előtt</span><span class="sxs-lookup"><span data-stu-id="310d2-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="310d2-174">`[ActionType <AutoHealActionType?>]`: Előre definiált műveletek.</span><span class="sxs-lookup"><span data-stu-id="310d2-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="310d2-175">`[AlwaysOn <Boolean?>]`: <code>true</code> Ha a mindig engedélyezve van, egyéb esetben <code>false</code> :</span><span class="sxs-lookup"><span data-stu-id="310d2-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-176">`[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.</span><span class="sxs-lookup"><span data-stu-id="310d2-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="310d2-177">`[ApiManagementConfigId <String>]`: APIM-Api azonosító.</span><span class="sxs-lookup"><span data-stu-id="310d2-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="310d2-178">`[AppCommandLine <String>]`: Az App parancssora az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="310d2-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="310d2-179">`[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.</span><span class="sxs-lookup"><span data-stu-id="310d2-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="310d2-180">`[Name <String>]`: Páros név.</span><span class="sxs-lookup"><span data-stu-id="310d2-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="310d2-181">`[Value <String>]`: Pair érték.</span><span class="sxs-lookup"><span data-stu-id="310d2-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="310d2-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Ha az automatikus gyógyulás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-183">`[AutoSwapSlotName <String>]`: Automatikus swap-tárolóhely neve.</span><span class="sxs-lookup"><span data-stu-id="310d2-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="310d2-184">`[ConnectionString <IConnStringInfo[]>]`: Kapcsolódási karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="310d2-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="310d2-185">`[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.</span><span class="sxs-lookup"><span data-stu-id="310d2-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="310d2-186">`[Name <String>]`: A kapcsolati karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="310d2-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="310d2-187">`[Type <ConnectionStringType?>]`: Adatbázis típusa.</span><span class="sxs-lookup"><span data-stu-id="310d2-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="310d2-188">`[CorAllowedOrigin <String[]>]`: Beilleszti vagy beállítja az eredeti hívások (például: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="310d2-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="310d2-189">Az összes engedélyezéséhez használja a "\*" billentyűt.</span><span class="sxs-lookup"><span data-stu-id="310d2-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="310d2-190">`[CorSupportCredentials <Boolean?>]`: Beolvassa vagy beállítja, hogy a hitelesítő adatokkal rendelkező CORS-kérelmek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="310d2-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="310d2-191"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsTovábbi részletekért tekintse meg.</span><span class="sxs-lookup"><span data-stu-id="310d2-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="310d2-192">`[CustomActionExe <String>]`: Végrehajtható fájl futtatása.</span><span class="sxs-lookup"><span data-stu-id="310d2-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="310d2-193">`[CustomActionParameter <String>]`: A végrehajtható fájl paramétereinek paraméterei.</span><span class="sxs-lookup"><span data-stu-id="310d2-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="310d2-194">`[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.</span><span class="sxs-lookup"><span data-stu-id="310d2-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="310d2-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Ha a részletes hibák naplózása engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-196">`[DocumentRoot <String>]`: Dokumentum gyökerét.</span><span class="sxs-lookup"><span data-stu-id="310d2-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="310d2-197">`[DynamicTagsJson <String>]`: A leküldéses regisztráció végpontjában a felhasználói jogcímekről kiértékelt dinamikus címkék listáját tartalmazó JSON karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="310d2-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="310d2-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: A Ramp-up szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="310d2-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="310d2-199">`[ActionHostName <String>]`: Annak a bővítőhelynek a neve, amelybe a forgalmat irányítja át.</span><span class="sxs-lookup"><span data-stu-id="310d2-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="310d2-200">Pl.</span><span class="sxs-lookup"><span data-stu-id="310d2-200">E.g.</span></span> <span data-ttu-id="310d2-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="310d2-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="310d2-202">`[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmust is megadhat a TiPCallback webhelyen, mely URL-címet lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="310d2-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="310d2-203">Lásd: a TiPCallback a szerelő és a szerződések számára.</span><span class="sxs-lookup"><span data-stu-id="310d2-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="310d2-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="310d2-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="310d2-205">`[ChangeIntervalInMinute <Int32?>]`: A ReroutePercentage újraértékeléséhez a percekben megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="310d2-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="310d2-206">`[ChangeStep <Double?>]`: Az automatikus Ramp up forgatókönyvben ez a lépés a Hozzáadás/Eltávolítás, <code>ReroutePercentage</code> amíg el nem éri a \n <code>MinReroutePercentage</code> vagy a         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="310d2-207">A webhely metrikáit a .\NCustom-döntési algoritmusban megadott minden N percben ellenőrizni <code>ChangeIntervalInMinutes</code> lehet a TiPCallback webhelyen, mely URL-címet lehet megadni <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="310d2-208">`[MaxReroutePercentage <Double?>]`: Itt adhatja meg azt a felső határt, amely alatt a ReroutePercentage marad.</span><span class="sxs-lookup"><span data-stu-id="310d2-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="310d2-209">`[MinReroutePercentage <Double?>]`: Itt adhatja meg azt az alsó határértéket, amely fölött a ReroutePercentage marad.</span><span class="sxs-lookup"><span data-stu-id="310d2-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="310d2-210">`[Name <String>]`: A műveletterv szabály neve.</span><span class="sxs-lookup"><span data-stu-id="310d2-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="310d2-211">Az ajánlott név arra a pontra mutat, amely a kísérletben szereplő forgalmat fogja fogadni.</span><span class="sxs-lookup"><span data-stu-id="310d2-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="310d2-212">`[ReroutePercentage <Double?>]`: Az átirányítani kívánt forgalom százalékos aránya <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="310d2-213">`[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="310d2-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="310d2-214">`[HandlerMapping <IHandlerMapping[]>]`: Kezelői megfeleltetések.</span><span class="sxs-lookup"><span data-stu-id="310d2-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="310d2-215">`[Argument <String>]`: A parancsfájl-feldolgozó által átadandó parancssori argumentumok.</span><span class="sxs-lookup"><span data-stu-id="310d2-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="310d2-216">`[Extension <String>]`: A kiterjesztéssel elvégezhető kérelmeket a megadott FastCGI-alkalmazás kezeli.</span><span class="sxs-lookup"><span data-stu-id="310d2-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="310d2-217">`[ScriptProcessor <String>]`: A FastCGI-alkalmazás abszolút elérési útja.</span><span class="sxs-lookup"><span data-stu-id="310d2-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="310d2-218">`[HealthCheckPath <String>]`: Állapot-ellenőrzés elérési útja</span><span class="sxs-lookup"><span data-stu-id="310d2-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="310d2-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: webhelyek beállítása, hogy az ügyfelek a http 2.0-s verziós kapcsolatot engedélyezzék</span><span class="sxs-lookup"><span data-stu-id="310d2-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="310d2-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Ha a http-naplózás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások a Main esetében.</span><span class="sxs-lookup"><span data-stu-id="310d2-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="310d2-222">`[Action <String>]`: Engedélyezze vagy tiltsa le az IP-címtartomány elérését.</span><span class="sxs-lookup"><span data-stu-id="310d2-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="310d2-223">`[Description <String>]`: IP-korlátozási szabály leírása.</span><span class="sxs-lookup"><span data-stu-id="310d2-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="310d2-224">`[IPAddress <String>]`: IP-cím: a biztonsági korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="310d2-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="310d2-225">Lehet egy egyszerű IPv4-cím (kötelező SubnetMask tulajdonság) vagy a CIDR-jelölés (például IPv4/Mask (vezető bit)) formájában.</span><span class="sxs-lookup"><span data-stu-id="310d2-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="310d2-226">Az CIDR esetében a SubnetMask tulajdonság nem adható meg.</span><span class="sxs-lookup"><span data-stu-id="310d2-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="310d2-227">`[Name <String>]`: IP-korlátozási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="310d2-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="310d2-228">`[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="310d2-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="310d2-229">`[SubnetMask <String>]`: Alhálózati maszk az IP-címek tartományához: a korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="310d2-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="310d2-230">`[SubnetTrafficTag <Int32?>]`: (belső) alhálózat-forgalmi címke</span><span class="sxs-lookup"><span data-stu-id="310d2-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="310d2-231">`[Tag <IPFilterTag?>]`: Itt határozhatja meg, hogy melyik IP-szűrőt fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="310d2-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="310d2-232">Ez a szolgáltatás támogatja az IP-szűrést a proxykban.</span><span class="sxs-lookup"><span data-stu-id="310d2-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="310d2-233">`[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="310d2-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="310d2-234">`[VnetTrafficTag <Int32?>]`: (belső) vnet forgalmi címke</span><span class="sxs-lookup"><span data-stu-id="310d2-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="310d2-235">`[JavaContainer <String>]`: Java tároló.</span><span class="sxs-lookup"><span data-stu-id="310d2-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="310d2-236">`[JavaContainerVersion <String>]`: Java tároló verziója.</span><span class="sxs-lookup"><span data-stu-id="310d2-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="310d2-237">`[JavaVersion <String>]`: Java-verzió.</span><span class="sxs-lookup"><span data-stu-id="310d2-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="310d2-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Megengedett maximális lemezhasználat MEGABÁJTban.</span><span class="sxs-lookup"><span data-stu-id="310d2-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="310d2-239">`[LimitMaxMemoryInMb <Int64?>]`: Az engedélyezett memória maximális kihasználtsága MEGABÁJTban.</span><span class="sxs-lookup"><span data-stu-id="310d2-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="310d2-240">`[LimitMaxPercentageCpu <Double?>]`: Megengedett maximális CPU-használati százalék</span><span class="sxs-lookup"><span data-stu-id="310d2-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="310d2-241">`[LinuxFxVersion <String>]`: Linux app-keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="310d2-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="310d2-242">`[LoadBalancing <SiteLoadBalancing?>]`: A webhely terheléselosztása.</span><span class="sxs-lookup"><span data-stu-id="310d2-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="310d2-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók: a könyvtár mérete korlátozva</span><span class="sxs-lookup"><span data-stu-id="310d2-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="310d2-245">`[MachineKeyDecryption <String>]`: A visszafejtéshez használt algoritmus.</span><span class="sxs-lookup"><span data-stu-id="310d2-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="310d2-246">`[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.</span><span class="sxs-lookup"><span data-stu-id="310d2-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="310d2-247">`[MachineKeyValidation <String>]`: MachineKey érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="310d2-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="310d2-248">`[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.</span><span class="sxs-lookup"><span data-stu-id="310d2-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="310d2-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt csővezeték üzemmód.</span><span class="sxs-lookup"><span data-stu-id="310d2-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="310d2-250">`[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás azonosítóját azonosító</span><span class="sxs-lookup"><span data-stu-id="310d2-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="310d2-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: az SSL-kérésekhez szükséges TLS minimális verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="310d2-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="310d2-252">`[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.</span><span class="sxs-lookup"><span data-stu-id="310d2-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="310d2-253">`[NodeVersion <String>]`: Node.js verziója.</span><span class="sxs-lookup"><span data-stu-id="310d2-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="310d2-254">`[NumberOfWorker <Int32?>]`: A munkavállalók száma.</span><span class="sxs-lookup"><span data-stu-id="310d2-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="310d2-255">`[PhpVersion <String>]`: A PHP verziója.</span><span class="sxs-lookup"><span data-stu-id="310d2-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="310d2-256">`[PowerShellVersion <String>]`: A PowerShell verziója.</span><span class="sxs-lookup"><span data-stu-id="310d2-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="310d2-257">`[PreWarmedInstanceCount <Int32?>]`: Az előmelegített példányok száma.</span><span class="sxs-lookup"><span data-stu-id="310d2-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="310d2-258">Ez a beállítás csak a fogyasztási és a rugalmas csomagokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="310d2-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="310d2-259">`[PublishingUsername <String>]`: Közzétételi Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="310d2-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="310d2-260">`[PushKind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="310d2-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="310d2-261">`[PythonVersion <String>]`: A Python verziója.</span><span class="sxs-lookup"><span data-stu-id="310d2-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="310d2-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Ha a távoli hibakeresés engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-263">`[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.</span><span class="sxs-lookup"><span data-stu-id="310d2-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="310d2-264">`[RequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="310d2-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="310d2-265">`[RequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="310d2-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="310d2-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Ha a kérés nyomkövetése engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-267">`[RequestTracingExpirationTime <DateTime?>]`: A nyomkövetés lejárati időpontjának kérése</span><span class="sxs-lookup"><span data-stu-id="310d2-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="310d2-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások az SCM-hez.</span><span class="sxs-lookup"><span data-stu-id="310d2-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="310d2-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Az SCM-re vonatkozó IP-biztonsági korlátozások fő.</span><span class="sxs-lookup"><span data-stu-id="310d2-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="310d2-270">`[ScmType <ScmType?>]`: SCM típus.</span><span class="sxs-lookup"><span data-stu-id="310d2-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="310d2-271">`[SlowRequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="310d2-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="310d2-272">`[SlowRequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="310d2-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="310d2-273">`[SlowRequestTimeTaken <String>]`: Idő.</span><span class="sxs-lookup"><span data-stu-id="310d2-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="310d2-274">`[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használt címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="310d2-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="310d2-275">`[TagsRequiringAuth <String>]`: A leküldéses regisztráció végpontján a felhasználó által használt hitelesítést igénylő kódok listáját tartalmazó, JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="310d2-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="310d2-276">A címkék tartalmazhatnak alfanumerikus karaktereket, a következőt: "_", "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="310d2-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="310d2-277">Az érvényesítést a PushRequestHandler kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="310d2-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="310d2-278">`[TracingOption <String>]`: Nyomkövetési beállítások.</span><span class="sxs-lookup"><span data-stu-id="310d2-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="310d2-279">`[TriggerPrivateBytesInKb <Int32?>]`: Privát bájton alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="310d2-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="310d2-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A szabályok az állapotkódok alapján.</span><span class="sxs-lookup"><span data-stu-id="310d2-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="310d2-281">`[Count <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="310d2-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="310d2-282">`[Status <Int32?>]`: HTTP-állapotkód.</span><span class="sxs-lookup"><span data-stu-id="310d2-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="310d2-283">`[SubStatus <Int32?>]`: Alállapot kérése</span><span class="sxs-lookup"><span data-stu-id="310d2-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="310d2-284">`[TimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="310d2-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="310d2-285">`[Win32Status <Int32?>]`: Win32-hibakód.</span><span class="sxs-lookup"><span data-stu-id="310d2-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="310d2-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bites munkavégző folyamat használata; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.</span><span class="sxs-lookup"><span data-stu-id="310d2-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="310d2-288">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="310d2-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="310d2-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> Ha engedélyezve van az előzetes bekapcsolás, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="310d2-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak a virtuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="310d2-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="310d2-291">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="310d2-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="310d2-292">`[VirtualPath <String>]`: A virtuális alkalmazás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="310d2-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="310d2-293">`[VirtualPath <String>]`: Virtuális elérési út.</span><span class="sxs-lookup"><span data-stu-id="310d2-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="310d2-294">`[VnetName <String>]`: Virtuális hálózati név.</span><span class="sxs-lookup"><span data-stu-id="310d2-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="310d2-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Ha a Webszoftvercsatorna engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="310d2-296">`[WindowsFxVersion <String>]`: Xenon alkalmazás kerete és verziója</span><span class="sxs-lookup"><span data-stu-id="310d2-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="310d2-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás-azonosító</span><span class="sxs-lookup"><span data-stu-id="310d2-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="310d2-298">`[ContainerSize <Int32?>]`: A függvény tárolójának mérete.</span><span class="sxs-lookup"><span data-stu-id="310d2-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="310d2-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximálisan engedélyezett napi memória-időkvóta (csak dinamikus alkalmazásokban alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="310d2-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="310d2-300">`[Enabled <Boolean?>]`: <code>true</code> Ha az alkalmazás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="310d2-301">Az érték hamis értékre állítása letiltja az alkalmazást (az alkalmazást kapcsolat nélkül jeleníti meg).</span><span class="sxs-lookup"><span data-stu-id="310d2-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="310d2-302">`[HostNameSslState <IHostNameSslState[]>]`: A gépnév SSL-Államok az App állomásnevek SSL-kötéseinek kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="310d2-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="310d2-303">`[HostType <HostType?>]`: Azt jelzi, hogy a gépnév normál vagy tárházas állomásnév-e.</span><span class="sxs-lookup"><span data-stu-id="310d2-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="310d2-304">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="310d2-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="310d2-305">`[SslState <SslState?>]`: SSL típusa.</span><span class="sxs-lookup"><span data-stu-id="310d2-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="310d2-306">`[Thumbprint <String>]`: SSL-tanúsítvány ujjlenyomata.</span><span class="sxs-lookup"><span data-stu-id="310d2-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="310d2-307">`[ToUpdate <Boolean?>]`: A <code>true</code> meglévő állomásnév frissítésének beállítása.</span><span class="sxs-lookup"><span data-stu-id="310d2-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="310d2-308">`[VirtualIP <String>]`: A gépnévhez rendelt virtuális IP-cím, ha az IP-alapú SSL engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="310d2-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="310d2-309">`[HostNamesDisabled <Boolean?>]`: az <code>true</code> app nyilvános állomásnevek letiltása; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="310d2-310">Ha <code>true</code> az App csak API-kezelési folyamaton keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="310d2-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="310d2-311">`[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="310d2-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="310d2-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: egy webhely beállítása csak HTTPS-kérelmek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="310d2-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="310d2-313">Http-kérelmek átirányításának problémái</span><span class="sxs-lookup"><span data-stu-id="310d2-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="310d2-314">`[HyperV <Boolean?>]`: Hyper-V homokozó.</span><span class="sxs-lookup"><span data-stu-id="310d2-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="310d2-315">`[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="310d2-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="310d2-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által kiosztott identitások listája.</span><span class="sxs-lookup"><span data-stu-id="310d2-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="310d2-317">A felhasználó személyazonosságát ismertető szótár fő hivatkozásai az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}"-ban az űrlapon lesznek.</span><span class="sxs-lookup"><span data-stu-id="310d2-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="310d2-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="310d2-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="310d2-319">`[IsXenon <Boolean?>]`: Elavult: Hyper-V homokozó.</span><span class="sxs-lookup"><span data-stu-id="310d2-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="310d2-320">`[RedundancyMode <RedundancyMode?>]`: Webhely-redundancia mód</span><span class="sxs-lookup"><span data-stu-id="310d2-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="310d2-321">`[Reserved <Boolean?>]`: <code>true</code> Ha fenn van foglalva, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="310d2-322">`[ScmSiteAlsoStopped <Boolean?>]`: az <code>true</code> SCM-(KUDU-) webhely leállítása, ha az alkalmazás le van állítva; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="310d2-323">Az alapértelmezett érték <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="310d2-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="310d2-324">`[ServerFarmId <String>]`: A társított app Service Plan ("/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}") erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="310d2-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="310d2-325">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="310d2-325">RELATED LINKS</span></span>

