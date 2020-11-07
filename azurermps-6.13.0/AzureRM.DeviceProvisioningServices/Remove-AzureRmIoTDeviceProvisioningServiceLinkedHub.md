---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680369"
---
# <span data-ttu-id="f3021-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="f3021-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="f3021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3021-102">SYNOPSIS</span></span>
<span data-ttu-id="f3021-103">Kapcsolt IoT-hub törlése Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="f3021-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3021-104">SYNTAX</span></span>

### <span data-ttu-id="f3021-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3021-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3021-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f3021-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3021-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f3021-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3021-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3021-108">DESCRIPTION</span></span>
<span data-ttu-id="f3021-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="f3021-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f3021-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f3021-110">EXAMPLES</span></span>

### <span data-ttu-id="f3021-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3021-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="f3021-112">Törölje a "myiothub" hivatkozással ellátott IoT-hubot egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="f3021-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="f3021-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3021-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="f3021-114">Törölje a "myiothub" hivatkozással ellátott IoT-hubot egy Azure IoT hub-eszköz kiépítési szolgáltatásához csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="f3021-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="f3021-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3021-115">PARAMETERS</span></span>

### <span data-ttu-id="f3021-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3021-116">-DefaultProfile</span></span>
<span data-ttu-id="f3021-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3021-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3021-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3021-118">-InputObject</span></span>
<span data-ttu-id="f3021-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="f3021-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f3021-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="f3021-120">-LinkedHubName</span></span>
<span data-ttu-id="f3021-121">A kapcsolt IoT-hub állomásneve</span><span class="sxs-lookup"><span data-stu-id="f3021-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="f3021-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3021-122">-Name</span></span>
<span data-ttu-id="f3021-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="f3021-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f3021-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3021-124">-PassThru</span></span>
<span data-ttu-id="f3021-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f3021-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f3021-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3021-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3021-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f3021-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f3021-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3021-128">-ResourceId</span></span>
<span data-ttu-id="f3021-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f3021-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f3021-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3021-130">-Confirm</span></span>
<span data-ttu-id="f3021-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3021-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3021-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3021-132">-WhatIf</span></span>
<span data-ttu-id="f3021-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3021-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3021-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3021-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3021-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3021-135">CommonParameters</span></span>
<span data-ttu-id="f3021-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3021-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3021-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3021-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3021-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3021-138">INPUTS</span></span>

### <span data-ttu-id="f3021-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="f3021-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="f3021-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3021-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f3021-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f3021-141">System.String</span></span>

## <span data-ttu-id="f3021-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3021-142">OUTPUTS</span></span>

### <span data-ttu-id="f3021-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3021-143">System.Boolean</span></span>

## <span data-ttu-id="f3021-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3021-144">NOTES</span></span>

## <span data-ttu-id="f3021-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3021-145">RELATED LINKS</span></span>
