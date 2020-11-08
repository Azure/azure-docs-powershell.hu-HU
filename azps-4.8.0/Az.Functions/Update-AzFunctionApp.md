---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025346"
---
# <span data-ttu-id="27140-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="27140-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="27140-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27140-102">SYNOPSIS</span></span>
<span data-ttu-id="27140-103">Frissít egy függvény alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="27140-103">Updates a function app.</span></span>

## <span data-ttu-id="27140-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27140-104">SYNTAX</span></span>

### <span data-ttu-id="27140-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27140-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27140-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="27140-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="27140-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="27140-107">DESCRIPTION</span></span>
<span data-ttu-id="27140-108">Frissít egy függvény alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="27140-108">Updates a function app.</span></span>

## <span data-ttu-id="27140-109">Példák</span><span class="sxs-lookup"><span data-stu-id="27140-109">EXAMPLES</span></span>

### <span data-ttu-id="27140-110">Példa 1: Update függvény app-üzemeltetési terv.</span><span class="sxs-lookup"><span data-stu-id="27140-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="27140-111">Ez a parancs frissíti a Function app üzemeltetési csomagját.</span><span class="sxs-lookup"><span data-stu-id="27140-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="27140-112">2. példa: SystemAssigned felügyelt identitás beállítása egy függvény alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="27140-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="27140-113">Ez a parancs a SystemAssigned felügyelt identitását állítja be.</span><span class="sxs-lookup"><span data-stu-id="27140-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="27140-114">3. példa: a Update függvény alkalmazás-betekintési funkciói.</span><span class="sxs-lookup"><span data-stu-id="27140-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="27140-115">Ez a parancs frissíti a Function App alkalmazásban betekintést.</span><span class="sxs-lookup"><span data-stu-id="27140-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="27140-116">3. példa: a felügyelt identitás eltávolítása egy függvény alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="27140-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="27140-117">Ez a parancs egy függvény alkalmazásból távolítja el a felügyelt identitást.</span><span class="sxs-lookup"><span data-stu-id="27140-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="27140-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27140-118">PARAMETERS</span></span>

### <span data-ttu-id="27140-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="27140-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="27140-120">A felvenni kívánt alkalmazás Instrumentation-kulcsa.</span><span class="sxs-lookup"><span data-stu-id="27140-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27140-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="27140-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="27140-122">A függvény alkalmazásba felvenni kívánt meglévő alkalmazás-betekintési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="27140-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27140-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27140-123">-AsJob</span></span>
<span data-ttu-id="27140-124">A parancsmagot háttérként futtatja.</span><span class="sxs-lookup"><span data-stu-id="27140-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="27140-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27140-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="27140-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="27140-126">-IdentityID</span></span>
<span data-ttu-id="27140-127">A függvény alkalmazáshoz társított felhasználói azonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27140-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="27140-128">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="27140-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="27140-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="27140-129">-IdentityType</span></span>
<span data-ttu-id="27140-130">A függvény alkalmazáshoz használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27140-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="27140-131">A "nincs" típus esetén a függvény alkalmazásban minden identitás törlődik.</span><span class="sxs-lookup"><span data-stu-id="27140-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="27140-132">A paraméter elfogadható értékei a következők:-SystemAssigned-UserAssigned-nincs</span><span class="sxs-lookup"><span data-stu-id="27140-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27140-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27140-133">-InputObject</span></span>
<span data-ttu-id="27140-134">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="27140-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27140-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27140-135">-Name</span></span>
<span data-ttu-id="27140-136">A függvény app neve.</span><span class="sxs-lookup"><span data-stu-id="27140-136">The name of the function app.</span></span>

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

### <span data-ttu-id="27140-137">-Várva</span><span class="sxs-lookup"><span data-stu-id="27140-137">-NoWait</span></span>
<span data-ttu-id="27140-138">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="27140-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="27140-139">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="27140-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="27140-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="27140-140">-PlanName</span></span>
<span data-ttu-id="27140-141">A szolgáltatás tervének neve.</span><span class="sxs-lookup"><span data-stu-id="27140-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="27140-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27140-142">-ResourceGroupName</span></span>
<span data-ttu-id="27140-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="27140-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="27140-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27140-144">-SubscriptionId</span></span>
<span data-ttu-id="27140-145">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27140-145">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="27140-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="27140-146">-Tag</span></span>
<span data-ttu-id="27140-147">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="27140-147">Resource tags.</span></span>

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

