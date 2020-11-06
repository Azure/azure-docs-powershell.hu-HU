---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495123"
---
# <span data-ttu-id="cc5ca-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="cc5ca-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="cc5ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5ca-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásának törlése</span><span class="sxs-lookup"><span data-stu-id="cc5ca-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc5ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc5ca-104">SYNTAX</span></span>

### <span data-ttu-id="cc5ca-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc5ca-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5ca-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc5ca-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5ca-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cc5ca-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc5ca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc5ca-108">DESCRIPTION</span></span>
<span data-ttu-id="cc5ca-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="cc5ca-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="cc5ca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cc5ca-110">EXAMPLES</span></span>

### <span data-ttu-id="cc5ca-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc5ca-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="cc5ca-112">Az Azure IoT hub eszközök kiépítési szolgáltatásának törlése "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="cc5ca-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="cc5ca-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cc5ca-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="cc5ca-114">Az Azure IoT hub-eszközök kiépítési szolgáltatása "myiotdps" a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="cc5ca-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc5ca-115">PARAMETERS</span></span>

### <span data-ttu-id="cc5ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5ca-116">-DefaultProfile</span></span>
<span data-ttu-id="cc5ca-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5ca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc5ca-118">-InputObject</span></span>
<span data-ttu-id="cc5ca-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="cc5ca-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cc5ca-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc5ca-120">-Name</span></span>
<span data-ttu-id="cc5ca-121">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="cc5ca-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cc5ca-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc5ca-122">-PassThru</span></span>
<span data-ttu-id="cc5ca-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cc5ca-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cc5ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc5ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc5ca-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cc5ca-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cc5ca-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc5ca-126">-ResourceId</span></span>
<span data-ttu-id="cc5ca-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cc5ca-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cc5ca-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc5ca-128">-Confirm</span></span>
<span data-ttu-id="cc5ca-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc5ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5ca-130">-WhatIf</span></span>
<span data-ttu-id="cc5ca-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5ca-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc5ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5ca-133">CommonParameters</span></span>
<span data-ttu-id="cc5ca-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc5ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5ca-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5ca-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5ca-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc5ca-136">INPUTS</span></span>

### <span data-ttu-id="cc5ca-137">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="cc5ca-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="cc5ca-138">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc5ca-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="cc5ca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cc5ca-139">System.String</span></span>

## <span data-ttu-id="cc5ca-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc5ca-140">OUTPUTS</span></span>

### <span data-ttu-id="cc5ca-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc5ca-141">System.Boolean</span></span>

## <span data-ttu-id="cc5ca-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc5ca-142">NOTES</span></span>

## <span data-ttu-id="cc5ca-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc5ca-143">RELATED LINKS</span></span>
