---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850182"
---
# <span data-ttu-id="550a8-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="550a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="550a8-102">SYNOPSIS</span></span>
<span data-ttu-id="550a8-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="550a8-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="550a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="550a8-104">SYNTAX</span></span>

### <span data-ttu-id="550a8-105">S1</span><span class="sxs-lookup"><span data-stu-id="550a8-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="550a8-106">S2</span><span class="sxs-lookup"><span data-stu-id="550a8-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="550a8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="550a8-107">DESCRIPTION</span></span>
<span data-ttu-id="550a8-108">A **set-AzureRmWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="550a8-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="550a8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="550a8-109">EXAMPLES</span></span>

### <span data-ttu-id="550a8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="550a8-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="550a8-111">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="550a8-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="550a8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="550a8-112">PARAMETERS</span></span>

### <span data-ttu-id="550a8-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="550a8-113">-AppServicePlan</span></span>
<span data-ttu-id="550a8-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="550a8-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="550a8-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="550a8-115">-AppSettings</span></span>
<span data-ttu-id="550a8-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="550a8-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="550a8-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="550a8-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="550a8-118">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="550a8-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="550a8-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="550a8-119">-ConnectionStrings</span></span>
<span data-ttu-id="550a8-120">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="550a8-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="550a8-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="550a8-121">-DefaultDocuments</span></span>
<span data-ttu-id="550a8-122">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="550a8-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="550a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550a8-123">-DefaultProfile</span></span>
<span data-ttu-id="550a8-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="550a8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="550a8-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="550a8-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="550a8-126">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="550a8-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="550a8-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="550a8-127">-HandlerMappings</span></span>
<span data-ttu-id="550a8-128">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="550a8-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="550a8-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="550a8-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="550a8-130">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="550a8-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="550a8-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="550a8-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="550a8-132">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="550a8-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="550a8-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="550a8-133">-Name</span></span>
<span data-ttu-id="550a8-134">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="550a8-134">WebApp Name</span></span>

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

### <span data-ttu-id="550a8-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="550a8-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="550a8-136">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="550a8-136">Net Framework Version</span></span>

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

### <span data-ttu-id="550a8-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="550a8-137">-NumberOfWorkers</span></span>
<span data-ttu-id="550a8-138">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="550a8-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="550a8-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="550a8-139">-PhpVersion</span></span>
<span data-ttu-id="550a8-140">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="550a8-140">Php Version</span></span>

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

### <span data-ttu-id="550a8-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="550a8-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="550a8-142">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="550a8-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="550a8-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550a8-143">-ResourceGroupName</span></span>
<span data-ttu-id="550a8-144">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="550a8-144">Resource Group Name</span></span>

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

### <span data-ttu-id="550a8-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="550a8-145">-Slot</span></span>
<span data-ttu-id="550a8-146">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="550a8-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="550a8-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="550a8-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="550a8-148">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="550a8-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="550a8-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="550a8-149">-WebApp</span></span>
<span data-ttu-id="550a8-150">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="550a8-150">WebApp Object</span></span>

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

### <span data-ttu-id="550a8-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="550a8-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="550a8-152">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="550a8-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="550a8-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="550a8-153">-HttpsOnly</span></span>
<span data-ttu-id="550a8-154">Az összes forgalom átirányításának engedélyezése/letiltása egy meglévő bővítőhelyen a HTTPS-re</span><span class="sxs-lookup"><span data-stu-id="550a8-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="550a8-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="550a8-155">-AssignIdentity</span></span>
<span data-ttu-id="550a8-156">MSI engedélyezése/letiltása meglévő bővítőhelyen [előzetes verzió]</span><span class="sxs-lookup"><span data-stu-id="550a8-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="550a8-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="550a8-157">-AsJob</span></span>
<span data-ttu-id="550a8-158">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="550a8-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="550a8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550a8-159">CommonParameters</span></span>
<span data-ttu-id="550a8-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="550a8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550a8-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="550a8-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550a8-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="550a8-162">INPUTS</span></span>

### <span data-ttu-id="550a8-163">Int32</span><span class="sxs-lookup"><span data-stu-id="550a8-163">Int32</span></span>
<span data-ttu-id="550a8-164">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="550a8-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="550a8-165">Webhely</span><span class="sxs-lookup"><span data-stu-id="550a8-165">Site</span></span>
<span data-ttu-id="550a8-166">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="550a8-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="550a8-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="550a8-167">OUTPUTS</span></span>

## <span data-ttu-id="550a8-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="550a8-168">NOTES</span></span>

## <span data-ttu-id="550a8-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="550a8-169">RELATED LINKS</span></span>

[<span data-ttu-id="550a8-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="550a8-171">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="550a8-172">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="550a8-173">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="550a8-174">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="550a8-175">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="550a8-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="550a8-176">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="550a8-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
