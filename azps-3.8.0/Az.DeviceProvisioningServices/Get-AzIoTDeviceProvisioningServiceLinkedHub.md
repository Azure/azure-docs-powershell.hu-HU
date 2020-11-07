---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845438"
---
# <span data-ttu-id="ac17d-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="ac17d-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="ac17d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac17d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac17d-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásaiban felsorolhatja az összes kapcsolt IoT-hub adatait, vagy megjelenítheti az adatokat.</span><span class="sxs-lookup"><span data-stu-id="ac17d-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ac17d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac17d-104">SYNTAX</span></span>

### <span data-ttu-id="ac17d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac17d-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac17d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ac17d-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac17d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ac17d-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac17d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac17d-108">DESCRIPTION</span></span>
<span data-ttu-id="ac17d-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ac17d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ac17d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ac17d-110">EXAMPLES</span></span>

### <span data-ttu-id="ac17d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac17d-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="ac17d-112">Az összes kapcsolt IoT listázása az "myiotdps"-ban</span><span class="sxs-lookup"><span data-stu-id="ac17d-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="ac17d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ac17d-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="ac17d-114">Az Azure IoT hub eszköz kiépítési szolgáltatásában a "myiothub1" kapcsolt IoT-hub részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="ac17d-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ac17d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac17d-115">PARAMETERS</span></span>

### <span data-ttu-id="ac17d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac17d-116">-DefaultProfile</span></span>
<span data-ttu-id="ac17d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac17d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac17d-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ac17d-118">-DpsObject</span></span>
<span data-ttu-id="ac17d-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="ac17d-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac17d-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="ac17d-120">-LinkedHubName</span></span>
<span data-ttu-id="ac17d-121">A kapcsolt IoT-hub állomásneve</span><span class="sxs-lookup"><span data-stu-id="ac17d-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="ac17d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac17d-122">-Name</span></span>
<span data-ttu-id="ac17d-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="ac17d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ac17d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac17d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac17d-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ac17d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ac17d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac17d-126">-ResourceId</span></span>
<span data-ttu-id="ac17d-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ac17d-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ac17d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac17d-128">CommonParameters</span></span>
<span data-ttu-id="ac17d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac17d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac17d-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac17d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac17d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac17d-131">INPUTS</span></span>

### <span data-ttu-id="ac17d-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ac17d-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ac17d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ac17d-133">System.String</span></span>

## <span data-ttu-id="ac17d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac17d-134">OUTPUTS</span></span>

### <span data-ttu-id="ac17d-135">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="ac17d-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="ac17d-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="ac17d-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="ac17d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac17d-137">NOTES</span></span>

## <span data-ttu-id="ac17d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac17d-138">RELATED LINKS</span></span>
