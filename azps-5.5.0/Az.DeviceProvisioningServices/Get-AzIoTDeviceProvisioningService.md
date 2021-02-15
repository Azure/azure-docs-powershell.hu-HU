---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204214"
---
# <span data-ttu-id="8d760-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="8d760-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="8d760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d760-102">SYNOPSIS</span></span>
<span data-ttu-id="8d760-103">Az Azure IoT-központ eszköz kiépítési szolgáltatásainak teljes listája vagy részleteinek megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="8d760-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="8d760-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d760-104">SYNTAX</span></span>

### <span data-ttu-id="8d760-105">ListIotDpsByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d760-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d760-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="8d760-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d760-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d760-107">DESCRIPTION</span></span>
<span data-ttu-id="8d760-108">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8d760-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8d760-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d760-109">EXAMPLES</span></span>

### <span data-ttu-id="8d760-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d760-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="8d760-111">List all Azure IoT Hub device provisioning services in a subscription.</span><span class="sxs-lookup"><span data-stu-id="8d760-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="8d760-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d760-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="8d760-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span><span class="sxs-lookup"><span data-stu-id="8d760-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="8d760-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="8d760-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="8d760-115">Az Azure IoT Hub eszköz kiépítési szolgáltatásának "myiotdps" részleteinek megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="8d760-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="8d760-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d760-116">PARAMETERS</span></span>

### <span data-ttu-id="8d760-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d760-117">-DefaultProfile</span></span>
<span data-ttu-id="8d760-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d760-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d760-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8d760-119">-Name</span></span>
<span data-ttu-id="8d760-120">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="8d760-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8d760-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d760-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d760-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8d760-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8d760-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d760-123">CommonParameters</span></span>
<span data-ttu-id="8d760-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d760-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d760-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d760-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d760-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d760-126">INPUTS</span></span>

### <span data-ttu-id="8d760-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d760-127">None</span></span>

## <span data-ttu-id="8d760-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d760-128">OUTPUTS</span></span>

### <span data-ttu-id="8d760-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8d760-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="8d760-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d760-130">NOTES</span></span>

## <span data-ttu-id="8d760-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d760-131">RELATED LINKS</span></span>
