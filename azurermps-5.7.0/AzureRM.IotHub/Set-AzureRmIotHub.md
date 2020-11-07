---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680715"
---
# <span data-ttu-id="6dd12-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="6dd12-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="6dd12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6dd12-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd12-103">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6dd12-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6dd12-104">SYNTAX</span></span>

### <span data-ttu-id="6dd12-105">UpdateSku (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6dd12-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd12-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="6dd12-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd12-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="6dd12-113">DESCRIPTION</span></span>
<span data-ttu-id="6dd12-114">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6dd12-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="6dd12-115">Példák</span><span class="sxs-lookup"><span data-stu-id="6dd12-115">EXAMPLES</span></span>

### <span data-ttu-id="6dd12-116">Példa 1 a SKU frissítése</span><span class="sxs-lookup"><span data-stu-id="6dd12-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="6dd12-117">Frissítse a SKU-ot S1-re, és a "myiothub" nevű IotHub az 5 egységre</span><span class="sxs-lookup"><span data-stu-id="6dd12-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="6dd12-118">2. példa a eventhub tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="6dd12-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="6dd12-119">A "myiothub" nevű IotHub telemetriai-és operationsmonitoringevents-eseményeinek frissítése a napok és a 4 közötti adatmegőrzési idő között</span><span class="sxs-lookup"><span data-stu-id="6dd12-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6dd12-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6dd12-120">PARAMETERS</span></span>

### <span data-ttu-id="6dd12-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="6dd12-121">-CloudToDevice</span></span>
<span data-ttu-id="6dd12-122">A felhőalapú eszközhöz tartozó parancssori várólista tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="6dd12-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd12-123">-DefaultProfile</span></span>
<span data-ttu-id="6dd12-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6dd12-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dd12-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="6dd12-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="6dd12-126">Megjelölés, amely azt adja meg, hogy a fájlfeltöltés esetén engedélyezve legyenek-e az értesítések.</span><span class="sxs-lookup"><span data-stu-id="6dd12-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="6dd12-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="6dd12-128">Retenciós idő napokban.</span><span class="sxs-lookup"><span data-stu-id="6dd12-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="6dd12-129">-FallbackRoute</span></span>
<span data-ttu-id="6dd12-130">Az útválasztási tartalék útvonala</span><span class="sxs-lookup"><span data-stu-id="6dd12-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="6dd12-131">-FileUploadContainerName</span></span>
<span data-ttu-id="6dd12-132">Annak a tárolónak a neve, amelybe fel szeretné tölteni a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="6dd12-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="6dd12-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="6dd12-134">A maximális kézbesítési szám a fájlfeltöltés-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="6dd12-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="6dd12-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="6dd12-136">A fájlfeltöltés értesítési várólistájában szereplő üzenetek értékének megadására szolgáló idő.</span><span class="sxs-lookup"><span data-stu-id="6dd12-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="6dd12-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="6dd12-138">A feltöltéshez létrehozott SAS-URI-hoz használható idő.</span><span class="sxs-lookup"><span data-stu-id="6dd12-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="6dd12-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="6dd12-140">A tárterület-kapcsolat karakterlánca a fájlok feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="6dd12-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6dd12-141">-Name</span></span>
<span data-ttu-id="6dd12-142">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="6dd12-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="6dd12-144">A műveletek figyeléséhez kapcsolódó tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="6dd12-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd12-145">-ResourceGroupName</span></span>
<span data-ttu-id="6dd12-146">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6dd12-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-147">-Útvonalak</span><span class="sxs-lookup"><span data-stu-id="6dd12-147">-Routes</span></span>
<span data-ttu-id="6dd12-148">Az útválasztáshoz hozzáadni kívánt útvonalak</span><span class="sxs-lookup"><span data-stu-id="6dd12-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="6dd12-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-149">-RoutingProperties</span></span>
<span data-ttu-id="6dd12-150">Az útválasztási üzenetek külső végpontokhoz való útválasztási tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="6dd12-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6dd12-151">-SkuName</span></span>
<span data-ttu-id="6dd12-152">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="6dd12-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-153">-Egységek</span><span class="sxs-lookup"><span data-stu-id="6dd12-153">-Units</span></span>
<span data-ttu-id="6dd12-154">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="6dd12-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6dd12-155">-Confirm</span></span>
<span data-ttu-id="6dd12-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6dd12-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd12-157">-WhatIf</span></span>
<span data-ttu-id="6dd12-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6dd12-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd12-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6dd12-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd12-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd12-160">CommonParameters</span></span>
<span data-ttu-id="6dd12-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6dd12-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd12-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd12-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd12-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dd12-163">INPUTS</span></span>

### <span data-ttu-id="6dd12-164">System. String</span><span class="sxs-lookup"><span data-stu-id="6dd12-164">System.String</span></span>
<span data-ttu-id="6dd12-165">Microsoft. Azure. Command. Management. IotHub. models. PSCloudToDeviceProperties Microsoft. Azure. Command. Management. IotHub. models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="6dd12-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="6dd12-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dd12-166">OUTPUTS</span></span>

### <span data-ttu-id="6dd12-167">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6dd12-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="6dd12-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6dd12-168">NOTES</span></span>

## <span data-ttu-id="6dd12-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6dd12-169">RELATED LINKS</span></span>

