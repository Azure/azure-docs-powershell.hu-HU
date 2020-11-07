---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ca32f2d0436ea16d8897f279239ce4de079d1550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672949"
---
# <span data-ttu-id="ab421-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="ab421-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="ab421-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab421-102">SYNOPSIS</span></span>
<span data-ttu-id="ab421-103">A kapcsolt IoT-hub az Azure IoT hub-eszköz kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="ab421-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab421-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab421-104">SYNTAX</span></span>

### <span data-ttu-id="ab421-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab421-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab421-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab421-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab421-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ab421-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab421-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab421-108">DESCRIPTION</span></span>
<span data-ttu-id="ab421-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ab421-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ab421-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ab421-110">EXAMPLES</span></span>

### <span data-ttu-id="ab421-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab421-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="ab421-112">A kapcsolt IoT-hub az Azure IoT hub-eszköz kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="ab421-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="ab421-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ab421-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="ab421-114">A IoT-hub az Azure IoT hub-eszközök kiépítési szolgáltatása a AllocationWeight és a ApplyAllocationPolicy segítségével.</span><span class="sxs-lookup"><span data-stu-id="ab421-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="ab421-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab421-115">PARAMETERS</span></span>

### <span data-ttu-id="ab421-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="ab421-116">-AllocationWeight</span></span>
<span data-ttu-id="ab421-117">A IoT-hub kiosztási súlya</span><span class="sxs-lookup"><span data-stu-id="ab421-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab421-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ab421-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="ab421-119">Logikai érték, amely azt jelzi, hogy a felosztási házirendet alkalmazza-e az IoT-hubhoz</span><span class="sxs-lookup"><span data-stu-id="ab421-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab421-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab421-120">-DefaultProfile</span></span>
<span data-ttu-id="ab421-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab421-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab421-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ab421-122">-DpsObject</span></span>
<span data-ttu-id="ab421-123">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="ab421-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ab421-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="ab421-124">-IotHubConnectionString</span></span>
<span data-ttu-id="ab421-125">Az IOT-hub erőforrás kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="ab421-125">Connection String of the Iot Hub resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab421-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="ab421-126">-IotHubLocation</span></span>
<span data-ttu-id="ab421-127">A IOT hub helye</span><span class="sxs-lookup"><span data-stu-id="ab421-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab421-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab421-128">-Name</span></span>
<span data-ttu-id="ab421-129">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="ab421-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ab421-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab421-130">-ResourceGroupName</span></span>
<span data-ttu-id="ab421-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ab421-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ab421-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab421-132">-ResourceId</span></span>
<span data-ttu-id="ab421-133">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ab421-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ab421-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab421-134">-Confirm</span></span>
<span data-ttu-id="ab421-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab421-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab421-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab421-136">-WhatIf</span></span>
<span data-ttu-id="ab421-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab421-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab421-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab421-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab421-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab421-139">CommonParameters</span></span>
<span data-ttu-id="ab421-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab421-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab421-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab421-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab421-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab421-142">INPUTS</span></span>

### <span data-ttu-id="ab421-143">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ab421-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="ab421-144">Paraméterek: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab421-144">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="ab421-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ab421-145">System.String</span></span>

## <span data-ttu-id="ab421-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab421-146">OUTPUTS</span></span>

### <span data-ttu-id="ab421-147">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="ab421-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="ab421-148">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="ab421-148">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="ab421-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab421-149">NOTES</span></span>

## <span data-ttu-id="ab421-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab421-150">RELATED LINKS</span></span>
