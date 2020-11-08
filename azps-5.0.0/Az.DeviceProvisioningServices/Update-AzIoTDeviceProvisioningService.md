---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 411d4594c94fe1eb031f60d6abbff35f5060d4e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185487"
---
# <span data-ttu-id="db477-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="db477-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="db477-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db477-102">SYNOPSIS</span></span>
<span data-ttu-id="db477-103">Az Azure IoT hub eszközök kiépítési szolgáltatásának frissítése</span><span class="sxs-lookup"><span data-stu-id="db477-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="db477-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db477-104">SYNTAX</span></span>

### <span data-ttu-id="db477-105">ResourceUpdateSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db477-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db477-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="db477-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db477-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="db477-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db477-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="db477-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db477-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="db477-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db477-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="db477-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db477-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="db477-111">DESCRIPTION</span></span>
<span data-ttu-id="db477-112">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="db477-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="db477-113">Példák</span><span class="sxs-lookup"><span data-stu-id="db477-113">EXAMPLES</span></span>

### <span data-ttu-id="db477-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db477-114">Example 1</span></span>
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

<span data-ttu-id="db477-115">A kiosztási házirend frissítése az Azure IoT hub eszközök kiépítési szolgáltatása "GeoLatency" című "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="db477-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="db477-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="db477-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="db477-117">" @tags " Hozzáadása egy Azure IoT hub-eszköz kiépítési szolgáltatásához "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="db477-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="db477-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="db477-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

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

<span data-ttu-id="db477-119">Törölje a címkét, és adjon hozzá új " @tags " szót az Azure IoT hub-eszközök kiépítési szolgáltatása "myiotdps" (pipeline) használatával.</span><span class="sxs-lookup"><span data-stu-id="db477-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="db477-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db477-120">PARAMETERS</span></span>

### <span data-ttu-id="db477-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="db477-121">-AllocationPolicy</span></span>
<span data-ttu-id="db477-122">IoT-eszközök kiépítési szolgáltatásának házirendje</span><span class="sxs-lookup"><span data-stu-id="db477-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="db477-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db477-123">-DefaultProfile</span></span>
<span data-ttu-id="db477-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db477-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db477-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db477-125">-InputObject</span></span>
<span data-ttu-id="db477-126">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="db477-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="db477-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db477-127">-Name</span></span>
<span data-ttu-id="db477-128">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="db477-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="db477-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="db477-129">-Reset</span></span>
<span data-ttu-id="db477-130">A IoT-eszközök kiépítési szolgáltatásának alaphelyzetbe állítása Címkék</span><span class="sxs-lookup"><span data-stu-id="db477-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="db477-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db477-131">-ResourceGroupName</span></span>
<span data-ttu-id="db477-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="db477-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="db477-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db477-133">-ResourceId</span></span>
<span data-ttu-id="db477-134">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="db477-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="db477-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="db477-135">-Tag</span></span>
<span data-ttu-id="db477-136">A IoT-eszközök kiépítési szolgáltatásának címkézése</span><span class="sxs-lookup"><span data-stu-id="db477-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="db477-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db477-137">-Confirm</span></span>
<span data-ttu-id="db477-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db477-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db477-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db477-139">-WhatIf</span></span>
<span data-ttu-id="db477-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db477-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db477-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db477-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db477-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db477-142">CommonParameters</span></span>
<span data-ttu-id="db477-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db477-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db477-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db477-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db477-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db477-145">INPUTS</span></span>

### <span data-ttu-id="db477-146">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="db477-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="db477-147">System. String</span><span class="sxs-lookup"><span data-stu-id="db477-147">System.String</span></span>

## <span data-ttu-id="db477-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db477-148">OUTPUTS</span></span>

### <span data-ttu-id="db477-149">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="db477-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="db477-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db477-150">NOTES</span></span>

## <span data-ttu-id="db477-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db477-151">RELATED LINKS</span></span>
