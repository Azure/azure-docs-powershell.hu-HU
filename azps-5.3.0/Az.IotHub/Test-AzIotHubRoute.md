---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386439"
---
# <span data-ttu-id="85015-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="85015-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="85015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85015-102">SYNOPSIS</span></span>
<span data-ttu-id="85015-103">Tesztútvonalak az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="85015-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="85015-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85015-104">SYNTAX</span></span>

### <span data-ttu-id="85015-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85015-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85015-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="85015-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85015-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="85015-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85015-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="85015-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85015-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="85015-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85015-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="85015-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85015-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="85015-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85015-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85015-112">DESCRIPTION</span></span>
<span data-ttu-id="85015-113">Egy adott útvonal tesztelése.</span><span class="sxs-lookup"><span data-stu-id="85015-113">Test a specific route.</span></span>

## <span data-ttu-id="85015-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85015-114">EXAMPLES</span></span>

### <span data-ttu-id="85015-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="85015-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="85015-116">Tesztelje az összes útvonalat a "DeviceMessages" forrással.</span><span class="sxs-lookup"><span data-stu-id="85015-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="85015-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="85015-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="85015-118">Egy adott útvonal tesztelése.</span><span class="sxs-lookup"><span data-stu-id="85015-118">Test a specific route.</span></span>

### <span data-ttu-id="85015-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="85015-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="85015-120">Tesztelje az egyik útvonalat, és a hiba okát.</span><span class="sxs-lookup"><span data-stu-id="85015-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="85015-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="85015-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="85015-122">Egy adott útvonal tesztelése Az AppProperty és a SystemProperty segítségével.</span><span class="sxs-lookup"><span data-stu-id="85015-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="85015-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85015-123">PARAMETERS</span></span>

### <span data-ttu-id="85015-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="85015-124">-AppProperty</span></span>
<span data-ttu-id="85015-125">Az útvonalüzenet apptulajdonságok</span><span class="sxs-lookup"><span data-stu-id="85015-125">App properties of the route message</span></span>

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

### <span data-ttu-id="85015-126">-Body</span><span class="sxs-lookup"><span data-stu-id="85015-126">-Body</span></span>
<span data-ttu-id="85015-127">Az útvonalüzenet törzse</span><span class="sxs-lookup"><span data-stu-id="85015-127">Body of the route message</span></span>

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

### <span data-ttu-id="85015-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85015-128">-DefaultProfile</span></span>
<span data-ttu-id="85015-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85015-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85015-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85015-130">-InputObject</span></span>
<span data-ttu-id="85015-131">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="85015-131">IotHub Object</span></span>

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

### <span data-ttu-id="85015-132">-Name</span><span class="sxs-lookup"><span data-stu-id="85015-132">-Name</span></span>
<span data-ttu-id="85015-133">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="85015-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="85015-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85015-134">-ResourceGroupName</span></span>
<span data-ttu-id="85015-135">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="85015-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="85015-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85015-136">-ResourceId</span></span>
<span data-ttu-id="85015-137">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="85015-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="85015-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="85015-138">-RouteName</span></span>
<span data-ttu-id="85015-139">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="85015-139">Name of the Route</span></span>

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

### <span data-ttu-id="85015-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="85015-140">-ShowError</span></span>
<span data-ttu-id="85015-141">Részletes hiba megjelenítése (ha létezik)</span><span class="sxs-lookup"><span data-stu-id="85015-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="85015-142">-Source</span><span class="sxs-lookup"><span data-stu-id="85015-142">-Source</span></span>
<span data-ttu-id="85015-143">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="85015-143">Source of the route</span></span>

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

### <span data-ttu-id="85015-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="85015-144">-SystemProperty</span></span>
<span data-ttu-id="85015-145">Az útvonalüzenet rendszertulajdonságok</span><span class="sxs-lookup"><span data-stu-id="85015-145">System properties of the route message</span></span>

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

### <span data-ttu-id="85015-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85015-146">CommonParameters</span></span>
<span data-ttu-id="85015-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85015-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85015-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85015-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85015-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85015-149">INPUTS</span></span>

### <span data-ttu-id="85015-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="85015-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="85015-151">System.String</span><span class="sxs-lookup"><span data-stu-id="85015-151">System.String</span></span>

## <span data-ttu-id="85015-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85015-152">OUTPUTS</span></span>

### <span data-ttu-id="85015-153">Microsoft.Azure.Commands.Management.iotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="85015-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="85015-154">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="85015-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="85015-155">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="85015-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="85015-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85015-156">NOTES</span></span>

## <span data-ttu-id="85015-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85015-157">RELATED LINKS</span></span>
