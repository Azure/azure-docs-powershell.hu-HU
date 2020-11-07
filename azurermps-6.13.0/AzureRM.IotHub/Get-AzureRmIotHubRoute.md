---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680097"
---
# <span data-ttu-id="99756-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="99756-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="99756-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99756-102">SYNOPSIS</span></span>
<span data-ttu-id="99756-103">Információk kérése az útvonalról az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="99756-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99756-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99756-104">SYNTAX</span></span>

### <span data-ttu-id="99756-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99756-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99756-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="99756-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99756-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="99756-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99756-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99756-108">DESCRIPTION</span></span>
<span data-ttu-id="99756-109">Információkat kaphat az útvonalról. A IoT-hub minden útvonalát elérheti, beolvashatja a végpontok útvonalait, vagy átadhatja az útvonalakat egy adott végpontra.</span><span class="sxs-lookup"><span data-stu-id="99756-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="99756-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99756-110">EXAMPLES</span></span>

### <span data-ttu-id="99756-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99756-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="99756-112">Az összes útvonal beolvasása a "myiothub" IoT hub-ról</span><span class="sxs-lookup"><span data-stu-id="99756-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="99756-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="99756-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="99756-114">Az útvonal adatainak átvétele "myiothub" IoT-hub-ról</span><span class="sxs-lookup"><span data-stu-id="99756-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="99756-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99756-115">PARAMETERS</span></span>

### <span data-ttu-id="99756-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99756-116">-DefaultProfile</span></span>
<span data-ttu-id="99756-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99756-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99756-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99756-118">-InputObject</span></span>
<span data-ttu-id="99756-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="99756-119">IotHub Object</span></span>

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

### <span data-ttu-id="99756-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99756-120">-Name</span></span>
<span data-ttu-id="99756-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="99756-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="99756-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99756-122">-ResourceGroupName</span></span>
<span data-ttu-id="99756-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="99756-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="99756-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99756-124">-ResourceId</span></span>
<span data-ttu-id="99756-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="99756-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="99756-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="99756-126">-RouteName</span></span>
<span data-ttu-id="99756-127">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="99756-127">Name of the Route</span></span>

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

### <span data-ttu-id="99756-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99756-128">CommonParameters</span></span>
<span data-ttu-id="99756-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99756-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99756-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99756-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99756-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99756-131">INPUTS</span></span>

### <span data-ttu-id="99756-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="99756-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="99756-133">System. String</span><span class="sxs-lookup"><span data-stu-id="99756-133">System.String</span></span>

## <span data-ttu-id="99756-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99756-134">OUTPUTS</span></span>

### <span data-ttu-id="99756-135">Microsoft. Azure. Command. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="99756-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="99756-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSRouteProperties, Microsoft. Azure. commands. IotHub, Version = 3.1.3.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99756-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="99756-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99756-137">NOTES</span></span>

## <span data-ttu-id="99756-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99756-138">RELATED LINKS</span></span>
