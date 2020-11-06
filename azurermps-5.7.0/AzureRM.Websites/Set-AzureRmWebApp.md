---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502303"
---
# <span data-ttu-id="378fd-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="378fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="378fd-102">SYNOPSIS</span></span>
<span data-ttu-id="378fd-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="378fd-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="378fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="378fd-104">SYNTAX</span></span>

### <span data-ttu-id="378fd-105">S1</span><span class="sxs-lookup"><span data-stu-id="378fd-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="378fd-106">S2</span><span class="sxs-lookup"><span data-stu-id="378fd-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="378fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="378fd-107">DESCRIPTION</span></span>
<span data-ttu-id="378fd-108">A **set-AzureRmWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="378fd-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="378fd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="378fd-109">EXAMPLES</span></span>

### <span data-ttu-id="378fd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="378fd-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="378fd-111">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="378fd-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="378fd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="378fd-112">PARAMETERS</span></span>

### <span data-ttu-id="378fd-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="378fd-113">-AppServicePlan</span></span>
<span data-ttu-id="378fd-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="378fd-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="378fd-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="378fd-115">-AppSettings</span></span>
<span data-ttu-id="378fd-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="378fd-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="378fd-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="378fd-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="378fd-118">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="378fd-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="378fd-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="378fd-119">-ConnectionStrings</span></span>
<span data-ttu-id="378fd-120">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="378fd-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="378fd-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="378fd-121">-DefaultDocuments</span></span>
<span data-ttu-id="378fd-122">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="378fd-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="378fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378fd-123">-DefaultProfile</span></span>
<span data-ttu-id="378fd-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="378fd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378fd-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="378fd-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="378fd-126">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="378fd-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="378fd-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="378fd-127">-HandlerMappings</span></span>
<span data-ttu-id="378fd-128">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="378fd-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="378fd-129">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="378fd-129">-HostNames</span></span>
<span data-ttu-id="378fd-130">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="378fd-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="378fd-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="378fd-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="378fd-132">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="378fd-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="378fd-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="378fd-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="378fd-134">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="378fd-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="378fd-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="378fd-135">-Name</span></span>
<span data-ttu-id="378fd-136">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="378fd-136">WebApp Name</span></span>

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

### <span data-ttu-id="378fd-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="378fd-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="378fd-138">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="378fd-138">Net Framework Version</span></span>

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

### <span data-ttu-id="378fd-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="378fd-139">-NumberOfWorkers</span></span>
<span data-ttu-id="378fd-140">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="378fd-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="378fd-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="378fd-141">-PhpVersion</span></span>
<span data-ttu-id="378fd-142">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="378fd-142">Php Version</span></span>

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

### <span data-ttu-id="378fd-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="378fd-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="378fd-144">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="378fd-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="378fd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378fd-145">-ResourceGroupName</span></span>
<span data-ttu-id="378fd-146">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="378fd-146">Resource Group Name</span></span>

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

### <span data-ttu-id="378fd-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="378fd-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="378fd-148">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="378fd-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="378fd-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-149">-WebApp</span></span>
<span data-ttu-id="378fd-150">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="378fd-150">WebApp Object</span></span>

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

### <span data-ttu-id="378fd-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="378fd-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="378fd-152">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="378fd-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="378fd-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="378fd-153">-AsJob</span></span>
<span data-ttu-id="378fd-154">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="378fd-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="378fd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378fd-155">CommonParameters</span></span>
<span data-ttu-id="378fd-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="378fd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378fd-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378fd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378fd-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="378fd-158">INPUTS</span></span>

### <span data-ttu-id="378fd-159">Int32</span><span class="sxs-lookup"><span data-stu-id="378fd-159">Int32</span></span>
<span data-ttu-id="378fd-160">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="378fd-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="378fd-161">Webhely</span><span class="sxs-lookup"><span data-stu-id="378fd-161">Site</span></span>
<span data-ttu-id="378fd-162">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="378fd-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="378fd-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="378fd-163">OUTPUTS</span></span>

## <span data-ttu-id="378fd-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="378fd-164">NOTES</span></span>

## <span data-ttu-id="378fd-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="378fd-165">RELATED LINKS</span></span>

[<span data-ttu-id="378fd-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="378fd-167">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="378fd-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="378fd-169">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="378fd-170">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="378fd-171">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="378fd-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
