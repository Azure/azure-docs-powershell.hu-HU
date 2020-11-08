---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185422"
---
# <span data-ttu-id="12db8-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="12db8-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="12db8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12db8-102">SYNOPSIS</span></span>
<span data-ttu-id="12db8-103">Egy függvény alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12db8-103">Creates a function app.</span></span>

## <span data-ttu-id="12db8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12db8-104">SYNTAX</span></span>

### <span data-ttu-id="12db8-105">Felhasználás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12db8-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12db8-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="12db8-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12db8-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="12db8-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12db8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="12db8-108">DESCRIPTION</span></span>
<span data-ttu-id="12db8-109">Egy függvény alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12db8-109">Creates a function app.</span></span>

## <span data-ttu-id="12db8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="12db8-110">EXAMPLES</span></span>

### <span data-ttu-id="12db8-111">1. példa: a használati PowerShell-függvény létrehozása a közép-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="12db8-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="12db8-112">Ez a parancs a közép-amerikai fogyasztási PowerShell-függvény alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12db8-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="12db8-113">2. példa: hozzon létre egy PowerShell-függvényt, amelyet egy szolgáltatási tervben fog tárolni.</span><span class="sxs-lookup"><span data-stu-id="12db8-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="12db8-114">Ez a parancs létrehoz egy PowerShell-függvény alkalmazást, amely egy szolgáltatási csomag keretében fog működni.</span><span class="sxs-lookup"><span data-stu-id="12db8-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="12db8-115">3. példa: a Function app létrehozása privát ACR-kép használatával.</span><span class="sxs-lookup"><span data-stu-id="12db8-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="12db8-116">Ez a parancs létrehoz egy függvény alkalmazást egy privát ACR-kép használatával.</span><span class="sxs-lookup"><span data-stu-id="12db8-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="12db8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12db8-117">PARAMETERS</span></span>

### <span data-ttu-id="12db8-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="12db8-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="12db8-119">A felvenni kívánt alkalmazás Instrumentation-kulcsa.</span><span class="sxs-lookup"><span data-stu-id="12db8-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="12db8-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="12db8-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="12db8-121">A függvény alkalmazásba felvenni kívánt meglévő alkalmazás-betekintési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="12db8-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="12db8-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="12db8-122">-AppSetting</span></span>
<span data-ttu-id="12db8-123">A Function app beállításai.</span><span class="sxs-lookup"><span data-stu-id="12db8-123">Function app settings.</span></span>

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

### <span data-ttu-id="12db8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12db8-124">-AsJob</span></span>
<span data-ttu-id="12db8-125">A parancsmagot háttérként futtatja.</span><span class="sxs-lookup"><span data-stu-id="12db8-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="12db8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12db8-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="12db8-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="12db8-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="12db8-128">Tiltsa le az alkalmazás-elemzések erőforrás-készítését a függvény app létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="12db8-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="12db8-129">Nem lesz elérhető naplózás.</span><span class="sxs-lookup"><span data-stu-id="12db8-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="12db8-130">-DockerImageName</span></span>
<span data-ttu-id="12db8-131">Csak Linux.</span><span class="sxs-lookup"><span data-stu-id="12db8-131">Linux only.</span></span>
<span data-ttu-id="12db8-132">Tároló képnév a dokkolóegység adatbázisából (például Publisher/Image-Name: címke).</span><span class="sxs-lookup"><span data-stu-id="12db8-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="12db8-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="12db8-134">A tároló beállításjegyzék-felhasználónevét és jelszavát.</span><span class="sxs-lookup"><span data-stu-id="12db8-134">The container registry user name and password.</span></span>
<span data-ttu-id="12db8-135">A privát kibocsátásiegység-forgalmi jegyzékekhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="12db8-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="12db8-136">-FunctionsVersion</span></span>
<span data-ttu-id="12db8-137">A függvények verziója.</span><span class="sxs-lookup"><span data-stu-id="12db8-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="12db8-138">-IdentityID</span></span>
<span data-ttu-id="12db8-139">A függvény alkalmazáshoz társított felhasználói azonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="12db8-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="12db8-140">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="12db8-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="12db8-141">-IdentityType</span></span>
<span data-ttu-id="12db8-142">A függvény alkalmazáshoz használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="12db8-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="12db8-143">A paraméter elfogadható értékei a következők:-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="12db8-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="12db8-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="12db8-144">-Location</span></span>
<span data-ttu-id="12db8-145">A fogyasztási terv helye.</span><span class="sxs-lookup"><span data-stu-id="12db8-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12db8-146">-Name</span></span>
<span data-ttu-id="12db8-147">A függvény app neve.</span><span class="sxs-lookup"><span data-stu-id="12db8-147">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-148">-Várva</span><span class="sxs-lookup"><span data-stu-id="12db8-148">-NoWait</span></span>
<span data-ttu-id="12db8-149">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="12db8-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="12db8-150">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="12db8-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="12db8-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="12db8-151">-OSType</span></span>
<span data-ttu-id="12db8-152">Az operációs rendszer a függvény app üzemeltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="12db8-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12db8-153">-PassThru</span></span>
<span data-ttu-id="12db8-154">Igaz érték visszaadása, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="12db8-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="12db8-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="12db8-155">-PlanName</span></span>
<span data-ttu-id="12db8-156">A szolgáltatás tervének neve.</span><span class="sxs-lookup"><span data-stu-id="12db8-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12db8-157">-ResourceGroupName</span></span>
<span data-ttu-id="12db8-158">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12db8-158">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-159">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="12db8-159">-Runtime</span></span>
<span data-ttu-id="12db8-160">A függvény futtatókörnyezete.</span><span class="sxs-lookup"><span data-stu-id="12db8-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="12db8-161">-RuntimeVersion</span></span>
<span data-ttu-id="12db8-162">A függvény futtatókörnyezete.</span><span class="sxs-lookup"><span data-stu-id="12db8-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="12db8-163">-StorageAccountName</span></span>
<span data-ttu-id="12db8-164">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="12db8-164">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12db8-165">-SubscriptionId</span></span>
<span data-ttu-id="12db8-166">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="12db8-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12db8-167">-Címke</span><span class="sxs-lookup"><span data-stu-id="12db8-167">-Tag</span></span>
<span data-ttu-id="12db8-168">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="12db8-168">Resource tags.</span></span>

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

### <span data-ttu-id="12db8-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12db8-169">-Confirm</span></span>
<span data-ttu-id="12db8-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12db8-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12db8-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12db8-171">-WhatIf</span></span>
<span data-ttu-id="12db8-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12db8-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12db8-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12db8-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12db8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12db8-174">CommonParameters</span></span>
<span data-ttu-id="12db8-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12db8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12db8-176">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12db8-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12db8-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12db8-177">INPUTS</span></span>

## <span data-ttu-id="12db8-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12db8-178">OUTPUTS</span></span>

### <span data-ttu-id="12db8-179">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="12db8-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="12db8-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12db8-180">NOTES</span></span>

<span data-ttu-id="12db8-181">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="12db8-181">ALIASES</span></span>

## <span data-ttu-id="12db8-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12db8-182">RELATED LINKS</span></span>
