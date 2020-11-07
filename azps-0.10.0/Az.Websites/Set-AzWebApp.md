---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842678"
---
# <span data-ttu-id="165b1-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-101">Set-AzWebApp</span></span>

## <span data-ttu-id="165b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="165b1-102">SYNOPSIS</span></span>
<span data-ttu-id="165b1-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="165b1-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="165b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="165b1-104">SYNTAX</span></span>

### <span data-ttu-id="165b1-105">S1</span><span class="sxs-lookup"><span data-stu-id="165b1-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="165b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="165b1-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="165b1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="165b1-107">DESCRIPTION</span></span>
<span data-ttu-id="165b1-108">A **set-AzWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="165b1-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="165b1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="165b1-109">EXAMPLES</span></span>

### <span data-ttu-id="165b1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="165b1-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="165b1-111">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="165b1-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="165b1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="165b1-112">PARAMETERS</span></span>

### <span data-ttu-id="165b1-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="165b1-113">-AppServicePlan</span></span>
<span data-ttu-id="165b1-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="165b1-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="165b1-115">-AppSettings</span></span>
<span data-ttu-id="165b1-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="165b1-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="165b1-117">-AsJob</span></span>
<span data-ttu-id="165b1-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="165b1-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="165b1-119">-AssignIdentity</span></span>
<span data-ttu-id="165b1-120">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="165b1-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="165b1-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="165b1-122">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="165b1-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="165b1-123">-ConnectionStrings</span></span>
<span data-ttu-id="165b1-124">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="165b1-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="165b1-125">-DefaultDocuments</span></span>
<span data-ttu-id="165b1-126">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="165b1-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165b1-127">-DefaultProfile</span></span>
<span data-ttu-id="165b1-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="165b1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="165b1-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="165b1-130">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="165b1-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="165b1-131">-HandlerMappings</span></span>
<span data-ttu-id="165b1-132">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="165b1-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="165b1-133">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="165b1-133">-HostNames</span></span>
<span data-ttu-id="165b1-134">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="165b1-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="165b1-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="165b1-136">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="165b1-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="165b1-137">-HttpsOnly</span></span>
<span data-ttu-id="165b1-138">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="165b1-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="165b1-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="165b1-140">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="165b1-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="165b1-141">-Name</span></span>
<span data-ttu-id="165b1-142">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="165b1-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="165b1-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="165b1-144">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="165b1-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="165b1-145">-NumberOfWorkers</span></span>
<span data-ttu-id="165b1-146">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="165b1-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="165b1-147">-PhpVersion</span></span>
<span data-ttu-id="165b1-148">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="165b1-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="165b1-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="165b1-150">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="165b1-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="165b1-151">-ResourceGroupName</span></span>
<span data-ttu-id="165b1-152">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="165b1-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="165b1-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="165b1-154">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="165b1-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-155">-WebApp</span></span>
<span data-ttu-id="165b1-156">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="165b1-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="165b1-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="165b1-158">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="165b1-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165b1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165b1-159">CommonParameters</span></span>
<span data-ttu-id="165b1-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="165b1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165b1-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="165b1-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165b1-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="165b1-162">INPUTS</span></span>

### <span data-ttu-id="165b1-163">Int32</span><span class="sxs-lookup"><span data-stu-id="165b1-163">Int32</span></span>
<span data-ttu-id="165b1-164">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="165b1-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="165b1-165">Webhely</span><span class="sxs-lookup"><span data-stu-id="165b1-165">Site</span></span>
<span data-ttu-id="165b1-166">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="165b1-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="165b1-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="165b1-167">OUTPUTS</span></span>

## <span data-ttu-id="165b1-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="165b1-168">NOTES</span></span>

## <span data-ttu-id="165b1-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="165b1-169">RELATED LINKS</span></span>

[<span data-ttu-id="165b1-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="165b1-171">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="165b1-172">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="165b1-173">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="165b1-174">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="165b1-175">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="165b1-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
