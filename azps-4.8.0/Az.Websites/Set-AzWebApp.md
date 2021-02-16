---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 46c5dae54bf4f59556e62256797a43221d0650b7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412350"
---
# <span data-ttu-id="e72ad-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-101">Set-AzWebApp</span></span>

## <span data-ttu-id="e72ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e72ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e72ad-103">Egy Azure Web Appot módosít.</span><span class="sxs-lookup"><span data-stu-id="e72ad-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="e72ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e72ad-104">SYNTAX</span></span>

### <span data-ttu-id="e72ad-105">S1</span><span class="sxs-lookup"><span data-stu-id="e72ad-105">S1</span></span>
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

### <span data-ttu-id="e72ad-106">S2</span><span class="sxs-lookup"><span data-stu-id="e72ad-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e72ad-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e72ad-107">DESCRIPTION</span></span>
<span data-ttu-id="e72ad-108">A **Set-AzWebApp** parancsmag beállít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="e72ad-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="e72ad-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e72ad-109">EXAMPLES</span></span>

### <span data-ttu-id="e72ad-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e72ad-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="e72ad-111">Ez a parancs módosítja a Default-Web-WestUS erőforráscsoporthoz társított Web App ContosoWebApp appszolgáltatási tervet.</span><span class="sxs-lookup"><span data-stu-id="e72ad-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e72ad-112">A hivatkozásra kattintva további információt olvashat az appszolgáltatási terv és a hozzá tartozó korlátozások módosításáról.</span><span class="sxs-lookup"><span data-stu-id="e72ad-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="e72ad-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="e72ad-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="e72ad-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e72ad-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="e72ad-115">Ez a parancs a HttpLoggingEnabled értéket igazra állítja a Default-Web-WestUS erőforráscsoporthoz társított Web App ContosoWebApp esetén</span><span class="sxs-lookup"><span data-stu-id="e72ad-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="e72ad-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="e72ad-116">Example 3</span></span>

<span data-ttu-id="e72ad-117">Egy Azure Web Appot módosít.</span><span class="sxs-lookup"><span data-stu-id="e72ad-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="e72ad-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="e72ad-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="e72ad-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e72ad-119">PARAMETERS</span></span>

### <span data-ttu-id="e72ad-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="e72ad-120">-AlwaysOn</span></span>
<span data-ttu-id="e72ad-121">Gondoskodjon arról, hogy a webalkalmazás mindig betöltődik, és ne legyen eltávolítva, miután inaktív volt.</span><span class="sxs-lookup"><span data-stu-id="e72ad-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="e72ad-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e72ad-122">-AppServicePlan</span></span>
<span data-ttu-id="e72ad-123">Appszolgáltatás-terv neve</span><span class="sxs-lookup"><span data-stu-id="e72ad-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="e72ad-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e72ad-124">-AppSettings</span></span>
<span data-ttu-id="e72ad-125">App Settings HashTable.</span><span class="sxs-lookup"><span data-stu-id="e72ad-125">App Settings HashTable.</span></span> <span data-ttu-id="e72ad-126">A rendszer lecseréli a meglévő alkalmazásbeállításokat, és eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="e72ad-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="e72ad-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e72ad-127">-AsJob</span></span>
<span data-ttu-id="e72ad-128">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e72ad-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e72ad-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e72ad-129">-AssignIdentity</span></span>
<span data-ttu-id="e72ad-130">MSI engedélyezése/letiltása meglévő Azure WebAppban vagy functionappban</span><span class="sxs-lookup"><span data-stu-id="e72ad-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="e72ad-131">-AutoSwapSzajName</span><span class="sxs-lookup"><span data-stu-id="e72ad-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="e72ad-132">Célhely neve az automatikus felcseréléshez</span><span class="sxs-lookup"><span data-stu-id="e72ad-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="e72ad-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="e72ad-133">-AzureStoragePath</span></span>
<span data-ttu-id="e72ad-134">Azure Storage csatlakoztatása egy tárolóhoz való webalkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="e72ad-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="e72ad-135">A New-AzureRmWebAppAzureStoragePath létrehozása</span><span class="sxs-lookup"><span data-stu-id="e72ad-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="e72ad-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e72ad-136">-ConnectionStrings</span></span>
<span data-ttu-id="e72ad-137">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="e72ad-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="e72ad-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="e72ad-138">-ContainerImageName</span></span>
<span data-ttu-id="e72ad-139">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="e72ad-139">Container Image Name</span></span>

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

