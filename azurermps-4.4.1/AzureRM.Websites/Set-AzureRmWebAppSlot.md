---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672048"
---
# <span data-ttu-id="e32f0-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="e32f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e32f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e32f0-103">Azure Web App-bővítőhely módosítása</span><span class="sxs-lookup"><span data-stu-id="e32f0-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e32f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e32f0-104">SYNTAX</span></span>

### <span data-ttu-id="e32f0-105">S1</span><span class="sxs-lookup"><span data-stu-id="e32f0-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e32f0-106">S2</span><span class="sxs-lookup"><span data-stu-id="e32f0-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e32f0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e32f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e32f0-108">A **set-AzureRmWebApp** parancsmag egy Azure Web App-bővítőhelyet állít be.</span><span class="sxs-lookup"><span data-stu-id="e32f0-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="e32f0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e32f0-109">EXAMPLES</span></span>

### <span data-ttu-id="e32f0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e32f0-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="e32f0-111">Ez a parancs a HttpLoggingEnabled-hoz igaz értéket állítja be az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp tartozó bővítőhelyek esetén, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="e32f0-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e32f0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e32f0-112">PARAMETERS</span></span>

### <span data-ttu-id="e32f0-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e32f0-113">-AppServicePlan</span></span>
<span data-ttu-id="e32f0-114">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="e32f0-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="e32f0-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e32f0-115">-AppSettings</span></span>
<span data-ttu-id="e32f0-116">Az app beállításai HashTable</span><span class="sxs-lookup"><span data-stu-id="e32f0-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="e32f0-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e32f0-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="e32f0-118">Az automatikus csere cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="e32f0-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="e32f0-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e32f0-119">-ConnectionStrings</span></span>
<span data-ttu-id="e32f0-120">Kapcsolati karakterláncok HashTable</span><span class="sxs-lookup"><span data-stu-id="e32f0-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="e32f0-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e32f0-121">-DefaultDocuments</span></span>
<span data-ttu-id="e32f0-122">Alapértelmezett dokumentumok karakterlánca tömb</span><span class="sxs-lookup"><span data-stu-id="e32f0-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="e32f0-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e32f0-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e32f0-124">Részletes hibák naplózása engedélyezve logikai beállítással</span><span class="sxs-lookup"><span data-stu-id="e32f0-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="e32f0-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e32f0-125">-HandlerMappings</span></span>
<span data-ttu-id="e32f0-126">Kezelői megfeleltetések IList</span><span class="sxs-lookup"><span data-stu-id="e32f0-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="e32f0-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e32f0-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e32f0-128">HttpLoggingEnabled logikai érték</span><span class="sxs-lookup"><span data-stu-id="e32f0-128">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="e32f0-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e32f0-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="e32f0-130">Felügyelt csővezeték üzemmód neve</span><span class="sxs-lookup"><span data-stu-id="e32f0-130">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="e32f0-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e32f0-131">-Name</span></span>
<span data-ttu-id="e32f0-132">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e32f0-132">WebApp Name</span></span>

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

### <span data-ttu-id="e32f0-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e32f0-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="e32f0-134">NET-keretrendszer verziója</span><span class="sxs-lookup"><span data-stu-id="e32f0-134">Net Framework Version</span></span>

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

### <span data-ttu-id="e32f0-135">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e32f0-135">-NumberOfWorkers</span></span>
<span data-ttu-id="e32f0-136">A kiosztani kívánt munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="e32f0-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="e32f0-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e32f0-137">-PhpVersion</span></span>
<span data-ttu-id="e32f0-138">PHP-verzió</span><span class="sxs-lookup"><span data-stu-id="e32f0-138">Php Version</span></span>

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

### <span data-ttu-id="e32f0-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e32f0-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="e32f0-140">Nyomkövetést engedélyező logikai érték kérése</span><span class="sxs-lookup"><span data-stu-id="e32f0-140">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="e32f0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32f0-141">-ResourceGroupName</span></span>
<span data-ttu-id="e32f0-142">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e32f0-142">Resource Group Name</span></span>

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

### <span data-ttu-id="e32f0-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="e32f0-143">-Slot</span></span>
<span data-ttu-id="e32f0-144">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="e32f0-144">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e32f0-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e32f0-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e32f0-146">A 32 bites munkafolyamat-folyamat használata logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="e32f0-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="e32f0-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e32f0-147">-WebApp</span></span>
<span data-ttu-id="e32f0-148">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e32f0-148">WebApp Object</span></span>

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

### <span data-ttu-id="e32f0-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e32f0-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="e32f0-150">Logikai alapú webszoftvercsatornák</span><span class="sxs-lookup"><span data-stu-id="e32f0-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="e32f0-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32f0-151">-DefaultProfile</span></span>
<span data-ttu-id="e32f0-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e32f0-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e32f0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32f0-153">CommonParameters</span></span>
<span data-ttu-id="e32f0-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e32f0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32f0-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32f0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32f0-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e32f0-156">INPUTS</span></span>

### <span data-ttu-id="e32f0-157">Int32</span><span class="sxs-lookup"><span data-stu-id="e32f0-157">Int32</span></span>
<span data-ttu-id="e32f0-158">A ' NumberOfWorkers ' paraméter az "Int32" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e32f0-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="e32f0-159">Webhely</span><span class="sxs-lookup"><span data-stu-id="e32f0-159">Site</span></span>
<span data-ttu-id="e32f0-160">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e32f0-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e32f0-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e32f0-161">OUTPUTS</span></span>

## <span data-ttu-id="e32f0-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e32f0-162">NOTES</span></span>

## <span data-ttu-id="e32f0-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e32f0-163">RELATED LINKS</span></span>

[<span data-ttu-id="e32f0-164">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e32f0-165">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="e32f0-166">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="e32f0-167">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="e32f0-168">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="e32f0-169">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32f0-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="e32f0-170">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e32f0-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
