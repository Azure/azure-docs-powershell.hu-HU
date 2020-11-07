---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839754"
---
# <span data-ttu-id="3496e-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-101">Set-AzWebApp</span></span>

## <span data-ttu-id="3496e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3496e-102">SYNOPSIS</span></span>
<span data-ttu-id="3496e-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="3496e-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="3496e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3496e-104">SYNTAX</span></span>

### <span data-ttu-id="3496e-105">S1</span><span class="sxs-lookup"><span data-stu-id="3496e-105">S1</span></span>
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
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3496e-106">S2</span><span class="sxs-lookup"><span data-stu-id="3496e-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3496e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3496e-107">DESCRIPTION</span></span>
<span data-ttu-id="3496e-108">A **set-AzWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="3496e-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="3496e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3496e-109">EXAMPLES</span></span>

### <span data-ttu-id="3496e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3496e-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="3496e-111">Ez a parancs megváltoztatja az erőforráscsoport alapértelmezett ContosoWebApp társított appservice-tervét – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3496e-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3496e-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="3496e-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="3496e-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="3496e-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="3496e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3496e-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="3496e-115">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="3496e-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3496e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3496e-116">PARAMETERS</span></span>

### <span data-ttu-id="3496e-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3496e-117">-AppServicePlan</span></span>
<span data-ttu-id="3496e-118">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="3496e-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="3496e-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3496e-119">-AppSettings</span></span>
<span data-ttu-id="3496e-120">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="3496e-120">App Settings HashTable.</span></span> <span data-ttu-id="3496e-121">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="3496e-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="3496e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3496e-122">-AsJob</span></span>
<span data-ttu-id="3496e-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3496e-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3496e-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3496e-124">-AssignIdentity</span></span>
<span data-ttu-id="3496e-125">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="3496e-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="3496e-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3496e-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="3496e-127">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="3496e-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3496e-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="3496e-128">-AzureStoragePath</span></span>
<span data-ttu-id="3496e-129">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="3496e-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="3496e-130">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="3496e-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="3496e-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3496e-131">-ConnectionStrings</span></span>
<span data-ttu-id="3496e-132">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="3496e-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3496e-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="3496e-133">-ContainerImageName</span></span>
<span data-ttu-id="3496e-134">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="3496e-134">Container Image Name</span></span>

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

### <span data-ttu-id="3496e-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="3496e-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="3496e-136">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="3496e-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="3496e-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="3496e-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="3496e-138">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="3496e-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="3496e-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="3496e-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="3496e-140">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="3496e-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="3496e-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="3496e-141">-DefaultDocuments</span></span>
<span data-ttu-id="3496e-142">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="3496e-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="3496e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3496e-143">-DefaultProfile</span></span>
<span data-ttu-id="3496e-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3496e-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3496e-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3496e-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3496e-146">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="3496e-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3496e-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="3496e-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="3496e-148">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="3496e-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="3496e-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3496e-149">-HandlerMappings</span></span>
<span data-ttu-id="3496e-150">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="3496e-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3496e-151">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="3496e-151">-HostNames</span></span>
<span data-ttu-id="3496e-152">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="3496e-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="3496e-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3496e-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3496e-154">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="3496e-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3496e-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3496e-155">-HttpsOnly</span></span>
<span data-ttu-id="3496e-156">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="3496e-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="3496e-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3496e-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="3496e-158">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="3496e-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3496e-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3496e-159">-Name</span></span>
<span data-ttu-id="3496e-160">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="3496e-160">WebApp Name</span></span>

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

### <span data-ttu-id="3496e-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3496e-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="3496e-162">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="3496e-162">Net Framework Version</span></span>

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

### <span data-ttu-id="3496e-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3496e-163">-NumberOfWorkers</span></span>
<span data-ttu-id="3496e-164">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="3496e-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3496e-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3496e-165">-PhpVersion</span></span>
<span data-ttu-id="3496e-166">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="3496e-166">Php Version</span></span>

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

### <span data-ttu-id="3496e-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3496e-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="3496e-168">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="3496e-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="3496e-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3496e-169">-ResourceGroupName</span></span>
<span data-ttu-id="3496e-170">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3496e-170">Resource Group Name</span></span>

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

### <span data-ttu-id="3496e-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3496e-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3496e-172">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="3496e-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3496e-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-173">-WebApp</span></span>
<span data-ttu-id="3496e-174">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="3496e-174">WebApp Object</span></span>

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

### <span data-ttu-id="3496e-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3496e-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="3496e-176">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="3496e-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="3496e-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3496e-177">CommonParameters</span></span>
<span data-ttu-id="3496e-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3496e-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3496e-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3496e-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3496e-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3496e-180">INPUTS</span></span>

### <span data-ttu-id="3496e-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3496e-181">System.Int32</span></span>

### <span data-ttu-id="3496e-182">System. String</span><span class="sxs-lookup"><span data-stu-id="3496e-182">System.String</span></span>

### <span data-ttu-id="3496e-183">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3496e-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3496e-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3496e-184">OUTPUTS</span></span>

### <span data-ttu-id="3496e-185">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3496e-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3496e-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3496e-186">NOTES</span></span>

## <span data-ttu-id="3496e-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3496e-187">RELATED LINKS</span></span>

[<span data-ttu-id="3496e-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3496e-189">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3496e-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3496e-191">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3496e-192">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3496e-193">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3496e-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
