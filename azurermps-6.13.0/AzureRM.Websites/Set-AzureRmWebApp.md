---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495571"
---
# <span data-ttu-id="64244-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="64244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64244-102">SYNOPSIS</span></span>
<span data-ttu-id="64244-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="64244-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64244-104">SYNTAX</span></span>

### <span data-ttu-id="64244-105">S1</span><span class="sxs-lookup"><span data-stu-id="64244-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64244-106">S2</span><span class="sxs-lookup"><span data-stu-id="64244-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64244-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="64244-107">DESCRIPTION</span></span>
<span data-ttu-id="64244-108">A **set-AzureRmWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="64244-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="64244-109">Példák</span><span class="sxs-lookup"><span data-stu-id="64244-109">EXAMPLES</span></span>

### <span data-ttu-id="64244-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64244-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="64244-111">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="64244-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="64244-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64244-112">PARAMETERS</span></span>

### <span data-ttu-id="64244-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="64244-113">-AppServicePlan</span></span>
<span data-ttu-id="64244-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="64244-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="64244-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="64244-115">-AppSettings</span></span>
<span data-ttu-id="64244-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="64244-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="64244-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64244-117">-AsJob</span></span>
<span data-ttu-id="64244-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64244-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64244-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="64244-119">-AssignIdentity</span></span>
<span data-ttu-id="64244-120">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="64244-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="64244-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="64244-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="64244-122">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="64244-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="64244-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="64244-123">-ConnectionStrings</span></span>
<span data-ttu-id="64244-124">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="64244-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="64244-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="64244-125">-ContainerImageName</span></span>
<span data-ttu-id="64244-126">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="64244-126">Container Image Name</span></span>

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

### <span data-ttu-id="64244-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="64244-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="64244-128">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="64244-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="64244-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="64244-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="64244-130">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="64244-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="64244-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="64244-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="64244-132">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="64244-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="64244-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="64244-133">-DefaultDocuments</span></span>
<span data-ttu-id="64244-134">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="64244-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="64244-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64244-135">-DefaultProfile</span></span>
<span data-ttu-id="64244-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64244-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64244-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="64244-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="64244-138">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="64244-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="64244-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="64244-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="64244-140">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="64244-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="64244-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="64244-141">-HandlerMappings</span></span>
<span data-ttu-id="64244-142">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="64244-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="64244-143">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="64244-143">-HostNames</span></span>
<span data-ttu-id="64244-144">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="64244-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="64244-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="64244-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="64244-146">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="64244-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="64244-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="64244-147">-HttpsOnly</span></span>
<span data-ttu-id="64244-148">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="64244-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="64244-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="64244-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="64244-150">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="64244-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="64244-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64244-151">-Name</span></span>
<span data-ttu-id="64244-152">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="64244-152">WebApp Name</span></span>

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

### <span data-ttu-id="64244-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="64244-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="64244-154">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="64244-154">Net Framework Version</span></span>

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

### <span data-ttu-id="64244-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="64244-155">-NumberOfWorkers</span></span>
<span data-ttu-id="64244-156">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="64244-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="64244-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="64244-157">-PhpVersion</span></span>
<span data-ttu-id="64244-158">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="64244-158">Php Version</span></span>

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

### <span data-ttu-id="64244-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="64244-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="64244-160">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="64244-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="64244-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64244-161">-ResourceGroupName</span></span>
<span data-ttu-id="64244-162">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="64244-162">Resource Group Name</span></span>

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

### <span data-ttu-id="64244-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="64244-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="64244-164">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="64244-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="64244-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="64244-165">-WebApp</span></span>
<span data-ttu-id="64244-166">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="64244-166">WebApp Object</span></span>

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

### <span data-ttu-id="64244-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="64244-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="64244-168">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="64244-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="64244-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64244-169">CommonParameters</span></span>
<span data-ttu-id="64244-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64244-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64244-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64244-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64244-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64244-172">INPUTS</span></span>

### <span data-ttu-id="64244-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="64244-173">System.Int32</span></span>
<span data-ttu-id="64244-174">Paraméterek: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="64244-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="64244-175">System. String</span><span class="sxs-lookup"><span data-stu-id="64244-175">System.String</span></span>

### <span data-ttu-id="64244-176">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="64244-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="64244-177">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="64244-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="64244-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64244-178">OUTPUTS</span></span>

### <span data-ttu-id="64244-179">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="64244-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="64244-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64244-180">NOTES</span></span>

## <span data-ttu-id="64244-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64244-181">RELATED LINKS</span></span>

[<span data-ttu-id="64244-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="64244-183">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="64244-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="64244-185">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="64244-186">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="64244-187">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64244-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
