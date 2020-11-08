---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182204"
---
# <span data-ttu-id="e3a8a-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e3a8a-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="e3a8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a8a-103">Útvonal létrehozása az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="e3a8a-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="e3a8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3a8a-104">SYNTAX</span></span>

### <span data-ttu-id="e3a8a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3a8a-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3a8a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3a8a-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3a8a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e3a8a-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3a8a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3a8a-108">DESCRIPTION</span></span>
<span data-ttu-id="e3a8a-109">Útvonal létrehozása adott adatforrás és feltétel kívánt végpontra való küldéséhez.</span><span class="sxs-lookup"><span data-stu-id="e3a8a-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="e3a8a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e3a8a-110">EXAMPLES</span></span>

### <span data-ttu-id="e3a8a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3a8a-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="e3a8a-112">Hozzon létre egy új útvonalat: "R1".</span><span class="sxs-lookup"><span data-stu-id="e3a8a-112">Create a new route "R1".</span></span>

## <span data-ttu-id="e3a8a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3a8a-113">PARAMETERS</span></span>

### <span data-ttu-id="e3a8a-114">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="e3a8a-114">-Condition</span></span>
<span data-ttu-id="e3a8a-115">A műveletterv szabály alkalmazásához kiértékelt feltétel</span><span class="sxs-lookup"><span data-stu-id="e3a8a-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="e3a8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a8a-116">-DefaultProfile</span></span>
<span data-ttu-id="e3a8a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3a8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a8a-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="e3a8a-118">-Enabled</span></span>
<span data-ttu-id="e3a8a-119">Útvonal engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e3a8a-119">Enable route</span></span>

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

### <span data-ttu-id="e3a8a-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e3a8a-120">-EndpointName</span></span>
<span data-ttu-id="e3a8a-121">A műveletterv végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="e3a8a-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="e3a8a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3a8a-122">-InputObject</span></span>
<span data-ttu-id="e3a8a-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="e3a8a-123">IotHub Object</span></span>

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

### <span data-ttu-id="e3a8a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3a8a-124">-Name</span></span>
<span data-ttu-id="e3a8a-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="e3a8a-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e3a8a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a8a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3a8a-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e3a8a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e3a8a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a8a-128">-ResourceId</span></span>
<span data-ttu-id="e3a8a-129">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e3a8a-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e3a8a-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e3a8a-130">-RouteName</span></span>
<span data-ttu-id="e3a8a-131">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="e3a8a-131">Name of the Route</span></span>

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

### <span data-ttu-id="e3a8a-132">-Forrás</span><span class="sxs-lookup"><span data-stu-id="e3a8a-132">-Source</span></span>
<span data-ttu-id="e3a8a-133">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="e3a8a-133">Source of the route</span></span>

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

### <span data-ttu-id="e3a8a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3a8a-134">-Confirm</span></span>
<span data-ttu-id="e3a8a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3a8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a8a-136">-WhatIf</span></span>
<span data-ttu-id="e3a8a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3a8a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a8a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3a8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a8a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a8a-139">CommonParameters</span></span>
<span data-ttu-id="e3a8a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3a8a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a8a-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a8a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a8a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3a8a-142">INPUTS</span></span>

### <span data-ttu-id="e3a8a-143">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e3a8a-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e3a8a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a8a-144">System.String</span></span>

## <span data-ttu-id="e3a8a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3a8a-145">OUTPUTS</span></span>

### <span data-ttu-id="e3a8a-146">Microsoft. Azure. Command. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="e3a8a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="e3a8a-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3a8a-147">NOTES</span></span>

## <span data-ttu-id="e3a8a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3a8a-148">RELATED LINKS</span></span>
