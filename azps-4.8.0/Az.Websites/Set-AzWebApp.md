---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025005"
---
# <span data-ttu-id="8241c-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-101">Set-AzWebApp</span></span>

## <span data-ttu-id="8241c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8241c-102">SYNOPSIS</span></span>
<span data-ttu-id="8241c-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="8241c-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="8241c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8241c-104">SYNTAX</span></span>

### <span data-ttu-id="8241c-105">S1</span><span class="sxs-lookup"><span data-stu-id="8241c-105">S1</span></span>
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

### <span data-ttu-id="8241c-106">S2</span><span class="sxs-lookup"><span data-stu-id="8241c-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8241c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8241c-107">DESCRIPTION</span></span>
<span data-ttu-id="8241c-108">A **set-AzWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="8241c-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="8241c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8241c-109">EXAMPLES</span></span>

### <span data-ttu-id="8241c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8241c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="8241c-111">Ez a parancs megváltoztatja az erőforráscsoport alapértelmezett ContosoWebApp társított appservice-tervét – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8241c-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="8241c-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="8241c-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="8241c-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="8241c-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="8241c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8241c-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="8241c-115">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="8241c-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="8241c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="8241c-116">Example 3</span></span>

<span data-ttu-id="8241c-117">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="8241c-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="8241c-118">autogenerated</span><span class="sxs-lookup"><span data-stu-id="8241c-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="8241c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8241c-119">PARAMETERS</span></span>

### <span data-ttu-id="8241c-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="8241c-120">-AlwaysOn</span></span>
<span data-ttu-id="8241c-121">Győződjön meg arról, hogy a webalkalmazás minden alkalommal töltődik be, és az üresjárat után nem töltődik be.</span><span class="sxs-lookup"><span data-stu-id="8241c-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="8241c-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8241c-122">-AppServicePlan</span></span>
<span data-ttu-id="8241c-123">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="8241c-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="8241c-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="8241c-124">-AppSettings</span></span>
<span data-ttu-id="8241c-125">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="8241c-125">App Settings HashTable.</span></span> <span data-ttu-id="8241c-126">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="8241c-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="8241c-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8241c-127">-AsJob</span></span>
<span data-ttu-id="8241c-128">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8241c-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8241c-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8241c-129">-AssignIdentity</span></span>
<span data-ttu-id="8241c-130">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="8241c-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="8241c-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8241c-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="8241c-132">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="8241c-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="8241c-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8241c-133">-AzureStoragePath</span></span>
<span data-ttu-id="8241c-134">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="8241c-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="8241c-135">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="8241c-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="8241c-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8241c-136">-ConnectionStrings</span></span>
<span data-ttu-id="8241c-137">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="8241c-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="8241c-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8241c-138">-ContainerImageName</span></span>
<span data-ttu-id="8241c-139">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="8241c-139">Container Image Name</span></span>

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

### <span data-ttu-id="8241c-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8241c-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8241c-141">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="8241c-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8241c-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8241c-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8241c-143">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="8241c-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8241c-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8241c-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="8241c-145">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="8241c-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8241c-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8241c-146">-DefaultDocuments</span></span>
<span data-ttu-id="8241c-147">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="8241c-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="8241c-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8241c-148">-DefaultProfile</span></span>
<span data-ttu-id="8241c-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8241c-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8241c-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8241c-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8241c-151">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="8241c-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="8241c-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8241c-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8241c-153">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="8241c-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8241c-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="8241c-154">-FtpsState</span></span>
<span data-ttu-id="8241c-155">Egy alkalmazás FTPS-értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="8241c-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="8241c-156">Megengedett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="8241c-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="8241c-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8241c-157">-HandlerMappings</span></span>
<span data-ttu-id="8241c-158">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="8241c-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="8241c-159">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="8241c-159">-HostNames</span></span>
<span data-ttu-id="8241c-160">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="8241c-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="8241c-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8241c-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8241c-162">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="8241c-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="8241c-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8241c-163">-HttpsOnly</span></span>
<span data-ttu-id="8241c-164">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="8241c-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="8241c-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8241c-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="8241c-166">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="8241c-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="8241c-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8241c-167">-MinTlsVersion</span></span>
<span data-ttu-id="8241c-168">Az SSL-kérelmekhez szükséges TLS minimális verziója.</span><span class="sxs-lookup"><span data-stu-id="8241c-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="8241c-169">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="8241c-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="8241c-170">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8241c-170">-Name</span></span>
<span data-ttu-id="8241c-171">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="8241c-171">WebApp Name</span></span>

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

### <span data-ttu-id="8241c-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8241c-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="8241c-173">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="8241c-173">Net Framework Version</span></span>

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

### <span data-ttu-id="8241c-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="8241c-174">-NumberOfWorkers</span></span>
<span data-ttu-id="8241c-175">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="8241c-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8241c-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8241c-176">-PhpVersion</span></span>
<span data-ttu-id="8241c-177">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="8241c-177">Php Version</span></span>

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

### <span data-ttu-id="8241c-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8241c-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="8241c-179">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8241c-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="8241c-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8241c-180">-ResourceGroupName</span></span>
<span data-ttu-id="8241c-181">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8241c-181">Resource Group Name</span></span>

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

### <span data-ttu-id="8241c-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8241c-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8241c-183">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="8241c-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="8241c-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-184">-WebApp</span></span>
<span data-ttu-id="8241c-185">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="8241c-185">WebApp Object</span></span>

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

### <span data-ttu-id="8241c-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8241c-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="8241c-187">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="8241c-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="8241c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8241c-188">CommonParameters</span></span>
<span data-ttu-id="8241c-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8241c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8241c-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8241c-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8241c-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8241c-191">INPUTS</span></span>

### <span data-ttu-id="8241c-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8241c-192">System.Int32</span></span>

### <span data-ttu-id="8241c-193">System. String</span><span class="sxs-lookup"><span data-stu-id="8241c-193">System.String</span></span>

### <span data-ttu-id="8241c-194">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8241c-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8241c-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8241c-195">OUTPUTS</span></span>

### <span data-ttu-id="8241c-196">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8241c-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8241c-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8241c-197">NOTES</span></span>
<span data-ttu-id="8241c-198">A megadott parancsmaggal elérhető parancsmag segítségével az Azure Web App **DOTNETCORE** frissíthetők</span><span class="sxs-lookup"><span data-stu-id="8241c-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="8241c-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-"-ResourceType Microsoft. Web/Sites/config-ResourceName" 2018-02-01 ContosoWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="8241c-200">Cserélje le az alapértelmezett-WestUS értékét az erőforráscsoport nevével és a WebApp ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="8241c-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="8241c-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8241c-201">RELATED LINKS</span></span>

[<span data-ttu-id="8241c-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8241c-203">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8241c-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8241c-205">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8241c-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8241c-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8241c-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="8241c-208">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="8241c-208">New-AzResource</span></span>](./New-AzResource.md)
