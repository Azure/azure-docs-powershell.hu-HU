---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495103"
---
# <span data-ttu-id="38bf1-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="38bf1-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="38bf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="38bf1-103">Végpont felvétele a IoT-hub-ba</span><span class="sxs-lookup"><span data-stu-id="38bf1-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38bf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38bf1-104">SYNTAX</span></span>

### <span data-ttu-id="38bf1-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38bf1-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38bf1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38bf1-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38bf1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38bf1-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38bf1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38bf1-108">DESCRIPTION</span></span>
<span data-ttu-id="38bf1-109">Új végpont felvétele a IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="38bf1-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="38bf1-110">A támogatott végpontokról további információt a következő témakörben talál: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="38bf1-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="38bf1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="38bf1-111">EXAMPLES</span></span>

### <span data-ttu-id="38bf1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38bf1-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="38bf1-113">Adjon hozzá egy új, "E2" EventHub a "myiothub" IoT hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="38bf1-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="38bf1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="38bf1-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="38bf1-115">Adjon hozzá egy új, "S1" AzureStorageContainer a "myiothub" IoT hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="38bf1-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="38bf1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38bf1-116">PARAMETERS</span></span>

### <span data-ttu-id="38bf1-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="38bf1-117">-ConnectionString</span></span>
<span data-ttu-id="38bf1-118">Az útválasztási végpont kapcsolati karakterlánca</span><span class="sxs-lookup"><span data-stu-id="38bf1-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bf1-119">-DefaultProfile</span></span>
<span data-ttu-id="38bf1-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38bf1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bf1-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="38bf1-121">-EndpointName</span></span>
<span data-ttu-id="38bf1-122">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="38bf1-122">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38bf1-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="38bf1-124">A végpont erőforráscsoport resoure</span><span class="sxs-lookup"><span data-stu-id="38bf1-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38bf1-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="38bf1-126">A végpont-erőforrás SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38bf1-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="38bf1-127">-EndpointType</span></span>
<span data-ttu-id="38bf1-128">A műveletterv végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="38bf1-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38bf1-129">-InputObject</span></span>
<span data-ttu-id="38bf1-130">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="38bf1-130">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38bf1-131">-Name</span></span>
<span data-ttu-id="38bf1-132">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="38bf1-132">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bf1-133">-ResourceGroupName</span></span>
<span data-ttu-id="38bf1-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="38bf1-134">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38bf1-135">-ResourceId</span></span>
<span data-ttu-id="38bf1-136">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="38bf1-136">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38bf1-137">-Confirm</span></span>
<span data-ttu-id="38bf1-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38bf1-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bf1-139">-WhatIf</span></span>
<span data-ttu-id="38bf1-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38bf1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bf1-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38bf1-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bf1-142">CommonParameters</span></span>
<span data-ttu-id="38bf1-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38bf1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bf1-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38bf1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bf1-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38bf1-145">INPUTS</span></span>

### <span data-ttu-id="38bf1-146">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="38bf1-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="38bf1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="38bf1-147">System.String</span></span>

## <span data-ttu-id="38bf1-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38bf1-148">OUTPUTS</span></span>

### <span data-ttu-id="38bf1-149">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="38bf1-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="38bf1-150">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint Microsoft. Azure. Command. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="38bf1-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="38bf1-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38bf1-151">NOTES</span></span>

## <span data-ttu-id="38bf1-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38bf1-152">RELATED LINKS</span></span>
