---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356914"
---
# <span data-ttu-id="91ede-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ede-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="91ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ede-102">SYNOPSIS</span></span>
<span data-ttu-id="91ede-103">Az IoT-központ végpontjának törlése</span><span class="sxs-lookup"><span data-stu-id="91ede-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="91ede-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91ede-104">SYNTAX</span></span>

### <span data-ttu-id="91ede-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91ede-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91ede-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91ede-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91ede-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91ede-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ede-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91ede-108">DESCRIPTION</span></span>
<span data-ttu-id="91ede-109">Egy végpont törlése.</span><span class="sxs-lookup"><span data-stu-id="91ede-109">Delete an endpoint.</span></span> <span data-ttu-id="91ede-110">Ne felejtsen el törölni minden olyan útvonalat, amely ezt a végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="91ede-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="91ede-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91ede-111">EXAMPLES</span></span>

### <span data-ttu-id="91ede-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="91ede-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="91ede-113">Törölje az "E2" végpontot a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="91ede-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="91ede-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91ede-114">PARAMETERS</span></span>

### <span data-ttu-id="91ede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ede-115">-DefaultProfile</span></span>
<span data-ttu-id="91ede-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91ede-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91ede-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="91ede-117">-EndpointName</span></span>
<span data-ttu-id="91ede-118">Az Útválasztási végpont neve</span><span class="sxs-lookup"><span data-stu-id="91ede-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="91ede-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="91ede-119">-EndpointType</span></span>
<span data-ttu-id="91ede-120">Az Útválasztási végpont típusa</span><span class="sxs-lookup"><span data-stu-id="91ede-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="91ede-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91ede-121">-InputObject</span></span>
<span data-ttu-id="91ede-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="91ede-122">IotHub Object</span></span>

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

### <span data-ttu-id="91ede-123">-Name</span><span class="sxs-lookup"><span data-stu-id="91ede-123">-Name</span></span>
<span data-ttu-id="91ede-124">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="91ede-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="91ede-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91ede-125">-PassThru</span></span>
<span data-ttu-id="91ede-126">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="91ede-126">Allows to return the boolean object.</span></span> <span data-ttu-id="91ede-127">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="91ede-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91ede-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ede-128">-ResourceGroupName</span></span>
<span data-ttu-id="91ede-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="91ede-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91ede-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91ede-130">-ResourceId</span></span>
<span data-ttu-id="91ede-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="91ede-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="91ede-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91ede-132">-Confirm</span></span>
<span data-ttu-id="91ede-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="91ede-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ede-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ede-134">-WhatIf</span></span>
<span data-ttu-id="91ede-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="91ede-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ede-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91ede-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ede-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ede-137">CommonParameters</span></span>
<span data-ttu-id="91ede-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ede-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ede-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ede-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ede-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91ede-140">INPUTS</span></span>

### <span data-ttu-id="91ede-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="91ede-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="91ede-142">System.String</span><span class="sxs-lookup"><span data-stu-id="91ede-142">System.String</span></span>

## <span data-ttu-id="91ede-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91ede-143">OUTPUTS</span></span>

### <span data-ttu-id="91ede-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91ede-144">System.Boolean</span></span>

## <span data-ttu-id="91ede-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91ede-145">NOTES</span></span>

## <span data-ttu-id="91ede-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91ede-146">RELATED LINKS</span></span>
