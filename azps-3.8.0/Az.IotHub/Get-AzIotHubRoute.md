---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013822"
---
# <span data-ttu-id="5b7ec-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="5b7ec-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="5b7ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7ec-103">Információk kérése az útvonalról az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="5b7ec-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="5b7ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b7ec-104">SYNTAX</span></span>

### <span data-ttu-id="5b7ec-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b7ec-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b7ec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b7ec-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b7ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b7ec-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b7ec-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b7ec-108">DESCRIPTION</span></span>
<span data-ttu-id="5b7ec-109">Információkat kaphat az útvonalról. A IoT-hub minden útvonalát elérheti, beolvashatja a végpontok útvonalait, vagy átadhatja az útvonalakat egy adott végpontra.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="5b7ec-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5b7ec-110">EXAMPLES</span></span>

### <span data-ttu-id="5b7ec-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5b7ec-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="5b7ec-112">Az összes útvonal beolvasása a "myiothub" IoT hub-ról</span><span class="sxs-lookup"><span data-stu-id="5b7ec-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="5b7ec-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5b7ec-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="5b7ec-114">Az útvonal adatainak átvétele "myiothub" IoT-hub-ról</span><span class="sxs-lookup"><span data-stu-id="5b7ec-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="5b7ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-115">PARAMETERS</span></span>

### <span data-ttu-id="5b7ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7ec-116">-DefaultProfile</span></span>
<span data-ttu-id="5b7ec-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b7ec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b7ec-118">-InputObject</span></span>
<span data-ttu-id="5b7ec-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="5b7ec-119">IotHub Object</span></span>

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

### <span data-ttu-id="5b7ec-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b7ec-120">-Name</span></span>
<span data-ttu-id="5b7ec-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="5b7ec-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5b7ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b7ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b7ec-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5b7ec-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5b7ec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7ec-124">-ResourceId</span></span>
<span data-ttu-id="5b7ec-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="5b7ec-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5b7ec-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="5b7ec-126">-RouteName</span></span>
<span data-ttu-id="5b7ec-127">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="5b7ec-127">Name of the Route</span></span>

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

### <span data-ttu-id="5b7ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7ec-128">CommonParameters</span></span>
<span data-ttu-id="5b7ec-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b7ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7ec-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b7ec-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7ec-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-131">INPUTS</span></span>

### <span data-ttu-id="5b7ec-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5b7ec-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5b7ec-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5b7ec-133">System.String</span></span>

## <span data-ttu-id="5b7ec-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-134">OUTPUTS</span></span>

### <span data-ttu-id="5b7ec-135">Microsoft. Azure. Command. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="5b7ec-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="5b7ec-136">Microsoft. Azure. Command. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="5b7ec-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="5b7ec-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b7ec-137">NOTES</span></span>

## <span data-ttu-id="5b7ec-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-138">RELATED LINKS</span></span>
