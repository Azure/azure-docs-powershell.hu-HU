---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680101"
---
# <span data-ttu-id="e6d4b-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6d4b-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="e6d4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d4b-103">Információk beszerzése a IoT-hub összes végpontján</span><span class="sxs-lookup"><span data-stu-id="e6d4b-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6d4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6d4b-104">SYNTAX</span></span>

### <span data-ttu-id="e6d4b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6d4b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6d4b-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d4b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e6d4b-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6d4b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6d4b-108">DESCRIPTION</span></span>
<span data-ttu-id="e6d4b-109">Információkat kaphat a végpontról.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="e6d4b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e6d4b-110">EXAMPLES</span></span>

### <span data-ttu-id="e6d4b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6d4b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="e6d4b-112">A "myiothub" IoT-hub összes végpontjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e6d4b-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e6d4b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6d4b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="e6d4b-114">A EventHub Type ("myiothub" IoT hub) végpontjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e6d4b-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="e6d4b-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e6d4b-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e6d4b-116">A EventHub Type ("myiothub" IoT hub) végpontjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e6d4b-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e6d4b-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="e6d4b-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e6d4b-118">Végponti adatok beszerzése "myiothub" IoT hub-ról</span><span class="sxs-lookup"><span data-stu-id="e6d4b-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e6d4b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6d4b-119">PARAMETERS</span></span>

### <span data-ttu-id="e6d4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d4b-120">-DefaultProfile</span></span>
<span data-ttu-id="e6d4b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6d4b-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e6d4b-122">-EndpointName</span></span>
<span data-ttu-id="e6d4b-123">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="e6d4b-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="e6d4b-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e6d4b-124">-EndpointType</span></span>
<span data-ttu-id="e6d4b-125">A műveletterv végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="e6d4b-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="e6d4b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6d4b-126">-InputObject</span></span>
<span data-ttu-id="e6d4b-127">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="e6d4b-127">IotHub Object</span></span>

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

### <span data-ttu-id="e6d4b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-128">-Name</span></span>
<span data-ttu-id="e6d4b-129">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="e6d4b-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e6d4b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6d4b-130">-ResourceGroupName</span></span>
<span data-ttu-id="e6d4b-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e6d4b-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e6d4b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6d4b-132">-ResourceId</span></span>
<span data-ttu-id="e6d4b-133">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e6d4b-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e6d4b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d4b-134">CommonParameters</span></span>
<span data-ttu-id="e6d4b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6d4b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d4b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6d4b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d4b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6d4b-137">INPUTS</span></span>

### <span data-ttu-id="e6d4b-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e6d4b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="e6d4b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e6d4b-139">System.String</span></span>

## <span data-ttu-id="e6d4b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6d4b-140">OUTPUTS</span></span>

### <span data-ttu-id="e6d4b-141">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6d4b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="e6d4b-142">System. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. commands. IotHub, Version = 3.1.3.0, Culture = semleges, PublicKeyToken = null]] Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint. Collection. Generic. list 1 [[Microsoft. Azure. `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` commands. Management. IotHub. models. PSRoutingStorageContainerProperties, Microsoft. Azure. commands. IotHub, Version = 3.1.3.0, Culture = semleges, PublicKeyToken = null]] System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRoutingCustomEndpoint. IotHub</span><span class="sxs-lookup"><span data-stu-id="e6d4b-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6d4b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6d4b-143">NOTES</span></span>

## <span data-ttu-id="e6d4b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6d4b-144">RELATED LINKS</span></span>
