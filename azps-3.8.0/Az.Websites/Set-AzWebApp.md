---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012902"
---
# <span data-ttu-id="353d6-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-101">Set-AzWebApp</span></span>

## <span data-ttu-id="353d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="353d6-102">SYNOPSIS</span></span>
<span data-ttu-id="353d6-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="353d6-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="353d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="353d6-104">SYNTAX</span></span>

### <span data-ttu-id="353d6-105">S1</span><span class="sxs-lookup"><span data-stu-id="353d6-105">S1</span></span>
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

### <span data-ttu-id="353d6-106">S2</span><span class="sxs-lookup"><span data-stu-id="353d6-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="353d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="353d6-107">DESCRIPTION</span></span>
<span data-ttu-id="353d6-108">A **set-AzWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="353d6-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="353d6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="353d6-109">EXAMPLES</span></span>

### <span data-ttu-id="353d6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="353d6-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="353d6-111">Ez a parancs megváltoztatja az erőforráscsoport alapértelmezett ContosoWebApp társított appservice-tervét – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="353d6-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="353d6-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="353d6-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="353d6-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="353d6-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="353d6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="353d6-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="353d6-115">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="353d6-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="353d6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="353d6-116">PARAMETERS</span></span>

### <span data-ttu-id="353d6-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="353d6-117">-AlwaysOn</span></span>
<span data-ttu-id="353d6-118">Győződjön meg arról, hogy a webalkalmazás minden alkalommal töltődik be, és az üresjárat után nem töltődik be.</span><span class="sxs-lookup"><span data-stu-id="353d6-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="353d6-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="353d6-119">-AppServicePlan</span></span>
<span data-ttu-id="353d6-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="353d6-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="353d6-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="353d6-121">-AppSettings</span></span>
<span data-ttu-id="353d6-122">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="353d6-122">App Settings HashTable.</span></span> <span data-ttu-id="353d6-123">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="353d6-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="353d6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="353d6-124">-AsJob</span></span>
<span data-ttu-id="353d6-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="353d6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="353d6-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="353d6-126">-AssignIdentity</span></span>
<span data-ttu-id="353d6-127">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="353d6-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="353d6-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="353d6-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="353d6-129">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="353d6-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="353d6-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="353d6-130">-AzureStoragePath</span></span>
<span data-ttu-id="353d6-131">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="353d6-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="353d6-132">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="353d6-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="353d6-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="353d6-133">-ConnectionStrings</span></span>
<span data-ttu-id="353d6-134">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="353d6-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="353d6-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="353d6-135">-ContainerImageName</span></span>
<span data-ttu-id="353d6-136">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="353d6-136">Container Image Name</span></span>

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

### <span data-ttu-id="353d6-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="353d6-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="353d6-138">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="353d6-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="353d6-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="353d6-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="353d6-140">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="353d6-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="353d6-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="353d6-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="353d6-142">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="353d6-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="353d6-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="353d6-143">-DefaultDocuments</span></span>
<span data-ttu-id="353d6-144">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="353d6-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="353d6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353d6-145">-DefaultProfile</span></span>
<span data-ttu-id="353d6-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="353d6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="353d6-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="353d6-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="353d6-148">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="353d6-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="353d6-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="353d6-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="353d6-150">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="353d6-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="353d6-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="353d6-151">-FtpsState</span></span>
<span data-ttu-id="353d6-152">Egy alkalmazás FTPS-értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="353d6-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="353d6-153">Megengedett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="353d6-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="353d6-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="353d6-154">-HandlerMappings</span></span>
<span data-ttu-id="353d6-155">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="353d6-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="353d6-156">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="353d6-156">-HostNames</span></span>
<span data-ttu-id="353d6-157">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="353d6-157">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="353d6-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="353d6-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="353d6-159">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="353d6-159">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="353d6-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="353d6-160">-HttpsOnly</span></span>
<span data-ttu-id="353d6-161">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="353d6-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="353d6-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="353d6-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="353d6-163">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="353d6-163">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="353d6-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="353d6-164">-MinTlsVersion</span></span>
<span data-ttu-id="353d6-165">Az SSL-kérelmekhez szükséges TLS minimális verziója.</span><span class="sxs-lookup"><span data-stu-id="353d6-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="353d6-166">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="353d6-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="353d6-167">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="353d6-167">-Name</span></span>
<span data-ttu-id="353d6-168">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="353d6-168">WebApp Name</span></span>

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

### <span data-ttu-id="353d6-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="353d6-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="353d6-170">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="353d6-170">Net Framework Version</span></span>

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

### <span data-ttu-id="353d6-171">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="353d6-171">-NumberOfWorkers</span></span>
<span data-ttu-id="353d6-172">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="353d6-172">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="353d6-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="353d6-173">-PhpVersion</span></span>
<span data-ttu-id="353d6-174">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="353d6-174">Php Version</span></span>

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

### <span data-ttu-id="353d6-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="353d6-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="353d6-176">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="353d6-176">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="353d6-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="353d6-177">-ResourceGroupName</span></span>
<span data-ttu-id="353d6-178">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="353d6-178">Resource Group Name</span></span>

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

### <span data-ttu-id="353d6-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="353d6-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="353d6-180">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="353d6-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="353d6-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-181">-WebApp</span></span>
<span data-ttu-id="353d6-182">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="353d6-182">WebApp Object</span></span>

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

### <span data-ttu-id="353d6-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="353d6-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="353d6-184">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="353d6-184">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="353d6-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353d6-185">CommonParameters</span></span>
<span data-ttu-id="353d6-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="353d6-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353d6-187">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="353d6-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353d6-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="353d6-188">INPUTS</span></span>

### <span data-ttu-id="353d6-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="353d6-189">System.Int32</span></span>

### <span data-ttu-id="353d6-190">System. String</span><span class="sxs-lookup"><span data-stu-id="353d6-190">System.String</span></span>

### <span data-ttu-id="353d6-191">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="353d6-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="353d6-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="353d6-192">OUTPUTS</span></span>

### <span data-ttu-id="353d6-193">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="353d6-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="353d6-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="353d6-194">NOTES</span></span>

## <span data-ttu-id="353d6-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="353d6-195">RELATED LINKS</span></span>

[<span data-ttu-id="353d6-196">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="353d6-197">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="353d6-198">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="353d6-199">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="353d6-200">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="353d6-201">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="353d6-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
