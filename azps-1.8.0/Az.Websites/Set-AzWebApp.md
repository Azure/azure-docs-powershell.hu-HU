---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668298"
---
# <span data-ttu-id="a26fb-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-101">Set-AzWebApp</span></span>



## <span data-ttu-id="a26fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a26fb-102">SYNOPSIS</span></span>

<span data-ttu-id="a26fb-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="a26fb-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="a26fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a26fb-104">SYNTAX</span></span>



### <span data-ttu-id="a26fb-105">S1</span><span class="sxs-lookup"><span data-stu-id="a26fb-105">S1</span></span>

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



### <span data-ttu-id="a26fb-106">S2</span><span class="sxs-lookup"><span data-stu-id="a26fb-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="a26fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a26fb-107">DESCRIPTION</span></span>

<span data-ttu-id="a26fb-108">A **set-AzWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="a26fb-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="a26fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a26fb-109">EXAMPLES</span></span>



### <span data-ttu-id="a26fb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a26fb-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="a26fb-111">Ez a parancs megváltoztatja az erőforráscsoport alapértelmezett ContosoWebApp társított appservice-tervét – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a26fb-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="a26fb-112">A hivatkozás segítségével learm többet a appservice-terv és a hozzájuk kapcsolódó korlátozások módosításáról.</span><span class="sxs-lookup"><span data-stu-id="a26fb-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="a26fb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a26fb-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="a26fb-114">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="a26fb-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="a26fb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a26fb-115">PARAMETERS</span></span>



### <span data-ttu-id="a26fb-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a26fb-116">-AppServicePlan</span></span>

<span data-ttu-id="a26fb-117">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="a26fb-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="a26fb-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a26fb-118">-AppSettings</span></span>

<span data-ttu-id="a26fb-119">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="a26fb-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="a26fb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a26fb-120">-AsJob</span></span>

<span data-ttu-id="a26fb-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a26fb-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="a26fb-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a26fb-122">-AssignIdentity</span></span>

<span data-ttu-id="a26fb-123">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="a26fb-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="a26fb-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="a26fb-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="a26fb-125">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="a26fb-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="a26fb-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a26fb-126">-AzureStoragePath</span></span>

<span data-ttu-id="a26fb-127">Azure-tárterület egy webalkalmazás tárolóhoz való csatlakoztatásához</span><span class="sxs-lookup"><span data-stu-id="a26fb-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="a26fb-128">A létrehozás New-AzureRmWebAppAzureStoragePath használata</span><span class="sxs-lookup"><span data-stu-id="a26fb-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



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



### <span data-ttu-id="a26fb-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="a26fb-129">-ConnectionStrings</span></span>

<span data-ttu-id="a26fb-130">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="a26fb-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="a26fb-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="a26fb-131">-ContainerImageName</span></span>

<span data-ttu-id="a26fb-132">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="a26fb-132">Container Image Name</span></span>



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



### <span data-ttu-id="a26fb-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="a26fb-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="a26fb-134">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="a26fb-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="a26fb-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="a26fb-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="a26fb-136">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="a26fb-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="a26fb-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="a26fb-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="a26fb-138">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="a26fb-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="a26fb-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a26fb-139">-DefaultDocuments</span></span>

<span data-ttu-id="a26fb-140">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="a26fb-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="a26fb-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26fb-141">-DefaultProfile</span></span>

<span data-ttu-id="a26fb-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a26fb-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="a26fb-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a26fb-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="a26fb-144">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="a26fb-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="a26fb-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="a26fb-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="a26fb-146">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="a26fb-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="a26fb-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a26fb-147">-HandlerMappings</span></span>

<span data-ttu-id="a26fb-148">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="a26fb-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="a26fb-149">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="a26fb-149">-HostNames</span></span>

<span data-ttu-id="a26fb-150">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="a26fb-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="a26fb-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a26fb-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="a26fb-152">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="a26fb-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="a26fb-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a26fb-153">-HttpsOnly</span></span>

<span data-ttu-id="a26fb-154">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="a26fb-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="a26fb-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a26fb-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="a26fb-156">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="a26fb-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="a26fb-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a26fb-157">-Name</span></span>

<span data-ttu-id="a26fb-158">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a26fb-158">WebApp Name</span></span>



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



### <span data-ttu-id="a26fb-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a26fb-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="a26fb-160">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="a26fb-160">Net Framework Version</span></span>



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



### <span data-ttu-id="a26fb-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a26fb-161">-NumberOfWorkers</span></span>

<span data-ttu-id="a26fb-162">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="a26fb-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="a26fb-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a26fb-163">-PhpVersion</span></span>

<span data-ttu-id="a26fb-164">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="a26fb-164">Php Version</span></span>



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



### <span data-ttu-id="a26fb-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a26fb-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="a26fb-166">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="a26fb-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="a26fb-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26fb-167">-ResourceGroupName</span></span>

<span data-ttu-id="a26fb-168">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a26fb-168">Resource Group Name</span></span>



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



### <span data-ttu-id="a26fb-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a26fb-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="a26fb-170">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="a26fb-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="a26fb-171">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-171">-WebApp</span></span>

<span data-ttu-id="a26fb-172">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="a26fb-172">WebApp Object</span></span>



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



### <span data-ttu-id="a26fb-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a26fb-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="a26fb-174">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="a26fb-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="a26fb-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26fb-175">CommonParameters</span></span>

<span data-ttu-id="a26fb-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a26fb-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26fb-177">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a26fb-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="a26fb-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a26fb-178">INPUTS</span></span>



### <span data-ttu-id="a26fb-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a26fb-179">System.Int32</span></span>



### <span data-ttu-id="a26fb-180">System. String</span><span class="sxs-lookup"><span data-stu-id="a26fb-180">System.String</span></span>



### <span data-ttu-id="a26fb-181">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a26fb-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="a26fb-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a26fb-182">OUTPUTS</span></span>



### <span data-ttu-id="a26fb-183">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a26fb-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="a26fb-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a26fb-184">NOTES</span></span>



## <span data-ttu-id="a26fb-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a26fb-185">RELATED LINKS</span></span>



[<span data-ttu-id="a26fb-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="a26fb-187">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="a26fb-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="a26fb-189">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="a26fb-190">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="a26fb-191">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a26fb-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

