---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: d941e59c3d0681b91cdef9d05617c665dcc83177
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670905"
---
# <span data-ttu-id="4bf22-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="4bf22-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="4bf22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bf22-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf22-103">A csatlakoztatott IoT-hub frissítése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="4bf22-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4bf22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bf22-104">SYNTAX</span></span>

### <span data-ttu-id="4bf22-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bf22-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf22-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4bf22-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf22-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4bf22-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bf22-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bf22-108">DESCRIPTION</span></span>
<span data-ttu-id="4bf22-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4bf22-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4bf22-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4bf22-110">EXAMPLES</span></span>

### <span data-ttu-id="4bf22-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4bf22-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="4bf22-112">Frissítse a "myiothub.azure-devices.net" kapcsolt IoT-hubot egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="4bf22-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4bf22-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bf22-113">PARAMETERS</span></span>

### <span data-ttu-id="4bf22-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="4bf22-114">-AllocationWeight</span></span>
<span data-ttu-id="4bf22-115">A IoT-hub kiosztási súlya</span><span class="sxs-lookup"><span data-stu-id="4bf22-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="4bf22-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="4bf22-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="4bf22-117">Elosztási házirend alkalmazása az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="4bf22-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="4bf22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf22-118">-DefaultProfile</span></span>
<span data-ttu-id="4bf22-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bf22-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bf22-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bf22-120">-InputObject</span></span>
<span data-ttu-id="4bf22-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="4bf22-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf22-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="4bf22-122">-LinkedHubName</span></span>
<span data-ttu-id="4bf22-123">A kapcsolt IoT-hub állomásneve</span><span class="sxs-lookup"><span data-stu-id="4bf22-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf22-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bf22-124">-Name</span></span>
<span data-ttu-id="4bf22-125">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="4bf22-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4bf22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf22-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bf22-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4bf22-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4bf22-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bf22-128">-ResourceId</span></span>
<span data-ttu-id="4bf22-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4bf22-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4bf22-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4bf22-130">-Confirm</span></span>
<span data-ttu-id="4bf22-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4bf22-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf22-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf22-132">-WhatIf</span></span>
<span data-ttu-id="4bf22-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4bf22-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf22-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bf22-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf22-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf22-135">CommonParameters</span></span>
<span data-ttu-id="4bf22-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bf22-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf22-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf22-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf22-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bf22-138">INPUTS</span></span>

### <span data-ttu-id="4bf22-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="4bf22-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="4bf22-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4bf22-140">System.String</span></span>

## <span data-ttu-id="4bf22-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bf22-141">OUTPUTS</span></span>

### <span data-ttu-id="4bf22-142">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="4bf22-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="4bf22-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bf22-143">NOTES</span></span>

## <span data-ttu-id="4bf22-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bf22-144">RELATED LINKS</span></span>
