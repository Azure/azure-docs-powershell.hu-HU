---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011891"
---
# <span data-ttu-id="d5958-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d5958-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="d5958-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5958-102">SYNOPSIS</span></span>
<span data-ttu-id="d5958-103">Tesztelési útvonalak az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="d5958-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="d5958-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5958-104">SYNTAX</span></span>

### <span data-ttu-id="d5958-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5958-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5958-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="d5958-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5958-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="d5958-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5958-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="d5958-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5958-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="d5958-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5958-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="d5958-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5958-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="d5958-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5958-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5958-112">DESCRIPTION</span></span>
<span data-ttu-id="d5958-113">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="d5958-113">Test a specific route.</span></span>

## <span data-ttu-id="d5958-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d5958-114">EXAMPLES</span></span>

### <span data-ttu-id="d5958-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5958-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="d5958-116">Az összes útvonal tesztelése a forrás "DeviceMessages" szöveggel.</span><span class="sxs-lookup"><span data-stu-id="d5958-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="d5958-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="d5958-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="d5958-118">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="d5958-118">Test a specific route.</span></span>

### <span data-ttu-id="d5958-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="d5958-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="d5958-120">Tesztelje az adott útvonalat, és jelenítse meg a hiba okát.</span><span class="sxs-lookup"><span data-stu-id="d5958-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="d5958-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5958-121">PARAMETERS</span></span>

### <span data-ttu-id="d5958-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="d5958-122">-AppProperty</span></span>
<span data-ttu-id="d5958-123">Az útválasztási üzenet app-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="d5958-123">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-124">-Body</span><span class="sxs-lookup"><span data-stu-id="d5958-124">-Body</span></span>
<span data-ttu-id="d5958-125">Az átirányító üzenet törzse</span><span class="sxs-lookup"><span data-stu-id="d5958-125">Body of the route message</span></span>

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

### <span data-ttu-id="d5958-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5958-126">-DefaultProfile</span></span>
<span data-ttu-id="d5958-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5958-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5958-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5958-128">-InputObject</span></span>
<span data-ttu-id="d5958-129">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="d5958-129">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5958-130">-Name</span></span>
<span data-ttu-id="d5958-131">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="d5958-131">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5958-132">-ResourceGroupName</span></span>
<span data-ttu-id="d5958-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d5958-133">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5958-134">-ResourceId</span></span>
<span data-ttu-id="d5958-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d5958-135">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="d5958-136">-RouteName</span></span>
<span data-ttu-id="d5958-137">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="d5958-137">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="d5958-138">-ShowError</span></span>
<span data-ttu-id="d5958-139">Részletes hiba megjelenítése, ha létezik</span><span class="sxs-lookup"><span data-stu-id="d5958-139">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-140">-Forrás</span><span class="sxs-lookup"><span data-stu-id="d5958-140">-Source</span></span>
<span data-ttu-id="d5958-141">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="d5958-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="d5958-142">-SystemProperty</span></span>
<span data-ttu-id="d5958-143">Az útválasztási üzenet rendszertulajdonságai</span><span class="sxs-lookup"><span data-stu-id="d5958-143">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5958-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5958-144">CommonParameters</span></span>
<span data-ttu-id="d5958-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5958-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5958-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5958-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5958-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5958-147">INPUTS</span></span>

### <span data-ttu-id="d5958-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d5958-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d5958-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d5958-149">System.String</span></span>

## <span data-ttu-id="d5958-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5958-150">OUTPUTS</span></span>

### <span data-ttu-id="d5958-151">Microsoft. Azure. Command. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="d5958-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="d5958-152">Microsoft. Azure. Command. Management. IotHub. models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="d5958-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="d5958-153">Microsoft. Azure. Command. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="d5958-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="d5958-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5958-154">NOTES</span></span>

## <span data-ttu-id="d5958-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5958-155">RELATED LINKS</span></span>
