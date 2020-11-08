---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002909"
---
# <span data-ttu-id="a66ef-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a66ef-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a66ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a66ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a66ef-103">Végpont felvétele a IoT-hub-ba</span><span class="sxs-lookup"><span data-stu-id="a66ef-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="a66ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a66ef-104">SYNTAX</span></span>

### <span data-ttu-id="a66ef-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a66ef-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a66ef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a66ef-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a66ef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a66ef-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a66ef-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a66ef-108">DESCRIPTION</span></span>
<span data-ttu-id="a66ef-109">Új végpont felvétele a IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="a66ef-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="a66ef-110">A támogatott végpontokról további információt a következő témakörben talál: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="a66ef-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="a66ef-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a66ef-111">EXAMPLES</span></span>

### <span data-ttu-id="a66ef-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a66ef-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a66ef-113">Adjon hozzá egy új, "E2" EventHub a "myiothub" IoT hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="a66ef-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a66ef-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a66ef-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="a66ef-115">Adjon hozzá egy új, "S1" AzureStorageContainer a "myiothub" IoT hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="a66ef-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a66ef-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a66ef-116">PARAMETERS</span></span>

### <span data-ttu-id="a66ef-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a66ef-117">-ConnectionString</span></span>
<span data-ttu-id="a66ef-118">Az útválasztási végpont kapcsolati karakterlánca</span><span class="sxs-lookup"><span data-stu-id="a66ef-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66ef-119">-DefaultProfile</span></span>
<span data-ttu-id="a66ef-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a66ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a66ef-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a66ef-121">-EndpointName</span></span>
<span data-ttu-id="a66ef-122">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="a66ef-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a66ef-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a66ef-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="a66ef-124">A végpont-erőforrás erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="a66ef-124">Resource group of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ef-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a66ef-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="a66ef-126">A végpont-erőforrás SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a66ef-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ef-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a66ef-127">-EndpointType</span></span>
<span data-ttu-id="a66ef-128">A műveletterv végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="a66ef-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ef-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a66ef-129">-ContainerName</span></span>
<span data-ttu-id="a66ef-130">A tárolási tároló neve</span><span class="sxs-lookup"><span data-stu-id="a66ef-130">Name of the storage container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ef-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="a66ef-131">-Encoding</span></span>
<span data-ttu-id="a66ef-132">Válassza ki, hogy milyen formátumban szeretné továbbítani az adatait.</span><span class="sxs-lookup"><span data-stu-id="a66ef-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="a66ef-133">Kiválaszthatja a JSON vagy a AVRO.</span><span class="sxs-lookup"><span data-stu-id="a66ef-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="a66ef-134">Az alapértelmezett beállítás a AVRO.</span><span class="sxs-lookup"><span data-stu-id="a66ef-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ef-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a66ef-135">-InputObject</span></span>
<span data-ttu-id="a66ef-136">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a66ef-136">IotHub Object</span></span>

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

### <span data-ttu-id="a66ef-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a66ef-137">-Name</span></span>
<span data-ttu-id="a66ef-138">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="a66ef-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a66ef-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a66ef-139">-ResourceGroupName</span></span>
<span data-ttu-id="a66ef-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a66ef-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a66ef-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a66ef-141">-ResourceId</span></span>
<span data-ttu-id="a66ef-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a66ef-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a66ef-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a66ef-143">-Confirm</span></span>
<span data-ttu-id="a66ef-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a66ef-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a66ef-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66ef-145">-WhatIf</span></span>
<span data-ttu-id="a66ef-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a66ef-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a66ef-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a66ef-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a66ef-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66ef-148">CommonParameters</span></span>
<span data-ttu-id="a66ef-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a66ef-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66ef-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66ef-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66ef-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a66ef-151">INPUTS</span></span>

### <span data-ttu-id="a66ef-152">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a66ef-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a66ef-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a66ef-153">System.String</span></span>

## <span data-ttu-id="a66ef-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a66ef-154">OUTPUTS</span></span>

### <span data-ttu-id="a66ef-155">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="a66ef-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="a66ef-156">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="a66ef-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="a66ef-157">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="a66ef-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="a66ef-158">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a66ef-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="a66ef-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a66ef-159">NOTES</span></span>

## <span data-ttu-id="a66ef-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a66ef-160">RELATED LINKS</span></span>
