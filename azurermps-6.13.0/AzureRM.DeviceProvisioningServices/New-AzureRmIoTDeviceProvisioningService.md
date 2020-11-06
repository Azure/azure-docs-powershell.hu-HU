---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 9665b0ae486c12aec350db572aee6fc4f718ed43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495125"
---
# <span data-ttu-id="32611-101">New-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="32611-101">New-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="32611-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32611-102">SYNOPSIS</span></span>
<span data-ttu-id="32611-103">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="32611-103">Create an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32611-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32611-104">SYNTAX</span></span>

```
New-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32611-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32611-105">DESCRIPTION</span></span>
<span data-ttu-id="32611-106">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="32611-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="32611-107">Példák</span><span class="sxs-lookup"><span data-stu-id="32611-107">EXAMPLES</span></span>

### <span data-ttu-id="32611-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="32611-108">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="32611-109">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatását az S1 standard árazási réteggel az erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="32611-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="32611-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="32611-110">Example 2</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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

<span data-ttu-id="32611-111">Hozzon létre egy Azure IoT hub-eszköz kiépítési szolgáltatást az S1 standard árképzési szinttel az "eastus" régióban.</span><span class="sxs-lookup"><span data-stu-id="32611-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="32611-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32611-112">PARAMETERS</span></span>

### <span data-ttu-id="32611-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="32611-113">-AllocationPolicy</span></span>
<span data-ttu-id="32611-114">IoT-eszközök kiépítési szolgáltatásának házirendje</span><span class="sxs-lookup"><span data-stu-id="32611-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="32611-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32611-115">-DefaultProfile</span></span>
<span data-ttu-id="32611-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32611-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32611-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="32611-117">-Location</span></span>
<span data-ttu-id="32611-118">Helyre</span><span class="sxs-lookup"><span data-stu-id="32611-118">Location</span></span>

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

### <span data-ttu-id="32611-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32611-119">-Name</span></span>
<span data-ttu-id="32611-120">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="32611-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="32611-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32611-121">-ResourceGroupName</span></span>
<span data-ttu-id="32611-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="32611-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="32611-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="32611-123">-SkuName</span></span>
<span data-ttu-id="32611-124">Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="32611-124">Sku</span></span>

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

### <span data-ttu-id="32611-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32611-125">-Confirm</span></span>
<span data-ttu-id="32611-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32611-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32611-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32611-127">-WhatIf</span></span>
<span data-ttu-id="32611-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32611-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32611-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32611-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32611-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32611-130">CommonParameters</span></span>
<span data-ttu-id="32611-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32611-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32611-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32611-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32611-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32611-133">INPUTS</span></span>

### <span data-ttu-id="32611-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="32611-134">None</span></span>

## <span data-ttu-id="32611-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32611-135">OUTPUTS</span></span>

### <span data-ttu-id="32611-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="32611-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="32611-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32611-137">NOTES</span></span>

## <span data-ttu-id="32611-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32611-138">RELATED LINKS</span></span>
