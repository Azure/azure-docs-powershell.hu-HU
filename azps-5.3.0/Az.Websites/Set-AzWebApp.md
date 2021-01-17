---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466962"
---
# <span data-ttu-id="f2802-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-101">Set-AzWebApp</span></span>

## <span data-ttu-id="f2802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2802-102">SYNOPSIS</span></span>
<span data-ttu-id="f2802-103">Egy Azure Web Appot módosít.</span><span class="sxs-lookup"><span data-stu-id="f2802-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="f2802-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2802-104">SYNTAX</span></span>

### <span data-ttu-id="f2802-105">S1</span><span class="sxs-lookup"><span data-stu-id="f2802-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2802-106">S2</span><span class="sxs-lookup"><span data-stu-id="f2802-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2802-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2802-107">DESCRIPTION</span></span>
<span data-ttu-id="f2802-108">A **Set-AzWebApp** parancsmag beállít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="f2802-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="f2802-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2802-109">EXAMPLES</span></span>

### <span data-ttu-id="f2802-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f2802-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="f2802-111">Ez a parancs módosítja a Default-Web-WestUS erőforráscsoporthoz társított Web App ContosoWebApp appszolgáltatási tervet.</span><span class="sxs-lookup"><span data-stu-id="f2802-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="f2802-112">A hivatkozásra kattintva további információt olvashat az appszolgáltatási terv és a hozzá tartozó korlátozások módosításáról.</span><span class="sxs-lookup"><span data-stu-id="f2802-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="f2802-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="f2802-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="f2802-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="f2802-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="f2802-115">Ez a parancs a HttpLoggingEnabled értéket igazra állítja a Default-Web-WestUS erőforráscsoporthoz társított Web App ContosoWebApp esetén</span><span class="sxs-lookup"><span data-stu-id="f2802-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="f2802-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="f2802-116">Example 3</span></span>

<span data-ttu-id="f2802-117">Egy Azure Web Appot módosít.</span><span class="sxs-lookup"><span data-stu-id="f2802-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="f2802-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="f2802-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="f2802-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="f2802-119">Example 4</span></span>

<span data-ttu-id="f2802-120">Az alábbi példa létrehoz egy myConnectionString for Web App ContosoWebApp nevű kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="f2802-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="f2802-121">Ez lecseréli a Web App ContosoWebApp összes meglévő kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="f2802-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="f2802-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2802-122">PARAMETERS</span></span>

