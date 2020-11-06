---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497139"
---
# <span data-ttu-id="bb8ab-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="bb8ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8ab-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="bb8ab-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb8ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb8ab-104">SYNTAX</span></span>

### <span data-ttu-id="bb8ab-105">S1</span><span class="sxs-lookup"><span data-stu-id="bb8ab-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8ab-106">S2</span><span class="sxs-lookup"><span data-stu-id="bb8ab-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb8ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb8ab-107">DESCRIPTION</span></span>
<span data-ttu-id="bb8ab-108">A **set-AzureRmWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="bb8ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bb8ab-109">EXAMPLES</span></span>

### <span data-ttu-id="bb8ab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb8ab-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="bb8ab-111">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="bb8ab-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bb8ab-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb8ab-112">PARAMETERS</span></span>

### <span data-ttu-id="bb8ab-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb8ab-113">-AppServicePlan</span></span>
<span data-ttu-id="bb8ab-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="bb8ab-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="bb8ab-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="bb8ab-115">-AppSettings</span></span>
<span data-ttu-id="bb8ab-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="bb8ab-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="bb8ab-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb8ab-117">-AsJob</span></span>
<span data-ttu-id="bb8ab-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bb8ab-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb8ab-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bb8ab-119">-AssignIdentity</span></span>
<span data-ttu-id="bb8ab-120">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="bb8ab-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="bb8ab-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="bb8ab-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="bb8ab-122">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="bb8ab-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="bb8ab-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="bb8ab-123">-ConnectionStrings</span></span>
<span data-ttu-id="bb8ab-124">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="bb8ab-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="bb8ab-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="bb8ab-125">-ContainerImageName</span></span>
<span data-ttu-id="bb8ab-126">Tároló képe</span><span class="sxs-lookup"><span data-stu-id="bb8ab-126">Container Image Name</span></span>

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

### <span data-ttu-id="bb8ab-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="bb8ab-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="bb8ab-128">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="bb8ab-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="bb8ab-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="bb8ab-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="bb8ab-130">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="bb8ab-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="bb8ab-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="bb8ab-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="bb8ab-132">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="bb8ab-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="bb8ab-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="bb8ab-133">-DefaultDocuments</span></span>
<span data-ttu-id="bb8ab-134">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="bb8ab-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="bb8ab-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8ab-135">-DefaultProfile</span></span>
<span data-ttu-id="bb8ab-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb8ab-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bb8ab-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="bb8ab-138">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="bb8ab-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="bb8ab-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="bb8ab-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="bb8ab-140">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="bb8ab-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="bb8ab-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="bb8ab-141">-HandlerMappings</span></span>
<span data-ttu-id="bb8ab-142">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="bb8ab-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="bb8ab-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bb8ab-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="bb8ab-144">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="bb8ab-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="bb8ab-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="bb8ab-145">-HttpsOnly</span></span>
<span data-ttu-id="bb8ab-146">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="bb8ab-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="bb8ab-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="bb8ab-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="bb8ab-148">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="bb8ab-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="bb8ab-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb8ab-149">-Name</span></span>
<span data-ttu-id="bb8ab-150">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="bb8ab-150">WebApp Name</span></span>

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

### <span data-ttu-id="bb8ab-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="bb8ab-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="bb8ab-152">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="bb8ab-152">Net Framework Version</span></span>

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

### <span data-ttu-id="bb8ab-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="bb8ab-153">-NumberOfWorkers</span></span>
<span data-ttu-id="bb8ab-154">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="bb8ab-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="bb8ab-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="bb8ab-155">-PhpVersion</span></span>
<span data-ttu-id="bb8ab-156">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="bb8ab-156">Php Version</span></span>

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

### <span data-ttu-id="bb8ab-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="bb8ab-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="bb8ab-158">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="bb8ab-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="bb8ab-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8ab-159">-ResourceGroupName</span></span>
<span data-ttu-id="bb8ab-160">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="bb8ab-160">Resource Group Name</span></span>

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

### <span data-ttu-id="bb8ab-161">-Slot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-161">-Slot</span></span>
<span data-ttu-id="bb8ab-162">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="bb8ab-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bb8ab-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="bb8ab-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="bb8ab-164">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="bb8ab-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="bb8ab-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bb8ab-165">-WebApp</span></span>
<span data-ttu-id="bb8ab-166">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="bb8ab-166">WebApp Object</span></span>

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

### <span data-ttu-id="bb8ab-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="bb8ab-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="bb8ab-168">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="bb8ab-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="bb8ab-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8ab-169">CommonParameters</span></span>
<span data-ttu-id="bb8ab-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb8ab-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8ab-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8ab-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8ab-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb8ab-172">INPUTS</span></span>

### <span data-ttu-id="bb8ab-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bb8ab-173">System.Int32</span></span>
<span data-ttu-id="bb8ab-174">Paraméterek: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb8ab-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="bb8ab-175">System. String</span><span class="sxs-lookup"><span data-stu-id="bb8ab-175">System.String</span></span>

### <span data-ttu-id="bb8ab-176">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="bb8ab-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="bb8ab-177">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb8ab-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="bb8ab-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb8ab-178">OUTPUTS</span></span>

### <span data-ttu-id="bb8ab-179">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="bb8ab-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="bb8ab-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb8ab-180">NOTES</span></span>

## <span data-ttu-id="bb8ab-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb8ab-181">RELATED LINKS</span></span>

[<span data-ttu-id="bb8ab-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="bb8ab-183">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="bb8ab-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="bb8ab-185">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="bb8ab-186">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="bb8ab-187">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb8ab-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="bb8ab-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb8ab-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
