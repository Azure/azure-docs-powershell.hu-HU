---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012601"
---
# <span data-ttu-id="c2b12-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="c2b12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2b12-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b12-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="c2b12-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="c2b12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2b12-104">SYNTAX</span></span>

### <span data-ttu-id="c2b12-105">S1</span><span class="sxs-lookup"><span data-stu-id="c2b12-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2b12-106">S2</span><span class="sxs-lookup"><span data-stu-id="c2b12-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b12-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2b12-107">DESCRIPTION</span></span>
<span data-ttu-id="c2b12-108">A **set-AzWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="c2b12-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="c2b12-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2b12-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b12-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c2b12-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c2b12-111">Ez a parancs megváltoztatja a Slot001 társított appservice-csomagot, az erőforráscsoport alapértelmezett WestUS-webhelyhez társított WebApp ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="c2b12-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c2b12-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="c2b12-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c2b12-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c2b12-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c2b12-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c2b12-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="c2b12-115">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c2b12-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c2b12-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2b12-116">PARAMETERS</span></span>

### <span data-ttu-id="c2b12-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c2b12-117">-AlwaysOn</span></span>
<span data-ttu-id="c2b12-118">Győződjön meg arról, hogy a webalkalmazás minden alkalommal töltődik be, és az üresjárat után nem töltődik be.</span><span class="sxs-lookup"><span data-stu-id="c2b12-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="c2b12-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2b12-119">-AppServicePlan</span></span>
<span data-ttu-id="c2b12-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="c2b12-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c2b12-121">-AppSettings</span></span>
<span data-ttu-id="c2b12-122">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="c2b12-122">App Settings HashTable.</span></span> <span data-ttu-id="c2b12-123">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="c2b12-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2b12-124">-AsJob</span></span>
<span data-ttu-id="c2b12-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2b12-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2b12-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c2b12-126">-AssignIdentity</span></span>
<span data-ttu-id="c2b12-127">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="c2b12-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="c2b12-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c2b12-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="c2b12-129">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="c2b12-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c2b12-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c2b12-130">-AzureStoragePath</span></span>
<span data-ttu-id="c2b12-131">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="c2b12-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c2b12-132">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="c2b12-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="c2b12-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c2b12-133">-ConnectionStrings</span></span>
<span data-ttu-id="c2b12-134">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="c2b12-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c2b12-135">-ContainerImageName</span></span>
<span data-ttu-id="c2b12-136">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="c2b12-136">Container Image Name</span></span>

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

### <span data-ttu-id="c2b12-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c2b12-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c2b12-138">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="c2b12-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c2b12-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c2b12-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c2b12-140">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="c2b12-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c2b12-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c2b12-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="c2b12-142">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="c2b12-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c2b12-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c2b12-143">-DefaultDocuments</span></span>
<span data-ttu-id="c2b12-144">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="c2b12-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b12-145">-DefaultProfile</span></span>
<span data-ttu-id="c2b12-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2b12-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b12-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c2b12-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c2b12-148">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="c2b12-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c2b12-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c2b12-150">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="c2b12-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c2b12-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c2b12-151">-FtpsState</span></span>
<span data-ttu-id="c2b12-152">Egy alkalmazás FTPS-értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="c2b12-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c2b12-153">Megengedett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="c2b12-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="c2b12-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c2b12-154">-HandlerMappings</span></span>
<span data-ttu-id="c2b12-155">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="c2b12-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c2b12-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c2b12-157">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="c2b12-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c2b12-158">-HttpsOnly</span></span>
<span data-ttu-id="c2b12-159">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="c2b12-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="c2b12-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c2b12-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="c2b12-161">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="c2b12-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c2b12-162">-MinTlsVersion</span></span>
<span data-ttu-id="c2b12-163">Az SSL-kérelmekhez szükséges TLS minimális verziója.</span><span class="sxs-lookup"><span data-stu-id="c2b12-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c2b12-164">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="c2b12-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="c2b12-165">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2b12-165">-Name</span></span>
<span data-ttu-id="c2b12-166">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c2b12-166">WebApp Name</span></span>

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

### <span data-ttu-id="c2b12-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c2b12-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="c2b12-168">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="c2b12-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c2b12-169">-NumberOfWorkers</span></span>
<span data-ttu-id="c2b12-170">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="c2b12-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c2b12-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c2b12-171">-PhpVersion</span></span>
<span data-ttu-id="c2b12-172">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="c2b12-172">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c2b12-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="c2b12-174">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="c2b12-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b12-175">-ResourceGroupName</span></span>
<span data-ttu-id="c2b12-176">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c2b12-176">Resource Group Name</span></span>

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

### <span data-ttu-id="c2b12-177">-Slot</span><span class="sxs-lookup"><span data-stu-id="c2b12-177">-Slot</span></span>
<span data-ttu-id="c2b12-178">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c2b12-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c2b12-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c2b12-180">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="c2b12-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b12-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c2b12-181">-WebApp</span></span>
<span data-ttu-id="c2b12-182">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c2b12-182">WebApp Object</span></span>

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

### <span data-ttu-id="c2b12-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c2b12-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="c2b12-184">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="c2b12-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="c2b12-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b12-185">CommonParameters</span></span>
<span data-ttu-id="c2b12-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2b12-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b12-187">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c2b12-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b12-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2b12-188">INPUTS</span></span>

### <span data-ttu-id="c2b12-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2b12-189">System.Int32</span></span>

### <span data-ttu-id="c2b12-190">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b12-190">System.String</span></span>

### <span data-ttu-id="c2b12-191">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c2b12-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c2b12-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2b12-192">OUTPUTS</span></span>

### <span data-ttu-id="c2b12-193">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c2b12-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c2b12-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2b12-194">NOTES</span></span>

## <span data-ttu-id="c2b12-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2b12-195">RELATED LINKS</span></span>

[<span data-ttu-id="c2b12-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c2b12-197">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c2b12-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c2b12-199">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c2b12-200">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c2b12-201">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2b12-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c2b12-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2b12-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
