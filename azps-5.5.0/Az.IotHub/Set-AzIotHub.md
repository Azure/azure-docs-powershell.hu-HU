---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157579"
---
# <span data-ttu-id="ccdd8-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="ccdd8-101">Set-AzIotHub</span></span>

## <span data-ttu-id="ccdd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccdd8-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdd8-103">Frissíti az IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="ccdd8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ccdd8-104">SYNTAX</span></span>

### <span data-ttu-id="ccdd8-105">UpdateSku (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccdd8-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdd8-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="ccdd8-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdd8-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="ccdd8-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdd8-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="ccdd8-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdd8-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="ccdd8-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdd8-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="ccdd8-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdd8-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="ccdd8-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdd8-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ccdd8-112">DESCRIPTION</span></span>
<span data-ttu-id="ccdd8-113">Frissíti az IotHub tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="ccdd8-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ccdd8-114">EXAMPLES</span></span>

### <span data-ttu-id="ccdd8-115">1. példa a termékváltozat frissítése</span><span class="sxs-lookup"><span data-stu-id="ccdd8-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="ccdd8-116">Frissítse a termékváltozatot S1-re, az egységeket pedig 5-re a "myiothub" nevű IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="ccdd8-117">2. példa az eventhub tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="ccdd8-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="ccdd8-118">Frissítse a telemetriai adatok megőrzési idejét napokban a 4-esre a "myiothub" nevű IotHub esetén.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ccdd8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccdd8-119">PARAMETERS</span></span>

### <span data-ttu-id="ccdd8-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="ccdd8-120">-CloudToDevice</span></span>
<span data-ttu-id="ccdd8-121">A felhőből az eszközre vonatkozó parancssor tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="ccdd8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdd8-122">-DefaultProfile</span></span>
<span data-ttu-id="ccdd8-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ccdd8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccdd8-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="ccdd8-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="ccdd8-125">Flag that specifies that notifications should be enabled for file upload.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="ccdd8-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="ccdd8-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="ccdd8-127">Adatmegőrzési idő napokban.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="ccdd8-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="ccdd8-128">-FallbackRoute</span></span>
<span data-ttu-id="ccdd8-129">Útválasztási tartalék útvonal</span><span class="sxs-lookup"><span data-stu-id="ccdd8-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="ccdd8-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="ccdd8-130">-FileUploadContainerName</span></span>
<span data-ttu-id="ccdd8-131">Annak a tárolónak a neve, amelybe fel kell töltenie a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="ccdd8-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="ccdd8-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="ccdd8-133">A fájlfeltöltési értesítések maximális kézbesítési száma.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="ccdd8-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="ccdd8-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="ccdd8-135">A fájlfeltöltési értesítési várólistán lévő üzenetek valós értékkel való feltöltésének ideje.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="ccdd8-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="ccdd8-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="ccdd8-137">Itt az ideje a fájlfeltöltéshez létrehozott SAS Uri-nak.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="ccdd8-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="ccdd8-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="ccdd8-139">A fájlok feltöltéséhez szükséges tárterület-kapcsolati karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="ccdd8-140">-Name</span><span class="sxs-lookup"><span data-stu-id="ccdd8-140">-Name</span></span>
<span data-ttu-id="ccdd8-141">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="ccdd8-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="ccdd8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdd8-142">-ResourceGroupName</span></span>
<span data-ttu-id="ccdd8-143">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ccdd8-143">Resource Group Name</span></span>

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

### <span data-ttu-id="ccdd8-144">-Routes</span><span class="sxs-lookup"><span data-stu-id="ccdd8-144">-Routes</span></span>
<span data-ttu-id="ccdd8-145">Útvonaltervezéshez hozzáadható útvonalak</span><span class="sxs-lookup"><span data-stu-id="ccdd8-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="ccdd8-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="ccdd8-146">-RoutingProperties</span></span>
<span data-ttu-id="ccdd8-147">The Routing properties for routing messages to external endpoints</span><span class="sxs-lookup"><span data-stu-id="ccdd8-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="ccdd8-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ccdd8-148">-SkuName</span></span>
<span data-ttu-id="ccdd8-149">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="ccdd8-150">-Egység</span><span class="sxs-lookup"><span data-stu-id="ccdd8-150">-Units</span></span>
<span data-ttu-id="ccdd8-151">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="ccdd8-151">Number of Units</span></span>

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

### <span data-ttu-id="ccdd8-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccdd8-152">-Confirm</span></span>
<span data-ttu-id="ccdd8-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccdd8-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdd8-154">-WhatIf</span></span>
<span data-ttu-id="ccdd8-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdd8-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccdd8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdd8-157">CommonParameters</span></span>
<span data-ttu-id="ccdd8-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdd8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdd8-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdd8-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdd8-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccdd8-160">INPUTS</span></span>

### <span data-ttu-id="ccdd8-161">System.String</span><span class="sxs-lookup"><span data-stu-id="ccdd8-161">System.String</span></span>

## <span data-ttu-id="ccdd8-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccdd8-162">OUTPUTS</span></span>

### <span data-ttu-id="ccdd8-163">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ccdd8-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="ccdd8-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ccdd8-164">NOTES</span></span>

## <span data-ttu-id="ccdd8-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccdd8-165">RELATED LINKS</span></span>
