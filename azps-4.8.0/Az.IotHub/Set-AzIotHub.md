---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025701"
---
# <span data-ttu-id="00186-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="00186-101">Set-AzIotHub</span></span>

## <span data-ttu-id="00186-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00186-102">SYNOPSIS</span></span>
<span data-ttu-id="00186-103">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="00186-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="00186-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00186-104">SYNTAX</span></span>

### <span data-ttu-id="00186-105">UpdateSku (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00186-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00186-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="00186-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00186-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="00186-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00186-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="00186-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00186-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="00186-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00186-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="00186-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00186-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="00186-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00186-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="00186-112">DESCRIPTION</span></span>
<span data-ttu-id="00186-113">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="00186-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="00186-114">Példák</span><span class="sxs-lookup"><span data-stu-id="00186-114">EXAMPLES</span></span>

### <span data-ttu-id="00186-115">Példa 1 a SKU frissítése</span><span class="sxs-lookup"><span data-stu-id="00186-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="00186-116">Frissítse a SKU-ot S1-re, és a "myiothub" nevű IotHub az 5 egységre</span><span class="sxs-lookup"><span data-stu-id="00186-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="00186-117">2. példa a eventhub tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="00186-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="00186-118">A telemetriai retenciós idejének frissítése a IotHub nevű "myiothub" nevű</span><span class="sxs-lookup"><span data-stu-id="00186-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="00186-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00186-119">PARAMETERS</span></span>

### <span data-ttu-id="00186-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="00186-120">-CloudToDevice</span></span>
<span data-ttu-id="00186-121">A felhőalapú eszközhöz tartozó parancssori várólista tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="00186-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="00186-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00186-122">-DefaultProfile</span></span>
<span data-ttu-id="00186-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="00186-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00186-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="00186-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="00186-125">Megjelölés, amely azt adja meg, hogy a fájlfeltöltés esetén engedélyezve legyenek-e az értesítések.</span><span class="sxs-lookup"><span data-stu-id="00186-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="00186-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="00186-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="00186-127">Retenciós idő napokban.</span><span class="sxs-lookup"><span data-stu-id="00186-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="00186-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="00186-128">-FallbackRoute</span></span>
<span data-ttu-id="00186-129">Az útválasztási tartalék útvonala</span><span class="sxs-lookup"><span data-stu-id="00186-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="00186-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="00186-130">-FileUploadContainerName</span></span>
<span data-ttu-id="00186-131">Annak a tárolónak a neve, amelybe fel szeretné tölteni a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="00186-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="00186-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="00186-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="00186-133">A maximális kézbesítési szám a fájlfeltöltés-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="00186-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="00186-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="00186-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="00186-135">A fájlfeltöltés értesítési várólistájában szereplő üzenetek értékének megadására szolgáló idő.</span><span class="sxs-lookup"><span data-stu-id="00186-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="00186-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="00186-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="00186-137">A feltöltéshez létrehozott SAS-URI-hoz használható idő.</span><span class="sxs-lookup"><span data-stu-id="00186-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="00186-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="00186-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="00186-139">A tárterület-kapcsolat karakterlánca a fájlok feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="00186-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="00186-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00186-140">-Name</span></span>
<span data-ttu-id="00186-141">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="00186-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="00186-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00186-142">-ResourceGroupName</span></span>
<span data-ttu-id="00186-143">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="00186-143">Resource Group Name</span></span>

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

### <span data-ttu-id="00186-144">-Útvonalak</span><span class="sxs-lookup"><span data-stu-id="00186-144">-Routes</span></span>
<span data-ttu-id="00186-145">Az útválasztáshoz hozzáadni kívánt útvonalak</span><span class="sxs-lookup"><span data-stu-id="00186-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="00186-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="00186-146">-RoutingProperties</span></span>
<span data-ttu-id="00186-147">Az útválasztási üzenetek külső végpontokhoz való útválasztási tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="00186-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="00186-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="00186-148">-SkuName</span></span>
<span data-ttu-id="00186-149">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="00186-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="00186-150">-Egységek</span><span class="sxs-lookup"><span data-stu-id="00186-150">-Units</span></span>
<span data-ttu-id="00186-151">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="00186-151">Number of Units</span></span>

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

### <span data-ttu-id="00186-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00186-152">-Confirm</span></span>
<span data-ttu-id="00186-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00186-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00186-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00186-154">-WhatIf</span></span>
<span data-ttu-id="00186-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00186-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00186-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00186-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00186-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00186-157">CommonParameters</span></span>
<span data-ttu-id="00186-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00186-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00186-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00186-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00186-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00186-160">INPUTS</span></span>

### <span data-ttu-id="00186-161">System. String</span><span class="sxs-lookup"><span data-stu-id="00186-161">System.String</span></span>

## <span data-ttu-id="00186-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00186-162">OUTPUTS</span></span>

### <span data-ttu-id="00186-163">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="00186-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="00186-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00186-164">NOTES</span></span>

## <span data-ttu-id="00186-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00186-165">RELATED LINKS</span></span>
