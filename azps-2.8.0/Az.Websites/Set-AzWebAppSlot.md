---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840049"
---
# <span data-ttu-id="d29a2-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="d29a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d29a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d29a2-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="d29a2-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="d29a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d29a2-104">SYNTAX</span></span>

### <span data-ttu-id="d29a2-105">S1</span><span class="sxs-lookup"><span data-stu-id="d29a2-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29a2-106">S2</span><span class="sxs-lookup"><span data-stu-id="d29a2-106">S2</span></span>
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

## <span data-ttu-id="d29a2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d29a2-107">DESCRIPTION</span></span>
<span data-ttu-id="d29a2-108">A **set-AzWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="d29a2-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="d29a2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d29a2-109">EXAMPLES</span></span>

### <span data-ttu-id="d29a2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d29a2-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="d29a2-111">Ez a parancs megváltoztatja a Slot001 társított appservice-csomagot, az erőforráscsoport alapértelmezett WestUS-webhelyhez társított WebApp ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="d29a2-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d29a2-112">A hivatkozás használatával többet is megtudhat a appservice-terv és a hozzájuk kapcsolódó kényszerek módosításáról.</span><span class="sxs-lookup"><span data-stu-id="d29a2-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="d29a2-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="d29a2-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="d29a2-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d29a2-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="d29a2-115">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="d29a2-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d29a2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d29a2-116">PARAMETERS</span></span>

### <span data-ttu-id="d29a2-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d29a2-117">-AppServicePlan</span></span>
<span data-ttu-id="d29a2-118">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="d29a2-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="d29a2-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d29a2-119">-AppSettings</span></span>
<span data-ttu-id="d29a2-120">Az app beállításai HashTable.</span><span class="sxs-lookup"><span data-stu-id="d29a2-120">App Settings HashTable.</span></span> <span data-ttu-id="d29a2-121">A meglévő alkalmazás-beállításokat a program lecseréli, majd eltávolítja a nem megadott beállításokat.</span><span class="sxs-lookup"><span data-stu-id="d29a2-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="d29a2-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d29a2-122">-AsJob</span></span>
<span data-ttu-id="d29a2-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d29a2-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d29a2-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d29a2-124">-AssignIdentity</span></span>
<span data-ttu-id="d29a2-125">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="d29a2-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="d29a2-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d29a2-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="d29a2-127">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="d29a2-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="d29a2-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d29a2-128">-AzureStoragePath</span></span>
<span data-ttu-id="d29a2-129">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="d29a2-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="d29a2-130">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="d29a2-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="d29a2-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d29a2-131">-ConnectionStrings</span></span>
<span data-ttu-id="d29a2-132">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="d29a2-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="d29a2-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d29a2-133">-ContainerImageName</span></span>
<span data-ttu-id="d29a2-134">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="d29a2-134">Container Image Name</span></span>

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

### <span data-ttu-id="d29a2-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d29a2-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="d29a2-136">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="d29a2-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="d29a2-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d29a2-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="d29a2-138">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="d29a2-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="d29a2-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d29a2-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="d29a2-140">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="d29a2-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="d29a2-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="d29a2-141">-DefaultDocuments</span></span>
<span data-ttu-id="d29a2-142">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="d29a2-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="d29a2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29a2-143">-DefaultProfile</span></span>
<span data-ttu-id="d29a2-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d29a2-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29a2-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d29a2-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="d29a2-146">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="d29a2-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="d29a2-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d29a2-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="d29a2-148">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="d29a2-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="d29a2-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d29a2-149">-HandlerMappings</span></span>
<span data-ttu-id="d29a2-150">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="d29a2-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="d29a2-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d29a2-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="d29a2-152">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="d29a2-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="d29a2-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d29a2-153">-HttpsOnly</span></span>
<span data-ttu-id="d29a2-154">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="d29a2-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="d29a2-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d29a2-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="d29a2-156">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="d29a2-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="d29a2-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d29a2-157">-Name</span></span>
<span data-ttu-id="d29a2-158">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d29a2-158">WebApp Name</span></span>

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

### <span data-ttu-id="d29a2-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d29a2-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="d29a2-160">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="d29a2-160">Net Framework Version</span></span>

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

### <span data-ttu-id="d29a2-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d29a2-161">-NumberOfWorkers</span></span>
<span data-ttu-id="d29a2-162">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="d29a2-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="d29a2-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d29a2-163">-PhpVersion</span></span>
<span data-ttu-id="d29a2-164">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="d29a2-164">Php Version</span></span>

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

### <span data-ttu-id="d29a2-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d29a2-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="d29a2-166">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="d29a2-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="d29a2-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d29a2-167">-ResourceGroupName</span></span>
<span data-ttu-id="d29a2-168">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d29a2-168">Resource Group Name</span></span>

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

### <span data-ttu-id="d29a2-169">-Slot</span><span class="sxs-lookup"><span data-stu-id="d29a2-169">-Slot</span></span>
<span data-ttu-id="d29a2-170">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="d29a2-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d29a2-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d29a2-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="d29a2-172">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="d29a2-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="d29a2-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d29a2-173">-WebApp</span></span>
<span data-ttu-id="d29a2-174">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="d29a2-174">WebApp Object</span></span>

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

### <span data-ttu-id="d29a2-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d29a2-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="d29a2-176">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="d29a2-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="d29a2-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29a2-177">CommonParameters</span></span>
<span data-ttu-id="d29a2-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d29a2-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29a2-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29a2-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29a2-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d29a2-180">INPUTS</span></span>

### <span data-ttu-id="d29a2-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d29a2-181">System.Int32</span></span>

### <span data-ttu-id="d29a2-182">System. String</span><span class="sxs-lookup"><span data-stu-id="d29a2-182">System.String</span></span>

### <span data-ttu-id="d29a2-183">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d29a2-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d29a2-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d29a2-184">OUTPUTS</span></span>

### <span data-ttu-id="d29a2-185">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d29a2-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d29a2-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d29a2-186">NOTES</span></span>

## <span data-ttu-id="d29a2-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d29a2-187">RELATED LINKS</span></span>

[<span data-ttu-id="d29a2-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d29a2-189">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d29a2-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d29a2-191">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d29a2-192">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d29a2-193">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d29a2-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d29a2-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d29a2-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
