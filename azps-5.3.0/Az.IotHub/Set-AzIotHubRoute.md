---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386467"
---
# <span data-ttu-id="12d07-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="12d07-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="12d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d07-102">SYNOPSIS</span></span>
<span data-ttu-id="12d07-103">Útvonal frissítése az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="12d07-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="12d07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12d07-104">SYNTAX</span></span>

### <span data-ttu-id="12d07-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12d07-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d07-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12d07-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12d07-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d07-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12d07-108">DESCRIPTION</span></span>
<span data-ttu-id="12d07-109">Útvonal szerkesztése</span><span class="sxs-lookup"><span data-stu-id="12d07-109">Edit a route.</span></span> <span data-ttu-id="12d07-110">Frissítheti az útvonal összes mezőjét, beleértve az adatforrást, a végpontot és az útválasztási lekérdezést, valamint engedélyezheti vagy letilthatja az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="12d07-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="12d07-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12d07-111">EXAMPLES</span></span>

### <span data-ttu-id="12d07-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="12d07-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="12d07-113">Az útvonal adatainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="12d07-113">Updating the route information.</span></span>

### <span data-ttu-id="12d07-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="12d07-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="12d07-115">Az útvonal adatainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="12d07-115">Updating the route information.</span></span>

### <span data-ttu-id="12d07-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="12d07-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="12d07-117">Az útvonal adatainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="12d07-117">Updating the route information.</span></span>

## <span data-ttu-id="12d07-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12d07-118">PARAMETERS</span></span>

### <span data-ttu-id="12d07-119">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="12d07-119">-Condition</span></span>
<span data-ttu-id="12d07-120">Az útválasztási szabály alkalmazásához kiértékelt feltétel</span><span class="sxs-lookup"><span data-stu-id="12d07-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="12d07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d07-121">-DefaultProfile</span></span>
<span data-ttu-id="12d07-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12d07-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d07-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="12d07-123">-Enabled</span></span>
<span data-ttu-id="12d07-124">Útvonal engedélyezése</span><span class="sxs-lookup"><span data-stu-id="12d07-124">Enable route</span></span>

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

### <span data-ttu-id="12d07-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="12d07-125">-EndpointName</span></span>
<span data-ttu-id="12d07-126">Az útválasztási végpont neve</span><span class="sxs-lookup"><span data-stu-id="12d07-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="12d07-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12d07-127">-InputObject</span></span>
<span data-ttu-id="12d07-128">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="12d07-128">IotHub Object</span></span>

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

### <span data-ttu-id="12d07-129">-Name</span><span class="sxs-lookup"><span data-stu-id="12d07-129">-Name</span></span>
<span data-ttu-id="12d07-130">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="12d07-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="12d07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d07-131">-ResourceGroupName</span></span>
<span data-ttu-id="12d07-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="12d07-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="12d07-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12d07-133">-ResourceId</span></span>
<span data-ttu-id="12d07-134">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="12d07-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="12d07-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="12d07-135">-RouteName</span></span>
<span data-ttu-id="12d07-136">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="12d07-136">Name of the Route</span></span>

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

### <span data-ttu-id="12d07-137">-Source</span><span class="sxs-lookup"><span data-stu-id="12d07-137">-Source</span></span>
<span data-ttu-id="12d07-138">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="12d07-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d07-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12d07-139">-Confirm</span></span>
<span data-ttu-id="12d07-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12d07-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d07-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d07-141">-WhatIf</span></span>
<span data-ttu-id="12d07-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12d07-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d07-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12d07-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d07-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d07-144">CommonParameters</span></span>
<span data-ttu-id="12d07-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d07-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d07-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d07-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d07-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12d07-147">INPUTS</span></span>

### <span data-ttu-id="12d07-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="12d07-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="12d07-149">System.String</span><span class="sxs-lookup"><span data-stu-id="12d07-149">System.String</span></span>

## <span data-ttu-id="12d07-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12d07-150">OUTPUTS</span></span>

### <span data-ttu-id="12d07-151">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="12d07-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="12d07-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12d07-152">NOTES</span></span>

## <span data-ttu-id="12d07-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12d07-153">RELATED LINKS</span></span>
