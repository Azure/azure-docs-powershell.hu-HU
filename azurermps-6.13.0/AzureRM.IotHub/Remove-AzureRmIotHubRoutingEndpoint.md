---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503652"
---
# <span data-ttu-id="cdb7c-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="cdb7c-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="cdb7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb7c-103">A IoT-hub végpontjának törlése</span><span class="sxs-lookup"><span data-stu-id="cdb7c-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdb7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdb7c-104">SYNTAX</span></span>

### <span data-ttu-id="cdb7c-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdb7c-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb7c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdb7c-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb7c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cdb7c-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb7c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdb7c-108">DESCRIPTION</span></span>
<span data-ttu-id="cdb7c-109">Végpont törlése</span><span class="sxs-lookup"><span data-stu-id="cdb7c-109">Delete an endpoint.</span></span> <span data-ttu-id="cdb7c-110">Ne felejtse el törölni a végpontot használó útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="cdb7c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cdb7c-111">EXAMPLES</span></span>

### <span data-ttu-id="cdb7c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cdb7c-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="cdb7c-113">Törölje a "E2" végpontot az "myiothub" IoT-hub-ról.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="cdb7c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdb7c-114">PARAMETERS</span></span>

### <span data-ttu-id="cdb7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb7c-115">-DefaultProfile</span></span>
<span data-ttu-id="cdb7c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb7c-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cdb7c-117">-EndpointName</span></span>
<span data-ttu-id="cdb7c-118">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="cdb7c-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cdb7c-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cdb7c-119">-EndpointType</span></span>
<span data-ttu-id="cdb7c-120">A műveletterv végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="cdb7c-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb7c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdb7c-121">-InputObject</span></span>
<span data-ttu-id="cdb7c-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="cdb7c-122">IotHub Object</span></span>

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

### <span data-ttu-id="cdb7c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdb7c-123">-Name</span></span>
<span data-ttu-id="cdb7c-124">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="cdb7c-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cdb7c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdb7c-125">-PassThru</span></span>
<span data-ttu-id="cdb7c-126">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-126">Allows to return the boolean object.</span></span> <span data-ttu-id="cdb7c-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb7c-128">-ResourceGroupName</span></span>
<span data-ttu-id="cdb7c-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cdb7c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cdb7c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb7c-130">-ResourceId</span></span>
<span data-ttu-id="cdb7c-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cdb7c-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cdb7c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdb7c-132">-Confirm</span></span>
<span data-ttu-id="cdb7c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb7c-134">-WhatIf</span></span>
<span data-ttu-id="cdb7c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb7c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdb7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb7c-137">CommonParameters</span></span>
<span data-ttu-id="cdb7c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdb7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb7c-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb7c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb7c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb7c-140">INPUTS</span></span>

### <span data-ttu-id="cdb7c-141">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cdb7c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="cdb7c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb7c-142">System.String</span></span>

## <span data-ttu-id="cdb7c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb7c-143">OUTPUTS</span></span>

### <span data-ttu-id="cdb7c-144">Microsoft. Azure. Command. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="cdb7c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="cdb7c-145">System. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. commands. IotHub, Version = 3.1.3.0, Culture = semleges, PublicKeyToken = null]] Microsoft. Azure. Command. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint. Collection. Generic. list 1 [[Microsoft. Azure. `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` commands. Management. IotHub. models. PSRoutingStorageContainerProperties, Microsoft. Azure. commands. IotHub, Version = 3.1.3.0, Culture = semleges, PublicKeyToken = null]] System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRoutingCustomEndpoint. IotHub</span><span class="sxs-lookup"><span data-stu-id="cdb7c-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cdb7c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdb7c-146">NOTES</span></span>

## <span data-ttu-id="cdb7c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdb7c-147">RELATED LINKS</span></span>
