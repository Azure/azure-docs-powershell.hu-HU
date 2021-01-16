---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480254"
---
# <span data-ttu-id="43e89-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="43e89-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="43e89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e89-102">SYNOPSIS</span></span>
<span data-ttu-id="43e89-103">Útvonal létrehozása az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="43e89-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="43e89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43e89-104">SYNTAX</span></span>

### <span data-ttu-id="43e89-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43e89-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e89-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43e89-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e89-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43e89-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43e89-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43e89-108">DESCRIPTION</span></span>
<span data-ttu-id="43e89-109">Hozzon létre egy útvonalat, amely adott adatforrást és feltételt küld egy kívánt végpontnak.</span><span class="sxs-lookup"><span data-stu-id="43e89-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="43e89-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43e89-110">EXAMPLES</span></span>

### <span data-ttu-id="43e89-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="43e89-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="43e89-112">Hozzon létre egy új "R1" útvonalat.</span><span class="sxs-lookup"><span data-stu-id="43e89-112">Create a new route "R1".</span></span>

## <span data-ttu-id="43e89-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43e89-113">PARAMETERS</span></span>

### <span data-ttu-id="43e89-114">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="43e89-114">-Condition</span></span>
<span data-ttu-id="43e89-115">Az útválasztási szabály alkalmazásához kiértékelt feltétel</span><span class="sxs-lookup"><span data-stu-id="43e89-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="43e89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e89-116">-DefaultProfile</span></span>
<span data-ttu-id="43e89-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43e89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e89-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="43e89-118">-Enabled</span></span>
<span data-ttu-id="43e89-119">Útvonal engedélyezése</span><span class="sxs-lookup"><span data-stu-id="43e89-119">Enable route</span></span>

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

### <span data-ttu-id="43e89-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="43e89-120">-EndpointName</span></span>
<span data-ttu-id="43e89-121">Az útválasztási végpont neve</span><span class="sxs-lookup"><span data-stu-id="43e89-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="43e89-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43e89-122">-InputObject</span></span>
<span data-ttu-id="43e89-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="43e89-123">IotHub Object</span></span>

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

### <span data-ttu-id="43e89-124">-Name</span><span class="sxs-lookup"><span data-stu-id="43e89-124">-Name</span></span>
<span data-ttu-id="43e89-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="43e89-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="43e89-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e89-126">-ResourceGroupName</span></span>
<span data-ttu-id="43e89-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="43e89-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43e89-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43e89-128">-ResourceId</span></span>
<span data-ttu-id="43e89-129">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="43e89-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="43e89-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="43e89-130">-RouteName</span></span>
<span data-ttu-id="43e89-131">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="43e89-131">Name of the Route</span></span>

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

### <span data-ttu-id="43e89-132">-Source</span><span class="sxs-lookup"><span data-stu-id="43e89-132">-Source</span></span>
<span data-ttu-id="43e89-133">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="43e89-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e89-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43e89-134">-Confirm</span></span>
<span data-ttu-id="43e89-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43e89-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e89-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e89-136">-WhatIf</span></span>
<span data-ttu-id="43e89-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43e89-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e89-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43e89-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e89-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e89-139">CommonParameters</span></span>
<span data-ttu-id="43e89-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e89-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e89-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43e89-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e89-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43e89-142">INPUTS</span></span>

### <span data-ttu-id="43e89-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="43e89-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="43e89-144">System.String</span><span class="sxs-lookup"><span data-stu-id="43e89-144">System.String</span></span>

## <span data-ttu-id="43e89-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43e89-145">OUTPUTS</span></span>

### <span data-ttu-id="43e89-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="43e89-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="43e89-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43e89-147">NOTES</span></span>

## <span data-ttu-id="43e89-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43e89-148">RELATED LINKS</span></span>
