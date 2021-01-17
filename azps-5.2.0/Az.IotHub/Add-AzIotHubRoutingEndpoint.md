---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346757"
---
# <span data-ttu-id="a6b19-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6b19-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a6b19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6b19-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b19-103">Végpont hozzáadása az IoT-központhoz</span><span class="sxs-lookup"><span data-stu-id="a6b19-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="a6b19-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6b19-104">SYNTAX</span></span>

### <span data-ttu-id="a6b19-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6b19-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6b19-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6b19-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6b19-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6b19-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b19-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6b19-108">DESCRIPTION</span></span>
<span data-ttu-id="a6b19-109">Vegyen fel egy új végpontot az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="a6b19-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="a6b19-110">A támogatott végpontokról további információt a https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="a6b19-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="a6b19-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6b19-111">EXAMPLES</span></span>

### <span data-ttu-id="a6b19-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a6b19-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a6b19-113">Vegyen fel egy új EventHub típusú "E2" végpontot egy "myiothub" IoT-központba.</span><span class="sxs-lookup"><span data-stu-id="a6b19-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a6b19-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a6b19-114">Example 2</span></span>
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

<span data-ttu-id="a6b19-115">Vegyen fel egy új AzureStorageContainer típusú "S1" végpontot egy "myiothub" IoT-központba.</span><span class="sxs-lookup"><span data-stu-id="a6b19-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a6b19-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6b19-116">PARAMETERS</span></span>

### <span data-ttu-id="a6b19-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a6b19-117">-ConnectionString</span></span>
<span data-ttu-id="a6b19-118">A Routing Endpoint kapcsolati karakterlánca</span><span class="sxs-lookup"><span data-stu-id="a6b19-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a6b19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b19-119">-DefaultProfile</span></span>
<span data-ttu-id="a6b19-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6b19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b19-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a6b19-121">-EndpointName</span></span>
<span data-ttu-id="a6b19-122">Az Útválasztási végpont neve</span><span class="sxs-lookup"><span data-stu-id="a6b19-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a6b19-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6b19-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="a6b19-124">A Végpont erőforrás erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="a6b19-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="a6b19-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6b19-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="a6b19-126">A Végpont erőforrás SubscriptionId-e</span><span class="sxs-lookup"><span data-stu-id="a6b19-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="a6b19-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a6b19-127">-EndpointType</span></span>
<span data-ttu-id="a6b19-128">Az Útválasztási végpont típusa</span><span class="sxs-lookup"><span data-stu-id="a6b19-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a6b19-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a6b19-129">-ContainerName</span></span>
<span data-ttu-id="a6b19-130">A tároló neve</span><span class="sxs-lookup"><span data-stu-id="a6b19-130">Name of the storage container</span></span>

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

### <span data-ttu-id="a6b19-131">-Kódolás</span><span class="sxs-lookup"><span data-stu-id="a6b19-131">-Encoding</span></span>
<span data-ttu-id="a6b19-132">Válassza ki azt a formátumot, amelyben az adatokat át szeretné irányítatni.</span><span class="sxs-lookup"><span data-stu-id="a6b19-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="a6b19-133">A JSON vagy az AVRO lehetőséget is választhatja.</span><span class="sxs-lookup"><span data-stu-id="a6b19-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="a6b19-134">Az alapértelmezett beállítás az AVRO.</span><span class="sxs-lookup"><span data-stu-id="a6b19-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="a6b19-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6b19-135">-InputObject</span></span>
<span data-ttu-id="a6b19-136">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a6b19-136">IotHub Object</span></span>

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

### <span data-ttu-id="a6b19-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a6b19-137">-Name</span></span>
<span data-ttu-id="a6b19-138">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="a6b19-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a6b19-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b19-139">-ResourceGroupName</span></span>
<span data-ttu-id="a6b19-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a6b19-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6b19-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6b19-141">-ResourceId</span></span>
<span data-ttu-id="a6b19-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a6b19-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a6b19-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6b19-143">-Confirm</span></span>
<span data-ttu-id="a6b19-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a6b19-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b19-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b19-145">-WhatIf</span></span>
<span data-ttu-id="a6b19-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a6b19-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b19-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6b19-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b19-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b19-148">CommonParameters</span></span>
<span data-ttu-id="a6b19-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b19-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b19-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b19-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b19-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6b19-151">INPUTS</span></span>

### <span data-ttu-id="a6b19-152">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a6b19-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a6b19-153">System.String</span><span class="sxs-lookup"><span data-stu-id="a6b19-153">System.String</span></span>

## <span data-ttu-id="a6b19-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6b19-154">OUTPUTS</span></span>

### <span data-ttu-id="a6b19-155">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6b19-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="a6b19-156">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6b19-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="a6b19-157">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6b19-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="a6b19-158">Microsoft.Azure.Commands.Management.iotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6b19-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="a6b19-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6b19-159">NOTES</span></span>

## <span data-ttu-id="a6b19-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6b19-160">RELATED LINKS</span></span>
