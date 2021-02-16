---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164450"
---
# <span data-ttu-id="a283b-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a283b-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="a283b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a283b-102">SYNOPSIS</span></span>
<span data-ttu-id="a283b-103">Módosít egy Azure Web App-helyet.</span><span class="sxs-lookup"><span data-stu-id="a283b-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="a283b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a283b-104">SYNTAX</span></span>

### <span data-ttu-id="a283b-105">S1</span><span class="sxs-lookup"><span data-stu-id="a283b-105">S1</span></span>
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

### <span data-ttu-id="a283b-106">S2</span><span class="sxs-lookup"><span data-stu-id="a283b-106">S2</span></span>
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

## <span data-ttu-id="a283b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a283b-107">DESCRIPTION</span></span>
<span data-ttu-id="a283b-108">A **Set-AzWebApp parancsmag** beállít egy Azure Web App Slotot.</span><span class="sxs-lookup"><span data-stu-id="a283b-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="a283b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a283b-109">EXAMPLES</span></span>

### <span data-ttu-id="a283b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a283b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="a283b-111">Ez a parancs módosítja a Slot001 alkalmazásszolgáltatási tervét a Default-Web-WestUS erőforráscsoporthoz társított ContosoWebApp webappban.</span><span class="sxs-lookup"><span data-stu-id="a283b-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="a283b-112">A hivatkozásra kattintva további információt olvashat az appszolgáltatási terv és a hozzá tartozó korlátozások módosításáról.</span><span class="sxs-lookup"><span data-stu-id="a283b-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="a283b-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="a283b-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="a283b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a283b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="a283b-115">Ez a parancs a HttpLoggingEnabled értéket igazra állítja a Default-Web-WestUS erőforráscsoporthoz társított Web App ContosoWebApphoz tartozó Slot Slot001 esetén</span><span class="sxs-lookup"><span data-stu-id="a283b-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="a283b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a283b-116">Example 3</span></span>

<span data-ttu-id="a283b-117">Módosít egy Azure Web App-helyet.</span><span class="sxs-lookup"><span data-stu-id="a283b-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="a283b-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="a283b-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="a283b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a283b-119">PARAMETERS</span></span>

