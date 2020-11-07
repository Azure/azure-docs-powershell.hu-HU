---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668293"
---
# <span data-ttu-id="04e37-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="04e37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04e37-102">SYNOPSIS</span></span>
<span data-ttu-id="04e37-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="04e37-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="04e37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04e37-104">SYNTAX</span></span>

### <span data-ttu-id="04e37-105">S1</span><span class="sxs-lookup"><span data-stu-id="04e37-105">S1</span></span>
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

### <span data-ttu-id="04e37-106">S2</span><span class="sxs-lookup"><span data-stu-id="04e37-106">S2</span></span>
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

## <span data-ttu-id="04e37-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="04e37-107">DESCRIPTION</span></span>
<span data-ttu-id="04e37-108">A **set-AzWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="04e37-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="04e37-109">Példák</span><span class="sxs-lookup"><span data-stu-id="04e37-109">EXAMPLES</span></span>

### <span data-ttu-id="04e37-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04e37-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="04e37-111">Ez a parancs megváltoztatja a Slot001 társított appservice-csomagot, az erőforráscsoport alapértelmezett WestUS-webhelyhez társított WebApp ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="04e37-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="04e37-112">A hivatkozás segítségével learm többet a appservice-terv és a hozzájuk kapcsolódó korlátozások módosításáról.</span><span class="sxs-lookup"><span data-stu-id="04e37-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="04e37-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="04e37-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="04e37-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="04e37-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="04e37-115">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="04e37-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="04e37-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04e37-116">PARAMETERS</span></span>

### <span data-ttu-id="04e37-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="04e37-117">-AppServicePlan</span></span>
<span data-ttu-id="04e37-118">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="04e37-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="04e37-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="04e37-119">-AppSettings</span></span>
<span data-ttu-id="04e37-120">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="04e37-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="04e37-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04e37-121">-AsJob</span></span>
<span data-ttu-id="04e37-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="04e37-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04e37-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="04e37-123">-AssignIdentity</span></span>
<span data-ttu-id="04e37-124">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="04e37-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="04e37-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="04e37-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="04e37-126">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="04e37-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="04e37-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="04e37-127">-AzureStoragePath</span></span>
<span data-ttu-id="04e37-128">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="04e37-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="04e37-129">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="04e37-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="04e37-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="04e37-130">-ConnectionStrings</span></span>
<span data-ttu-id="04e37-131">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="04e37-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="04e37-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="04e37-132">-ContainerImageName</span></span>
<span data-ttu-id="04e37-133">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="04e37-133">Container Image Name</span></span>

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

### <span data-ttu-id="04e37-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="04e37-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="04e37-135">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="04e37-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="04e37-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="04e37-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="04e37-137">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="04e37-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="04e37-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="04e37-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="04e37-139">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="04e37-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="04e37-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="04e37-140">-DefaultDocuments</span></span>
<span data-ttu-id="04e37-141">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="04e37-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="04e37-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e37-142">-DefaultProfile</span></span>
<span data-ttu-id="04e37-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04e37-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04e37-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="04e37-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="04e37-145">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="04e37-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="04e37-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="04e37-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="04e37-147">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="04e37-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="04e37-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="04e37-148">-HandlerMappings</span></span>
<span data-ttu-id="04e37-149">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="04e37-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="04e37-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="04e37-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="04e37-151">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="04e37-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="04e37-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="04e37-152">-HttpsOnly</span></span>
<span data-ttu-id="04e37-153">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="04e37-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="04e37-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="04e37-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="04e37-155">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="04e37-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="04e37-156">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04e37-156">-Name</span></span>
<span data-ttu-id="04e37-157">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="04e37-157">WebApp Name</span></span>

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

### <span data-ttu-id="04e37-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="04e37-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="04e37-159">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="04e37-159">Net Framework Version</span></span>

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

### <span data-ttu-id="04e37-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="04e37-160">-NumberOfWorkers</span></span>
<span data-ttu-id="04e37-161">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="04e37-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="04e37-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="04e37-162">-PhpVersion</span></span>
<span data-ttu-id="04e37-163">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="04e37-163">Php Version</span></span>

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

### <span data-ttu-id="04e37-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="04e37-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="04e37-165">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="04e37-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="04e37-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e37-166">-ResourceGroupName</span></span>
<span data-ttu-id="04e37-167">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="04e37-167">Resource Group Name</span></span>

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

### <span data-ttu-id="04e37-168">-Slot</span><span class="sxs-lookup"><span data-stu-id="04e37-168">-Slot</span></span>
<span data-ttu-id="04e37-169">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="04e37-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="04e37-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="04e37-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="04e37-171">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="04e37-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="04e37-172">-WebApp</span><span class="sxs-lookup"><span data-stu-id="04e37-172">-WebApp</span></span>
<span data-ttu-id="04e37-173">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="04e37-173">WebApp Object</span></span>

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

### <span data-ttu-id="04e37-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="04e37-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="04e37-175">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="04e37-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="04e37-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e37-176">CommonParameters</span></span>
<span data-ttu-id="04e37-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04e37-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e37-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e37-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e37-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e37-179">INPUTS</span></span>

### <span data-ttu-id="04e37-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="04e37-180">System.Int32</span></span>

### <span data-ttu-id="04e37-181">System. String</span><span class="sxs-lookup"><span data-stu-id="04e37-181">System.String</span></span>

### <span data-ttu-id="04e37-182">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="04e37-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="04e37-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e37-183">OUTPUTS</span></span>

### <span data-ttu-id="04e37-184">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="04e37-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="04e37-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04e37-185">NOTES</span></span>

## <span data-ttu-id="04e37-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04e37-186">RELATED LINKS</span></span>

[<span data-ttu-id="04e37-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="04e37-188">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="04e37-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="04e37-190">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="04e37-191">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="04e37-192">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04e37-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="04e37-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="04e37-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
