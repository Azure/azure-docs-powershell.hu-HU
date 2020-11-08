---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195128"
---
# <span data-ttu-id="56d78-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="56d78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56d78-102">SYNOPSIS</span></span>
<span data-ttu-id="56d78-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="56d78-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="56d78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56d78-104">SYNTAX</span></span>

### <span data-ttu-id="56d78-105">S1</span><span class="sxs-lookup"><span data-stu-id="56d78-105">S1</span></span>
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

### <span data-ttu-id="56d78-106">S2</span><span class="sxs-lookup"><span data-stu-id="56d78-106">S2</span></span>
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

## <span data-ttu-id="56d78-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="56d78-107">DESCRIPTION</span></span>
<span data-ttu-id="56d78-108">A **set-AzWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="56d78-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="56d78-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56d78-109">EXAMPLES</span></span>

### <span data-ttu-id="56d78-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56d78-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="56d78-111">Ez a parancs megváltoztatja a Slot001 társított appservice-csomagot, az erőforráscsoport alapértelmezett WestUS-webhelyhez társított WebApp ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="56d78-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="56d78-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="56d78-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="56d78-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="56d78-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="56d78-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="56d78-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="56d78-115">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="56d78-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="56d78-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="56d78-116">Example 3</span></span>

<span data-ttu-id="56d78-117">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="56d78-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="56d78-118">autogenerated</span><span class="sxs-lookup"><span data-stu-id="56d78-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="56d78-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56d78-119">PARAMETERS</span></span>

### <span data-ttu-id="56d78-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="56d78-120">-AlwaysOn</span></span>
<span data-ttu-id="56d78-121">Győződjön meg arról, hogy a webalkalmazás minden alkalommal töltődik be, és az üresjárat után nem töltődik be.</span><span class="sxs-lookup"><span data-stu-id="56d78-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="56d78-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="56d78-122">-AppServicePlan</span></span>
<span data-ttu-id="56d78-123">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="56d78-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="56d78-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="56d78-124">-AppSettings</span></span>
<span data-ttu-id="56d78-125">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="56d78-125">App Settings HashTable.</span></span> <span data-ttu-id="56d78-126">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="56d78-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="56d78-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56d78-127">-AsJob</span></span>
<span data-ttu-id="56d78-128">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="56d78-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56d78-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="56d78-129">-AssignIdentity</span></span>
<span data-ttu-id="56d78-130">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="56d78-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="56d78-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="56d78-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="56d78-132">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="56d78-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="56d78-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="56d78-133">-AzureStoragePath</span></span>
<span data-ttu-id="56d78-134">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="56d78-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="56d78-135">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="56d78-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="56d78-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="56d78-136">-ConnectionStrings</span></span>
<span data-ttu-id="56d78-137">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="56d78-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="56d78-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="56d78-138">-ContainerImageName</span></span>
<span data-ttu-id="56d78-139">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="56d78-139">Container Image Name</span></span>

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

### <span data-ttu-id="56d78-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="56d78-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="56d78-141">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="56d78-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="56d78-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="56d78-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="56d78-143">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="56d78-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="56d78-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="56d78-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="56d78-145">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="56d78-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="56d78-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="56d78-146">-DefaultDocuments</span></span>
<span data-ttu-id="56d78-147">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="56d78-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="56d78-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d78-148">-DefaultProfile</span></span>
<span data-ttu-id="56d78-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56d78-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d78-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="56d78-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="56d78-151">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="56d78-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="56d78-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="56d78-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="56d78-153">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="56d78-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="56d78-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="56d78-154">-FtpsState</span></span>
<span data-ttu-id="56d78-155">Egy alkalmazás FTPS-értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="56d78-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="56d78-156">Megengedett értékek [AllAllowed | Letiltva | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="56d78-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="56d78-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="56d78-157">-HandlerMappings</span></span>
<span data-ttu-id="56d78-158">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="56d78-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="56d78-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="56d78-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="56d78-160">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="56d78-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="56d78-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="56d78-161">-HttpsOnly</span></span>
<span data-ttu-id="56d78-162">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="56d78-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="56d78-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="56d78-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="56d78-164">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="56d78-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="56d78-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="56d78-165">-MinTlsVersion</span></span>
<span data-ttu-id="56d78-166">Az SSL-kérelmekhez szükséges TLS minimális verziója.</span><span class="sxs-lookup"><span data-stu-id="56d78-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="56d78-167">Engedélyezett értékek [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="56d78-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="56d78-168">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56d78-168">-Name</span></span>
<span data-ttu-id="56d78-169">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="56d78-169">WebApp Name</span></span>

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

### <span data-ttu-id="56d78-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="56d78-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="56d78-171">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="56d78-171">Net Framework Version</span></span>

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

### <span data-ttu-id="56d78-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="56d78-172">-NumberOfWorkers</span></span>
<span data-ttu-id="56d78-173">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="56d78-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="56d78-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="56d78-174">-PhpVersion</span></span>
<span data-ttu-id="56d78-175">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="56d78-175">Php Version</span></span>

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

### <span data-ttu-id="56d78-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="56d78-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="56d78-177">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="56d78-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="56d78-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d78-178">-ResourceGroupName</span></span>
<span data-ttu-id="56d78-179">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="56d78-179">Resource Group Name</span></span>

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

### <span data-ttu-id="56d78-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="56d78-180">-Slot</span></span>
<span data-ttu-id="56d78-181">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="56d78-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="56d78-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="56d78-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="56d78-183">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="56d78-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="56d78-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="56d78-184">-WebApp</span></span>
<span data-ttu-id="56d78-185">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="56d78-185">WebApp Object</span></span>

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

### <span data-ttu-id="56d78-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="56d78-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="56d78-187">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="56d78-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="56d78-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d78-188">CommonParameters</span></span>
<span data-ttu-id="56d78-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56d78-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d78-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56d78-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d78-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56d78-191">INPUTS</span></span>

### <span data-ttu-id="56d78-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="56d78-192">System.Int32</span></span>

### <span data-ttu-id="56d78-193">System. String</span><span class="sxs-lookup"><span data-stu-id="56d78-193">System.String</span></span>

### <span data-ttu-id="56d78-194">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="56d78-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="56d78-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56d78-195">OUTPUTS</span></span>

### <span data-ttu-id="56d78-196">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="56d78-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="56d78-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56d78-197">NOTES</span></span>

## <span data-ttu-id="56d78-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56d78-198">RELATED LINKS</span></span>

[<span data-ttu-id="56d78-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="56d78-200">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="56d78-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="56d78-202">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="56d78-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="56d78-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56d78-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="56d78-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="56d78-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
