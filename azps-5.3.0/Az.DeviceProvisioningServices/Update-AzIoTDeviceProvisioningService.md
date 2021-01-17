---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376919"
---
# <span data-ttu-id="6c392-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="6c392-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="6c392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c392-102">SYNOPSIS</span></span>
<span data-ttu-id="6c392-103">Frissítsen egy Azure IoT-központ eszköz-kiépítési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="6c392-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="6c392-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c392-104">SYNTAX</span></span>

### <span data-ttu-id="6c392-105">ResourceUpdateSet (Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c392-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c392-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="6c392-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c392-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="6c392-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c392-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="6c392-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c392-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="6c392-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c392-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="6c392-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c392-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c392-111">DESCRIPTION</span></span>
<span data-ttu-id="6c392-112">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="6c392-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="6c392-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c392-113">EXAMPLES</span></span>

### <span data-ttu-id="6c392-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="6c392-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="6c392-115">Frissítse a kiosztási házirendet egy Azure IoT-központbeli eszközkiosztási szolgáltatás "myiotdps" "GeoLatency" szolgáltatására.</span><span class="sxs-lookup"><span data-stu-id="6c392-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="6c392-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="6c392-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="6c392-117">Vegyen fel címkéket az Azure IoT Hub eszköz kiépítési szolgáltatásának "myiotdps" szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="6c392-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="6c392-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="6c392-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="6c392-119">Címke törlése és új címkék hozzáadása egy Azure IoT Hub-eszköz kiépítési szolgáltatásához "myiotdps" folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="6c392-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="6c392-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c392-120">PARAMETERS</span></span>

### <span data-ttu-id="6c392-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="6c392-121">-AllocationPolicy</span></span>
<span data-ttu-id="6c392-122">IoT-eszközkiosztási szolgáltatásfoglalási házirend</span><span class="sxs-lookup"><span data-stu-id="6c392-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c392-123">-DefaultProfile</span></span>
<span data-ttu-id="6c392-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c392-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c392-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c392-125">-InputObject</span></span>
<span data-ttu-id="6c392-126">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="6c392-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6c392-127">-Name</span></span>
<span data-ttu-id="6c392-128">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="6c392-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="6c392-129">-Reset</span></span>
<span data-ttu-id="6c392-130">IoT-eszközök kiépítési szolgáltatáscímkéinek alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="6c392-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c392-131">-ResourceGroupName</span></span>
<span data-ttu-id="6c392-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6c392-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c392-133">-ResourceId</span></span>
<span data-ttu-id="6c392-134">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6c392-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c392-135">-Tag</span></span>
<span data-ttu-id="6c392-136">IoT-eszköz kiépítési szolgáltatáscímke-gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="6c392-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c392-137">-Confirm</span></span>
<span data-ttu-id="6c392-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6c392-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c392-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c392-139">-WhatIf</span></span>
<span data-ttu-id="6c392-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6c392-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c392-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c392-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c392-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c392-142">CommonParameters</span></span>
<span data-ttu-id="6c392-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c392-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c392-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c392-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c392-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c392-145">INPUTS</span></span>

### <span data-ttu-id="6c392-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6c392-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6c392-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6c392-147">System.String</span></span>

## <span data-ttu-id="6c392-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c392-148">OUTPUTS</span></span>

### <span data-ttu-id="6c392-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6c392-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="6c392-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c392-150">NOTES</span></span>

## <span data-ttu-id="6c392-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c392-151">RELATED LINKS</span></span>
