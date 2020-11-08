---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionApp.md
ms.openlocfilehash: c12c5e3b3f9b8d0ec172b8a2f53951e5a11a0d9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185419"
---
# <span data-ttu-id="62827-101">Remove-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="62827-101">Remove-AzFunctionApp</span></span>

## <span data-ttu-id="62827-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62827-102">SYNOPSIS</span></span>
<span data-ttu-id="62827-103">Egy függvény alkalmazás törlése</span><span class="sxs-lookup"><span data-stu-id="62827-103">Deletes a function app.</span></span>

## <span data-ttu-id="62827-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62827-104">SYNTAX</span></span>

### <span data-ttu-id="62827-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62827-105">ByName (Default)</span></span>
```
Remove-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62827-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="62827-106">ByObjectInput</span></span>
```
Remove-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62827-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="62827-107">DESCRIPTION</span></span>
<span data-ttu-id="62827-108">Egy függvény alkalmazás törlése</span><span class="sxs-lookup"><span data-stu-id="62827-108">Deletes a function app.</span></span>

## <span data-ttu-id="62827-109">Példák</span><span class="sxs-lookup"><span data-stu-id="62827-109">EXAMPLES</span></span>

### <span data-ttu-id="62827-110">Példa 1: a Function app beszerzése névvel és törléssel</span><span class="sxs-lookup"><span data-stu-id="62827-110">Example 1: Get a function app by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionApp -Force
```

<span data-ttu-id="62827-111">Ez a parancs a függvény alkalmazását névvel és törléssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62827-111">This command gets a function app by name and delete it.</span></span>

### <span data-ttu-id="62827-112">2. példa: a Function app törlése név szerint.</span><span class="sxs-lookup"><span data-stu-id="62827-112">Example 2: Delete a function app by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="62827-113">Ez a parancs törli a függvény alkalmazását név szerint.</span><span class="sxs-lookup"><span data-stu-id="62827-113">This command deletes a function app by name.</span></span>

## <span data-ttu-id="62827-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62827-114">PARAMETERS</span></span>

### <span data-ttu-id="62827-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62827-115">-DefaultProfile</span></span>
<span data-ttu-id="62827-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62827-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62827-117">-Force</span><span class="sxs-lookup"><span data-stu-id="62827-117">-Force</span></span>
<span data-ttu-id="62827-118">Arra kényszeríti a parancsmagot, hogy ne kelljen megerősítésre kérnie a függvény alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="62827-118">Forces the cmdlet to remove the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="62827-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62827-119">-InputObject</span></span>
<span data-ttu-id="62827-120">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="62827-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="62827-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62827-121">-Name</span></span>
<span data-ttu-id="62827-122">A függvény app neve.</span><span class="sxs-lookup"><span data-stu-id="62827-122">The name of function app.</span></span>

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

### <span data-ttu-id="62827-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62827-123">-PassThru</span></span>
<span data-ttu-id="62827-124">Igaz érték visszaadása, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="62827-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="62827-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62827-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="62827-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62827-126">-SubscriptionId</span></span>
<span data-ttu-id="62827-127">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62827-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="62827-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62827-128">-Confirm</span></span>
<span data-ttu-id="62827-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62827-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62827-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62827-130">-WhatIf</span></span>
<span data-ttu-id="62827-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62827-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62827-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62827-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62827-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62827-133">CommonParameters</span></span>
<span data-ttu-id="62827-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62827-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62827-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62827-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62827-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62827-136">INPUTS</span></span>

### <span data-ttu-id="62827-137">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="62827-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="62827-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62827-138">OUTPUTS</span></span>

### <span data-ttu-id="62827-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62827-139">System.Boolean</span></span>

## <span data-ttu-id="62827-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62827-140">NOTES</span></span>

<span data-ttu-id="62827-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="62827-141">ALIASES</span></span>

<span data-ttu-id="62827-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="62827-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62827-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="62827-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62827-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="62827-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62827-145">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="62827-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="62827-146">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="62827-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="62827-147">`CloningInfoSourceWebAppId <String>`: A forrás app ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62827-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="62827-148">Az App-erőforrás-azonosító a gyártási résidők és a/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} más bővítőhelyekhez való/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}.</span><span class="sxs-lookup"><span data-stu-id="62827-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="62827-149">`[Kind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="62827-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="62827-150">`[Tag <IResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="62827-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="62827-151">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="62827-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="62827-152">`[ClientAffinityEnabled <Boolean?>]`: az <code>true</code> ügyfél-affinitás engedélyezéséhez: a <code>false</code> munkamenet-affinitást tartalmazó cookie-k küldésének leállítása, amely az ügyfélalkalmazás ugyanazon példányra irányuló kérelme.</span><span class="sxs-lookup"><span data-stu-id="62827-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="62827-153">Alapértelmezés: <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="62827-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyféltanúsítvány-alapú hitelesítés engedélyezéséhez (TLS-alapú kölcsönös hitelesítés); egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="62827-155">Alapértelmezés: <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="62827-156">`[ClientCertExclusionPath <String>]`: ügyféltanúsítvány-alapú hitelesítés vesszővel elválasztott kizárási útvonalak</span><span class="sxs-lookup"><span data-stu-id="62827-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="62827-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazás beállításai felülbírálják a klónozott alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="62827-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="62827-158">Ha meg van adva, ezek a beállítások felülbírálják a forrás alkalmazásból klónozott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="62827-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="62827-159">Egyéb esetben a Source App alkalmazás beállításai megőrződnek.</span><span class="sxs-lookup"><span data-stu-id="62827-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="62827-160">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="62827-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="62827-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Egyéni állomásnevek klónozása a Source app-ból; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="62827-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrás-irányítás klónozása forrás alkalmazásból; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="62827-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> a forrás-és a rendeltetési app terheléselosztásának beállítása.</span><span class="sxs-lookup"><span data-stu-id="62827-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="62827-164">`[CloningInfoCorrelationId <String>]`: A klónozási művelet korrelációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62827-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="62827-165">Ez az azonosító több klónozási műveletet köt össze, hogy ugyanazt a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="62827-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="62827-166">`[CloningInfoHostingEnvironment <String>]`: Alkalmazás-szolgáltatási környezet.</span><span class="sxs-lookup"><span data-stu-id="62827-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="62827-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a cél-app felülírása; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="62827-168">`[CloningInfoSourceWebAppLocation <String>]`: A Source app: Nyugat-amerikai vagy észak-európai verzió helye</span><span class="sxs-lookup"><span data-stu-id="62827-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="62827-169">`[CloningInfoTrafficManagerProfileId <String>]`: A használni kívánt forgalomirányító-profil ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62827-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="62827-170">A Traffic Manager erőforrás-AZONOSÍTÓja az űrlap/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="62827-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="62827-171">`[CloningInfoTrafficManagerProfileName <String>]`: A létrehozandó Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="62827-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="62827-172">Erre csak akkor van szükség, ha a Traffic Manager profilja még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="62827-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="62827-173">`[Config <ISiteConfig>]`: Az alkalmazás konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="62827-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="62827-174">`IsPushEnabled <Boolean>`: Megadhatja vagy beállíthatja, hogy a leküldéses végpont engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="62827-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="62827-175">`[ActionMinProcessExecutionTime <String>]`: A folyamat végrehajtásának minimális ideje a művelet megkezdése előtt</span><span class="sxs-lookup"><span data-stu-id="62827-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="62827-176">`[ActionType <AutoHealActionType?>]`: Előre definiált műveletek.</span><span class="sxs-lookup"><span data-stu-id="62827-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="62827-177">`[AlwaysOn <Boolean?>]`: <code>true</code> Ha a mindig engedélyezve van, egyéb esetben <code>false</code> :</span><span class="sxs-lookup"><span data-stu-id="62827-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-178">`[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.</span><span class="sxs-lookup"><span data-stu-id="62827-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="62827-179">`[ApiManagementConfigId <String>]`: APIM-Api azonosító.</span><span class="sxs-lookup"><span data-stu-id="62827-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="62827-180">`[AppCommandLine <String>]`: Az App parancssora az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="62827-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="62827-181">`[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.</span><span class="sxs-lookup"><span data-stu-id="62827-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="62827-182">`[Name <String>]`: Páros név.</span><span class="sxs-lookup"><span data-stu-id="62827-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="62827-183">`[Value <String>]`: Pair érték.</span><span class="sxs-lookup"><span data-stu-id="62827-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="62827-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Ha az automatikus gyógyulás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-185">`[AutoSwapSlotName <String>]`: Automatikus swap-tárolóhely neve.</span><span class="sxs-lookup"><span data-stu-id="62827-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="62827-186">`[ConnectionString <IConnStringInfo[]>]`: Kapcsolódási karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="62827-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="62827-187">`[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.</span><span class="sxs-lookup"><span data-stu-id="62827-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="62827-188">`[Name <String>]`: A kapcsolati karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="62827-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="62827-189">`[Type <ConnectionStringType?>]`: Adatbázis típusa.</span><span class="sxs-lookup"><span data-stu-id="62827-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="62827-190">`[CorAllowedOrigin <String[]>]`: Beilleszti vagy beállítja az eredeti hívások (például: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="62827-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="62827-191">Az összes engedélyezéséhez használja a "\*" billentyűt.</span><span class="sxs-lookup"><span data-stu-id="62827-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="62827-192">`[CorSupportCredentials <Boolean?>]`: Beolvassa vagy beállítja, hogy a hitelesítő adatokkal rendelkező CORS-kérelmek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="62827-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="62827-193"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsTovábbi részletekért tekintse meg.</span><span class="sxs-lookup"><span data-stu-id="62827-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="62827-194">`[CustomActionExe <String>]`: Végrehajtható fájl futtatása.</span><span class="sxs-lookup"><span data-stu-id="62827-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="62827-195">`[CustomActionParameter <String>]`: A végrehajtható fájl paramétereinek paraméterei.</span><span class="sxs-lookup"><span data-stu-id="62827-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="62827-196">`[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.</span><span class="sxs-lookup"><span data-stu-id="62827-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="62827-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Ha a részletes hibák naplózása engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-198">`[DocumentRoot <String>]`: Dokumentum gyökerét.</span><span class="sxs-lookup"><span data-stu-id="62827-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="62827-199">`[DynamicTagsJson <String>]`: A leküldéses regisztráció végpontjában a felhasználói jogcímekről kiértékelt dinamikus címkék listáját tartalmazó JSON karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="62827-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="62827-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: A Ramp-up szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="62827-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="62827-201">`[ActionHostName <String>]`: Annak a bővítőhelynek a neve, amelybe a forgalmat irányítja át.</span><span class="sxs-lookup"><span data-stu-id="62827-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="62827-202">Pl.</span><span class="sxs-lookup"><span data-stu-id="62827-202">E.g.</span></span> <span data-ttu-id="62827-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="62827-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="62827-204">`[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmust is megadhat a TiPCallback webhelyen, mely URL-címet lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="62827-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="62827-205">Lásd: a TiPCallback a szerelő és a szerződések számára.</span><span class="sxs-lookup"><span data-stu-id="62827-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="62827-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="62827-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="62827-207">`[ChangeIntervalInMinute <Int32?>]`: A ReroutePercentage újraértékeléséhez a percekben megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="62827-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="62827-208">`[ChangeStep <Double?>]`: Az automatikus Ramp up forgatókönyvben ez a lépés a Hozzáadás/Eltávolítás, <code>ReroutePercentage</code> amíg el nem éri a \n <code>MinReroutePercentage</code> vagy a         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="62827-209">A webhely metrikáit a .\NCustom-döntési algoritmusban megadott minden N percben ellenőrizni <code>ChangeIntervalInMinutes</code> lehet a TiPCallback webhelyen, mely URL-címet lehet megadni <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="62827-210">`[MaxReroutePercentage <Double?>]`: Itt adhatja meg azt a felső határt, amely alatt a ReroutePercentage marad.</span><span class="sxs-lookup"><span data-stu-id="62827-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="62827-211">`[MinReroutePercentage <Double?>]`: Itt adhatja meg azt az alsó határértéket, amely fölött a ReroutePercentage marad.</span><span class="sxs-lookup"><span data-stu-id="62827-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="62827-212">`[Name <String>]`: A műveletterv szabály neve.</span><span class="sxs-lookup"><span data-stu-id="62827-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="62827-213">Az ajánlott név arra a pontra mutat, amely a kísérletben szereplő forgalmat fogja fogadni.</span><span class="sxs-lookup"><span data-stu-id="62827-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="62827-214">`[ReroutePercentage <Double?>]`: Az átirányítani kívánt forgalom százalékos aránya <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="62827-215">`[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="62827-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="62827-216">`[HandlerMapping <IHandlerMapping[]>]`: Kezelői megfeleltetések.</span><span class="sxs-lookup"><span data-stu-id="62827-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="62827-217">`[Argument <String>]`: A parancsfájl-feldolgozó által átadandó parancssori argumentumok.</span><span class="sxs-lookup"><span data-stu-id="62827-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="62827-218">`[Extension <String>]`: A kiterjesztéssel elvégezhető kérelmeket a megadott FastCGI-alkalmazás kezeli.</span><span class="sxs-lookup"><span data-stu-id="62827-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="62827-219">`[ScriptProcessor <String>]`: A FastCGI-alkalmazás abszolút elérési útja.</span><span class="sxs-lookup"><span data-stu-id="62827-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="62827-220">`[HealthCheckPath <String>]`: Állapot-ellenőrzés elérési útja</span><span class="sxs-lookup"><span data-stu-id="62827-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="62827-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: webhelyek beállítása, hogy az ügyfelek a http 2.0-s verziós kapcsolatot engedélyezzék</span><span class="sxs-lookup"><span data-stu-id="62827-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="62827-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Ha a http-naplózás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások a Main esetében.</span><span class="sxs-lookup"><span data-stu-id="62827-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="62827-224">`[Action <String>]`: Engedélyezze vagy tiltsa le az IP-címtartomány elérését.</span><span class="sxs-lookup"><span data-stu-id="62827-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="62827-225">`[Description <String>]`: IP-korlátozási szabály leírása.</span><span class="sxs-lookup"><span data-stu-id="62827-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="62827-226">`[IPAddress <String>]`: IP-cím: a biztonsági korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="62827-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="62827-227">Lehet egy egyszerű IPv4-cím (kötelező SubnetMask tulajdonság) vagy a CIDR-jelölés (például IPv4/Mask (vezető bit)) formájában.</span><span class="sxs-lookup"><span data-stu-id="62827-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="62827-228">Az CIDR esetében a SubnetMask tulajdonság nem adható meg.</span><span class="sxs-lookup"><span data-stu-id="62827-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="62827-229">`[Name <String>]`: IP-korlátozási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="62827-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="62827-230">`[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="62827-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="62827-231">`[SubnetMask <String>]`: Alhálózati maszk az IP-címek tartományához: a korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="62827-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="62827-232">`[SubnetTrafficTag <Int32?>]`: (belső) alhálózat-forgalmi címke</span><span class="sxs-lookup"><span data-stu-id="62827-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="62827-233">`[Tag <IPFilterTag?>]`: Itt határozhatja meg, hogy melyik IP-szűrőt fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="62827-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="62827-234">Ez a szolgáltatás támogatja az IP-szűrést a proxykban.</span><span class="sxs-lookup"><span data-stu-id="62827-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="62827-235">`[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="62827-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="62827-236">`[VnetTrafficTag <Int32?>]`: (belső) vnet forgalmi címke</span><span class="sxs-lookup"><span data-stu-id="62827-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="62827-237">`[JavaContainer <String>]`: Java tároló.</span><span class="sxs-lookup"><span data-stu-id="62827-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="62827-238">`[JavaContainerVersion <String>]`: Java tároló verziója.</span><span class="sxs-lookup"><span data-stu-id="62827-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="62827-239">`[JavaVersion <String>]`: Java-verzió.</span><span class="sxs-lookup"><span data-stu-id="62827-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="62827-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Megengedett maximális lemezhasználat MEGABÁJTban.</span><span class="sxs-lookup"><span data-stu-id="62827-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="62827-241">`[LimitMaxMemoryInMb <Int64?>]`: Az engedélyezett memória maximális kihasználtsága MEGABÁJTban.</span><span class="sxs-lookup"><span data-stu-id="62827-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="62827-242">`[LimitMaxPercentageCpu <Double?>]`: Megengedett maximális CPU-használati százalék</span><span class="sxs-lookup"><span data-stu-id="62827-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="62827-243">`[LinuxFxVersion <String>]`: Linux app-keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="62827-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="62827-244">`[LoadBalancing <SiteLoadBalancing?>]`: A webhely terheléselosztása.</span><span class="sxs-lookup"><span data-stu-id="62827-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="62827-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók: a könyvtár mérete korlátozva</span><span class="sxs-lookup"><span data-stu-id="62827-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="62827-247">`[MachineKeyDecryption <String>]`: A visszafejtéshez használt algoritmus.</span><span class="sxs-lookup"><span data-stu-id="62827-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="62827-248">`[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.</span><span class="sxs-lookup"><span data-stu-id="62827-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="62827-249">`[MachineKeyValidation <String>]`: MachineKey érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="62827-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="62827-250">`[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.</span><span class="sxs-lookup"><span data-stu-id="62827-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="62827-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt csővezeték üzemmód.</span><span class="sxs-lookup"><span data-stu-id="62827-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="62827-252">`[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás azonosítóját azonosító</span><span class="sxs-lookup"><span data-stu-id="62827-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="62827-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: az SSL-kérésekhez szükséges TLS minimális verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="62827-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="62827-254">`[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.</span><span class="sxs-lookup"><span data-stu-id="62827-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="62827-255">`[NodeVersion <String>]`: Node.js verziója.</span><span class="sxs-lookup"><span data-stu-id="62827-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="62827-256">`[NumberOfWorker <Int32?>]`: A munkavállalók száma.</span><span class="sxs-lookup"><span data-stu-id="62827-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="62827-257">`[PhpVersion <String>]`: A PHP verziója.</span><span class="sxs-lookup"><span data-stu-id="62827-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="62827-258">`[PowerShellVersion <String>]`: A PowerShell verziója.</span><span class="sxs-lookup"><span data-stu-id="62827-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="62827-259">`[PreWarmedInstanceCount <Int32?>]`: Az előmelegített példányok száma.</span><span class="sxs-lookup"><span data-stu-id="62827-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="62827-260">Ez a beállítás csak a fogyasztási és a rugalmas csomagokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="62827-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="62827-261">`[PublishingUsername <String>]`: Közzétételi Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="62827-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="62827-262">`[PushKind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="62827-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="62827-263">`[PythonVersion <String>]`: A Python verziója.</span><span class="sxs-lookup"><span data-stu-id="62827-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="62827-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Ha a távoli hibakeresés engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-265">`[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.</span><span class="sxs-lookup"><span data-stu-id="62827-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="62827-266">`[RequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="62827-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="62827-267">`[RequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="62827-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="62827-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Ha a kérés nyomkövetése engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-269">`[RequestTracingExpirationTime <DateTime?>]`: A nyomkövetés lejárati időpontjának kérése</span><span class="sxs-lookup"><span data-stu-id="62827-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="62827-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások az SCM-hez.</span><span class="sxs-lookup"><span data-stu-id="62827-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="62827-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Az SCM-re vonatkozó IP-biztonsági korlátozások fő.</span><span class="sxs-lookup"><span data-stu-id="62827-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="62827-272">`[ScmType <ScmType?>]`: SCM típus.</span><span class="sxs-lookup"><span data-stu-id="62827-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="62827-273">`[SlowRequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="62827-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="62827-274">`[SlowRequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="62827-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="62827-275">`[SlowRequestTimeTaken <String>]`: Idő.</span><span class="sxs-lookup"><span data-stu-id="62827-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="62827-276">`[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használt címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="62827-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="62827-277">`[TagsRequiringAuth <String>]`: A leküldéses regisztráció végpontján a felhasználó által használt hitelesítést igénylő kódok listáját tartalmazó, JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="62827-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="62827-278">A címkék tartalmazhatnak alfanumerikus karaktereket, a következőt: "_", "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="62827-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="62827-279">Az érvényesítést a PushRequestHandler kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="62827-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="62827-280">`[TracingOption <String>]`: Nyomkövetési beállítások.</span><span class="sxs-lookup"><span data-stu-id="62827-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="62827-281">`[TriggerPrivateBytesInKb <Int32?>]`: Privát bájton alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="62827-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="62827-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A szabályok az állapotkódok alapján.</span><span class="sxs-lookup"><span data-stu-id="62827-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="62827-283">`[Count <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="62827-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="62827-284">`[Status <Int32?>]`: HTTP-állapotkód.</span><span class="sxs-lookup"><span data-stu-id="62827-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="62827-285">`[SubStatus <Int32?>]`: Alállapot kérése</span><span class="sxs-lookup"><span data-stu-id="62827-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="62827-286">`[TimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="62827-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="62827-287">`[Win32Status <Int32?>]`: Win32-hibakód.</span><span class="sxs-lookup"><span data-stu-id="62827-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="62827-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bites munkavégző folyamat használata; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.</span><span class="sxs-lookup"><span data-stu-id="62827-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="62827-290">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="62827-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="62827-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> Ha engedélyezve van az előzetes bekapcsolás, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="62827-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak a virtuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="62827-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="62827-293">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="62827-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="62827-294">`[VirtualPath <String>]`: A virtuális alkalmazás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="62827-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="62827-295">`[VirtualPath <String>]`: Virtuális elérési út.</span><span class="sxs-lookup"><span data-stu-id="62827-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="62827-296">`[VnetName <String>]`: Virtuális hálózati név.</span><span class="sxs-lookup"><span data-stu-id="62827-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="62827-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Ha a Webszoftvercsatorna engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="62827-298">`[WindowsFxVersion <String>]`: Xenon alkalmazás kerete és verziója</span><span class="sxs-lookup"><span data-stu-id="62827-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="62827-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás-azonosító</span><span class="sxs-lookup"><span data-stu-id="62827-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="62827-300">`[ContainerSize <Int32?>]`: A függvény tárolójának mérete.</span><span class="sxs-lookup"><span data-stu-id="62827-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="62827-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximálisan engedélyezett napi memória-időkvóta (csak dinamikus alkalmazásokban alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="62827-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="62827-302">`[Enabled <Boolean?>]`: <code>true</code> Ha az alkalmazás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="62827-303">Az érték hamis értékre állítása letiltja az alkalmazást (az alkalmazást kapcsolat nélkül jeleníti meg).</span><span class="sxs-lookup"><span data-stu-id="62827-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="62827-304">`[HostNameSslState <IHostNameSslState[]>]`: A gépnév SSL-Államok az App állomásnevek SSL-kötéseinek kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="62827-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="62827-305">`[HostType <HostType?>]`: Azt jelzi, hogy a gépnév normál vagy tárházas állomásnév-e.</span><span class="sxs-lookup"><span data-stu-id="62827-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="62827-306">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="62827-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="62827-307">`[SslState <SslState?>]`: SSL típusa.</span><span class="sxs-lookup"><span data-stu-id="62827-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="62827-308">`[Thumbprint <String>]`: SSL-tanúsítvány ujjlenyomata.</span><span class="sxs-lookup"><span data-stu-id="62827-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="62827-309">`[ToUpdate <Boolean?>]`: A <code>true</code> meglévő állomásnév frissítésének beállítása.</span><span class="sxs-lookup"><span data-stu-id="62827-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="62827-310">`[VirtualIP <String>]`: A gépnévhez rendelt virtuális IP-cím, ha az IP-alapú SSL engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="62827-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="62827-311">`[HostNamesDisabled <Boolean?>]`: az <code>true</code> app nyilvános állomásnevek letiltása; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="62827-312">Ha <code>true</code> az App csak API-kezelési folyamaton keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="62827-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="62827-313">`[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62827-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="62827-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: egy webhely beállítása csak HTTPS-kérelmek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="62827-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="62827-315">Http-kérelmek átirányításának problémái</span><span class="sxs-lookup"><span data-stu-id="62827-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="62827-316">`[HyperV <Boolean?>]`: Hyper-V homokozó.</span><span class="sxs-lookup"><span data-stu-id="62827-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="62827-317">`[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="62827-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="62827-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által kiosztott identitások listája.</span><span class="sxs-lookup"><span data-stu-id="62827-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="62827-319">A felhasználó személyazonosságát ismertető szótár fő hivatkozásai az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}"-ban az űrlapon lesznek.</span><span class="sxs-lookup"><span data-stu-id="62827-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="62827-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="62827-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="62827-321">`[IsXenon <Boolean?>]`: Elavult: Hyper-V homokozó.</span><span class="sxs-lookup"><span data-stu-id="62827-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="62827-322">`[RedundancyMode <RedundancyMode?>]`: Webhely-redundancia mód</span><span class="sxs-lookup"><span data-stu-id="62827-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="62827-323">`[Reserved <Boolean?>]`: <code>true</code> Ha fenn van foglalva, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="62827-324">`[ScmSiteAlsoStopped <Boolean?>]`: az <code>true</code> SCM-(KUDU-) webhely leállítása, ha az alkalmazás le van állítva; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="62827-325">Az alapértelmezett érték <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="62827-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="62827-326">`[ServerFarmId <String>]`: A társított app Service Plan ("/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}") erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62827-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="62827-327">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62827-327">RELATED LINKS</span></span>
