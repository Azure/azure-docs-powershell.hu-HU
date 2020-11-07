---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ac9d9423bf0098f0f6cf7abba958eb2b08404778
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670923"
---
# <span data-ttu-id="258a2-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="258a2-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="258a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="258a2-102">SYNOPSIS</span></span>
<span data-ttu-id="258a2-103">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="258a2-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="258a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="258a2-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="258a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="258a2-105">DESCRIPTION</span></span>
<span data-ttu-id="258a2-106">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="258a2-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="258a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="258a2-107">EXAMPLES</span></span>

### <span data-ttu-id="258a2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="258a2-108">Example 1</span></span>
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

<span data-ttu-id="258a2-109">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatását az S1 standard árazási réteggel az erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="258a2-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="258a2-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="258a2-110">Example 2</span></span>
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

<span data-ttu-id="258a2-111">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatást az S1 standard árképzési szinttel az "eastus" régióban.</span><span class="sxs-lookup"><span data-stu-id="258a2-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="258a2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="258a2-112">PARAMETERS</span></span>

### <span data-ttu-id="258a2-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="258a2-113">-AllocationPolicy</span></span>
<span data-ttu-id="258a2-114">IoT-eszközök kiépítési szolgáltatásának házirendje</span><span class="sxs-lookup"><span data-stu-id="258a2-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="258a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258a2-115">-DefaultProfile</span></span>
<span data-ttu-id="258a2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="258a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="258a2-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="258a2-117">-Location</span></span>
<span data-ttu-id="258a2-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="258a2-118">Location</span></span>

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

### <span data-ttu-id="258a2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="258a2-119">-Name</span></span>
<span data-ttu-id="258a2-120">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="258a2-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="258a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="258a2-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="258a2-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="258a2-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="258a2-123">-SkuName</span></span>
<span data-ttu-id="258a2-124">Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="258a2-124">Sku</span></span>

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

### <span data-ttu-id="258a2-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="258a2-125">-Confirm</span></span>
<span data-ttu-id="258a2-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="258a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="258a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="258a2-127">-WhatIf</span></span>
<span data-ttu-id="258a2-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="258a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="258a2-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="258a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="258a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258a2-130">CommonParameters</span></span>
<span data-ttu-id="258a2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="258a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258a2-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258a2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="258a2-133">INPUTS</span></span>

### <span data-ttu-id="258a2-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="258a2-134">None</span></span>

## <span data-ttu-id="258a2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="258a2-135">OUTPUTS</span></span>

### <span data-ttu-id="258a2-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="258a2-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="258a2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="258a2-137">NOTES</span></span>

## <span data-ttu-id="258a2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="258a2-138">RELATED LINKS</span></span>
