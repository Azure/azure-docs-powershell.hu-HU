---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182734"
---
# <span data-ttu-id="a64f7-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a64f7-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a64f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a64f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a64f7-103">Információk beszerzése a IoT-hub összes végpontján</span><span class="sxs-lookup"><span data-stu-id="a64f7-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="a64f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a64f7-104">SYNTAX</span></span>

### <span data-ttu-id="a64f7-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a64f7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a64f7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a64f7-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a64f7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a64f7-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a64f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a64f7-108">DESCRIPTION</span></span>
<span data-ttu-id="a64f7-109">Információkat kaphat a végpontról.</span><span class="sxs-lookup"><span data-stu-id="a64f7-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="a64f7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a64f7-110">EXAMPLES</span></span>

### <span data-ttu-id="a64f7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a64f7-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="a64f7-112">A "myiothub" IoT-hub összes végpontjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a64f7-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a64f7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a64f7-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="a64f7-114">A EventHub Type ("myiothub" IoT hub) végpontjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a64f7-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="a64f7-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a64f7-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a64f7-116">A EventHub Type ("myiothub" IoT hub) végpontjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a64f7-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a64f7-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="a64f7-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a64f7-118">Végponti adatok beszerzése "myiothub" IoT hub-ról</span><span class="sxs-lookup"><span data-stu-id="a64f7-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a64f7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a64f7-119">PARAMETERS</span></span>

### <span data-ttu-id="a64f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a64f7-120">-DefaultProfile</span></span>
<span data-ttu-id="a64f7-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a64f7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a64f7-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a64f7-122">-EndpointName</span></span>
<span data-ttu-id="a64f7-123">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="a64f7-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a64f7-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a64f7-124">-EndpointType</span></span>
<span data-ttu-id="a64f7-125">A műveletterv végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="a64f7-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64f7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a64f7-126">-InputObject</span></span>
<span data-ttu-id="a64f7-127">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a64f7-127">IotHub Object</span></span>

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

### <span data-ttu-id="a64f7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a64f7-128">-Name</span></span>
<span data-ttu-id="a64f7-129">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="a64f7-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a64f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a64f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="a64f7-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a64f7-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a64f7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a64f7-132">-ResourceId</span></span>
<span data-ttu-id="a64f7-133">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a64f7-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a64f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a64f7-134">CommonParameters</span></span>
<span data-ttu-id="a64f7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a64f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a64f7-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a64f7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a64f7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a64f7-137">INPUTS</span></span>

### <span data-ttu-id="a64f7-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a64f7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a64f7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a64f7-139">System.String</span></span>

## <span data-ttu-id="a64f7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a64f7-140">OUTPUTS</span></span>

### <span data-ttu-id="a64f7-141">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="a64f7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="a64f7-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. parancsmagok. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a64f7-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a64f7-143">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="a64f7-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="a64f7-144">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="a64f7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="a64f7-145">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="a64f7-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="a64f7-146">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="a64f7-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="a64f7-147">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a64f7-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="a64f7-148">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="a64f7-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="a64f7-149">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="a64f7-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="a64f7-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a64f7-150">NOTES</span></span>

## <span data-ttu-id="a64f7-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a64f7-151">RELATED LINKS</span></span>
