---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185528"
---
# <span data-ttu-id="2658b-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="2658b-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="2658b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2658b-102">SYNOPSIS</span></span>
<span data-ttu-id="2658b-103">A kapcsolt IoT-hub az Azure IoT hub-eszköz kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="2658b-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2658b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2658b-104">SYNTAX</span></span>

### <span data-ttu-id="2658b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2658b-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2658b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2658b-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2658b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2658b-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2658b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2658b-108">DESCRIPTION</span></span>
<span data-ttu-id="2658b-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2658b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2658b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2658b-110">EXAMPLES</span></span>

### <span data-ttu-id="2658b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2658b-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="2658b-112">A kapcsolt IoT-hub az Azure IoT hub-eszköz kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="2658b-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="2658b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2658b-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="2658b-114">A IoT-hub az Azure IoT hub-eszközök kiépítési szolgáltatása a AllocationWeight és a ApplyAllocationPolicy segítségével.</span><span class="sxs-lookup"><span data-stu-id="2658b-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="2658b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2658b-115">PARAMETERS</span></span>

### <span data-ttu-id="2658b-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="2658b-116">-AllocationWeight</span></span>
<span data-ttu-id="2658b-117">A IoT-hub kiosztási súlya</span><span class="sxs-lookup"><span data-stu-id="2658b-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="2658b-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="2658b-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="2658b-119">Logikai érték, amely azt jelzi, hogy a felosztási házirendet alkalmazza-e az IoT-hubhoz</span><span class="sxs-lookup"><span data-stu-id="2658b-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="2658b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2658b-120">-DefaultProfile</span></span>
<span data-ttu-id="2658b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2658b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2658b-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2658b-122">-DpsObject</span></span>
<span data-ttu-id="2658b-123">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="2658b-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2658b-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="2658b-124">-IotHubConnectionString</span></span>
<span data-ttu-id="2658b-125">Az IOT-hub erőforrás kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="2658b-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="2658b-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="2658b-126">-IotHubLocation</span></span>
<span data-ttu-id="2658b-127">A IOT hub helye</span><span class="sxs-lookup"><span data-stu-id="2658b-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="2658b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2658b-128">-Name</span></span>
<span data-ttu-id="2658b-129">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="2658b-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2658b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2658b-130">-ResourceGroupName</span></span>
<span data-ttu-id="2658b-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2658b-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2658b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2658b-132">-ResourceId</span></span>
<span data-ttu-id="2658b-133">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2658b-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2658b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2658b-134">-Confirm</span></span>
<span data-ttu-id="2658b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2658b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2658b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2658b-136">-WhatIf</span></span>
<span data-ttu-id="2658b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2658b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2658b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2658b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2658b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2658b-139">CommonParameters</span></span>
<span data-ttu-id="2658b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2658b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2658b-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2658b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2658b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2658b-142">INPUTS</span></span>

### <span data-ttu-id="2658b-143">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2658b-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2658b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2658b-144">System.String</span></span>

## <span data-ttu-id="2658b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2658b-145">OUTPUTS</span></span>

### <span data-ttu-id="2658b-146">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="2658b-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="2658b-147">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="2658b-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="2658b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2658b-148">NOTES</span></span>

## <span data-ttu-id="2658b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2658b-149">RELATED LINKS</span></span>