### <span data-ttu-id="f2802-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="f2802-123">-AlwaysOn</span></span>
<span data-ttu-id="f2802-124">Gondoskodjon arról, hogy a webalkalmazás mindig betöltődik, és ne legyen eltávolítva, miután inaktív volt.</span><span class="sxs-lookup"><span data-stu-id="f2802-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f2802-125">-AppServicePlan</span></span>
<span data-ttu-id="f2802-126">Appszolgáltatás-terv neve</span><span class="sxs-lookup"><span data-stu-id="f2802-126">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="f2802-127">-AppSettings</span></span>
<span data-ttu-id="f2802-128">App Settings HashTable.</span><span class="sxs-lookup"><span data-stu-id="f2802-128">App Settings HashTable.</span></span> <span data-ttu-id="f2802-129">A rendszer lecseréli a meglévő alkalmazásbeállításokat, és eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="f2802-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2802-130">-AsJob</span></span>
<span data-ttu-id="f2802-131">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f2802-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2802-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f2802-132">-AssignIdentity</span></span>
<span data-ttu-id="f2802-133">MSI engedélyezése/letiltása meglévő Azure WebAppban vagy functionappban</span><span class="sxs-lookup"><span data-stu-id="f2802-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-134">-AutoSwapSzajName</span><span class="sxs-lookup"><span data-stu-id="f2802-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="f2802-135">Célhely neve az automatikus felcseréléshez</span><span class="sxs-lookup"><span data-stu-id="f2802-135">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="f2802-136">-AzureStoragePath</span></span>
<span data-ttu-id="f2802-137">Azure Storage, amely egy tárolóhoz való webalkalmazásba csatolható.</span><span class="sxs-lookup"><span data-stu-id="f2802-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="f2802-138">A New-AzureRmWebAppAzureStoragePath létrehozása</span><span class="sxs-lookup"><span data-stu-id="f2802-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="f2802-139">-ConnectionStrings</span></span>
<span data-ttu-id="f2802-140">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="f2802-140">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f2802-141">-ContainerImageName</span></span>
<span data-ttu-id="f2802-142">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="f2802-142">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f2802-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f2802-144">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="f2802-144">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f2802-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f2802-146">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="f2802-146">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f2802-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="f2802-148">Private Container Registry Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="f2802-148">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="f2802-149">-DefaultDocuments</span></span>
<span data-ttu-id="f2802-150">Default Documents String Array</span><span class="sxs-lookup"><span data-stu-id="f2802-150">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2802-151">-DefaultProfile</span></span>
<span data-ttu-id="f2802-152">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2802-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f2802-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="f2802-154">Részletes hibanaplózás engedélyezése logikai</span><span class="sxs-lookup"><span data-stu-id="f2802-154">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f2802-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f2802-156">Engedélyezi/letiltja a tároló folyamatos üzembe helyezését webhook</span><span class="sxs-lookup"><span data-stu-id="f2802-156">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="f2802-157">-FtpsState</span></span>
<span data-ttu-id="f2802-158">Adja meg egy alkalmazás Ftps-állapotának értékét.</span><span class="sxs-lookup"><span data-stu-id="f2802-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="f2802-159">Engedélyezett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="f2802-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="f2802-160">-HandlerMappings</span></span>
<span data-ttu-id="f2802-161">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="f2802-161">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="f2802-162">-HostNames</span></span>
<span data-ttu-id="f2802-163">WebApp HostNames karakterlánctömb</span><span class="sxs-lookup"><span data-stu-id="f2802-163">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f2802-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="f2802-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="f2802-165">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f2802-166">-HttpsOnly</span></span>
<span data-ttu-id="f2802-167">Az összes forgalom HTTPS-re való átirányításának engedélyezése/letiltása meglévő Azure WebAppon vagy functionappon</span><span class="sxs-lookup"><span data-stu-id="f2802-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="f2802-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="f2802-169">Felügyelt folyamat mód neve</span><span class="sxs-lookup"><span data-stu-id="f2802-169">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f2802-170">-MinTlsVersion</span></span>
<span data-ttu-id="f2802-171">Az SSL-kérelmekhez minimálisan szükséges TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="f2802-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="f2802-172">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="f2802-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-173">-Name</span><span class="sxs-lookup"><span data-stu-id="f2802-173">-Name</span></span>
<span data-ttu-id="f2802-174">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f2802-174">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="f2802-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="f2802-176">Net-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="f2802-176">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="f2802-177">-NumberOfWorkers</span></span>
<span data-ttu-id="f2802-178">A kiosztandó dolgozók száma</span><span class="sxs-lookup"><span data-stu-id="f2802-178">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="f2802-179">-PhpVersion</span></span>
<span data-ttu-id="f2802-180">Php verzió</span><span class="sxs-lookup"><span data-stu-id="f2802-180">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="f2802-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="f2802-182">Request Tracing Enabled</span><span class="sxs-lookup"><span data-stu-id="f2802-182">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2802-183">-ResourceGroupName</span></span>
<span data-ttu-id="f2802-184">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f2802-184">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="f2802-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="f2802-186">A 32 bites worker process boolean használata</span><span class="sxs-lookup"><span data-stu-id="f2802-186">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-187">-WebApp</span></span>
<span data-ttu-id="f2802-188">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="f2802-188">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="f2802-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="f2802-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="f2802-190">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2802-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2802-191">CommonParameters</span></span>
<span data-ttu-id="f2802-192">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2802-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2802-193">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2802-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2802-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2802-194">INPUTS</span></span>

### <span data-ttu-id="f2802-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f2802-195">System.Int32</span></span>

### <span data-ttu-id="f2802-196">System.String</span><span class="sxs-lookup"><span data-stu-id="f2802-196">System.String</span></span>

### <span data-ttu-id="f2802-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f2802-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f2802-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2802-198">OUTPUTS</span></span>

### <span data-ttu-id="f2802-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f2802-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f2802-200">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2802-200">NOTES</span></span>
<span data-ttu-id="f2802-201">Az alábbi parancsmag segítséget nyújt az Azure Web App **DOTNETCORE-re frissítéséhez**</span><span class="sxs-lookup"><span data-stu-id="f2802-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="f2802-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="f2802-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="f2802-203">Cserélje le a Default-Web-WestUS értékeket az erőforráscsoport nevére, a ContosoWebAppra pedig a webapp nevére.</span><span class="sxs-lookup"><span data-stu-id="f2802-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="f2802-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2802-204">RELATED LINKS</span></span>

[<span data-ttu-id="f2802-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="f2802-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="f2802-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="f2802-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="f2802-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="f2802-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f2802-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="f2802-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="f2802-211">New-AzResource</span></span>](./New-AzResource.md)
