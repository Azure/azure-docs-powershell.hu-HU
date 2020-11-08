---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194847"
---
# <span data-ttu-id="c9c67-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-101">Set-AzWebApp</span></span>

## <span data-ttu-id="c9c67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9c67-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c67-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="c9c67-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="c9c67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9c67-104">SYNTAX</span></span>

### <span data-ttu-id="c9c67-105">S1</span><span class="sxs-lookup"><span data-stu-id="c9c67-105">S1</span></span>
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

### <span data-ttu-id="c9c67-106">S2</span><span class="sxs-lookup"><span data-stu-id="c9c67-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9c67-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9c67-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c67-108">A **set-AzWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="c9c67-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c9c67-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9c67-109">EXAMPLES</span></span>

### <span data-ttu-id="c9c67-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9c67-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c9c67-111">Ez a parancs megváltoztatja az erőforráscsoport alapértelmezett ContosoWebApp társított appservice-tervét – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9c67-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c9c67-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="c9c67-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c9c67-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c9c67-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c9c67-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9c67-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c9c67-115">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c9c67-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="c9c67-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9c67-116">Example 3</span></span>

<span data-ttu-id="c9c67-117">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="c9c67-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="c9c67-118">autogenerated</span><span class="sxs-lookup"><span data-stu-id="c9c67-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="c9c67-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="c9c67-119">Example 4</span></span>

<span data-ttu-id="c9c67-120">Az alábbi példa létrehoz egy myConnectionString a Web App ContosoWebApp nevű kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="c9c67-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="c9c67-121">Ezzel lecseréli az összes létező kapcsolati karakterláncot a Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="c9c67-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="c9c67-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9c67-122">PARAMETERS</span></span>

### <span data-ttu-id="c9c67-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c9c67-123">-AlwaysOn</span></span>
<span data-ttu-id="c9c67-124">Győződjön meg arról, hogy a webalkalmazás minden alkalommal töltődik be, és az üresjárat után nem töltődik be.</span><span class="sxs-lookup"><span data-stu-id="c9c67-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="c9c67-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c9c67-125">-AppServicePlan</span></span>
<span data-ttu-id="c9c67-126">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="c9c67-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="c9c67-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c9c67-127">-AppSettings</span></span>
<span data-ttu-id="c9c67-128">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="c9c67-128">App Settings HashTable.</span></span> <span data-ttu-id="c9c67-129">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="c9c67-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="c9c67-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9c67-130">-AsJob</span></span>
<span data-ttu-id="c9c67-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c9c67-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9c67-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c9c67-132">-AssignIdentity</span></span>
<span data-ttu-id="c9c67-133">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="c9c67-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c9c67-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c9c67-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="c9c67-135">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="c9c67-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c9c67-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c9c67-136">-AzureStoragePath</span></span>
<span data-ttu-id="c9c67-137">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="c9c67-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c9c67-138">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="c9c67-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="c9c67-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c9c67-139">-ConnectionStrings</span></span>
<span data-ttu-id="c9c67-140">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="c9c67-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="c9c67-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c9c67-141">-ContainerImageName</span></span>
<span data-ttu-id="c9c67-142">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="c9c67-142">Container Image Name</span></span>

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

### <span data-ttu-id="c9c67-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c9c67-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c9c67-144">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="c9c67-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c9c67-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c9c67-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c9c67-146">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="c9c67-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c9c67-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c9c67-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="c9c67-148">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="c9c67-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c9c67-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c9c67-149">-DefaultDocuments</span></span>
<span data-ttu-id="c9c67-150">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="c9c67-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="c9c67-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c67-151">-DefaultProfile</span></span>
<span data-ttu-id="c9c67-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9c67-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9c67-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c9c67-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c9c67-154">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="c9c67-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="c9c67-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c9c67-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c9c67-156">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="c9c67-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c9c67-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c9c67-157">-FtpsState</span></span>
<span data-ttu-id="c9c67-158">Egy alkalmazás FTPS-értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="c9c67-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c9c67-159">Megengedett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="c9c67-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="c9c67-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c9c67-160">-HandlerMappings</span></span>
<span data-ttu-id="c9c67-161">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="c9c67-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c9c67-162">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="c9c67-162">-HostNames</span></span>
<span data-ttu-id="c9c67-163">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="c9c67-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="c9c67-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c9c67-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c9c67-165">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="c9c67-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="c9c67-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c9c67-166">-HttpsOnly</span></span>
<span data-ttu-id="c9c67-167">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="c9c67-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c9c67-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c9c67-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="c9c67-169">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="c9c67-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="c9c67-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c9c67-170">-MinTlsVersion</span></span>
<span data-ttu-id="c9c67-171">Az SSL-kérelmekhez szükséges TLS minimális verziója.</span><span class="sxs-lookup"><span data-stu-id="c9c67-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c9c67-172">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="c9c67-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="c9c67-173">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9c67-173">-Name</span></span>
<span data-ttu-id="c9c67-174">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c9c67-174">WebApp Name</span></span>

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

### <span data-ttu-id="c9c67-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c9c67-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="c9c67-176">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="c9c67-176">Net Framework Version</span></span>

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

### <span data-ttu-id="c9c67-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c9c67-177">-NumberOfWorkers</span></span>
<span data-ttu-id="c9c67-178">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="c9c67-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c9c67-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c9c67-179">-PhpVersion</span></span>
<span data-ttu-id="c9c67-180">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="c9c67-180">Php Version</span></span>

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

### <span data-ttu-id="c9c67-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c9c67-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="c9c67-182">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="c9c67-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="c9c67-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c67-183">-ResourceGroupName</span></span>
<span data-ttu-id="c9c67-184">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c9c67-184">Resource Group Name</span></span>

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

### <span data-ttu-id="c9c67-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c9c67-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c9c67-186">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="c9c67-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="c9c67-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-187">-WebApp</span></span>
<span data-ttu-id="c9c67-188">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c9c67-188">WebApp Object</span></span>

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

### <span data-ttu-id="c9c67-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c9c67-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="c9c67-190">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="c9c67-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="c9c67-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c67-191">CommonParameters</span></span>
<span data-ttu-id="c9c67-192">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9c67-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c67-193">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9c67-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c67-194">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c67-194">INPUTS</span></span>

### <span data-ttu-id="c9c67-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c9c67-195">System.Int32</span></span>

### <span data-ttu-id="c9c67-196">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c67-196">System.String</span></span>

### <span data-ttu-id="c9c67-197">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c9c67-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9c67-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c67-198">OUTPUTS</span></span>

### <span data-ttu-id="c9c67-199">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c9c67-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9c67-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9c67-200">NOTES</span></span>
<span data-ttu-id="c9c67-201">A megadott parancsmaggal elérhető parancsmag segítségével az Azure Web App **DOTNETCORE** frissíthetők</span><span class="sxs-lookup"><span data-stu-id="c9c67-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="c9c67-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-"-ResourceType Microsoft. Web/Sites/config-ResourceName" 2018-02-01 ContosoWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="c9c67-203">Cserélje le az alapértelmezett-WestUS értékét az erőforráscsoport nevével és a WebApp ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="c9c67-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="c9c67-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9c67-204">RELATED LINKS</span></span>

[<span data-ttu-id="c9c67-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c9c67-206">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c9c67-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c9c67-208">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c9c67-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c9c67-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9c67-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="c9c67-211">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="c9c67-211">New-AzResource</span></span>](./New-AzResource.md)
