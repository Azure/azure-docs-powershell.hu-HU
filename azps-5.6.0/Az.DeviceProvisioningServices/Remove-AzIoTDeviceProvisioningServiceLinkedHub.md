---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: fc1b8bbe14fb35e7613ac1ed09ecf87624920081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935241"
---
# <span data-ttu-id="26aea-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="26aea-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="26aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26aea-102">SYNOPSIS</span></span>
<span data-ttu-id="26aea-103">Törölhet egy csatolt IoT-központot egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="26aea-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="26aea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26aea-104">SYNTAX</span></span>

### <span data-ttu-id="26aea-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26aea-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26aea-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26aea-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26aea-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="26aea-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26aea-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26aea-108">DESCRIPTION</span></span>
<span data-ttu-id="26aea-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="26aea-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="26aea-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26aea-110">EXAMPLES</span></span>

### <span data-ttu-id="26aea-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="26aea-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="26aea-112">A csatolt IoT-központ "myiothub" törlése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="26aea-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="26aea-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="26aea-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="26aea-114">A csatolt IoT-központ "myiothub" törlése egy Azure IoT-központ eszköz kiépítési szolgáltatásában folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="26aea-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="26aea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26aea-115">PARAMETERS</span></span>

### <span data-ttu-id="26aea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26aea-116">-DefaultProfile</span></span>
<span data-ttu-id="26aea-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26aea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26aea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26aea-118">-InputObject</span></span>
<span data-ttu-id="26aea-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="26aea-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="26aea-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="26aea-120">-LinkedHubName</span></span>
<span data-ttu-id="26aea-121">A csatolt IoT-központ állomásneve</span><span class="sxs-lookup"><span data-stu-id="26aea-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="26aea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="26aea-122">-Name</span></span>
<span data-ttu-id="26aea-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="26aea-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="26aea-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26aea-124">-PassThru</span></span>
<span data-ttu-id="26aea-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="26aea-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="26aea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26aea-126">-ResourceGroupName</span></span>
<span data-ttu-id="26aea-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="26aea-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="26aea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26aea-128">-ResourceId</span></span>
<span data-ttu-id="26aea-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="26aea-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="26aea-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26aea-130">-Confirm</span></span>
<span data-ttu-id="26aea-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26aea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26aea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26aea-132">-WhatIf</span></span>
<span data-ttu-id="26aea-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26aea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26aea-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26aea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26aea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26aea-135">CommonParameters</span></span>
<span data-ttu-id="26aea-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26aea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26aea-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26aea-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26aea-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26aea-138">INPUTS</span></span>

### <span data-ttu-id="26aea-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="26aea-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="26aea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="26aea-140">System.String</span></span>

## <span data-ttu-id="26aea-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26aea-141">OUTPUTS</span></span>

### <span data-ttu-id="26aea-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26aea-142">System.Boolean</span></span>

## <span data-ttu-id="26aea-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26aea-143">NOTES</span></span>

## <span data-ttu-id="26aea-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26aea-144">RELATED LINKS</span></span>
