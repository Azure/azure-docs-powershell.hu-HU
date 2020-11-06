---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: dd9bc81ef24530369a26ff290270a39c8ab1ff40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491934"
---
# <span data-ttu-id="9a4ad-101">Get-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="9a4ad-101">Get-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="9a4ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4ad-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásainak teljes listája vagy megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a4ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a4ad-104">SYNTAX</span></span>

### <span data-ttu-id="9a4ad-105">ListIotDpsByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a4ad-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningService [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a4ad-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="9a4ad-106">GetIotDpsByName</span></span>
```
Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a4ad-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a4ad-107">DESCRIPTION</span></span>
<span data-ttu-id="9a4ad-108">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="9a4ad-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9a4ad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9a4ad-109">EXAMPLES</span></span>

### <span data-ttu-id="9a4ad-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9a4ad-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="9a4ad-111">Az összes Azure IoT hub-eszköz kiépítési szolgáltatásainak listázása az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="9a4ad-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9a4ad-112">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="9a4ad-113">Az Azure IoT hub eszközök kiépítési szolgáltatásainak listázása az "myresourcegroup" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="9a4ad-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="9a4ad-114">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="9a4ad-115">Az Azure IoT hub-eszközök kiépítési szolgáltatása "myiotdps" adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="9a4ad-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a4ad-116">PARAMETERS</span></span>

### <span data-ttu-id="9a4ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4ad-117">-DefaultProfile</span></span>
<span data-ttu-id="9a4ad-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a4ad-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a4ad-119">-Name</span></span>
<span data-ttu-id="9a4ad-120">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="9a4ad-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a4ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a4ad-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9a4ad-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4ad-123">CommonParameters</span></span>
<span data-ttu-id="9a4ad-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a4ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4ad-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4ad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4ad-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a4ad-126">INPUTS</span></span>

### <span data-ttu-id="9a4ad-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a4ad-127">None</span></span>

## <span data-ttu-id="9a4ad-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a4ad-128">OUTPUTS</span></span>

### <span data-ttu-id="9a4ad-129">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9a4ad-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="9a4ad-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a4ad-130">NOTES</span></span>

## <span data-ttu-id="9a4ad-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a4ad-131">RELATED LINKS</span></span>
