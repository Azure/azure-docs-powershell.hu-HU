---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 4065e44d9ec0ed2512438356231176a1de10e7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935193"
---
# <span data-ttu-id="91841-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="91841-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="91841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91841-102">SYNOPSIS</span></span>
<span data-ttu-id="91841-103">Az Azure IoT-központ eszköz kiépítési szolgáltatásában frissítheti a csatolt IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="91841-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="91841-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91841-104">SYNTAX</span></span>

### <span data-ttu-id="91841-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91841-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91841-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91841-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91841-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91841-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91841-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91841-108">DESCRIPTION</span></span>
<span data-ttu-id="91841-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="91841-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="91841-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91841-110">EXAMPLES</span></span>

### <span data-ttu-id="91841-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="91841-111">Example 1</span></span>
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

<span data-ttu-id="91841-112">A csatolt IoT-központ "myiothub.azure-devices.net" frissítése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="91841-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="91841-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91841-113">PARAMETERS</span></span>

### <span data-ttu-id="91841-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="91841-114">-AllocationWeight</span></span>
<span data-ttu-id="91841-115">Az IoT-központ kiosztási súlya</span><span class="sxs-lookup"><span data-stu-id="91841-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="91841-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="91841-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="91841-117">Hozzárendelési házirend alkalmazása az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="91841-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="91841-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91841-118">-DefaultProfile</span></span>
<span data-ttu-id="91841-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91841-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91841-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91841-120">-InputObject</span></span>
<span data-ttu-id="91841-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="91841-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="91841-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="91841-122">-LinkedHubName</span></span>
<span data-ttu-id="91841-123">A csatolt IoT-központ állomásneve</span><span class="sxs-lookup"><span data-stu-id="91841-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="91841-124">-Name</span><span class="sxs-lookup"><span data-stu-id="91841-124">-Name</span></span>
<span data-ttu-id="91841-125">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="91841-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="91841-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91841-126">-ResourceGroupName</span></span>
<span data-ttu-id="91841-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="91841-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91841-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91841-128">-ResourceId</span></span>
<span data-ttu-id="91841-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="91841-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="91841-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91841-130">-Confirm</span></span>
<span data-ttu-id="91841-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="91841-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91841-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91841-132">-WhatIf</span></span>
<span data-ttu-id="91841-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="91841-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91841-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91841-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91841-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91841-135">CommonParameters</span></span>
<span data-ttu-id="91841-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91841-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91841-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91841-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91841-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91841-138">INPUTS</span></span>

### <span data-ttu-id="91841-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="91841-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="91841-140">System.String</span><span class="sxs-lookup"><span data-stu-id="91841-140">System.String</span></span>

## <span data-ttu-id="91841-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91841-141">OUTPUTS</span></span>

### <span data-ttu-id="91841-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="91841-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="91841-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91841-143">NOTES</span></span>

## <span data-ttu-id="91841-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91841-144">RELATED LINKS</span></span>
