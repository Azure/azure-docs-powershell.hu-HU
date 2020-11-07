---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: ca7fe171e95d87dd054f0dac27e1a5ccd07396a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835825"
---
# <span data-ttu-id="e94fd-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e94fd-101">Set-AzIotHub</span></span>

## <span data-ttu-id="e94fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e94fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e94fd-103">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e94fd-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="e94fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e94fd-104">SYNTAX</span></span>

### <span data-ttu-id="e94fd-105">UpdateSku (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e94fd-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-110">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-111">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94fd-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="e94fd-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e94fd-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="e94fd-113">DESCRIPTION</span></span>
<span data-ttu-id="e94fd-114">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e94fd-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="e94fd-115">Példák</span><span class="sxs-lookup"><span data-stu-id="e94fd-115">EXAMPLES</span></span>

### <span data-ttu-id="e94fd-116">Példa 1 a SKU frissítése</span><span class="sxs-lookup"><span data-stu-id="e94fd-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="e94fd-117">Frissítse a SKU-ot S1-re, és a "myiothub" nevű IotHub az 5 egységre</span><span class="sxs-lookup"><span data-stu-id="e94fd-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e94fd-118">2. példa a eventhub tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="e94fd-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="e94fd-119">A "myiothub" nevű IotHub telemetriai-és operationsmonitoringevents-eseményeinek frissítése a napok és a 4 közötti adatmegőrzési idő között</span><span class="sxs-lookup"><span data-stu-id="e94fd-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e94fd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e94fd-120">PARAMETERS</span></span>

### <span data-ttu-id="e94fd-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="e94fd-121">-CloudToDevice</span></span>
<span data-ttu-id="e94fd-122">A felhőalapú eszközhöz tartozó parancssori várólista tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="e94fd-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94fd-123">-DefaultProfile</span></span>
<span data-ttu-id="e94fd-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e94fd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e94fd-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="e94fd-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="e94fd-126">Megjelölés, amely azt adja meg, hogy a fájlfeltöltés esetén engedélyezve legyenek-e az értesítések.</span><span class="sxs-lookup"><span data-stu-id="e94fd-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="e94fd-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="e94fd-128">Retenciós idő napokban.</span><span class="sxs-lookup"><span data-stu-id="e94fd-128">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="e94fd-129">-FallbackRoute</span></span>
<span data-ttu-id="e94fd-130">Az útválasztási tartalék útvonala</span><span class="sxs-lookup"><span data-stu-id="e94fd-130">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="e94fd-131">-FileUploadContainerName</span></span>
<span data-ttu-id="e94fd-132">Annak a tárolónak a neve, amelybe fel szeretné tölteni a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="e94fd-132">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e94fd-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="e94fd-134">A maximális kézbesítési szám a fájlfeltöltés-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="e94fd-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="e94fd-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="e94fd-136">A fájlfeltöltés értesítési várólistájában szereplő üzenetek értékének megadására szolgáló idő.</span><span class="sxs-lookup"><span data-stu-id="e94fd-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="e94fd-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="e94fd-138">A feltöltéshez létrehozott SAS-URI-hoz használható idő.</span><span class="sxs-lookup"><span data-stu-id="e94fd-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="e94fd-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="e94fd-140">A tárterület-kapcsolat karakterlánca a fájlok feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="e94fd-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e94fd-141">-Name</span></span>
<span data-ttu-id="e94fd-142">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="e94fd-142">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="e94fd-144">A műveletek figyeléséhez kapcsolódó tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="e94fd-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94fd-145">-ResourceGroupName</span></span>
<span data-ttu-id="e94fd-146">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e94fd-146">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-147">-Útvonalak</span><span class="sxs-lookup"><span data-stu-id="e94fd-147">-Routes</span></span>
<span data-ttu-id="e94fd-148">Az útválasztáshoz hozzáadni kívánt útvonalak</span><span class="sxs-lookup"><span data-stu-id="e94fd-148">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="e94fd-149">-RoutingProperties</span></span>
<span data-ttu-id="e94fd-150">Az útválasztási üzenetek külső végpontokhoz való útválasztási tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="e94fd-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e94fd-151">-SkuName</span></span>
<span data-ttu-id="e94fd-152">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="e94fd-152">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-153">-Egységek</span><span class="sxs-lookup"><span data-stu-id="e94fd-153">-Units</span></span>
<span data-ttu-id="e94fd-154">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="e94fd-154">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e94fd-155">-Confirm</span></span>
<span data-ttu-id="e94fd-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e94fd-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94fd-157">-WhatIf</span></span>
<span data-ttu-id="e94fd-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e94fd-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94fd-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e94fd-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94fd-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94fd-160">CommonParameters</span></span>
<span data-ttu-id="e94fd-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e94fd-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94fd-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e94fd-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94fd-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e94fd-163">INPUTS</span></span>

### <span data-ttu-id="e94fd-164">System. String</span><span class="sxs-lookup"><span data-stu-id="e94fd-164">System.String</span></span>

## <span data-ttu-id="e94fd-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e94fd-165">OUTPUTS</span></span>

### <span data-ttu-id="e94fd-166">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e94fd-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e94fd-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e94fd-167">NOTES</span></span>

## <span data-ttu-id="e94fd-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e94fd-168">RELATED LINKS</span></span>