### <span data-ttu-id="a283b-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="a283b-120">-AlwaysOn</span></span>
<span data-ttu-id="a283b-121">Gondoskodjon arról, hogy a webalkalmazás mindig betöltődik, és ne legyen eltávolítva, miután inaktív volt.</span><span class="sxs-lookup"><span data-stu-id="a283b-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="a283b-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a283b-122">-AppServicePlan</span></span>
<span data-ttu-id="a283b-123">Appszolgáltatás-terv neve</span><span class="sxs-lookup"><span data-stu-id="a283b-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="a283b-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a283b-124">-AppSettings</span></span>
<span data-ttu-id="a283b-125">App Settings HashTable.</span><span class="sxs-lookup"><span data-stu-id="a283b-125">App Settings HashTable.</span></span> <span data-ttu-id="a283b-126">A rendszer lecseréli a meglévő alkalmazásbeállításokat, és eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="a283b-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="a283b-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a283b-127">-AsJob</span></span>
<span data-ttu-id="a283b-128">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a283b-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a283b-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a283b-129">-AssignIdentity</span></span>
<span data-ttu-id="a283b-130">Az MSI engedélyezése/letiltása meglévő tárolóhelyen [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="a283b-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="a283b-131">-AutoSwapSzajName</span><span class="sxs-lookup"><span data-stu-id="a283b-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="a283b-132">Célhely neve az automatikus felcseréléshez</span><span class="sxs-lookup"><span data-stu-id="a283b-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="a283b-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a283b-133">-AzureStoragePath</span></span>
<span data-ttu-id="a283b-134">Azure Storage, amely egy tárolóhoz való webalkalmazásba csatolható.</span><span class="sxs-lookup"><span data-stu-id="a283b-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="a283b-135">A New-AzureRmWebAppAzureStoragePath létrehozása</span><span class="sxs-lookup"><span data-stu-id="a283b-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="a283b-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="a283b-136">-ConnectionStrings</span></span>
<span data-ttu-id="a283b-137">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="a283b-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="a283b-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="a283b-138">-ContainerImageName</span></span>
<span data-ttu-id="a283b-139">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="a283b-139">Container Image Name</span></span>

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

### <span data-ttu-id="a283b-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="a283b-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="a283b-141">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="a283b-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="a283b-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="a283b-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="a283b-143">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="a283b-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="a283b-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="a283b-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="a283b-145">Private Container Registry Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="a283b-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="a283b-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a283b-146">-DefaultDocuments</span></span>
<span data-ttu-id="a283b-147">Default Documents String Array</span><span class="sxs-lookup"><span data-stu-id="a283b-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="a283b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a283b-148">-DefaultProfile</span></span>
<span data-ttu-id="a283b-149">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a283b-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a283b-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a283b-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="a283b-151">Részletes hibanaplózás engedélyezése logikai</span><span class="sxs-lookup"><span data-stu-id="a283b-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="a283b-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="a283b-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="a283b-153">Engedélyezi/letiltja a tároló folyamatos üzembe helyezését webhook</span><span class="sxs-lookup"><span data-stu-id="a283b-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="a283b-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="a283b-154">-FtpsState</span></span>
<span data-ttu-id="a283b-155">Adja meg egy alkalmazás Ftps state (Ftps állapota) értékét.</span><span class="sxs-lookup"><span data-stu-id="a283b-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="a283b-156">Engedélyezett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="a283b-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="a283b-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a283b-157">-HandlerMappings</span></span>
<span data-ttu-id="a283b-158">Handler Mappings IList</span><span class="sxs-lookup"><span data-stu-id="a283b-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="a283b-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a283b-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="a283b-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a283b-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="a283b-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a283b-161">-HttpsOnly</span></span>
<span data-ttu-id="a283b-162">Az összes adatforgalom HTTPS-re való átirányításának engedélyezése/letiltása egy meglévő tárolóhelyen</span><span class="sxs-lookup"><span data-stu-id="a283b-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="a283b-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a283b-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="a283b-164">Felügyelt folyamat mód neve</span><span class="sxs-lookup"><span data-stu-id="a283b-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="a283b-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a283b-165">-MinTlsVersion</span></span>
<span data-ttu-id="a283b-166">Az SSL-kérelmekhez minimálisan szükséges TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="a283b-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="a283b-167">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="a283b-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="a283b-168">-Name</span><span class="sxs-lookup"><span data-stu-id="a283b-168">-Name</span></span>
<span data-ttu-id="a283b-169">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a283b-169">WebApp Name</span></span>

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

### <span data-ttu-id="a283b-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a283b-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="a283b-171">Net-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="a283b-171">Net Framework Version</span></span>

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

### <span data-ttu-id="a283b-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a283b-172">-NumberOfWorkers</span></span>
<span data-ttu-id="a283b-173">A kiosztandó dolgozók száma</span><span class="sxs-lookup"><span data-stu-id="a283b-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="a283b-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a283b-174">-PhpVersion</span></span>
<span data-ttu-id="a283b-175">Php verzió</span><span class="sxs-lookup"><span data-stu-id="a283b-175">Php Version</span></span>

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

### <span data-ttu-id="a283b-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a283b-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="a283b-177">Request Tracing Enabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a283b-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="a283b-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a283b-178">-ResourceGroupName</span></span>
<span data-ttu-id="a283b-179">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a283b-179">Resource Group Name</span></span>

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

### <span data-ttu-id="a283b-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="a283b-180">-Slot</span></span>
<span data-ttu-id="a283b-181">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="a283b-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a283b-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a283b-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="a283b-183">A 32 bites worker process boolean használata</span><span class="sxs-lookup"><span data-stu-id="a283b-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="a283b-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a283b-184">-WebApp</span></span>
<span data-ttu-id="a283b-185">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="a283b-185">WebApp Object</span></span>

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

### <span data-ttu-id="a283b-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a283b-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="a283b-187">Web Sockets Enabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a283b-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="a283b-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a283b-188">CommonParameters</span></span>
<span data-ttu-id="a283b-189">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a283b-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a283b-190">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a283b-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a283b-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a283b-191">INPUTS</span></span>

### <span data-ttu-id="a283b-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a283b-192">System.Int32</span></span>

### <span data-ttu-id="a283b-193">System.String</span><span class="sxs-lookup"><span data-stu-id="a283b-193">System.String</span></span>

### <span data-ttu-id="a283b-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a283b-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a283b-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a283b-195">OUTPUTS</span></span>

### <span data-ttu-id="a283b-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a283b-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a283b-197">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a283b-197">NOTES</span></span>

## <span data-ttu-id="a283b-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a283b-198">RELATED LINKS</span></span>

[<span data-ttu-id="a283b-199">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a283b-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a283b-200">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="a283b-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="a283b-201">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a283b-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="a283b-202">Restart-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a283b-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="a283b-203">Start-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a283b-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="a283b-204">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a283b-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="a283b-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a283b-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
