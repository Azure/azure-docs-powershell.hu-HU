---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842677"
---
# <span data-ttu-id="c3daf-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="c3daf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3daf-102">SYNOPSIS</span></span>
<span data-ttu-id="c3daf-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="c3daf-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="c3daf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3daf-104">SYNTAX</span></span>

### <span data-ttu-id="c3daf-105">S1</span><span class="sxs-lookup"><span data-stu-id="c3daf-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3daf-106">S2</span><span class="sxs-lookup"><span data-stu-id="c3daf-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3daf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3daf-107">DESCRIPTION</span></span>
<span data-ttu-id="c3daf-108">A **set-AzWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="c3daf-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="c3daf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c3daf-109">EXAMPLES</span></span>

### <span data-ttu-id="c3daf-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3daf-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="c3daf-111">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c3daf-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c3daf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3daf-112">PARAMETERS</span></span>

### <span data-ttu-id="c3daf-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c3daf-113">-AppServicePlan</span></span>
<span data-ttu-id="c3daf-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="c3daf-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c3daf-115">-AppSettings</span></span>
<span data-ttu-id="c3daf-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="c3daf-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c3daf-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="c3daf-118">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="c3daf-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c3daf-119">-ConnectionStrings</span></span>
<span data-ttu-id="c3daf-120">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="c3daf-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c3daf-121">-DefaultDocuments</span></span>
<span data-ttu-id="c3daf-122">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="c3daf-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3daf-123">-DefaultProfile</span></span>
<span data-ttu-id="c3daf-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3daf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3daf-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3daf-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c3daf-126">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="c3daf-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c3daf-127">-HandlerMappings</span></span>
<span data-ttu-id="c3daf-128">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="c3daf-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c3daf-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3daf-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c3daf-130">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="c3daf-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c3daf-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="c3daf-132">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="c3daf-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3daf-133">-Name</span></span>
<span data-ttu-id="c3daf-134">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c3daf-134">WebApp Name</span></span>

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

### <span data-ttu-id="c3daf-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c3daf-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="c3daf-136">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="c3daf-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c3daf-137">-NumberOfWorkers</span></span>
<span data-ttu-id="c3daf-138">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="c3daf-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c3daf-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c3daf-139">-PhpVersion</span></span>
<span data-ttu-id="c3daf-140">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="c3daf-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3daf-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="c3daf-142">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="c3daf-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3daf-143">-ResourceGroupName</span></span>
<span data-ttu-id="c3daf-144">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c3daf-144">Resource Group Name</span></span>

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

### <span data-ttu-id="c3daf-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="c3daf-145">-Slot</span></span>
<span data-ttu-id="c3daf-146">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c3daf-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c3daf-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c3daf-148">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="c3daf-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3daf-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c3daf-149">-WebApp</span></span>
<span data-ttu-id="c3daf-150">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c3daf-150">WebApp Object</span></span>

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

### <span data-ttu-id="c3daf-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c3daf-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="c3daf-152">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="c3daf-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="c3daf-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c3daf-153">-HttpsOnly</span></span>
<span data-ttu-id="c3daf-154">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="c3daf-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="c3daf-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c3daf-155">-AssignIdentity</span></span>
<span data-ttu-id="c3daf-156">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="c3daf-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="c3daf-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3daf-157">-AsJob</span></span>
<span data-ttu-id="c3daf-158">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c3daf-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3daf-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3daf-159">CommonParameters</span></span>
<span data-ttu-id="c3daf-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3daf-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3daf-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3daf-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3daf-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3daf-162">INPUTS</span></span>

### <span data-ttu-id="c3daf-163">Int32</span><span class="sxs-lookup"><span data-stu-id="c3daf-163">Int32</span></span>
<span data-ttu-id="c3daf-164">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c3daf-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="c3daf-165">Webhely</span><span class="sxs-lookup"><span data-stu-id="c3daf-165">Site</span></span>
<span data-ttu-id="c3daf-166">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c3daf-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c3daf-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3daf-167">OUTPUTS</span></span>

## <span data-ttu-id="c3daf-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3daf-168">NOTES</span></span>

## <span data-ttu-id="c3daf-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3daf-169">RELATED LINKS</span></span>

[<span data-ttu-id="c3daf-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c3daf-171">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c3daf-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c3daf-173">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c3daf-174">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c3daf-175">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3daf-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c3daf-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c3daf-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
