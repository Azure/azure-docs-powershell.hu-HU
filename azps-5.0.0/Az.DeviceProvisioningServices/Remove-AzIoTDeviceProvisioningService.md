---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185503"
---
# <span data-ttu-id="6c16e-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="6c16e-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="6c16e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c16e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c16e-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásának törlése</span><span class="sxs-lookup"><span data-stu-id="6c16e-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="6c16e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c16e-104">SYNTAX</span></span>

### <span data-ttu-id="6c16e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c16e-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c16e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6c16e-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c16e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6c16e-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c16e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c16e-108">DESCRIPTION</span></span>
<span data-ttu-id="6c16e-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="6c16e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="6c16e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6c16e-110">EXAMPLES</span></span>

### <span data-ttu-id="6c16e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6c16e-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="6c16e-112">Az Azure IoT hub eszközök kiépítési szolgáltatásának törlése "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="6c16e-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="6c16e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6c16e-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="6c16e-114">Az Azure IoT hub-eszközök kiépítési szolgáltatása "myiotdps" a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="6c16e-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="6c16e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c16e-115">PARAMETERS</span></span>

### <span data-ttu-id="6c16e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c16e-116">-DefaultProfile</span></span>
<span data-ttu-id="6c16e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c16e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c16e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c16e-118">-InputObject</span></span>
<span data-ttu-id="6c16e-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="6c16e-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6c16e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c16e-120">-Name</span></span>
<span data-ttu-id="6c16e-121">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="6c16e-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6c16e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c16e-122">-PassThru</span></span>
<span data-ttu-id="6c16e-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6c16e-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6c16e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c16e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c16e-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6c16e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6c16e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c16e-126">-ResourceId</span></span>
<span data-ttu-id="6c16e-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6c16e-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6c16e-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c16e-128">-Confirm</span></span>
<span data-ttu-id="6c16e-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c16e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c16e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c16e-130">-WhatIf</span></span>
<span data-ttu-id="6c16e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c16e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c16e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c16e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c16e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c16e-133">CommonParameters</span></span>
<span data-ttu-id="6c16e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c16e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c16e-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c16e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c16e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c16e-136">INPUTS</span></span>

### <span data-ttu-id="6c16e-137">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6c16e-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6c16e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6c16e-138">System.String</span></span>

## <span data-ttu-id="6c16e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c16e-139">OUTPUTS</span></span>

### <span data-ttu-id="6c16e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c16e-140">System.Boolean</span></span>

## <span data-ttu-id="6c16e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c16e-141">NOTES</span></span>

## <span data-ttu-id="6c16e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c16e-142">RELATED LINKS</span></span>