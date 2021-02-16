---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153243"
---
# <span data-ttu-id="27d76-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="27d76-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="27d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27d76-102">SYNOPSIS</span></span>
<span data-ttu-id="27d76-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span><span class="sxs-lookup"><span data-stu-id="27d76-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="27d76-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27d76-104">SYNTAX</span></span>

### <span data-ttu-id="27d76-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27d76-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d76-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27d76-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d76-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27d76-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27d76-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27d76-108">DESCRIPTION</span></span>
<span data-ttu-id="27d76-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="27d76-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="27d76-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27d76-110">EXAMPLES</span></span>

### <span data-ttu-id="27d76-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="27d76-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="27d76-112">List all linked IoT hubs in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="27d76-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="27d76-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="27d76-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="27d76-114">Az Összekapcsolt IoT-központ "myiothub1" részleteinek megjelenítése egy Azure IoT-központ eszközépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="27d76-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="27d76-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27d76-115">PARAMETERS</span></span>

### <span data-ttu-id="27d76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d76-116">-DefaultProfile</span></span>
<span data-ttu-id="27d76-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27d76-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d76-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="27d76-118">-DpsObject</span></span>
<span data-ttu-id="27d76-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="27d76-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="27d76-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="27d76-120">-LinkedHubName</span></span>
<span data-ttu-id="27d76-121">Csatolt IoT-központ állomásneve</span><span class="sxs-lookup"><span data-stu-id="27d76-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="27d76-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27d76-122">-Name</span></span>
<span data-ttu-id="27d76-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="27d76-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="27d76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d76-124">-ResourceGroupName</span></span>
<span data-ttu-id="27d76-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="27d76-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27d76-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27d76-126">-ResourceId</span></span>
<span data-ttu-id="27d76-127">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="27d76-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="27d76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d76-128">CommonParameters</span></span>
<span data-ttu-id="27d76-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d76-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d76-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d76-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27d76-131">INPUTS</span></span>

### <span data-ttu-id="27d76-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="27d76-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="27d76-133">System.String</span><span class="sxs-lookup"><span data-stu-id="27d76-133">System.String</span></span>

## <span data-ttu-id="27d76-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d76-134">OUTPUTS</span></span>

### <span data-ttu-id="27d76-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="27d76-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="27d76-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="27d76-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="27d76-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27d76-137">NOTES</span></span>

## <span data-ttu-id="27d76-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27d76-138">RELATED LINKS</span></span>
