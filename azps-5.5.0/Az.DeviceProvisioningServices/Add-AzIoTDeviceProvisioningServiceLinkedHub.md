---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167666"
---
# <span data-ttu-id="75b2a-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="75b2a-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="75b2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="75b2a-103">Összekapcsolta az IoT-központot egy Azure IoT-központ eszköz kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="75b2a-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="75b2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75b2a-104">SYNTAX</span></span>

### <span data-ttu-id="75b2a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75b2a-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b2a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75b2a-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b2a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="75b2a-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b2a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75b2a-108">DESCRIPTION</span></span>
<span data-ttu-id="75b2a-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="75b2a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="75b2a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75b2a-110">EXAMPLES</span></span>

### <span data-ttu-id="75b2a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="75b2a-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="75b2a-112">Összekapcsolta az IoT-központot egy Azure IoT-központ eszköz kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="75b2a-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="75b2a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="75b2a-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="75b2a-114">Az IoT-központ összekapcsolva van egy Azure IoT-központ eszközkiosztási szolgáltatásával a AllocationWeight és az ApplyAllocationPolicy szolgáltatóval.</span><span class="sxs-lookup"><span data-stu-id="75b2a-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="75b2a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75b2a-115">PARAMETERS</span></span>

### <span data-ttu-id="75b2a-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="75b2a-116">-AllocationWeight</span></span>
<span data-ttu-id="75b2a-117">Az IoT-központ kiosztási súlya</span><span class="sxs-lookup"><span data-stu-id="75b2a-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="75b2a-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="75b2a-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="75b2a-119">Logikai érték, amely azt jelzi, hogy az IoT-központra alkalmazza-e a hozzárendelési házirendet</span><span class="sxs-lookup"><span data-stu-id="75b2a-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="75b2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b2a-120">-DefaultProfile</span></span>
<span data-ttu-id="75b2a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75b2a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b2a-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="75b2a-122">-DpsObject</span></span>
<span data-ttu-id="75b2a-123">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="75b2a-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="75b2a-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="75b2a-124">-IotHubConnectionString</span></span>
<span data-ttu-id="75b2a-125">Az Iot Hub erőforrás kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="75b2a-125">Connection String of the Iot Hub resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b2a-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="75b2a-126">-IotHubLocation</span></span>
<span data-ttu-id="75b2a-127">Az Iot-központ helye</span><span class="sxs-lookup"><span data-stu-id="75b2a-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b2a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="75b2a-128">-Name</span></span>
<span data-ttu-id="75b2a-129">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="75b2a-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="75b2a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b2a-130">-ResourceGroupName</span></span>
<span data-ttu-id="75b2a-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="75b2a-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="75b2a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75b2a-132">-ResourceId</span></span>
<span data-ttu-id="75b2a-133">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="75b2a-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="75b2a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75b2a-134">-Confirm</span></span>
<span data-ttu-id="75b2a-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75b2a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b2a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b2a-136">-WhatIf</span></span>
<span data-ttu-id="75b2a-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75b2a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b2a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75b2a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b2a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b2a-139">CommonParameters</span></span>
<span data-ttu-id="75b2a-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b2a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b2a-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b2a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b2a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75b2a-142">INPUTS</span></span>

### <span data-ttu-id="75b2a-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="75b2a-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="75b2a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="75b2a-144">System.String</span></span>

## <span data-ttu-id="75b2a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75b2a-145">OUTPUTS</span></span>

### <span data-ttu-id="75b2a-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="75b2a-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="75b2a-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="75b2a-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="75b2a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75b2a-148">NOTES</span></span>

## <span data-ttu-id="75b2a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75b2a-149">RELATED LINKS</span></span>
