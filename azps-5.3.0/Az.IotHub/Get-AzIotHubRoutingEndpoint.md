---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480143"
---
# <span data-ttu-id="d148d-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="d148d-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="d148d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d148d-102">SYNOPSIS</span></span>
<span data-ttu-id="d148d-103">Információ az IoT-központ összes végpontjáról</span><span class="sxs-lookup"><span data-stu-id="d148d-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="d148d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d148d-104">SYNTAX</span></span>

### <span data-ttu-id="d148d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d148d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d148d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d148d-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d148d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d148d-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d148d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d148d-108">DESCRIPTION</span></span>
<span data-ttu-id="d148d-109">Információ a végpontról.</span><span class="sxs-lookup"><span data-stu-id="d148d-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="d148d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d148d-110">EXAMPLES</span></span>

### <span data-ttu-id="d148d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d148d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="d148d-112">Szerezze be az összes végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="d148d-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d148d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d148d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="d148d-114">Szerezze be az EventHub típusú összes végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="d148d-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="d148d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d148d-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="d148d-116">Szerezze be az EventHub típusú összes végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="d148d-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d148d-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="d148d-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="d148d-118">Végpontinformációk lekérte a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="d148d-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d148d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d148d-119">PARAMETERS</span></span>

### <span data-ttu-id="d148d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d148d-120">-DefaultProfile</span></span>
<span data-ttu-id="d148d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d148d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d148d-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d148d-122">-EndpointName</span></span>
<span data-ttu-id="d148d-123">Az Útválasztási végpont neve</span><span class="sxs-lookup"><span data-stu-id="d148d-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="d148d-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d148d-124">-EndpointType</span></span>
<span data-ttu-id="d148d-125">Az Útválasztási végpont típusa</span><span class="sxs-lookup"><span data-stu-id="d148d-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="d148d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d148d-126">-InputObject</span></span>
<span data-ttu-id="d148d-127">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="d148d-127">IotHub Object</span></span>

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

### <span data-ttu-id="d148d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d148d-128">-Name</span></span>
<span data-ttu-id="d148d-129">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="d148d-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d148d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d148d-130">-ResourceGroupName</span></span>
<span data-ttu-id="d148d-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d148d-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d148d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d148d-132">-ResourceId</span></span>
<span data-ttu-id="d148d-133">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d148d-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d148d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d148d-134">CommonParameters</span></span>
<span data-ttu-id="d148d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d148d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d148d-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d148d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d148d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d148d-137">INPUTS</span></span>

### <span data-ttu-id="d148d-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d148d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d148d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d148d-139">System.String</span></span>

## <span data-ttu-id="d148d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d148d-140">OUTPUTS</span></span>

### <span data-ttu-id="d148d-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="d148d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="d148d-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d148d-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d148d-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="d148d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="d148d-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="d148d-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="d148d-145">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="d148d-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="d148d-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="d148d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="d148d-147">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d148d-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="d148d-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="d148d-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="d148d-149">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="d148d-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="d148d-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d148d-150">NOTES</span></span>

## <span data-ttu-id="d148d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d148d-151">RELATED LINKS</span></span>
