---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493804"
---
# <span data-ttu-id="79e96-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="79e96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79e96-102">SYNOPSIS</span></span>
<span data-ttu-id="79e96-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="79e96-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79e96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79e96-104">SYNTAX</span></span>

### <span data-ttu-id="79e96-105">S1</span><span class="sxs-lookup"><span data-stu-id="79e96-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e96-106">S2</span><span class="sxs-lookup"><span data-stu-id="79e96-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e96-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="79e96-107">DESCRIPTION</span></span>
<span data-ttu-id="79e96-108">A **set-AzureRmWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="79e96-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="79e96-109">Példák</span><span class="sxs-lookup"><span data-stu-id="79e96-109">EXAMPLES</span></span>

### <span data-ttu-id="79e96-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="79e96-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="79e96-111">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="79e96-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="79e96-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79e96-112">PARAMETERS</span></span>

### <span data-ttu-id="79e96-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="79e96-113">-AppServicePlan</span></span>
<span data-ttu-id="79e96-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="79e96-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="79e96-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="79e96-115">-AppSettings</span></span>
<span data-ttu-id="79e96-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="79e96-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="79e96-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="79e96-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="79e96-118">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="79e96-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="79e96-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="79e96-119">-ConnectionStrings</span></span>
<span data-ttu-id="79e96-120">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="79e96-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="79e96-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="79e96-121">-DefaultDocuments</span></span>
<span data-ttu-id="79e96-122">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="79e96-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="79e96-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="79e96-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="79e96-124">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="79e96-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="79e96-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="79e96-125">-HandlerMappings</span></span>
<span data-ttu-id="79e96-126">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="79e96-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="79e96-127">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="79e96-127">-HostNames</span></span>
<span data-ttu-id="79e96-128">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="79e96-128">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="79e96-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="79e96-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="79e96-130">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="79e96-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="79e96-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="79e96-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="79e96-132">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="79e96-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="79e96-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79e96-133">-Name</span></span>
<span data-ttu-id="79e96-134">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="79e96-134">WebApp Name</span></span>

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

### <span data-ttu-id="79e96-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="79e96-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="79e96-136">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="79e96-136">Net Framework Version</span></span>

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

### <span data-ttu-id="79e96-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="79e96-137">-NumberOfWorkers</span></span>
<span data-ttu-id="79e96-138">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="79e96-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="79e96-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="79e96-139">-PhpVersion</span></span>
<span data-ttu-id="79e96-140">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="79e96-140">Php Version</span></span>

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

### <span data-ttu-id="79e96-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="79e96-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="79e96-142">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="79e96-142">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="79e96-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e96-143">-ResourceGroupName</span></span>
<span data-ttu-id="79e96-144">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="79e96-144">Resource Group Name</span></span>

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

### <span data-ttu-id="79e96-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="79e96-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="79e96-146">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="79e96-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="79e96-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-147">-WebApp</span></span>
<span data-ttu-id="79e96-148">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="79e96-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79e96-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="79e96-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="79e96-150">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="79e96-150">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="79e96-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e96-151">-DefaultProfile</span></span>
<span data-ttu-id="79e96-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79e96-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e96-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e96-153">CommonParameters</span></span>
<span data-ttu-id="79e96-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79e96-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e96-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e96-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e96-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79e96-156">INPUTS</span></span>

### <span data-ttu-id="79e96-157">Int32</span><span class="sxs-lookup"><span data-stu-id="79e96-157">Int32</span></span>
<span data-ttu-id="79e96-158">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="79e96-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="79e96-159">Webhely</span><span class="sxs-lookup"><span data-stu-id="79e96-159">Site</span></span>
<span data-ttu-id="79e96-160">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="79e96-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="79e96-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79e96-161">OUTPUTS</span></span>

## <span data-ttu-id="79e96-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79e96-162">NOTES</span></span>

## <span data-ttu-id="79e96-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79e96-163">RELATED LINKS</span></span>

[<span data-ttu-id="79e96-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="79e96-165">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="79e96-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="79e96-167">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="79e96-168">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="79e96-169">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79e96-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