### <span data-ttu-id="e72ad-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="e72ad-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="e72ad-141">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="e72ad-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="e72ad-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="e72ad-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="e72ad-143">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="e72ad-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="e72ad-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="e72ad-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="e72ad-145">Private Container Registry Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="e72ad-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="e72ad-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e72ad-146">-DefaultDocuments</span></span>
<span data-ttu-id="e72ad-147">Default Documents String Array</span><span class="sxs-lookup"><span data-stu-id="e72ad-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="e72ad-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72ad-148">-DefaultProfile</span></span>
<span data-ttu-id="e72ad-149">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e72ad-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e72ad-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e72ad-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e72ad-151">Részletes hibanaplózás engedélyezése logikai</span><span class="sxs-lookup"><span data-stu-id="e72ad-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="e72ad-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="e72ad-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="e72ad-153">Engedélyezi/letiltja a tároló folyamatos üzembe helyezését webhook</span><span class="sxs-lookup"><span data-stu-id="e72ad-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="e72ad-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="e72ad-154">-FtpsState</span></span>
<span data-ttu-id="e72ad-155">Adja meg egy alkalmazás Ftps state (Ftps állapota) értékét.</span><span class="sxs-lookup"><span data-stu-id="e72ad-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="e72ad-156">Engedélyezett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="e72ad-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="e72ad-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e72ad-157">-HandlerMappings</span></span>
<span data-ttu-id="e72ad-158">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="e72ad-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="e72ad-159">-HostNames</span><span class="sxs-lookup"><span data-stu-id="e72ad-159">-HostNames</span></span>
<span data-ttu-id="e72ad-160">WebApp HostNames karakterlánctömb</span><span class="sxs-lookup"><span data-stu-id="e72ad-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="e72ad-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e72ad-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e72ad-162">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="e72ad-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="e72ad-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e72ad-163">-HttpsOnly</span></span>
<span data-ttu-id="e72ad-164">Az összes forgalom HTTPS-re való átirányításának engedélyezése/letiltása meglévő Azure WebAppon vagy functionappon</span><span class="sxs-lookup"><span data-stu-id="e72ad-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="e72ad-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e72ad-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="e72ad-166">Felügyelt folyamat mód neve</span><span class="sxs-lookup"><span data-stu-id="e72ad-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="e72ad-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e72ad-167">-MinTlsVersion</span></span>
<span data-ttu-id="e72ad-168">Az SSL-kérelmekhez minimálisan szükséges TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="e72ad-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="e72ad-169">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="e72ad-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="e72ad-170">-Name</span><span class="sxs-lookup"><span data-stu-id="e72ad-170">-Name</span></span>
<span data-ttu-id="e72ad-171">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e72ad-171">WebApp Name</span></span>

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

### <span data-ttu-id="e72ad-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e72ad-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="e72ad-173">Net-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="e72ad-173">Net Framework Version</span></span>

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

### <span data-ttu-id="e72ad-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e72ad-174">-NumberOfWorkers</span></span>
<span data-ttu-id="e72ad-175">A kiosztandó dolgozók száma</span><span class="sxs-lookup"><span data-stu-id="e72ad-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="e72ad-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e72ad-176">-PhpVersion</span></span>
<span data-ttu-id="e72ad-177">Php verzió</span><span class="sxs-lookup"><span data-stu-id="e72ad-177">Php Version</span></span>

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

### <span data-ttu-id="e72ad-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e72ad-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="e72ad-179">Request Tracing Enabled</span><span class="sxs-lookup"><span data-stu-id="e72ad-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="e72ad-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72ad-180">-ResourceGroupName</span></span>
<span data-ttu-id="e72ad-181">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e72ad-181">Resource Group Name</span></span>

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

### <span data-ttu-id="e72ad-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e72ad-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e72ad-183">A 32 bites worker process boolean használata</span><span class="sxs-lookup"><span data-stu-id="e72ad-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="e72ad-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-184">-WebApp</span></span>
<span data-ttu-id="e72ad-185">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="e72ad-185">WebApp Object</span></span>

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

### <span data-ttu-id="e72ad-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e72ad-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="e72ad-187">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="e72ad-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="e72ad-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72ad-188">CommonParameters</span></span>
<span data-ttu-id="e72ad-189">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72ad-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72ad-190">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e72ad-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72ad-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e72ad-191">INPUTS</span></span>

### <span data-ttu-id="e72ad-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e72ad-192">System.Int32</span></span>

### <span data-ttu-id="e72ad-193">System.String</span><span class="sxs-lookup"><span data-stu-id="e72ad-193">System.String</span></span>

### <span data-ttu-id="e72ad-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e72ad-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e72ad-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e72ad-195">OUTPUTS</span></span>

### <span data-ttu-id="e72ad-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e72ad-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e72ad-197">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e72ad-197">NOTES</span></span>
<span data-ttu-id="e72ad-198">Az alábbi parancsmag segítséget nyújt az Azure Web App **DOTNETCORE-hoz való frissítéséhez**</span><span class="sxs-lookup"><span data-stu-id="e72ad-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="e72ad-199">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="e72ad-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="e72ad-200">Cserélje le a Default-Web-WestUS értékeket az erőforráscsoport nevére, a ContosoWebAppra pedig a webapp nevére.</span><span class="sxs-lookup"><span data-stu-id="e72ad-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="e72ad-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e72ad-201">RELATED LINKS</span></span>

[<span data-ttu-id="e72ad-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e72ad-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e72ad-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e72ad-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e72ad-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e72ad-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e72ad-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

