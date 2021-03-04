---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 99df3feae227aff03d49bfd029f34be4bc32d250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928170"
---
# <span data-ttu-id="bfe10-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="bfe10-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="bfe10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe10-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe10-103">Azure IoT-központbeli eszköz kiépítési szolgáltatásának törlése.</span><span class="sxs-lookup"><span data-stu-id="bfe10-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="bfe10-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfe10-104">SYNTAX</span></span>

### <span data-ttu-id="bfe10-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfe10-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe10-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bfe10-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe10-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bfe10-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfe10-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfe10-108">DESCRIPTION</span></span>
<span data-ttu-id="bfe10-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="bfe10-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="bfe10-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfe10-110">EXAMPLES</span></span>

### <span data-ttu-id="bfe10-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bfe10-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="bfe10-112">Töröljön egy Azure IoT-központbeli eszköz kiépítési szolgáltatást (myiotdps).</span><span class="sxs-lookup"><span data-stu-id="bfe10-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="bfe10-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bfe10-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="bfe10-114">Törölhet egy Azure IoT Hub-eszköz kiépítési szolgáltatását (myiotdps) a folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="bfe10-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="bfe10-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfe10-115">PARAMETERS</span></span>

### <span data-ttu-id="bfe10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe10-116">-DefaultProfile</span></span>
<span data-ttu-id="bfe10-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfe10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfe10-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfe10-118">-InputObject</span></span>
<span data-ttu-id="bfe10-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="bfe10-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="bfe10-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bfe10-120">-Name</span></span>
<span data-ttu-id="bfe10-121">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="bfe10-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bfe10-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfe10-122">-PassThru</span></span>
<span data-ttu-id="bfe10-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bfe10-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bfe10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe10-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfe10-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bfe10-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bfe10-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfe10-126">-ResourceId</span></span>
<span data-ttu-id="bfe10-127">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bfe10-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bfe10-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfe10-128">-Confirm</span></span>
<span data-ttu-id="bfe10-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bfe10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfe10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe10-130">-WhatIf</span></span>
<span data-ttu-id="bfe10-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bfe10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfe10-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfe10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfe10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe10-133">CommonParameters</span></span>
<span data-ttu-id="bfe10-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe10-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe10-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe10-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfe10-136">INPUTS</span></span>

### <span data-ttu-id="bfe10-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bfe10-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="bfe10-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bfe10-138">System.String</span></span>

## <span data-ttu-id="bfe10-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfe10-139">OUTPUTS</span></span>

### <span data-ttu-id="bfe10-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfe10-140">System.Boolean</span></span>

## <span data-ttu-id="bfe10-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfe10-141">NOTES</span></span>

## <span data-ttu-id="bfe10-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfe10-142">RELATED LINKS</span></span>
