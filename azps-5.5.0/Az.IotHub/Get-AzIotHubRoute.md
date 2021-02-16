---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203904"
---
# <span data-ttu-id="53305-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="53305-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="53305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53305-102">SYNOPSIS</span></span>
<span data-ttu-id="53305-103">Információ az útvonalról az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="53305-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="53305-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53305-104">SYNTAX</span></span>

### <span data-ttu-id="53305-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53305-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53305-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53305-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53305-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53305-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53305-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53305-108">DESCRIPTION</span></span>
<span data-ttu-id="53305-109">Információ az útvonalról. Az Összes útvonalat lekértheti egy IoT-központból, útvonalakat kaphat egy végponttípushoz, vagy útvonalokat kaphat egy adott végponthoz.</span><span class="sxs-lookup"><span data-stu-id="53305-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="53305-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53305-110">EXAMPLES</span></span>

### <span data-ttu-id="53305-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="53305-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="53305-112">Szerezze be az összes útvonalat a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="53305-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="53305-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="53305-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="53305-114">Útvonalinformációk a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="53305-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="53305-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53305-115">PARAMETERS</span></span>

### <span data-ttu-id="53305-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53305-116">-DefaultProfile</span></span>
<span data-ttu-id="53305-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53305-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53305-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53305-118">-InputObject</span></span>
<span data-ttu-id="53305-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="53305-119">IotHub Object</span></span>

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

### <span data-ttu-id="53305-120">-Name</span><span class="sxs-lookup"><span data-stu-id="53305-120">-Name</span></span>
<span data-ttu-id="53305-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="53305-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="53305-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53305-122">-ResourceGroupName</span></span>
<span data-ttu-id="53305-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="53305-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="53305-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53305-124">-ResourceId</span></span>
<span data-ttu-id="53305-125">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="53305-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="53305-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="53305-126">-RouteName</span></span>
<span data-ttu-id="53305-127">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="53305-127">Name of the Route</span></span>

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

### <span data-ttu-id="53305-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53305-128">CommonParameters</span></span>
<span data-ttu-id="53305-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53305-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53305-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53305-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53305-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53305-131">INPUTS</span></span>

### <span data-ttu-id="53305-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="53305-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="53305-133">System.String</span><span class="sxs-lookup"><span data-stu-id="53305-133">System.String</span></span>

## <span data-ttu-id="53305-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53305-134">OUTPUTS</span></span>

### <span data-ttu-id="53305-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="53305-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="53305-136">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="53305-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="53305-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53305-137">NOTES</span></span>

## <span data-ttu-id="53305-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53305-138">RELATED LINKS</span></span>
