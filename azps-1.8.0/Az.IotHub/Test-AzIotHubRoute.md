---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: c31bb4ab7f26d563d73067c5bf5be427c38bdaf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835814"
---
# <span data-ttu-id="3cc1d-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3cc1d-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="3cc1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc1d-103">Tesztelési útvonalak az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="3cc1d-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="3cc1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cc1d-104">SYNTAX</span></span>

### <span data-ttu-id="3cc1d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cc1d-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="3cc1d-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cc1d-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="3cc1d-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3cc1d-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="3cc1d-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cc1d-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="3cc1d-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3cc1d-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="3cc1d-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cc1d-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="3cc1d-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cc1d-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cc1d-112">DESCRIPTION</span></span>
<span data-ttu-id="3cc1d-113">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="3cc1d-113">Test a specific route.</span></span>

## <span data-ttu-id="3cc1d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="3cc1d-114">EXAMPLES</span></span>

### <span data-ttu-id="3cc1d-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3cc1d-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="3cc1d-116">Az összes útvonal tesztelése a forrás "DeviceMessges" szöveggel.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="3cc1d-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="3cc1d-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="3cc1d-118">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="3cc1d-118">Test a specific route.</span></span>

### <span data-ttu-id="3cc1d-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="3cc1d-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="3cc1d-120">Tesztelje az adott útvonalat, és jelenítse meg a hiba okát.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="3cc1d-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cc1d-121">PARAMETERS</span></span>

### <span data-ttu-id="3cc1d-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="3cc1d-122">-AppProperty</span></span>
<span data-ttu-id="3cc1d-123">Az útválasztási üzenet app-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="3cc1d-123">App properties of the route message</span></span>

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

### <span data-ttu-id="3cc1d-124">-Body</span><span class="sxs-lookup"><span data-stu-id="3cc1d-124">-Body</span></span>
<span data-ttu-id="3cc1d-125">Az átirányító üzenet törzse</span><span class="sxs-lookup"><span data-stu-id="3cc1d-125">Body of the route message</span></span>

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

### <span data-ttu-id="3cc1d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc1d-126">-DefaultProfile</span></span>
<span data-ttu-id="3cc1d-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cc1d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc1d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cc1d-128">-InputObject</span></span>
<span data-ttu-id="3cc1d-129">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="3cc1d-129">IotHub Object</span></span>

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

### <span data-ttu-id="3cc1d-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cc1d-130">-Name</span></span>
<span data-ttu-id="3cc1d-131">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="3cc1d-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3cc1d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc1d-132">-ResourceGroupName</span></span>
<span data-ttu-id="3cc1d-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3cc1d-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3cc1d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc1d-134">-ResourceId</span></span>
<span data-ttu-id="3cc1d-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3cc1d-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3cc1d-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3cc1d-136">-RouteName</span></span>
<span data-ttu-id="3cc1d-137">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="3cc1d-137">Name of the Route</span></span>

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

### <span data-ttu-id="3cc1d-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="3cc1d-138">-ShowError</span></span>
<span data-ttu-id="3cc1d-139">Részletes hiba megjelenítése, ha létezik</span><span class="sxs-lookup"><span data-stu-id="3cc1d-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="3cc1d-140">-Forrás</span><span class="sxs-lookup"><span data-stu-id="3cc1d-140">-Source</span></span>
<span data-ttu-id="3cc1d-141">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="3cc1d-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc1d-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="3cc1d-142">-SystemProperty</span></span>
<span data-ttu-id="3cc1d-143">Az útválasztási üzenet rendszertulajdonságai</span><span class="sxs-lookup"><span data-stu-id="3cc1d-143">System properties of the route message</span></span>

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

### <span data-ttu-id="3cc1d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc1d-144">CommonParameters</span></span>
<span data-ttu-id="3cc1d-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cc1d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc1d-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc1d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc1d-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cc1d-147">INPUTS</span></span>

### <span data-ttu-id="3cc1d-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3cc1d-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3cc1d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc1d-149">System.String</span></span>

## <span data-ttu-id="3cc1d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cc1d-150">OUTPUTS</span></span>

### <span data-ttu-id="3cc1d-151">Microsoft. Azure. Command. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="3cc1d-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="3cc1d-152">Microsoft. Azure. Command. Management. IotHub. models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="3cc1d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="3cc1d-153">Microsoft. Azure. Command. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="3cc1d-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="3cc1d-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cc1d-154">NOTES</span></span>

## <span data-ttu-id="3cc1d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cc1d-155">RELATED LINKS</span></span>
