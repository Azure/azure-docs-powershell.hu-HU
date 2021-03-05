---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: d6c0269fd0db63160e7258124bb605b43bcc5f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015221"
---
# <span data-ttu-id="f08e2-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="f08e2-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="f08e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f08e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f08e2-103">Eltávolítja az appbeállításokat egy függvényalkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="f08e2-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="f08e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f08e2-104">SYNTAX</span></span>

### <span data-ttu-id="f08e2-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f08e2-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f08e2-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="f08e2-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f08e2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f08e2-107">DESCRIPTION</span></span>
<span data-ttu-id="f08e2-108">Eltávolítja az appbeállításokat egy függvényalkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="f08e2-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="f08e2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f08e2-109">EXAMPLES</span></span>

### <span data-ttu-id="f08e2-110">1. példa: Alkalmazásbeállítások eltávolítása egy függvényalkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="f08e2-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="f08e2-111">Ez a parancs eltávolítja az appbeállításokat egy függvényalkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="f08e2-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="f08e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f08e2-112">PARAMETERS</span></span>

### <span data-ttu-id="f08e2-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="f08e2-113">-AppSettingName</span></span>
<span data-ttu-id="f08e2-114">A függvényalkalmazásból eltávolítható függvényalkalmazás-beállítások listája.</span><span class="sxs-lookup"><span data-stu-id="f08e2-114">List of function app settings to be removed from the function app.</span></span>

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

### <span data-ttu-id="f08e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08e2-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="f08e2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f08e2-116">-Force</span></span>
<span data-ttu-id="f08e2-117">A parancsmag kényszerítését a függvényalkalmazás beállításának eltávolítására anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f08e2-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f08e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f08e2-118">-InputObject</span></span>
<span data-ttu-id="f08e2-119">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="f08e2-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f08e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f08e2-120">-Name</span></span>
<span data-ttu-id="f08e2-121">A függvényalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-121">Name of the function app.</span></span>

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

### <span data-ttu-id="f08e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f08e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f08e2-123">Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="f08e2-123">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="f08e2-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f08e2-124">-SubscriptionId</span></span>
<span data-ttu-id="f08e2-125">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-125">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="f08e2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f08e2-126">-Confirm</span></span>
<span data-ttu-id="f08e2-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f08e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f08e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f08e2-128">-WhatIf</span></span>
<span data-ttu-id="f08e2-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f08e2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f08e2-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f08e2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f08e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08e2-131">CommonParameters</span></span>
<span data-ttu-id="f08e2-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f08e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08e2-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f08e2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08e2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f08e2-134">INPUTS</span></span>

### <span data-ttu-id="f08e2-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="f08e2-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="f08e2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f08e2-136">OUTPUTS</span></span>

### <span data-ttu-id="f08e2-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="f08e2-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="f08e2-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f08e2-138">NOTES</span></span>

<span data-ttu-id="f08e2-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f08e2-139">ALIASES</span></span>

