---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: bb6094644b9f2cbd831aa8d64a142d5888a5bcc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013653"
---
# <span data-ttu-id="78060-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="78060-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="78060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78060-102">SYNOPSIS</span></span>
<span data-ttu-id="78060-103">Hozzon létre egy Azure IoT-központbeli eszköz kiépítési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="78060-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="78060-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78060-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78060-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78060-105">DESCRIPTION</span></span>
<span data-ttu-id="78060-106">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="78060-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="78060-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78060-107">EXAMPLES</span></span>

### <span data-ttu-id="78060-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="78060-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="78060-109">Hozzon létre egy Azure IoT Hub eszközkiépítési szolgáltatást az erőforráscsoport régiójában található szabványos S1 árazási szint és címkék segítségével.</span><span class="sxs-lookup"><span data-stu-id="78060-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="78060-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="78060-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="78060-111">Hozzon létre egy Azure IoT-központbeli eszközkiépítési szolgáltatást az S1 standard árazási szint használatával a "eastus" régióban.</span><span class="sxs-lookup"><span data-stu-id="78060-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="78060-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78060-112">PARAMETERS</span></span>

### <span data-ttu-id="78060-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="78060-113">-AllocationPolicy</span></span>
<span data-ttu-id="78060-114">IoT-eszközkiosztási szolgáltatásfoglalási házirend</span><span class="sxs-lookup"><span data-stu-id="78060-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78060-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78060-115">-DefaultProfile</span></span>
<span data-ttu-id="78060-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78060-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78060-117">-Location</span><span class="sxs-lookup"><span data-stu-id="78060-117">-Location</span></span>
<span data-ttu-id="78060-118">Hely</span><span class="sxs-lookup"><span data-stu-id="78060-118">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78060-119">-Name</span><span class="sxs-lookup"><span data-stu-id="78060-119">-Name</span></span>
<span data-ttu-id="78060-120">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="78060-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="78060-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78060-121">-ResourceGroupName</span></span>
<span data-ttu-id="78060-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="78060-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78060-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="78060-123">-SkuName</span></span>
<span data-ttu-id="78060-124">Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="78060-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78060-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="78060-125">-Tag</span></span>
<span data-ttu-id="78060-126">IoT-eszköz kiépítési szolgáltatás példánycímkéi.</span><span class="sxs-lookup"><span data-stu-id="78060-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="78060-127">Property bag in key-value pairs in a form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="78060-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78060-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78060-128">-Confirm</span></span>
<span data-ttu-id="78060-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="78060-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78060-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78060-130">-WhatIf</span></span>
<span data-ttu-id="78060-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="78060-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78060-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78060-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78060-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78060-133">CommonParameters</span></span>
<span data-ttu-id="78060-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78060-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78060-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78060-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78060-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78060-136">INPUTS</span></span>

### <span data-ttu-id="78060-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="78060-137">None</span></span>

## <span data-ttu-id="78060-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78060-138">OUTPUTS</span></span>

### <span data-ttu-id="78060-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="78060-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="78060-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78060-140">NOTES</span></span>

## <span data-ttu-id="78060-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78060-141">RELATED LINKS</span></span>
