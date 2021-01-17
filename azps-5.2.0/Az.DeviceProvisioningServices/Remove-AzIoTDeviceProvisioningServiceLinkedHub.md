---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340902"
---
# <span data-ttu-id="7c413-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="7c413-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="7c413-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c413-102">SYNOPSIS</span></span>
<span data-ttu-id="7c413-103">Törölhet egy csatolt IoT-központot egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7c413-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7c413-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c413-104">SYNTAX</span></span>

### <span data-ttu-id="7c413-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c413-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c413-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c413-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c413-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c413-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c413-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c413-108">DESCRIPTION</span></span>
<span data-ttu-id="7c413-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7c413-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7c413-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c413-110">EXAMPLES</span></span>

### <span data-ttu-id="7c413-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c413-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="7c413-112">A csatolt IoT-központ "myiothub" törlése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7c413-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7c413-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7c413-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="7c413-114">A csatolt IoT-központ "myiothub" törlése egy Azure IoT-központ eszköz kiépítési szolgáltatásában folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="7c413-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="7c413-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c413-115">PARAMETERS</span></span>

### <span data-ttu-id="7c413-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c413-116">-DefaultProfile</span></span>
<span data-ttu-id="7c413-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c413-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c413-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c413-118">-InputObject</span></span>
<span data-ttu-id="7c413-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="7c413-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7c413-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="7c413-120">-LinkedHubName</span></span>
<span data-ttu-id="7c413-121">A csatolt IoT-központ állomásneve</span><span class="sxs-lookup"><span data-stu-id="7c413-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="7c413-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7c413-122">-Name</span></span>
<span data-ttu-id="7c413-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="7c413-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7c413-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c413-124">-PassThru</span></span>
<span data-ttu-id="7c413-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7c413-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7c413-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c413-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c413-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7c413-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c413-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c413-128">-ResourceId</span></span>
<span data-ttu-id="7c413-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7c413-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7c413-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c413-130">-Confirm</span></span>
<span data-ttu-id="7c413-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c413-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c413-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c413-132">-WhatIf</span></span>
<span data-ttu-id="7c413-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c413-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c413-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c413-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c413-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c413-135">CommonParameters</span></span>
<span data-ttu-id="7c413-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c413-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c413-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c413-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c413-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c413-138">INPUTS</span></span>

### <span data-ttu-id="7c413-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="7c413-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="7c413-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7c413-140">System.String</span></span>

## <span data-ttu-id="7c413-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c413-141">OUTPUTS</span></span>

### <span data-ttu-id="7c413-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c413-142">System.Boolean</span></span>

## <span data-ttu-id="7c413-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c413-143">NOTES</span></span>

## <span data-ttu-id="7c413-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c413-144">RELATED LINKS</span></span>
