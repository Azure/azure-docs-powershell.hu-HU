---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 80032ab2a677683ff876aca499f7e0ee682e6fd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499524"
---
# <span data-ttu-id="0626e-101">Update-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0626e-101">Update-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0626e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0626e-102">SYNOPSIS</span></span>
<span data-ttu-id="0626e-103">Az Azure IoT hub eszközök kiépítési szolgáltatásának frissítése</span><span class="sxs-lookup"><span data-stu-id="0626e-103">Update an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0626e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0626e-104">SYNTAX</span></span>

### <span data-ttu-id="0626e-105">ResourceUpdateSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0626e-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626e-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0626e-106">InputObjectUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626e-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0626e-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0626e-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0626e-108">ResourceIdUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626e-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0626e-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626e-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0626e-110">ResourceCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0626e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="0626e-111">DESCRIPTION</span></span>
<span data-ttu-id="0626e-112">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0626e-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0626e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0626e-113">EXAMPLES</span></span>

### <span data-ttu-id="0626e-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0626e-114">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

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

<span data-ttu-id="0626e-115">A kiosztási házirend frissítése az Azure IoT hub eszközök kiépítési szolgáltatása "GeoLatency" című "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="0626e-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0626e-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="0626e-116">Example 2</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="0626e-117">" @tags " Hozzáadása egy Azure IoT hub-eszköz kiépítési szolgáltatásához "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="0626e-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0626e-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="0626e-118">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzureRmIoTDps -Tag @tags -Reset

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

<span data-ttu-id="0626e-119">Törölje a címkét, és adjon hozzá új " @tags " szót az Azure IoT hub-eszközök kiépítési szolgáltatása "myiotdps" (pipeline) használatával.</span><span class="sxs-lookup"><span data-stu-id="0626e-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="0626e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0626e-120">PARAMETERS</span></span>

### <span data-ttu-id="0626e-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0626e-121">-AllocationPolicy</span></span>
<span data-ttu-id="0626e-122">IoT-eszközök kiépítési szolgáltatásának házirendje</span><span class="sxs-lookup"><span data-stu-id="0626e-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="0626e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0626e-123">-DefaultProfile</span></span>
<span data-ttu-id="0626e-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0626e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0626e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0626e-125">-InputObject</span></span>
<span data-ttu-id="0626e-126">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="0626e-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0626e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0626e-127">-Name</span></span>
<span data-ttu-id="0626e-128">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="0626e-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0626e-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="0626e-129">-Reset</span></span>
<span data-ttu-id="0626e-130">A IoT-eszközök kiépítési szolgáltatásának alaphelyzetbe állítása Címkék</span><span class="sxs-lookup"><span data-stu-id="0626e-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="0626e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0626e-131">-ResourceGroupName</span></span>
<span data-ttu-id="0626e-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0626e-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0626e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0626e-133">-ResourceId</span></span>
<span data-ttu-id="0626e-134">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0626e-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0626e-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="0626e-135">-Tag</span></span>
<span data-ttu-id="0626e-136">A IoT-eszközök kiépítési szolgáltatásának címkézése</span><span class="sxs-lookup"><span data-stu-id="0626e-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="0626e-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0626e-137">-Confirm</span></span>
<span data-ttu-id="0626e-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0626e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0626e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0626e-139">-WhatIf</span></span>
<span data-ttu-id="0626e-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0626e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0626e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0626e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0626e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0626e-142">CommonParameters</span></span>
<span data-ttu-id="0626e-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0626e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0626e-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0626e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0626e-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0626e-145">INPUTS</span></span>

### <span data-ttu-id="0626e-146">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0626e-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="0626e-147">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0626e-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0626e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0626e-148">System.String</span></span>

## <span data-ttu-id="0626e-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0626e-149">OUTPUTS</span></span>

### <span data-ttu-id="0626e-150">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0626e-150">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="0626e-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0626e-151">NOTES</span></span>

## <span data-ttu-id="0626e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0626e-152">RELATED LINKS</span></span>