### <span data-ttu-id="27140-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27140-148">-Confirm</span></span>
<span data-ttu-id="27140-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27140-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27140-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27140-150">-WhatIf</span></span>
<span data-ttu-id="27140-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27140-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27140-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27140-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27140-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27140-153">CommonParameters</span></span>
<span data-ttu-id="27140-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27140-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27140-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27140-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27140-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27140-156">INPUTS</span></span>

### <span data-ttu-id="27140-157">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="27140-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="27140-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27140-158">OUTPUTS</span></span>

### <span data-ttu-id="27140-159">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="27140-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="27140-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27140-160">NOTES</span></span>

<span data-ttu-id="27140-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="27140-161">ALIASES</span></span>

<span data-ttu-id="27140-162">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="27140-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27140-163">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="27140-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27140-164">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="27140-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27140-165">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="27140-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="27140-166">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="27140-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="27140-167">`CloningInfoSourceWebAppId <String>`: A forrás app ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27140-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="27140-168">Az App-erőforrás-azonosító a gyártási résidők és a/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} más bővítőhelyekhez való/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}.</span><span class="sxs-lookup"><span data-stu-id="27140-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="27140-169">`[Kind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="27140-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="27140-170">`[Tag <IResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="27140-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="27140-171">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="27140-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="27140-172">`[ClientAffinityEnabled <Boolean?>]`: az <code>true</code> ügyfél-affinitás engedélyezéséhez: a <code>false</code> munkamenet-affinitást tartalmazó cookie-k küldésének leállítása, amely az ügyfélalkalmazás ugyanazon példányra irányuló kérelme.</span><span class="sxs-lookup"><span data-stu-id="27140-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="27140-173">Alapértelmezés: <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="27140-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> az ügyféltanúsítvány-alapú hitelesítés engedélyezéséhez (TLS-alapú kölcsönös hitelesítés); egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="27140-175">Alapértelmezés: <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="27140-176">`[ClientCertExclusionPath <String>]`: ügyféltanúsítvány-alapú hitelesítés vesszővel elválasztott kizárási útvonalak</span><span class="sxs-lookup"><span data-stu-id="27140-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="27140-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Az alkalmazás beállításai felülbírálják a klónozott alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="27140-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="27140-178">Ha meg van adva, ezek a beállítások felülbírálják a forrás alkalmazásból klónozott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="27140-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="27140-179">Egyéb esetben a Source App alkalmazás beállításai megőrződnek.</span><span class="sxs-lookup"><span data-stu-id="27140-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="27140-180">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="27140-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="27140-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Egyéni állomásnevek klónozása a Source app-ból; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="27140-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> a forrás-irányítás klónozása forrás alkalmazásból; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="27140-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> a forrás-és a rendeltetési app terheléselosztásának beállítása.</span><span class="sxs-lookup"><span data-stu-id="27140-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="27140-184">`[CloningInfoCorrelationId <String>]`: A klónozási művelet korrelációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27140-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="27140-185">Ez az azonosító több klónozási műveletet köt össze, hogy ugyanazt a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="27140-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="27140-186">`[CloningInfoHostingEnvironment <String>]`: Alkalmazás-szolgáltatási környezet.</span><span class="sxs-lookup"><span data-stu-id="27140-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="27140-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> a cél-app felülírása; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="27140-188">`[CloningInfoSourceWebAppLocation <String>]`: A Source app: Nyugat-amerikai vagy észak-európai verzió helye</span><span class="sxs-lookup"><span data-stu-id="27140-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="27140-189">`[CloningInfoTrafficManagerProfileId <String>]`: A használni kívánt forgalomirányító-profil ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27140-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="27140-190">A Traffic Manager erőforrás-AZONOSÍTÓja az űrlap/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="27140-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="27140-191">`[CloningInfoTrafficManagerProfileName <String>]`: A létrehozandó Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="27140-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="27140-192">Erre csak akkor van szükség, ha a Traffic Manager profilja még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="27140-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="27140-193">`[Config <ISiteConfig>]`: Az alkalmazás konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="27140-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="27140-194">`IsPushEnabled <Boolean>`: Megadhatja vagy beállíthatja, hogy a leküldéses végpont engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="27140-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="27140-195">`[ActionMinProcessExecutionTime <String>]`: A folyamat végrehajtásának minimális ideje a művelet megkezdése előtt</span><span class="sxs-lookup"><span data-stu-id="27140-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="27140-196">`[ActionType <AutoHealActionType?>]`: Előre definiált műveletek.</span><span class="sxs-lookup"><span data-stu-id="27140-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="27140-197">`[AlwaysOn <Boolean?>]`: <code>true</code> Ha a mindig engedélyezve van, egyéb esetben <code>false</code> :</span><span class="sxs-lookup"><span data-stu-id="27140-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-198">`[ApiDefinitionUrl <String>]`: Az API-definíció URL-címe.</span><span class="sxs-lookup"><span data-stu-id="27140-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="27140-199">`[ApiManagementConfigId <String>]`: APIM-Api azonosító.</span><span class="sxs-lookup"><span data-stu-id="27140-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="27140-200">`[AppCommandLine <String>]`: Az App parancssora az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="27140-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="27140-201">`[AppSetting <INameValuePair[]>]`: Alkalmazásbeállítások.</span><span class="sxs-lookup"><span data-stu-id="27140-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="27140-202">`[Name <String>]`: Páros név.</span><span class="sxs-lookup"><span data-stu-id="27140-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="27140-203">`[Value <String>]`: Pair érték.</span><span class="sxs-lookup"><span data-stu-id="27140-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="27140-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Ha az automatikus gyógyulás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-205">`[AutoSwapSlotName <String>]`: Automatikus swap-tárolóhely neve.</span><span class="sxs-lookup"><span data-stu-id="27140-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="27140-206">`[ConnectionString <IConnStringInfo[]>]`: Kapcsolódási karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="27140-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="27140-207">`[ConnectionString <String>]`: Kapcsolati karakterlánc értéke.</span><span class="sxs-lookup"><span data-stu-id="27140-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="27140-208">`[Name <String>]`: A kapcsolati karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="27140-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="27140-209">`[Type <ConnectionStringType?>]`: Adatbázis típusa.</span><span class="sxs-lookup"><span data-stu-id="27140-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="27140-210">`[CorAllowedOrigin <String[]>]`: Beilleszti vagy beállítja az eredeti hívások (például: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="27140-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="27140-211">Az összes engedélyezéséhez használja a "\*" billentyűt.</span><span class="sxs-lookup"><span data-stu-id="27140-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="27140-212">`[CorSupportCredentials <Boolean?>]`: Beolvassa vagy beállítja, hogy a hitelesítő adatokkal rendelkező CORS-kérelmek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="27140-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="27140-213"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsTovábbi részletekért tekintse meg.</span><span class="sxs-lookup"><span data-stu-id="27140-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="27140-214">`[CustomActionExe <String>]`: Végrehajtható fájl futtatása.</span><span class="sxs-lookup"><span data-stu-id="27140-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="27140-215">`[CustomActionParameter <String>]`: A végrehajtható fájl paramétereinek paraméterei.</span><span class="sxs-lookup"><span data-stu-id="27140-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="27140-216">`[DefaultDocument <String[]>]`: Alapértelmezett dokumentumok.</span><span class="sxs-lookup"><span data-stu-id="27140-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="27140-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Ha a részletes hibák naplózása engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-218">`[DocumentRoot <String>]`: Dokumentum gyökerét.</span><span class="sxs-lookup"><span data-stu-id="27140-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="27140-219">`[DynamicTagsJson <String>]`: A leküldéses regisztráció végpontjában a felhasználói jogcímekről kiértékelt dinamikus címkék listáját tartalmazó JSON karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="27140-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="27140-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: A Ramp-up szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="27140-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="27140-221">`[ActionHostName <String>]`: Annak a bővítőhelynek a neve, amelybe a forgalmat irányítja át.</span><span class="sxs-lookup"><span data-stu-id="27140-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="27140-222">Pl.</span><span class="sxs-lookup"><span data-stu-id="27140-222">E.g.</span></span> <span data-ttu-id="27140-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="27140-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="27140-224">`[ChangeDecisionCallbackUrl <String>]`: Egyéni döntési algoritmust is megadhat a TiPCallback webhelyen, mely URL-címet lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="27140-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="27140-225">Lásd: a TiPCallback a szerelő és a szerződések számára.</span><span class="sxs-lookup"><span data-stu-id="27140-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="27140-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="27140-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="27140-227">`[ChangeIntervalInMinute <Int32?>]`: A ReroutePercentage újraértékeléséhez a percekben megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="27140-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="27140-228">`[ChangeStep <Double?>]`: Az automatikus Ramp up forgatókönyvben ez a lépés a Hozzáadás/Eltávolítás, <code>ReroutePercentage</code> amíg el nem éri a \n <code>MinReroutePercentage</code> vagy a         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="27140-229">A webhely metrikáit a .\NCustom-döntési algoritmusban megadott minden N percben ellenőrizni <code>ChangeIntervalInMinutes</code> lehet a TiPCallback webhelyen, mely URL-címet lehet megadni <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="27140-230">`[MaxReroutePercentage <Double?>]`: Itt adhatja meg azt a felső határt, amely alatt a ReroutePercentage marad.</span><span class="sxs-lookup"><span data-stu-id="27140-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="27140-231">`[MinReroutePercentage <Double?>]`: Itt adhatja meg azt az alsó határértéket, amely fölött a ReroutePercentage marad.</span><span class="sxs-lookup"><span data-stu-id="27140-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="27140-232">`[Name <String>]`: A műveletterv szabály neve.</span><span class="sxs-lookup"><span data-stu-id="27140-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="27140-233">Az ajánlott név arra a pontra mutat, amely a kísérletben szereplő forgalmat fogja fogadni.</span><span class="sxs-lookup"><span data-stu-id="27140-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="27140-234">`[ReroutePercentage <Double?>]`: Az átirányítani kívánt forgalom százalékos aránya <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="27140-235">`[FtpsState <FtpsState?>]`: FTP/FTPS szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="27140-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="27140-236">`[HandlerMapping <IHandlerMapping[]>]`: Kezelői megfeleltetések.</span><span class="sxs-lookup"><span data-stu-id="27140-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="27140-237">`[Argument <String>]`: A parancsfájl-feldolgozó által átadandó parancssori argumentumok.</span><span class="sxs-lookup"><span data-stu-id="27140-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="27140-238">`[Extension <String>]`: A kiterjesztéssel elvégezhető kérelmeket a megadott FastCGI-alkalmazás kezeli.</span><span class="sxs-lookup"><span data-stu-id="27140-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="27140-239">`[ScriptProcessor <String>]`: A FastCGI-alkalmazás abszolút elérési útja.</span><span class="sxs-lookup"><span data-stu-id="27140-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="27140-240">`[HealthCheckPath <String>]`: Állapot-ellenőrzés elérési útja</span><span class="sxs-lookup"><span data-stu-id="27140-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="27140-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: webhelyek beállítása, hogy az ügyfelek a http 2.0-s verziós kapcsolatot engedélyezzék</span><span class="sxs-lookup"><span data-stu-id="27140-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="27140-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Ha a http-naplózás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások a Main esetében.</span><span class="sxs-lookup"><span data-stu-id="27140-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="27140-244">`[Action <String>]`: Engedélyezze vagy tiltsa le az IP-címtartomány elérését.</span><span class="sxs-lookup"><span data-stu-id="27140-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="27140-245">`[Description <String>]`: IP-korlátozási szabály leírása.</span><span class="sxs-lookup"><span data-stu-id="27140-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="27140-246">`[IPAddress <String>]`: IP-cím: a biztonsági korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="27140-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="27140-247">Lehet egy egyszerű IPv4-cím (kötelező SubnetMask tulajdonság) vagy a CIDR-jelölés (például IPv4/Mask (vezető bit)) formájában.</span><span class="sxs-lookup"><span data-stu-id="27140-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="27140-248">Az CIDR esetében a SubnetMask tulajdonság nem adható meg.</span><span class="sxs-lookup"><span data-stu-id="27140-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="27140-249">`[Name <String>]`: IP-korlátozási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="27140-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="27140-250">`[Priority <Int32?>]`: Az IP-korlátozási szabály prioritása.</span><span class="sxs-lookup"><span data-stu-id="27140-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="27140-251">`[SubnetMask <String>]`: Alhálózati maszk az IP-címek tartományához: a korlátozás érvényes.</span><span class="sxs-lookup"><span data-stu-id="27140-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="27140-252">`[SubnetTrafficTag <Int32?>]`: (belső) alhálózat-forgalmi címke</span><span class="sxs-lookup"><span data-stu-id="27140-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="27140-253">`[Tag <IPFilterTag?>]`: Itt határozhatja meg, hogy melyik IP-szűrőt fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="27140-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="27140-254">Ez a szolgáltatás támogatja az IP-szűrést a proxykban.</span><span class="sxs-lookup"><span data-stu-id="27140-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="27140-255">`[VnetSubnetResourceId <String>]`: Virtuális hálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="27140-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="27140-256">`[VnetTrafficTag <Int32?>]`: (belső) vnet forgalmi címke</span><span class="sxs-lookup"><span data-stu-id="27140-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="27140-257">`[JavaContainer <String>]`: Java tároló.</span><span class="sxs-lookup"><span data-stu-id="27140-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="27140-258">`[JavaContainerVersion <String>]`: Java tároló verziója.</span><span class="sxs-lookup"><span data-stu-id="27140-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="27140-259">`[JavaVersion <String>]`: Java-verzió.</span><span class="sxs-lookup"><span data-stu-id="27140-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="27140-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Megengedett maximális lemezhasználat MEGABÁJTban.</span><span class="sxs-lookup"><span data-stu-id="27140-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="27140-261">`[LimitMaxMemoryInMb <Int64?>]`: Az engedélyezett memória maximális kihasználtsága MEGABÁJTban.</span><span class="sxs-lookup"><span data-stu-id="27140-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="27140-262">`[LimitMaxPercentageCpu <Double?>]`: Megengedett maximális CPU-használati százalék</span><span class="sxs-lookup"><span data-stu-id="27140-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="27140-263">`[LinuxFxVersion <String>]`: Linux app-keretrendszer és verzió</span><span class="sxs-lookup"><span data-stu-id="27140-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="27140-264">`[LoadBalancing <SiteLoadBalancing?>]`: A webhely terheléselosztása.</span><span class="sxs-lookup"><span data-stu-id="27140-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="27140-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> a helyi MySQL engedélyezéséhez; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-naplók: a könyvtár mérete korlátozva</span><span class="sxs-lookup"><span data-stu-id="27140-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="27140-267">`[MachineKeyDecryption <String>]`: A visszafejtéshez használt algoritmus.</span><span class="sxs-lookup"><span data-stu-id="27140-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="27140-268">`[MachineKeyDecryptionKey <String>]`: Visszafejtési kulcs.</span><span class="sxs-lookup"><span data-stu-id="27140-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="27140-269">`[MachineKeyValidation <String>]`: MachineKey érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="27140-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="27140-270">`[MachineKeyValidationKey <String>]`: Érvényesítési kulcs.</span><span class="sxs-lookup"><span data-stu-id="27140-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="27140-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Felügyelt csővezeték üzemmód.</span><span class="sxs-lookup"><span data-stu-id="27140-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="27140-272">`[ManagedServiceIdentityId <Int32?>]`: Felügyelt szolgáltatás azonosítóját azonosító</span><span class="sxs-lookup"><span data-stu-id="27140-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="27140-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: az SSL-kérésekhez szükséges TLS minimális verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="27140-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="27140-274">`[NetFrameworkVersion <String>]`: .NET-keretrendszer verziója.</span><span class="sxs-lookup"><span data-stu-id="27140-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="27140-275">`[NodeVersion <String>]`: Node.js verziója.</span><span class="sxs-lookup"><span data-stu-id="27140-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="27140-276">`[NumberOfWorker <Int32?>]`: A munkavállalók száma.</span><span class="sxs-lookup"><span data-stu-id="27140-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="27140-277">`[PhpVersion <String>]`: A PHP verziója.</span><span class="sxs-lookup"><span data-stu-id="27140-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="27140-278">`[PowerShellVersion <String>]`: A PowerShell verziója.</span><span class="sxs-lookup"><span data-stu-id="27140-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="27140-279">`[PreWarmedInstanceCount <Int32?>]`: Az előmelegített példányok száma.</span><span class="sxs-lookup"><span data-stu-id="27140-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="27140-280">Ez a beállítás csak a fogyasztási és a rugalmas csomagokra érvényes.</span><span class="sxs-lookup"><span data-stu-id="27140-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="27140-281">`[PublishingUsername <String>]`: Közzétételi Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="27140-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="27140-282">`[PushKind <String>]`: Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="27140-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="27140-283">`[PythonVersion <String>]`: A Python verziója.</span><span class="sxs-lookup"><span data-stu-id="27140-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="27140-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Ha a távoli hibakeresés engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-285">`[RemoteDebuggingVersion <String>]`: Távoli hibakeresési verzió.</span><span class="sxs-lookup"><span data-stu-id="27140-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="27140-286">`[RequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="27140-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="27140-287">`[RequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="27140-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="27140-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Ha a kérés nyomkövetése engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-289">`[RequestTracingExpirationTime <DateTime?>]`: A nyomkövetés lejárati időpontjának kérése</span><span class="sxs-lookup"><span data-stu-id="27140-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="27140-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-biztonsági korlátozások az SCM-hez.</span><span class="sxs-lookup"><span data-stu-id="27140-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="27140-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Az SCM-re vonatkozó IP-biztonsági korlátozások fő.</span><span class="sxs-lookup"><span data-stu-id="27140-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="27140-292">`[ScmType <ScmType?>]`: SCM típus.</span><span class="sxs-lookup"><span data-stu-id="27140-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="27140-293">`[SlowRequestCount <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="27140-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="27140-294">`[SlowRequestTimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="27140-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="27140-295">`[SlowRequestTimeTaken <String>]`: Idő.</span><span class="sxs-lookup"><span data-stu-id="27140-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="27140-296">`[TagWhitelistJson <String>]`: A leküldéses regisztrációs végpont által használt címkék listáját tartalmazó JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="27140-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="27140-297">`[TagsRequiringAuth <String>]`: A leküldéses regisztráció végpontján a felhasználó által használt hitelesítést igénylő kódok listáját tartalmazó, JSON-karakterláncot kap vagy állít be.</span><span class="sxs-lookup"><span data-stu-id="27140-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="27140-298">A címkék tartalmazhatnak alfanumerikus karaktereket, a következőt: "_", "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="27140-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="27140-299">Az érvényesítést a PushRequestHandler kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="27140-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="27140-300">`[TracingOption <String>]`: Nyomkövetési beállítások.</span><span class="sxs-lookup"><span data-stu-id="27140-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="27140-301">`[TriggerPrivateBytesInKb <Int32?>]`: Privát bájton alapuló szabály.</span><span class="sxs-lookup"><span data-stu-id="27140-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="27140-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A szabályok az állapotkódok alapján.</span><span class="sxs-lookup"><span data-stu-id="27140-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="27140-303">`[Count <Int32?>]`: Kérések száma.</span><span class="sxs-lookup"><span data-stu-id="27140-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="27140-304">`[Status <Int32?>]`: HTTP-állapotkód.</span><span class="sxs-lookup"><span data-stu-id="27140-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="27140-305">`[SubStatus <Int32?>]`: Alállapot kérése</span><span class="sxs-lookup"><span data-stu-id="27140-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="27140-306">`[TimeInterval <String>]`: Időintervallum.</span><span class="sxs-lookup"><span data-stu-id="27140-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="27140-307">`[Win32Status <Int32?>]`: Win32-hibakód.</span><span class="sxs-lookup"><span data-stu-id="27140-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="27140-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bites munkavégző folyamat használata; egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtuális alkalmazások.</span><span class="sxs-lookup"><span data-stu-id="27140-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="27140-310">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="27140-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="27140-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> Ha engedélyezve van az előzetes bekapcsolás, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="27140-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuális könyvtárak a virtuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="27140-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="27140-313">`[PhysicalPath <String>]`: Fizikai elérési út.</span><span class="sxs-lookup"><span data-stu-id="27140-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="27140-314">`[VirtualPath <String>]`: A virtuális alkalmazás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="27140-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="27140-315">`[VirtualPath <String>]`: Virtuális elérési út.</span><span class="sxs-lookup"><span data-stu-id="27140-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="27140-316">`[VnetName <String>]`: Virtuális hálózati név.</span><span class="sxs-lookup"><span data-stu-id="27140-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="27140-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Ha a Webszoftvercsatorna engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="27140-318">`[WindowsFxVersion <String>]`: Xenon alkalmazás kerete és verziója</span><span class="sxs-lookup"><span data-stu-id="27140-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="27140-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit felügyelt szolgáltatás-azonosító</span><span class="sxs-lookup"><span data-stu-id="27140-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="27140-320">`[ContainerSize <Int32?>]`: A függvény tárolójának mérete.</span><span class="sxs-lookup"><span data-stu-id="27140-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="27140-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximálisan engedélyezett napi memória-időkvóta (csak dinamikus alkalmazásokban alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="27140-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="27140-322">`[Enabled <Boolean?>]`: <code>true</code> Ha az alkalmazás engedélyezve van, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="27140-323">Az érték hamis értékre állítása letiltja az alkalmazást (az alkalmazást kapcsolat nélkül jeleníti meg).</span><span class="sxs-lookup"><span data-stu-id="27140-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="27140-324">`[HostNameSslState <IHostNameSslState[]>]`: A gépnév SSL-Államok az App állomásnevek SSL-kötéseinek kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="27140-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="27140-325">`[HostType <HostType?>]`: Azt jelzi, hogy a gépnév normál vagy tárházas állomásnév-e.</span><span class="sxs-lookup"><span data-stu-id="27140-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="27140-326">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="27140-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="27140-327">`[SslState <SslState?>]`: SSL típusa.</span><span class="sxs-lookup"><span data-stu-id="27140-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="27140-328">`[Thumbprint <String>]`: SSL-tanúsítvány ujjlenyomata.</span><span class="sxs-lookup"><span data-stu-id="27140-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="27140-329">`[ToUpdate <Boolean?>]`: A <code>true</code> meglévő állomásnév frissítésének beállítása.</span><span class="sxs-lookup"><span data-stu-id="27140-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="27140-330">`[VirtualIP <String>]`: A gépnévhez rendelt virtuális IP-cím, ha az IP-alapú SSL engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="27140-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="27140-331">`[HostNamesDisabled <Boolean?>]`: az <code>true</code> app nyilvános állomásnevek letiltása; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="27140-332">Ha <code>true</code> az App csak API-kezelési folyamaton keresztül érhető el.</span><span class="sxs-lookup"><span data-stu-id="27140-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="27140-333">`[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27140-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="27140-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: egy webhely beállítása csak HTTPS-kérelmek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="27140-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="27140-335">Http-kérelmek átirányításának problémái</span><span class="sxs-lookup"><span data-stu-id="27140-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="27140-336">`[HyperV <Boolean?>]`: Hyper-V homokozó.</span><span class="sxs-lookup"><span data-stu-id="27140-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="27140-337">`[IdentityType <ManagedServiceIdentityType?>]`: A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="27140-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="27140-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Az erőforráshoz társított felhasználó által kiosztott identitások listája.</span><span class="sxs-lookup"><span data-stu-id="27140-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="27140-339">A felhasználó személyazonosságát ismertető szótár fő hivatkozásai az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}"-ban az űrlapon lesznek.</span><span class="sxs-lookup"><span data-stu-id="27140-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="27140-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="27140-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="27140-341">`[IsXenon <Boolean?>]`: Elavult: Hyper-V homokozó.</span><span class="sxs-lookup"><span data-stu-id="27140-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="27140-342">`[RedundancyMode <RedundancyMode?>]`: Webhely-redundancia mód</span><span class="sxs-lookup"><span data-stu-id="27140-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="27140-343">`[Reserved <Boolean?>]`: <code>true</code> Ha fenn van foglalva, egyéb esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="27140-344">`[ScmSiteAlsoStopped <Boolean?>]`: az <code>true</code> SCM-(KUDU-) webhely leállítása, ha az alkalmazás le van állítva; ellenkező esetben <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="27140-345">Az alapértelmezett érték <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="27140-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="27140-346">`[ServerFarmId <String>]`: A társított app Service Plan ("/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}") erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27140-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="27140-347">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27140-347">RELATED LINKS</span></span>

