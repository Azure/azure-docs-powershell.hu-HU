---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155435"
---
# <span data-ttu-id="0abbb-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="0abbb-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="0abbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0abbb-102">SYNOPSIS</span></span>
<span data-ttu-id="0abbb-103">Információ az IoT-központ összes végpontjáról</span><span class="sxs-lookup"><span data-stu-id="0abbb-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="0abbb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0abbb-104">SYNTAX</span></span>

### <span data-ttu-id="0abbb-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0abbb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0abbb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0abbb-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0abbb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0abbb-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0abbb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0abbb-108">DESCRIPTION</span></span>
<span data-ttu-id="0abbb-109">Információ a végpontról.</span><span class="sxs-lookup"><span data-stu-id="0abbb-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="0abbb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0abbb-110">EXAMPLES</span></span>

### <span data-ttu-id="0abbb-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0abbb-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="0abbb-112">Szerezze be az összes végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="0abbb-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="0abbb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0abbb-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="0abbb-114">Szerezze be az EventHub típusú összes végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="0abbb-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="0abbb-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="0abbb-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="0abbb-116">Szerezze be az EventHub típusú összes végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="0abbb-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="0abbb-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="0abbb-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="0abbb-118">Végpontinformációk lekérte a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="0abbb-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="0abbb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0abbb-119">PARAMETERS</span></span>

### <span data-ttu-id="0abbb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abbb-120">-DefaultProfile</span></span>
<span data-ttu-id="0abbb-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0abbb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0abbb-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0abbb-122">-EndpointName</span></span>
<span data-ttu-id="0abbb-123">Az Útválasztási végpont neve</span><span class="sxs-lookup"><span data-stu-id="0abbb-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="0abbb-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0abbb-124">-EndpointType</span></span>
<span data-ttu-id="0abbb-125">Az Útválasztási végpont típusa</span><span class="sxs-lookup"><span data-stu-id="0abbb-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="0abbb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0abbb-126">-InputObject</span></span>
<span data-ttu-id="0abbb-127">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="0abbb-127">IotHub Object</span></span>

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

### <span data-ttu-id="0abbb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0abbb-128">-Name</span></span>
<span data-ttu-id="0abbb-129">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="0abbb-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0abbb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abbb-130">-ResourceGroupName</span></span>
<span data-ttu-id="0abbb-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0abbb-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0abbb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0abbb-132">-ResourceId</span></span>
<span data-ttu-id="0abbb-133">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0abbb-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0abbb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abbb-134">CommonParameters</span></span>
<span data-ttu-id="0abbb-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0abbb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abbb-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0abbb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abbb-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0abbb-137">INPUTS</span></span>

### <span data-ttu-id="0abbb-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0abbb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0abbb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0abbb-139">System.String</span></span>

## <span data-ttu-id="0abbb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0abbb-140">OUTPUTS</span></span>

### <span data-ttu-id="0abbb-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="0abbb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="0abbb-142">System.Collections.Generic.List'1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0abbb-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0abbb-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="0abbb-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="0abbb-144">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="0abbb-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="0abbb-145">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="0abbb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="0abbb-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="0abbb-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="0abbb-147">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0abbb-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="0abbb-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="0abbb-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="0abbb-149">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="0abbb-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="0abbb-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0abbb-150">NOTES</span></span>

## <span data-ttu-id="0abbb-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0abbb-151">RELATED LINKS</span></span>
