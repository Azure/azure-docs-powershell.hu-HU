---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185496"
---
# <span data-ttu-id="7808d-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="7808d-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="7808d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7808d-102">SYNOPSIS</span></span>
<span data-ttu-id="7808d-103">Kapcsolt IoT-hub törlése Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7808d-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7808d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7808d-104">SYNTAX</span></span>

### <span data-ttu-id="7808d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7808d-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7808d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7808d-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7808d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7808d-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7808d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7808d-108">DESCRIPTION</span></span>
<span data-ttu-id="7808d-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7808d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7808d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7808d-110">EXAMPLES</span></span>

### <span data-ttu-id="7808d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7808d-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="7808d-112">Törölje a "myiothub" hivatkozással ellátott IoT-hubot egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7808d-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7808d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7808d-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="7808d-114">Törölje a "myiothub" hivatkozással ellátott IoT-hubot egy Azure IoT hub-eszköz kiépítési szolgáltatásához csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="7808d-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="7808d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7808d-115">PARAMETERS</span></span>

### <span data-ttu-id="7808d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7808d-116">-DefaultProfile</span></span>
<span data-ttu-id="7808d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7808d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7808d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7808d-118">-InputObject</span></span>
<span data-ttu-id="7808d-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="7808d-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7808d-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="7808d-120">-LinkedHubName</span></span>
<span data-ttu-id="7808d-121">A kapcsolt IoT-hub állomásneve</span><span class="sxs-lookup"><span data-stu-id="7808d-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="7808d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7808d-122">-Name</span></span>
<span data-ttu-id="7808d-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="7808d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7808d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7808d-124">-PassThru</span></span>
<span data-ttu-id="7808d-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7808d-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7808d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7808d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7808d-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7808d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7808d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7808d-128">-ResourceId</span></span>
<span data-ttu-id="7808d-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7808d-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7808d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7808d-130">-Confirm</span></span>
<span data-ttu-id="7808d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7808d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7808d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7808d-132">-WhatIf</span></span>
<span data-ttu-id="7808d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7808d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7808d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7808d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7808d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7808d-135">CommonParameters</span></span>
<span data-ttu-id="7808d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7808d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7808d-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7808d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7808d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7808d-138">INPUTS</span></span>

### <span data-ttu-id="7808d-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="7808d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="7808d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7808d-140">System.String</span></span>

## <span data-ttu-id="7808d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7808d-141">OUTPUTS</span></span>

### <span data-ttu-id="7808d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7808d-142">System.Boolean</span></span>

## <span data-ttu-id="7808d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7808d-143">NOTES</span></span>

## <span data-ttu-id="7808d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7808d-144">RELATED LINKS</span></span>