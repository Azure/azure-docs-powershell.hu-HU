---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347046"
---
# <span data-ttu-id="92d4a-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="92d4a-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="92d4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="92d4a-103">Az Azure IoT-központ eszköz kiépítési szolgáltatásában frissítheti a csatolt IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="92d4a-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="92d4a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92d4a-104">SYNTAX</span></span>

### <span data-ttu-id="92d4a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92d4a-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d4a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92d4a-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d4a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92d4a-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d4a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92d4a-108">DESCRIPTION</span></span>
<span data-ttu-id="92d4a-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="92d4a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="92d4a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92d4a-110">EXAMPLES</span></span>

### <span data-ttu-id="92d4a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="92d4a-111">Example 1</span></span>
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

<span data-ttu-id="92d4a-112">A csatolt IoT-központ "myiothub.azure-devices.net" frissítése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="92d4a-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="92d4a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92d4a-113">PARAMETERS</span></span>

### <span data-ttu-id="92d4a-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="92d4a-114">-AllocationWeight</span></span>
<span data-ttu-id="92d4a-115">Az IoT-központ kiosztási súlya</span><span class="sxs-lookup"><span data-stu-id="92d4a-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="92d4a-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="92d4a-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="92d4a-117">Hozzárendelési házirend alkalmazása az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="92d4a-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="92d4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d4a-118">-DefaultProfile</span></span>
<span data-ttu-id="92d4a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92d4a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d4a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92d4a-120">-InputObject</span></span>
<span data-ttu-id="92d4a-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="92d4a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="92d4a-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="92d4a-122">-LinkedHubName</span></span>
<span data-ttu-id="92d4a-123">A csatolt IoT-központ állomásneve</span><span class="sxs-lookup"><span data-stu-id="92d4a-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="92d4a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="92d4a-124">-Name</span></span>
<span data-ttu-id="92d4a-125">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="92d4a-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="92d4a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d4a-126">-ResourceGroupName</span></span>
<span data-ttu-id="92d4a-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="92d4a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="92d4a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d4a-128">-ResourceId</span></span>
<span data-ttu-id="92d4a-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="92d4a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="92d4a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92d4a-130">-Confirm</span></span>
<span data-ttu-id="92d4a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92d4a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d4a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d4a-132">-WhatIf</span></span>
<span data-ttu-id="92d4a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92d4a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92d4a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92d4a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d4a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d4a-135">CommonParameters</span></span>
<span data-ttu-id="92d4a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d4a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d4a-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d4a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d4a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92d4a-138">INPUTS</span></span>

### <span data-ttu-id="92d4a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="92d4a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="92d4a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="92d4a-140">System.String</span></span>

## <span data-ttu-id="92d4a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92d4a-141">OUTPUTS</span></span>

### <span data-ttu-id="92d4a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="92d4a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="92d4a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92d4a-143">NOTES</span></span>

## <span data-ttu-id="92d4a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92d4a-144">RELATED LINKS</span></span>