<span data-ttu-id="f08e2-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f08e2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f08e2-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f08e2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f08e2-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f08e2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f08e2-143">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="f08e2-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="f08e2-144">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f08e2-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="f08e2-145">`CloningInfoSourceWebAppId <String>`: ARM forrásalkalmazás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="f08e2-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="f08e2-146">Az alkalmazáserőforrás-azonosító a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}, production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.</span><span class="sxs-lookup"><span data-stu-id="f08e2-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="f08e2-147">`[Kind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="f08e2-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="f08e2-148">`[Tag <IResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="f08e2-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f08e2-149">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="f08e2-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f08e2-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> az ügyfélkapcsolat engedélyezéséhez; a munkamenet-affinitás cookie-k küldésének megállítása, amelyek az ügyfélalkalmazások kérését ugyanannak a munkamenetnek a példányára <code>false</code> irányítják.</span><span class="sxs-lookup"><span data-stu-id="f08e2-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="f08e2-151">Az alapértelmezett érték <code>true</code> a .</span><span class="sxs-lookup"><span data-stu-id="f08e2-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="f08e2-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyfél tanúsítvány-hitelesítésének (TLS közös hitelesítés) engedélyezéséhez; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="f08e2-153">Az alapértelmezett érték <code>false</code> a .</span><span class="sxs-lookup"><span data-stu-id="f08e2-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="f08e2-154">`[ClientCertExclusionPath <String>]`: Ügyfél tanúsítványának hitelesítése vesszővel elválasztott kivétel elérési útjai</span><span class="sxs-lookup"><span data-stu-id="f08e2-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="f08e2-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazásbeállítási felülbírálások a klónozott appok esetén.</span><span class="sxs-lookup"><span data-stu-id="f08e2-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="f08e2-156">Ha meg van adva, ezek a beállítások felülbírálják a forrásalkalmazásból klónozott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="f08e2-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="f08e2-157">Ellenkező esetben a forrásalkalmazás alkalmazásbeállítása megmarad.</span><span class="sxs-lookup"><span data-stu-id="f08e2-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="f08e2-158">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="f08e2-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f08e2-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> az egyéni állomásnevek klónozása a forrásalkalmazásból, ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f08e2-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrásalkalmazásból a forrásvezérlők klónozása; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f08e2-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> konfigurálhatja a terheléselosztást a forrás- és célalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="f08e2-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="f08e2-162">`[CloningInfoCorrelationId <String>]`: A cloning művelet korrelációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="f08e2-163">Ez az azonosító több cloning műveletet hoz létre ugyanannak a pillanatfelvételnek a végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="f08e2-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="f08e2-164">`[CloningInfoHostingEnvironment <String>]`: App szolgáltatási környezet.</span><span class="sxs-lookup"><span data-stu-id="f08e2-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="f08e2-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a célalkalmazás felülírása; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f08e2-166">`[CloningInfoSourceWebAppLocation <String>]`: A forrásalkalmazás helye, pl. Nyugat-Usa vagy Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="f08e2-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="f08e2-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM a Traffic Manager-profil erőforrás-azonosítóját, ha létezik ilyen.</span><span class="sxs-lookup"><span data-stu-id="f08e2-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="f08e2-168">A Traffic Manager erőforrás-azonosítója a következő űrlapból áll: /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="f08e2-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="f08e2-169">`[CloningInfoTrafficManagerProfileName <String>]`: A létrehozni szükséges Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="f08e2-170">Erre csak akkor van szükség, ha a Traffic Manager-profil még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="f08e2-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="f08e2-171">`[Config <ISiteConfig>]`: Az app konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="f08e2-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="f08e2-172">`IsPushEnabled <Boolean>`: Jelölőt kap vagy állít be, amely jelzi, hogy a leküldéses végpont engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="f08e2-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="f08e2-173">`[ActionMinProcessExecutionTime <String>]`: A művelet végrehajtása előtt a folyamat minimálisan szükséges ideje</span><span class="sxs-lookup"><span data-stu-id="f08e2-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="f08e2-174">`[ActionType <AutoHealActionType?>]`: Előre meghatározott teendő.</span><span class="sxs-lookup"><span data-stu-id="f08e2-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="f08e2-175">`[AlwaysOn <Boolean?>]`: <code>true</code> ha a Mindig be van kapcsolva, egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-176">`[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.</span><span class="sxs-lookup"><span data-stu-id="f08e2-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="f08e2-177">`[ApiManagementConfigId <String>]`: APIM-Api azonosító.</span><span class="sxs-lookup"><span data-stu-id="f08e2-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="f08e2-178">`[AppCommandLine <String>]`: Elindítandó alkalmazás parancssora.</span><span class="sxs-lookup"><span data-stu-id="f08e2-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="f08e2-179">`[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.</span><span class="sxs-lookup"><span data-stu-id="f08e2-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="f08e2-180">`[Name <String>]`: Párnév.</span><span class="sxs-lookup"><span data-stu-id="f08e2-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="f08e2-181">`[Value <String>]`: Érték párosítása.</span><span class="sxs-lookup"><span data-stu-id="f08e2-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="f08e2-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> ha az Automatikus lejátszás funkció be van kapcsolva; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-183">`[AutoSwapSlotName <String>]`: Az automatikus cserehely neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="f08e2-184">`[ConnectionString <IConnStringInfo[]>]`: Kapcsolati karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="f08e2-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="f08e2-185">`[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.</span><span class="sxs-lookup"><span data-stu-id="f08e2-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="f08e2-186">`[Name <String>]`: A kapcsolati karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="f08e2-187">`[Type <ConnectionStringType?>]`: Az adatbázis típusa.</span><span class="sxs-lookup"><span data-stu-id="f08e2-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="f08e2-188">`[CorAllowedOrigin <String[]>]`: Beállítja vagy beállítja azon forráslistát, amely lehetővé teszi a több forrásból való hívásokat (például: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="f08e2-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="f08e2-189">Az összes engedélyezése a "\*" szóra van állítva.</span><span class="sxs-lookup"><span data-stu-id="f08e2-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="f08e2-190">`[CorSupportCredentials <Boolean?>]`: Beállítja vagy beállítja, hogy engedélyezettek-e a hitelesítő adatokkal megadott CORS-kérések.</span><span class="sxs-lookup"><span data-stu-id="f08e2-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="f08e2-191">További         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         részleteket itt talál.</span><span class="sxs-lookup"><span data-stu-id="f08e2-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="f08e2-192">`[CustomActionExe <String>]`: Futtatható végrehajtható fájl.</span><span class="sxs-lookup"><span data-stu-id="f08e2-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="f08e2-193">`[CustomActionParameter <String>]`: A végrehajtható fájl paraméterei.</span><span class="sxs-lookup"><span data-stu-id="f08e2-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="f08e2-194">`[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.</span><span class="sxs-lookup"><span data-stu-id="f08e2-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="f08e2-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ha a részletes hibanaplózás engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-196">`[DocumentRoot <String>]`: Dokumentumgyök.</span><span class="sxs-lookup"><span data-stu-id="f08e2-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="f08e2-197">`[DynamicTagsJson <String>]`: Olyan JSON-karakterláncot kap vagy állít be, amely a leküldéses regisztrációs végponton található felhasználói igények alapján kiértékelésre kerül a dinamikus címkék listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f08e2-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="f08e2-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: A felfutási szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="f08e2-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="f08e2-199">`[ActionHostName <String>]`: Annak a tárolóhelynek a állomásneve, amelybe a forgalmat átirányítja a rendszer, ha úgy dönt.</span><span class="sxs-lookup"><span data-stu-id="f08e2-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="f08e2-200">Például:</span><span class="sxs-lookup"><span data-stu-id="f08e2-200">E.g.</span></span> <span data-ttu-id="f08e2-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="f08e2-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="f08e2-202">`[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmus is meg lehet adni a TiPCallback webhelybővítményben, amely URL-címet is meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="f08e2-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="f08e2-203">Lásd a TiPCallback webhelybővítményét az állványhoz és a szerződésekhez.</span><span class="sxs-lookup"><span data-stu-id="f08e2-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="f08e2-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="f08e2-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="f08e2-205">`[ChangeIntervalInMinute <Int32?>]`: Az ReroutePercentage átértékelhető intervallumát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="f08e2-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="f08e2-206">`[ChangeStep <Double?>]`: Automatikus felfutási helyzetben ez a lépés a hozzáadás/eltávolítás, amíg el nem éri a <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> vagy         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="f08e2-207">A webhely metrikákat a .\nCustom döntési algoritmusban megadott N percenként ellenőrzi a <code>ChangeIntervalInMinutes</code> TiPCallback webhelybővítmény, amely az URL-címet meg lehet <code>ChangeDecisionCallbackUrl</code> adni.</span><span class="sxs-lookup"><span data-stu-id="f08e2-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="f08e2-208">`[MaxReroutePercentage <Double?>]`: Azt a felső határot adja meg, amely alatt a ReroutePercentage meg fog maradni.</span><span class="sxs-lookup"><span data-stu-id="f08e2-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="f08e2-209">`[MinReroutePercentage <Double?>]`: Azt az alsó határértéket adja meg, amely fölött az ReroutePercentage meg fog maradni.</span><span class="sxs-lookup"><span data-stu-id="f08e2-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="f08e2-210">`[Name <String>]`: Az útválasztási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="f08e2-211">Az ajánlott név a kísérlet során a forgalmat tároló tárolóhelyre mutat.</span><span class="sxs-lookup"><span data-stu-id="f08e2-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="f08e2-212">`[ReroutePercentage <Double?>]`: Azon forgalom százalékos aránya, amelyre a rendszer átirányítja <code>ActionHostName</code> a forgalmat.</span><span class="sxs-lookup"><span data-stu-id="f08e2-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="f08e2-213">`[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás állapota</span><span class="sxs-lookup"><span data-stu-id="f08e2-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="f08e2-214">`[HandlerMapping <IHandlerMapping[]>]`: Kezelői leképezések.</span><span class="sxs-lookup"><span data-stu-id="f08e2-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="f08e2-215">`[Argument <String>]`: A parancsprogram-processzornak át kell adandó parancssori argumentumokat.</span><span class="sxs-lookup"><span data-stu-id="f08e2-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="f08e2-216">`[Extension <String>]`: Az ilyen kiterjesztésű kérelmeket a megadott FastCGI alkalmazással kezeljük.</span><span class="sxs-lookup"><span data-stu-id="f08e2-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="f08e2-217">`[ScriptProcessor <String>]`: A FastCGI alkalmazás abszolút elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f08e2-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="f08e2-218">`[HealthCheckPath <String>]`: Állapot-ellenőrzés útvonala</span><span class="sxs-lookup"><span data-stu-id="f08e2-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="f08e2-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfigurál egy webhelyet, amely engedélyezi az ügyfeleknek a http2.0-s kapcsolaton keresztüli csatlakozást</span><span class="sxs-lookup"><span data-stu-id="f08e2-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="f08e2-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> ha a HTTP-naplózás engedélyezve van; egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: A fő IP-biztonsági korlátozásai.</span><span class="sxs-lookup"><span data-stu-id="f08e2-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="f08e2-222">`[Action <String>]`: Hozzáférés engedélyezése vagy elutasítása ehhez az IP-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f08e2-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="f08e2-223">`[Description <String>]`: IP-korlátozási szabály leírása.</span><span class="sxs-lookup"><span data-stu-id="f08e2-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="f08e2-224">`[IPAddress <String>]`: Az IP-cím, amelyre a biztonsági korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="f08e2-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="f08e2-225">Ez lehet csak ipv4-cím (kötelező AlhálózatiMaszk tulajdonság) vagy CIDR-cím, például ipv4/mask (leading bit match).</span><span class="sxs-lookup"><span data-stu-id="f08e2-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="f08e2-226">CIDR esetén az Alhálózatimaszk tulajdonságot nem kell megadni.</span><span class="sxs-lookup"><span data-stu-id="f08e2-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="f08e2-227">`[Name <String>]`: IP-korlátozási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="f08e2-228">`[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="f08e2-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="f08e2-229">`[SubnetMask <String>]`: Az IP-címek tartományának alhálózati maszkja, amelyekre a korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="f08e2-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="f08e2-230">`[SubnetTrafficTag <Int32?>]`: (belső) Alhálózati adatforgalom címkéje</span><span class="sxs-lookup"><span data-stu-id="f08e2-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="f08e2-231">`[Tag <IPFilterTag?>]`: Meghatározza, hogy mire fogja használni ezt az IP-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="f08e2-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="f08e2-232">Ez a proxyk IP-szűrésének támogatását támogatja.</span><span class="sxs-lookup"><span data-stu-id="f08e2-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="f08e2-233">`[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f08e2-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="f08e2-234">`[VnetTrafficTag <Int32?>]`: (belső) Vnet-adatforgalom címkéje</span><span class="sxs-lookup"><span data-stu-id="f08e2-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="f08e2-235">`[JavaContainer <String>]`: Java tároló.</span><span class="sxs-lookup"><span data-stu-id="f08e2-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="f08e2-236">`[JavaContainerVersion <String>]`: Java-tároló verziója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="f08e2-237">`[JavaVersion <String>]`: Java verzió.</span><span class="sxs-lookup"><span data-stu-id="f08e2-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="f08e2-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximális lemezméret-használat MB-ban.</span><span class="sxs-lookup"><span data-stu-id="f08e2-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="f08e2-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximális memóriahasználat MB-ban.</span><span class="sxs-lookup"><span data-stu-id="f08e2-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="f08e2-240">`[LimitMaxPercentageCpu <Double?>]`: Maximális engedélyezett processzorhasználati százalékérték.</span><span class="sxs-lookup"><span data-stu-id="f08e2-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="f08e2-241">`[LinuxFxVersion <String>]`: Linux app keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="f08e2-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="f08e2-242">`[LoadBalancing <SiteLoadBalancing?>]`: Webhely terheléselosztása.</span><span class="sxs-lookup"><span data-stu-id="f08e2-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="f08e2-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók címtárméretkorlátja.</span><span class="sxs-lookup"><span data-stu-id="f08e2-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="f08e2-245">`[MachineKeyDecryption <String>]`: A visszafejtési algoritmus.</span><span class="sxs-lookup"><span data-stu-id="f08e2-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="f08e2-246">`[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.</span><span class="sxs-lookup"><span data-stu-id="f08e2-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="f08e2-247">`[MachineKeyValidation <String>]`: Gépkulcs érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="f08e2-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="f08e2-248">`[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.</span><span class="sxs-lookup"><span data-stu-id="f08e2-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="f08e2-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt folyamat mód.</span><span class="sxs-lookup"><span data-stu-id="f08e2-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="f08e2-250">`[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás identitásazonosítója</span><span class="sxs-lookup"><span data-stu-id="f08e2-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="f08e2-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Az SSL-kérelmekhez minimálisan szükséges TLS-verzió konfigurálása</span><span class="sxs-lookup"><span data-stu-id="f08e2-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="f08e2-252">`[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="f08e2-253">`[NodeVersion <String>]`: A Node.js.</span><span class="sxs-lookup"><span data-stu-id="f08e2-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="f08e2-254">`[NumberOfWorker <Int32?>]`: Dolgozók száma.</span><span class="sxs-lookup"><span data-stu-id="f08e2-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="f08e2-255">`[PhpVersion <String>]`: A PHP verziója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="f08e2-256">`[PowerShellVersion <String>]`: A PowerShell verziója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="f08e2-257">`[PreWarmedInstanceCount <Int32?>]`: Awarmed példányok száma.</span><span class="sxs-lookup"><span data-stu-id="f08e2-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="f08e2-258">Ez a beállítás csak a fogyasztási és rugalmas csomagokra vonatkozik</span><span class="sxs-lookup"><span data-stu-id="f08e2-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="f08e2-259">`[PublishingUsername <String>]`: Közzétételi felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="f08e2-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="f08e2-260">`[PushKind <String>]`: Az erőforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="f08e2-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="f08e2-261">`[PythonVersion <String>]`: A Python verziója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="f08e2-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> ha a távoli hibakeresés engedélyezve van; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-263">`[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.</span><span class="sxs-lookup"><span data-stu-id="f08e2-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="f08e2-264">`[RequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="f08e2-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="f08e2-265">`[RequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="f08e2-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="f08e2-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> ha a kéréskövetés engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-267">`[RequestTracingExpirationTime <DateTime?>]`: A lejárati idő nyomon követésének kérése.</span><span class="sxs-lookup"><span data-stu-id="f08e2-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="f08e2-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: AZ SCM IP-biztonsági korlátozásai.</span><span class="sxs-lookup"><span data-stu-id="f08e2-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="f08e2-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-biztonsági korlátozások az scm fő használatára.</span><span class="sxs-lookup"><span data-stu-id="f08e2-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="f08e2-270">`[ScmType <ScmType?>]`: SCM típus.</span><span class="sxs-lookup"><span data-stu-id="f08e2-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="f08e2-271">`[SlowRequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="f08e2-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="f08e2-272">`[SlowRequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="f08e2-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="f08e2-273">`[SlowRequestTimeTaken <String>]`: A szükséges idő.</span><span class="sxs-lookup"><span data-stu-id="f08e2-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="f08e2-274">`[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használható címkék listáját tartalmazó JSON-karakterláncot állít be vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="f08e2-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="f08e2-275">`[TagsRequiringAuth <String>]`: A leküldéses regisztrációs végponton felhasználói hitelesítést igénylő címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="f08e2-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="f08e2-276">A címkék alfanumerikus karakterekből állhatnak, és a következő karakterekből állhatnak: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="f08e2-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="f08e2-277">Az érvényesítést a PushRequestHandlerben kell elvégezni.</span><span class="sxs-lookup"><span data-stu-id="f08e2-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="f08e2-278">`[TracingOption <String>]`: Nyomkövetési beállítások.</span><span class="sxs-lookup"><span data-stu-id="f08e2-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="f08e2-279">`[TriggerPrivateBytesInKb <Int32?>]`: Egy magánjellegű bájton alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="f08e2-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="f08e2-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Egy állapotkódon alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="f08e2-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="f08e2-281">`[Count <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="f08e2-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="f08e2-282">`[Status <Int32?>]`: HTTP-állapotkód.</span><span class="sxs-lookup"><span data-stu-id="f08e2-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="f08e2-283">`[SubStatus <Int32?>]`: Alállapot kérése.</span><span class="sxs-lookup"><span data-stu-id="f08e2-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="f08e2-284">`[TimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="f08e2-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="f08e2-285">`[Win32Status <Int32?>]`: Win32 hibakód.</span><span class="sxs-lookup"><span data-stu-id="f08e2-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="f08e2-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> a 32 bites munkavégző folyamathoz; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.</span><span class="sxs-lookup"><span data-stu-id="f08e2-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="f08e2-288">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="f08e2-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="f08e2-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> ha az előbetöltés engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="f08e2-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak virtuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="f08e2-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="f08e2-291">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="f08e2-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="f08e2-292">`[VirtualPath <String>]`: Virtuális alkalmazás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f08e2-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="f08e2-293">`[VirtualPath <String>]`: Virtuális elérési út.</span><span class="sxs-lookup"><span data-stu-id="f08e2-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="f08e2-294">`[VnetName <String>]`: Virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="f08e2-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="f08e2-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> ha a WebSocket engedélyezve van, egyébként <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="f08e2-296">`[WindowsFxVersion <String>]`: Xenon app keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="f08e2-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="f08e2-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás identitásazonosítója</span><span class="sxs-lookup"><span data-stu-id="f08e2-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="f08e2-298">`[ContainerSize <Int32?>]`: A függvénytároló mérete.</span><span class="sxs-lookup"><span data-stu-id="f08e2-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="f08e2-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximális napi memóriaidő-kvóta (csak dinamikus alkalmazások esetén alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="f08e2-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="f08e2-300">`[Enabled <Boolean?>]`: <code>true</code> ha az alkalmazás engedélyezve van; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="f08e2-301">Ennek az értéknek a hamis értékre állításával letiltja az appot (offline állapotba vált).</span><span class="sxs-lookup"><span data-stu-id="f08e2-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="f08e2-302">`[HostNameSslState <IHostNameSslState[]>]`: Az SSL-állomásnevek SSL-államai az alkalmazás állomásnevéhez szükséges SSL-kötések kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="f08e2-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="f08e2-303">`[HostType <HostType?>]`: Azt jelzi, hogy az állomásnév normál vagy tárházi állomásnév-e.</span><span class="sxs-lookup"><span data-stu-id="f08e2-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="f08e2-304">`[Name <String>]`: Állomásnév.</span><span class="sxs-lookup"><span data-stu-id="f08e2-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="f08e2-305">`[SslState <SslState?>]`: SSL-típus.</span><span class="sxs-lookup"><span data-stu-id="f08e2-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="f08e2-306">`[Thumbprint <String>]`: SSL-tanúsítvány thumbprint.</span><span class="sxs-lookup"><span data-stu-id="f08e2-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="f08e2-307">`[ToUpdate <Boolean?>]`: A meglévő <code>true</code> állomásnév frissítésére van beállítva.</span><span class="sxs-lookup"><span data-stu-id="f08e2-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="f08e2-308">`[VirtualIP <String>]`: Az IP-alapú SSL engedélyezése esetén az állomásnévhez hozzárendelt virtuális IP-cím.</span><span class="sxs-lookup"><span data-stu-id="f08e2-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="f08e2-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> az app nyilvános állomásnevének letiltásához; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="f08e2-310">Ha <code>true</code> az app csak API-kezelési folyamaton keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="f08e2-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="f08e2-311">`[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f08e2-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="f08e2-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: úgy konfigurál egy webhelyet, hogy csak a https-kérelmeket fogadja el.</span><span class="sxs-lookup"><span data-stu-id="f08e2-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="f08e2-313">A http-kérelmek problémáinak átirányítása</span><span class="sxs-lookup"><span data-stu-id="f08e2-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="f08e2-314">`[HyperV <Boolean?>]`: Hyper-V védőfal.</span><span class="sxs-lookup"><span data-stu-id="f08e2-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="f08e2-315">`[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="f08e2-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="f08e2-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által hozzárendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="f08e2-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="f08e2-317">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="f08e2-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="f08e2-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="f08e2-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f08e2-319">`[IsXenon <Boolean?>]`: Elavult: Hyper-V védőfal.</span><span class="sxs-lookup"><span data-stu-id="f08e2-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="f08e2-320">`[RedundancyMode <RedundancyMode?>]`: Webhely redundancia üzemmódja</span><span class="sxs-lookup"><span data-stu-id="f08e2-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="f08e2-321">`[Reserved <Boolean?>]`: <code>true</code> ha foglalt; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="f08e2-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> leállítja az SCM (KUDU) webhelyet az alkalmazás leállításakor; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="f08e2-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="f08e2-323">Az alapértelmezett érték <code>false</code> a .</span><span class="sxs-lookup"><span data-stu-id="f08e2-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="f08e2-324">`[ServerFarmId <String>]`: A társított App Service-csomag erőforrás-azonosítója, formátuma: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="f08e2-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="f08e2-325">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f08e2-325">RELATED LINKS</span></span>

