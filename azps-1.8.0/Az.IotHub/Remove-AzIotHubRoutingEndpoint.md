---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1ff1ba2d8e3a4a7ce8a80c364ff8ccee3e91d8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835829"
---
# <span data-ttu-id="4d188-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d188-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="4d188-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d188-102">SYNOPSIS</span></span>
<span data-ttu-id="4d188-103">A IoT-hub végpontjának törlése</span><span class="sxs-lookup"><span data-stu-id="4d188-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="4d188-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d188-104">SYNTAX</span></span>

### <span data-ttu-id="4d188-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d188-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d188-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d188-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d188-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d188-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d188-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d188-108">DESCRIPTION</span></span>
<span data-ttu-id="4d188-109">Végpont törlése</span><span class="sxs-lookup"><span data-stu-id="4d188-109">Delete an endpoint.</span></span> <span data-ttu-id="4d188-110">Ne felejtse el törölni a végpontot használó útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="4d188-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="4d188-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4d188-111">EXAMPLES</span></span>

### <span data-ttu-id="4d188-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d188-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="4d188-113">Törölje a "E2" végpontot az "myiothub" IoT-hub-ról.</span><span class="sxs-lookup"><span data-stu-id="4d188-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="4d188-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d188-114">PARAMETERS</span></span>

### <span data-ttu-id="4d188-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d188-115">-DefaultProfile</span></span>
<span data-ttu-id="4d188-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d188-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d188-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4d188-117">-EndpointName</span></span>
<span data-ttu-id="4d188-118">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="4d188-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4d188-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="4d188-119">-EndpointType</span></span>
<span data-ttu-id="4d188-120">A műveletterv végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="4d188-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4d188-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d188-121">-InputObject</span></span>
<span data-ttu-id="4d188-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="4d188-122">IotHub Object</span></span>

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

### <span data-ttu-id="4d188-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d188-123">-Name</span></span>
<span data-ttu-id="4d188-124">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="4d188-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4d188-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d188-125">-PassThru</span></span>
<span data-ttu-id="4d188-126">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="4d188-126">Allows to return the boolean object.</span></span> <span data-ttu-id="4d188-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4d188-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d188-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d188-128">-ResourceGroupName</span></span>
<span data-ttu-id="4d188-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4d188-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4d188-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d188-130">-ResourceId</span></span>
<span data-ttu-id="4d188-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4d188-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4d188-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d188-132">-Confirm</span></span>
<span data-ttu-id="4d188-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d188-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d188-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d188-134">-WhatIf</span></span>
<span data-ttu-id="4d188-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d188-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d188-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d188-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d188-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d188-137">CommonParameters</span></span>
<span data-ttu-id="4d188-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d188-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d188-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d188-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d188-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d188-140">INPUTS</span></span>

### <span data-ttu-id="4d188-141">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4d188-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4d188-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4d188-142">System.String</span></span>

## <span data-ttu-id="4d188-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d188-143">OUTPUTS</span></span>

### <span data-ttu-id="4d188-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d188-144">System.Boolean</span></span>

## <span data-ttu-id="4d188-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d188-145">NOTES</span></span>

## <span data-ttu-id="4d188-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d188-146">RELATED LINKS</span></span>
