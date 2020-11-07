---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 3d5252f30d8d4393d84f77e1ae1076c9c8054d91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843917"
---
# <span data-ttu-id="b7687-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="b7687-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="b7687-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7687-102">SYNOPSIS</span></span>
<span data-ttu-id="b7687-103">Tesztelési útvonalak az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="b7687-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="b7687-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7687-104">SYNTAX</span></span>

### <span data-ttu-id="b7687-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7687-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7687-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="b7687-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7687-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="b7687-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7687-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="b7687-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7687-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="b7687-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7687-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="b7687-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7687-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="b7687-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7687-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7687-112">DESCRIPTION</span></span>
<span data-ttu-id="b7687-113">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="b7687-113">Test a specific route.</span></span>

## <span data-ttu-id="b7687-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b7687-114">EXAMPLES</span></span>

### <span data-ttu-id="b7687-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7687-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="b7687-116">Az összes útvonal tesztelése a forrás "DeviceMessages" szöveggel.</span><span class="sxs-lookup"><span data-stu-id="b7687-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="b7687-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="b7687-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="b7687-118">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="b7687-118">Test a specific route.</span></span>

### <span data-ttu-id="b7687-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="b7687-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="b7687-120">Tesztelje az adott útvonalat, és jelenítse meg a hiba okát.</span><span class="sxs-lookup"><span data-stu-id="b7687-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="b7687-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7687-121">PARAMETERS</span></span>

### <span data-ttu-id="b7687-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="b7687-122">-AppProperty</span></span>
<span data-ttu-id="b7687-123">Az útválasztási üzenet app-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="b7687-123">App properties of the route message</span></span>

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

### <span data-ttu-id="b7687-124">-Body</span><span class="sxs-lookup"><span data-stu-id="b7687-124">-Body</span></span>
<span data-ttu-id="b7687-125">Az átirányító üzenet törzse</span><span class="sxs-lookup"><span data-stu-id="b7687-125">Body of the route message</span></span>

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

### <span data-ttu-id="b7687-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7687-126">-DefaultProfile</span></span>
<span data-ttu-id="b7687-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7687-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7687-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7687-128">-InputObject</span></span>
<span data-ttu-id="b7687-129">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="b7687-129">IotHub Object</span></span>

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

### <span data-ttu-id="b7687-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7687-130">-Name</span></span>
<span data-ttu-id="b7687-131">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="b7687-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b7687-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7687-132">-ResourceGroupName</span></span>
<span data-ttu-id="b7687-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b7687-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b7687-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7687-134">-ResourceId</span></span>
<span data-ttu-id="b7687-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b7687-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b7687-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="b7687-136">-RouteName</span></span>
<span data-ttu-id="b7687-137">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="b7687-137">Name of the Route</span></span>

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

### <span data-ttu-id="b7687-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="b7687-138">-ShowError</span></span>
<span data-ttu-id="b7687-139">Részletes hiba megjelenítése, ha létezik</span><span class="sxs-lookup"><span data-stu-id="b7687-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="b7687-140">-Forrás</span><span class="sxs-lookup"><span data-stu-id="b7687-140">-Source</span></span>
<span data-ttu-id="b7687-141">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="b7687-141">Source of the route</span></span>

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

### <span data-ttu-id="b7687-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="b7687-142">-SystemProperty</span></span>
<span data-ttu-id="b7687-143">Az útválasztási üzenet rendszertulajdonságai</span><span class="sxs-lookup"><span data-stu-id="b7687-143">System properties of the route message</span></span>

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

### <span data-ttu-id="b7687-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7687-144">CommonParameters</span></span>
<span data-ttu-id="b7687-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7687-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7687-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7687-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7687-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7687-147">INPUTS</span></span>

### <span data-ttu-id="b7687-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b7687-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b7687-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b7687-149">System.String</span></span>

## <span data-ttu-id="b7687-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7687-150">OUTPUTS</span></span>

### <span data-ttu-id="b7687-151">Microsoft. Azure. Command. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="b7687-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="b7687-152">Microsoft. Azure. Command. Management. IotHub. models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="b7687-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="b7687-153">Microsoft. Azure. Command. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="b7687-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="b7687-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7687-154">NOTES</span></span>

## <span data-ttu-id="b7687-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7687-155">RELATED LINKS</span></span>
