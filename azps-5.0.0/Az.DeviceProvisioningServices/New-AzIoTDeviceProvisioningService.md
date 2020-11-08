---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185509"
---
# <span data-ttu-id="04cc0-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="04cc0-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="04cc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="04cc0-103">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="04cc0-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="04cc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04cc0-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04cc0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="04cc0-106">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="04cc0-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="04cc0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="04cc0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04cc0-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="04cc0-109">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatását az S1 standard árazási réteggel az erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="04cc0-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="04cc0-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="04cc0-110">Example 2</span></span>
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

<span data-ttu-id="04cc0-111">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatást az S1 standard árképzési szinttel az "eastus" régióban.</span><span class="sxs-lookup"><span data-stu-id="04cc0-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="04cc0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04cc0-112">PARAMETERS</span></span>

### <span data-ttu-id="04cc0-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="04cc0-113">-AllocationPolicy</span></span>
<span data-ttu-id="04cc0-114">IoT-eszközök kiépítési szolgáltatásának házirendje</span><span class="sxs-lookup"><span data-stu-id="04cc0-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="04cc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cc0-115">-DefaultProfile</span></span>
<span data-ttu-id="04cc0-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04cc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04cc0-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="04cc0-117">-Location</span></span>
<span data-ttu-id="04cc0-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="04cc0-118">Location</span></span>

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

### <span data-ttu-id="04cc0-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04cc0-119">-Name</span></span>
<span data-ttu-id="04cc0-120">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="04cc0-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="04cc0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04cc0-121">-ResourceGroupName</span></span>
<span data-ttu-id="04cc0-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="04cc0-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="04cc0-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="04cc0-123">-SkuName</span></span>
<span data-ttu-id="04cc0-124">Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="04cc0-124">Sku</span></span>

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

### <span data-ttu-id="04cc0-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04cc0-125">-Confirm</span></span>
<span data-ttu-id="04cc0-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04cc0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04cc0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04cc0-127">-WhatIf</span></span>
<span data-ttu-id="04cc0-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04cc0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04cc0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04cc0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04cc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cc0-130">CommonParameters</span></span>
<span data-ttu-id="04cc0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04cc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cc0-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04cc0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cc0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04cc0-133">INPUTS</span></span>

### <span data-ttu-id="04cc0-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="04cc0-134">None</span></span>

## <span data-ttu-id="04cc0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04cc0-135">OUTPUTS</span></span>

### <span data-ttu-id="04cc0-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="04cc0-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="04cc0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04cc0-137">NOTES</span></span>

## <span data-ttu-id="04cc0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04cc0-138">RELATED LINKS</span></span>
