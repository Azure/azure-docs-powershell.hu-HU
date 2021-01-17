---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340853"
---
# <span data-ttu-id="69663-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="69663-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="69663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69663-102">SYNOPSIS</span></span>
<span data-ttu-id="69663-103">Függvényalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="69663-103">Creates a function app.</span></span>

## <span data-ttu-id="69663-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69663-104">SYNTAX</span></span>

### <span data-ttu-id="69663-105">Felhasználás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69663-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69663-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69663-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69663-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="69663-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69663-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69663-108">DESCRIPTION</span></span>
<span data-ttu-id="69663-109">Függvényalkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="69663-109">Creates a function app.</span></span>

## <span data-ttu-id="69663-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69663-110">EXAMPLES</span></span>

### <span data-ttu-id="69663-111">1. példa: Fogyasztási PowerShell-függvényalkalmazás létrehozása Közép-Usa-ban.</span><span class="sxs-lookup"><span data-stu-id="69663-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="69663-112">Ez a parancs létrehoz egy fogyasztási PowerShell-függvényalkalmazást az Egyesült Államok középső felében.</span><span class="sxs-lookup"><span data-stu-id="69663-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="69663-113">2. példa: Hozzon létre egy PowerShell-függvényalkalmazást, amely egy szolgáltatástervben fog működni.</span><span class="sxs-lookup"><span data-stu-id="69663-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="69663-114">Ez a parancs létrehoz egy PowerShell-függvényalkalmazást, amely egy szolgáltatástervben fog működni.</span><span class="sxs-lookup"><span data-stu-id="69663-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="69663-115">3. példa: Függvényalkalmazás létrehozása privát ACR-kép használatával.</span><span class="sxs-lookup"><span data-stu-id="69663-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="69663-116">Ez a parancs egy függvényalkalmazást hoz létre egy privát ACR-kép használatával.</span><span class="sxs-lookup"><span data-stu-id="69663-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="69663-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69663-117">PARAMETERS</span></span>

### <span data-ttu-id="69663-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="69663-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="69663-119">Az App Insights hozzáadható eszközkulcsa.</span><span class="sxs-lookup"><span data-stu-id="69663-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="69663-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="69663-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="69663-121">A függvényalkalmazáshoz hozzáadható meglévő App Insights-projekt neve.</span><span class="sxs-lookup"><span data-stu-id="69663-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="69663-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="69663-122">-AppSetting</span></span>
<span data-ttu-id="69663-123">A függvényalkalmazás beállításai.</span><span class="sxs-lookup"><span data-stu-id="69663-123">Function app settings.</span></span>

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

### <span data-ttu-id="69663-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69663-124">-AsJob</span></span>
<span data-ttu-id="69663-125">A parancsmagot háttérként futtatja.</span><span class="sxs-lookup"><span data-stu-id="69663-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="69663-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69663-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="69663-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="69663-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="69663-128">Tiltsa le az alkalmazáselemzési erőforrások létrehozását a függvényalkalmazás létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="69663-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="69663-129">Naplók nem érhetők el.</span><span class="sxs-lookup"><span data-stu-id="69663-129">No logs will be available.</span></span>

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

### <span data-ttu-id="69663-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="69663-130">-DockerImageName</span></span>
<span data-ttu-id="69663-131">Csak Linux.</span><span class="sxs-lookup"><span data-stu-id="69663-131">Linux only.</span></span>
<span data-ttu-id="69663-132">Container image name from Docker Registry, pl. publisher/image-name:tag.</span><span class="sxs-lookup"><span data-stu-id="69663-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="69663-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="69663-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="69663-134">A tároló beállításjegyzékének felhasználóneve és jelszava.</span><span class="sxs-lookup"><span data-stu-id="69663-134">The container registry user name and password.</span></span>
<span data-ttu-id="69663-135">A privát registries esetén kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="69663-135">Required for private registries.</span></span>

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

### <span data-ttu-id="69663-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="69663-136">-FunctionsVersion</span></span>
<span data-ttu-id="69663-137">A Függvények verzió.</span><span class="sxs-lookup"><span data-stu-id="69663-137">The Functions version.</span></span>

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

### <span data-ttu-id="69663-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="69663-138">-IdentityID</span></span>
<span data-ttu-id="69663-139">A függvényalkalmazáshoz társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69663-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="69663-140">A felhasználói identitáshivatkozások ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="69663-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="69663-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="69663-141">-IdentityType</span></span>
<span data-ttu-id="69663-142">A függvényalkalmazáshoz használt identitás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="69663-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="69663-143">A paraméter elfogadható értékei: - SystemAssigned - UserAssigned</span><span class="sxs-lookup"><span data-stu-id="69663-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="69663-144">-Location</span><span class="sxs-lookup"><span data-stu-id="69663-144">-Location</span></span>
<span data-ttu-id="69663-145">A fogyasztási terv helye.</span><span class="sxs-lookup"><span data-stu-id="69663-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="69663-146">-Name</span><span class="sxs-lookup"><span data-stu-id="69663-146">-Name</span></span>
<span data-ttu-id="69663-147">A függvényalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="69663-147">The name of the function app.</span></span>

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

### <span data-ttu-id="69663-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69663-148">-NoWait</span></span>
<span data-ttu-id="69663-149">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="69663-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="69663-150">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="69663-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="69663-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="69663-151">-OSType</span></span>
<span data-ttu-id="69663-152">A függvényalkalmazást szolgáltató operációs rendszer.</span><span class="sxs-lookup"><span data-stu-id="69663-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="69663-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69663-153">-PassThru</span></span>
<span data-ttu-id="69663-154">Eredménye igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="69663-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="69663-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="69663-155">-PlanName</span></span>
<span data-ttu-id="69663-156">A szolgáltatásterv neve.</span><span class="sxs-lookup"><span data-stu-id="69663-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="69663-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69663-157">-ResourceGroupName</span></span>
<span data-ttu-id="69663-158">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="69663-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="69663-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="69663-159">-Runtime</span></span>
<span data-ttu-id="69663-160">A függvény futásidejű.</span><span class="sxs-lookup"><span data-stu-id="69663-160">The function runtime.</span></span>

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

### <span data-ttu-id="69663-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="69663-161">-RuntimeVersion</span></span>
<span data-ttu-id="69663-162">A függvény futásidejű.</span><span class="sxs-lookup"><span data-stu-id="69663-162">The function runtime.</span></span>

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

### <span data-ttu-id="69663-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="69663-163">-StorageAccountName</span></span>
<span data-ttu-id="69663-164">A tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="69663-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="69663-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69663-165">-SubscriptionId</span></span>
<span data-ttu-id="69663-166">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="69663-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="69663-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="69663-167">-Tag</span></span>
<span data-ttu-id="69663-168">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="69663-168">Resource tags.</span></span>

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

### <span data-ttu-id="69663-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69663-169">-Confirm</span></span>
<span data-ttu-id="69663-170">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69663-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69663-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69663-171">-WhatIf</span></span>
<span data-ttu-id="69663-172">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69663-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69663-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69663-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69663-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69663-174">CommonParameters</span></span>
<span data-ttu-id="69663-175">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69663-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69663-176">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69663-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69663-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69663-177">INPUTS</span></span>

## <span data-ttu-id="69663-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69663-178">OUTPUTS</span></span>

### <span data-ttu-id="69663-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="69663-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="69663-180">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69663-180">NOTES</span></span>

<span data-ttu-id="69663-181">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="69663-181">ALIASES</span></span>

## <span data-ttu-id="69663-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69663-182">RELATED LINKS</span></span>

