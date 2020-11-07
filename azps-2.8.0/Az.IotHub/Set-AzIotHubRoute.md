---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 97304a55c75291e03d92aae1436344819402fcff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666231"
---
# <span data-ttu-id="69888-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="69888-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="69888-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69888-102">SYNOPSIS</span></span>
<span data-ttu-id="69888-103">Útvonal frissítése az IoT hub-ban</span><span class="sxs-lookup"><span data-stu-id="69888-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="69888-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69888-104">SYNTAX</span></span>

### <span data-ttu-id="69888-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69888-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69888-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="69888-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69888-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69888-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69888-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="69888-108">DESCRIPTION</span></span>
<span data-ttu-id="69888-109">Útvonal szerkesztése</span><span class="sxs-lookup"><span data-stu-id="69888-109">Edit a route.</span></span> <span data-ttu-id="69888-110">Frissítheti az útvonal összes mezőjét, például az adatforrást, a végpontot, az útválasztási lekérdezést, valamint engedélyezheti vagy letilthatja az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="69888-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="69888-111">Példák</span><span class="sxs-lookup"><span data-stu-id="69888-111">EXAMPLES</span></span>

### <span data-ttu-id="69888-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="69888-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="69888-113">Az útvonal adatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="69888-113">Updating the route information.</span></span>

### <span data-ttu-id="69888-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="69888-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="69888-115">Az útvonal adatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="69888-115">Updating the route information.</span></span>

### <span data-ttu-id="69888-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="69888-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="69888-117">Az útvonal adatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="69888-117">Updating the route information.</span></span>

## <span data-ttu-id="69888-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69888-118">PARAMETERS</span></span>

### <span data-ttu-id="69888-119">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="69888-119">-Condition</span></span>
<span data-ttu-id="69888-120">A műveletterv szabály alkalmazásához kiértékelt feltétel</span><span class="sxs-lookup"><span data-stu-id="69888-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="69888-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69888-121">-DefaultProfile</span></span>
<span data-ttu-id="69888-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69888-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69888-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="69888-123">-Enabled</span></span>
<span data-ttu-id="69888-124">Útvonal engedélyezése</span><span class="sxs-lookup"><span data-stu-id="69888-124">Enable route</span></span>

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

### <span data-ttu-id="69888-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="69888-125">-EndpointName</span></span>
<span data-ttu-id="69888-126">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="69888-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="69888-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69888-127">-InputObject</span></span>
<span data-ttu-id="69888-128">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="69888-128">IotHub Object</span></span>

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

### <span data-ttu-id="69888-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69888-129">-Name</span></span>
<span data-ttu-id="69888-130">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="69888-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="69888-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69888-131">-ResourceGroupName</span></span>
<span data-ttu-id="69888-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="69888-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="69888-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69888-133">-ResourceId</span></span>
<span data-ttu-id="69888-134">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="69888-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="69888-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="69888-135">-RouteName</span></span>
<span data-ttu-id="69888-136">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="69888-136">Name of the Route</span></span>

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

### <span data-ttu-id="69888-137">-Forrás</span><span class="sxs-lookup"><span data-stu-id="69888-137">-Source</span></span>
<span data-ttu-id="69888-138">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="69888-138">Source of the route</span></span>

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

### <span data-ttu-id="69888-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69888-139">-Confirm</span></span>
<span data-ttu-id="69888-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69888-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69888-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69888-141">-WhatIf</span></span>
<span data-ttu-id="69888-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69888-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69888-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69888-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69888-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69888-144">CommonParameters</span></span>
<span data-ttu-id="69888-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69888-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69888-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69888-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69888-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69888-147">INPUTS</span></span>

### <span data-ttu-id="69888-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="69888-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="69888-149">System. String</span><span class="sxs-lookup"><span data-stu-id="69888-149">System.String</span></span>

## <span data-ttu-id="69888-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69888-150">OUTPUTS</span></span>

### <span data-ttu-id="69888-151">Microsoft. Azure. Command. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="69888-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="69888-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69888-152">NOTES</span></span>

## <span data-ttu-id="69888-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69888-153">RELATED LINKS</span></span>
