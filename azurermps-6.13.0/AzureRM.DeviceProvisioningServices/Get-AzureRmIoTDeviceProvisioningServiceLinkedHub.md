---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: bae363b984f148ff55f34eaa04b1ba85eaad4449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491931"
---
# <span data-ttu-id="230bc-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="230bc-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="230bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="230bc-102">SYNOPSIS</span></span>
<span data-ttu-id="230bc-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásaiban felsorolhatja az összes kapcsolt IoT-hub adatait, vagy megjelenítheti az adatokat.</span><span class="sxs-lookup"><span data-stu-id="230bc-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="230bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="230bc-104">SYNTAX</span></span>

### <span data-ttu-id="230bc-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="230bc-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230bc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="230bc-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230bc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="230bc-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="230bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="230bc-108">DESCRIPTION</span></span>
<span data-ttu-id="230bc-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="230bc-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="230bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="230bc-110">EXAMPLES</span></span>

### <span data-ttu-id="230bc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="230bc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="230bc-112">Az összes kapcsolt IoT listázása az "myiotdps"-ban</span><span class="sxs-lookup"><span data-stu-id="230bc-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="230bc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="230bc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="230bc-114">Az Azure IoT hub eszköz kiépítési szolgáltatásában a "myiothub1" kapcsolt IoT-hub részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="230bc-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="230bc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="230bc-115">PARAMETERS</span></span>

### <span data-ttu-id="230bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230bc-116">-DefaultProfile</span></span>
<span data-ttu-id="230bc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="230bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="230bc-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="230bc-118">-DpsObject</span></span>
<span data-ttu-id="230bc-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="230bc-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="230bc-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="230bc-120">-LinkedHubName</span></span>
<span data-ttu-id="230bc-121">A kapcsolt IoT-hub állomásneve</span><span class="sxs-lookup"><span data-stu-id="230bc-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="230bc-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="230bc-122">-Name</span></span>
<span data-ttu-id="230bc-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="230bc-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="230bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="230bc-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="230bc-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="230bc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="230bc-126">-ResourceId</span></span>
<span data-ttu-id="230bc-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="230bc-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="230bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230bc-128">CommonParameters</span></span>
<span data-ttu-id="230bc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="230bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230bc-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="230bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230bc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="230bc-131">INPUTS</span></span>

### <span data-ttu-id="230bc-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="230bc-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="230bc-133">Paraméterek: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="230bc-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="230bc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="230bc-134">System.String</span></span>

## <span data-ttu-id="230bc-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="230bc-135">OUTPUTS</span></span>

### <span data-ttu-id="230bc-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="230bc-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="230bc-137">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="230bc-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="230bc-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="230bc-138">NOTES</span></span>

## <span data-ttu-id="230bc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="230bc-139">RELATED LINKS</span></span>
