---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011417"
---
# <span data-ttu-id="781cc-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="781cc-101">Set-AzIotHub</span></span>

## <span data-ttu-id="781cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="781cc-102">SYNOPSIS</span></span>
<span data-ttu-id="781cc-103">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="781cc-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="781cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="781cc-104">SYNTAX</span></span>

### <span data-ttu-id="781cc-105">UpdateSku (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="781cc-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781cc-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="781cc-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781cc-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="781cc-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781cc-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="781cc-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781cc-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="781cc-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781cc-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="781cc-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781cc-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="781cc-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="781cc-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="781cc-112">DESCRIPTION</span></span>
<span data-ttu-id="781cc-113">Frissíti egy IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="781cc-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="781cc-114">Példák</span><span class="sxs-lookup"><span data-stu-id="781cc-114">EXAMPLES</span></span>

### <span data-ttu-id="781cc-115">Példa 1 a SKU frissítése</span><span class="sxs-lookup"><span data-stu-id="781cc-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="781cc-116">Frissítse a SKU-ot S1-re, és a "myiothub" nevű IotHub az 5 egységre</span><span class="sxs-lookup"><span data-stu-id="781cc-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="781cc-117">2. példa a eventhub tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="781cc-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="781cc-118">A telemetriai retenciós idejének frissítése a IotHub nevű "myiothub" nevű</span><span class="sxs-lookup"><span data-stu-id="781cc-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="781cc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="781cc-119">PARAMETERS</span></span>

### <span data-ttu-id="781cc-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="781cc-120">-CloudToDevice</span></span>
<span data-ttu-id="781cc-121">A felhőalapú eszközhöz tartozó parancssori várólista tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="781cc-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="781cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781cc-122">-DefaultProfile</span></span>
<span data-ttu-id="781cc-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="781cc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="781cc-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="781cc-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="781cc-125">Megjelölés, amely azt adja meg, hogy a fájlfeltöltés esetén engedélyezve legyenek-e az értesítések.</span><span class="sxs-lookup"><span data-stu-id="781cc-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="781cc-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="781cc-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="781cc-127">Retenciós idő napokban.</span><span class="sxs-lookup"><span data-stu-id="781cc-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="781cc-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="781cc-128">-FallbackRoute</span></span>
<span data-ttu-id="781cc-129">Az útválasztási tartalék útvonala</span><span class="sxs-lookup"><span data-stu-id="781cc-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="781cc-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="781cc-130">-FileUploadContainerName</span></span>
<span data-ttu-id="781cc-131">Annak a tárolónak a neve, amelybe fel szeretné tölteni a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="781cc-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="781cc-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="781cc-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="781cc-133">A maximális kézbesítési szám a fájlfeltöltés-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="781cc-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="781cc-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="781cc-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="781cc-135">A fájlfeltöltés értesítési várólistájában szereplő üzenetek értékének megadására szolgáló idő.</span><span class="sxs-lookup"><span data-stu-id="781cc-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="781cc-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="781cc-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="781cc-137">A feltöltéshez létrehozott SAS-URI-hoz használható idő.</span><span class="sxs-lookup"><span data-stu-id="781cc-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="781cc-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="781cc-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="781cc-139">A tárterület-kapcsolat karakterlánca a fájlok feltöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="781cc-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="781cc-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="781cc-140">-Name</span></span>
<span data-ttu-id="781cc-141">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="781cc-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="781cc-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781cc-142">-ResourceGroupName</span></span>
<span data-ttu-id="781cc-143">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="781cc-143">Resource Group Name</span></span>

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

### <span data-ttu-id="781cc-144">-Útvonalak</span><span class="sxs-lookup"><span data-stu-id="781cc-144">-Routes</span></span>
<span data-ttu-id="781cc-145">Az útválasztáshoz hozzáadni kívánt útvonalak</span><span class="sxs-lookup"><span data-stu-id="781cc-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="781cc-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="781cc-146">-RoutingProperties</span></span>
<span data-ttu-id="781cc-147">Az útválasztási üzenetek külső végpontokhoz való útválasztási tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="781cc-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="781cc-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="781cc-148">-SkuName</span></span>
<span data-ttu-id="781cc-149">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="781cc-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="781cc-150">-Egységek</span><span class="sxs-lookup"><span data-stu-id="781cc-150">-Units</span></span>
<span data-ttu-id="781cc-151">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="781cc-151">Number of Units</span></span>

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

### <span data-ttu-id="781cc-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="781cc-152">-Confirm</span></span>
<span data-ttu-id="781cc-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="781cc-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="781cc-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="781cc-154">-WhatIf</span></span>
<span data-ttu-id="781cc-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="781cc-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="781cc-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="781cc-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="781cc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781cc-157">CommonParameters</span></span>
<span data-ttu-id="781cc-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="781cc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781cc-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="781cc-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781cc-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="781cc-160">INPUTS</span></span>

### <span data-ttu-id="781cc-161">System. String</span><span class="sxs-lookup"><span data-stu-id="781cc-161">System.String</span></span>

## <span data-ttu-id="781cc-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="781cc-162">OUTPUTS</span></span>

### <span data-ttu-id="781cc-163">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="781cc-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="781cc-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="781cc-164">NOTES</span></span>

## <span data-ttu-id="781cc-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="781cc-165">RELATED LINKS</span></span>
