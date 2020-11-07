---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/test-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
ms.openlocfilehash: f51ba85215d252959b974a39ea864b1c98fce460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680091"
---
# <span data-ttu-id="fd55d-101">Test-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="fd55d-101">Test-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="fd55d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd55d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd55d-103">Tesztelési útvonalak az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="fd55d-103">Test routes in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd55d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd55d-104">SYNTAX</span></span>

### <span data-ttu-id="fd55d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd55d-105">ResourceSet (Default)</span></span>
```
Test-AzureRmIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd55d-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="fd55d-106">InputObjectTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd55d-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="fd55d-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd55d-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="fd55d-108">TestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd55d-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="fd55d-109">TestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource>
 [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd55d-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="fd55d-110">ResourceIdTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd55d-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="fd55d-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd55d-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd55d-112">DESCRIPTION</span></span>
<span data-ttu-id="fd55d-113">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="fd55d-113">Test a specific route.</span></span>

## <span data-ttu-id="fd55d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="fd55d-114">EXAMPLES</span></span>

### <span data-ttu-id="fd55d-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd55d-115">Example 1</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="fd55d-116">Az összes útvonal tesztelése a forrás "DeviceMessges" szöveggel.</span><span class="sxs-lookup"><span data-stu-id="fd55d-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="fd55d-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd55d-117">Example 2</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="fd55d-118">Adott útvonal tesztelése</span><span class="sxs-lookup"><span data-stu-id="fd55d-118">Test a specific route.</span></span>

### <span data-ttu-id="fd55d-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="fd55d-119">Example 3</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="fd55d-120">Tesztelje az adott útvonalat, és jelenítse meg a hiba okát.</span><span class="sxs-lookup"><span data-stu-id="fd55d-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="fd55d-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd55d-121">PARAMETERS</span></span>

### <span data-ttu-id="fd55d-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="fd55d-122">-AppProperty</span></span>
<span data-ttu-id="fd55d-123">Az útválasztási üzenet app-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="fd55d-123">App properties of the route message</span></span>

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

### <span data-ttu-id="fd55d-124">-Body</span><span class="sxs-lookup"><span data-stu-id="fd55d-124">-Body</span></span>
<span data-ttu-id="fd55d-125">Az átirányító üzenet törzse</span><span class="sxs-lookup"><span data-stu-id="fd55d-125">Body of the route message</span></span>

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

### <span data-ttu-id="fd55d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd55d-126">-DefaultProfile</span></span>
<span data-ttu-id="fd55d-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd55d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd55d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd55d-128">-InputObject</span></span>
<span data-ttu-id="fd55d-129">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="fd55d-129">IotHub Object</span></span>

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

### <span data-ttu-id="fd55d-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd55d-130">-Name</span></span>
<span data-ttu-id="fd55d-131">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="fd55d-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fd55d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd55d-132">-ResourceGroupName</span></span>
<span data-ttu-id="fd55d-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fd55d-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd55d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd55d-134">-ResourceId</span></span>
<span data-ttu-id="fd55d-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="fd55d-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fd55d-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="fd55d-136">-RouteName</span></span>
<span data-ttu-id="fd55d-137">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="fd55d-137">Name of the Route</span></span>

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

### <span data-ttu-id="fd55d-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="fd55d-138">-ShowError</span></span>
<span data-ttu-id="fd55d-139">Részletes hiba megjelenítése, ha létezik</span><span class="sxs-lookup"><span data-stu-id="fd55d-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="fd55d-140">-Forrás</span><span class="sxs-lookup"><span data-stu-id="fd55d-140">-Source</span></span>
<span data-ttu-id="fd55d-141">Az útvonal forrása</span><span class="sxs-lookup"><span data-stu-id="fd55d-141">Source of the route</span></span>

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

### <span data-ttu-id="fd55d-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="fd55d-142">-SystemProperty</span></span>
<span data-ttu-id="fd55d-143">Az útválasztási üzenet rendszertulajdonságai</span><span class="sxs-lookup"><span data-stu-id="fd55d-143">System properties of the route message</span></span>

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

### <span data-ttu-id="fd55d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd55d-144">CommonParameters</span></span>
<span data-ttu-id="fd55d-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd55d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd55d-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd55d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd55d-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd55d-147">INPUTS</span></span>

### <span data-ttu-id="fd55d-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fd55d-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="fd55d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fd55d-149">System.String</span></span>

## <span data-ttu-id="fd55d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd55d-150">OUTPUTS</span></span>

### <span data-ttu-id="fd55d-151">Microsoft. Azure. Command. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="fd55d-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>
<span data-ttu-id="fd55d-152">Microsoft. Azure. Command. Management. IotHub. models. PSRouteCompilationError System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRouteProperties, Microsoft. Azure. commands. IotHub, Version = 3.1.3.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fd55d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fd55d-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd55d-153">NOTES</span></span>

## <span data-ttu-id="fd55d-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd55d-154">RELATED LINKS</span></span>
