---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848958"
---
# <span data-ttu-id="b25c1-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="b25c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b25c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b25c1-103">Azure Web App módosítása</span><span class="sxs-lookup"><span data-stu-id="b25c1-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b25c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b25c1-104">SYNTAX</span></span>

### <span data-ttu-id="b25c1-105">S1</span><span class="sxs-lookup"><span data-stu-id="b25c1-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b25c1-106">S2</span><span class="sxs-lookup"><span data-stu-id="b25c1-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b25c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b25c1-107">DESCRIPTION</span></span>
<span data-ttu-id="b25c1-108">A **set-AzureRmWebApp** parancsmag az Azure web app alkalmazást állítja be.</span><span class="sxs-lookup"><span data-stu-id="b25c1-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="b25c1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b25c1-109">EXAMPLES</span></span>

### <span data-ttu-id="b25c1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b25c1-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="b25c1-111">Ez a parancs a HttpLoggingEnabled-hoz True for Web App ContosoWebApp társítja az erőforráscsoport alapértelmezett verziójában – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="b25c1-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b25c1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b25c1-112">PARAMETERS</span></span>

### <span data-ttu-id="b25c1-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b25c1-113">-AppServicePlan</span></span>
<span data-ttu-id="b25c1-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="b25c1-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="b25c1-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="b25c1-115">-AppSettings</span></span>
<span data-ttu-id="b25c1-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="b25c1-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="b25c1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b25c1-117">-AsJob</span></span>
<span data-ttu-id="b25c1-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b25c1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b25c1-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b25c1-119">-AssignIdentity</span></span>
<span data-ttu-id="b25c1-120">MSI engedélyezése/letiltása meglévő Azure WebApp-vagy functionapp [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="b25c1-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

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

### <span data-ttu-id="b25c1-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="b25c1-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="b25c1-122">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="b25c1-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="b25c1-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="b25c1-123">-ConnectionStrings</span></span>
<span data-ttu-id="b25c1-124">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="b25c1-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="b25c1-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="b25c1-125">-DefaultDocuments</span></span>
<span data-ttu-id="b25c1-126">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="b25c1-126">Default Documents String Array</span></span>

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

### <span data-ttu-id="b25c1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25c1-127">-DefaultProfile</span></span>
<span data-ttu-id="b25c1-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b25c1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b25c1-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b25c1-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="b25c1-130">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="b25c1-130">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="b25c1-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="b25c1-131">-HandlerMappings</span></span>
<span data-ttu-id="b25c1-132">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="b25c1-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="b25c1-133">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="b25c1-133">-HostNames</span></span>
<span data-ttu-id="b25c1-134">WebApp-állomásnevek karakterlánc-tömbje</span><span class="sxs-lookup"><span data-stu-id="b25c1-134">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="b25c1-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b25c1-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="b25c1-136">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="b25c1-136">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="b25c1-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b25c1-137">-HttpsOnly</span></span>
<span data-ttu-id="b25c1-138">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő Azure WebApp-vagy functionapp</span><span class="sxs-lookup"><span data-stu-id="b25c1-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="b25c1-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="b25c1-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="b25c1-140">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="b25c1-140">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="b25c1-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b25c1-141">-Name</span></span>
<span data-ttu-id="b25c1-142">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b25c1-142">WebApp Name</span></span>

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

### <span data-ttu-id="b25c1-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="b25c1-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="b25c1-144">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="b25c1-144">Net Framework Version</span></span>

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

### <span data-ttu-id="b25c1-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="b25c1-145">-NumberOfWorkers</span></span>
<span data-ttu-id="b25c1-146">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="b25c1-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="b25c1-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="b25c1-147">-PhpVersion</span></span>
<span data-ttu-id="b25c1-148">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="b25c1-148">Php Version</span></span>

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

### <span data-ttu-id="b25c1-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="b25c1-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="b25c1-150">Nyomkövetés kérése engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b25c1-150">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="b25c1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25c1-151">-ResourceGroupName</span></span>
<span data-ttu-id="b25c1-152">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b25c1-152">Resource Group Name</span></span>

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

### <span data-ttu-id="b25c1-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="b25c1-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="b25c1-154">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="b25c1-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="b25c1-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-155">-WebApp</span></span>
<span data-ttu-id="b25c1-156">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="b25c1-156">WebApp Object</span></span>

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

### <span data-ttu-id="b25c1-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b25c1-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="b25c1-158">WebSocketsEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="b25c1-158">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="b25c1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25c1-159">CommonParameters</span></span>
<span data-ttu-id="b25c1-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b25c1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25c1-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25c1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25c1-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b25c1-162">INPUTS</span></span>

### <span data-ttu-id="b25c1-163">Int32</span><span class="sxs-lookup"><span data-stu-id="b25c1-163">Int32</span></span>
<span data-ttu-id="b25c1-164">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b25c1-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="b25c1-165">Webhely</span><span class="sxs-lookup"><span data-stu-id="b25c1-165">Site</span></span>
<span data-ttu-id="b25c1-166">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b25c1-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b25c1-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b25c1-167">OUTPUTS</span></span>

## <span data-ttu-id="b25c1-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b25c1-168">NOTES</span></span>

## <span data-ttu-id="b25c1-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b25c1-169">RELATED LINKS</span></span>

[<span data-ttu-id="b25c1-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b25c1-171">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b25c1-172">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b25c1-173">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b25c1-174">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b25c1-175">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b25c1-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
