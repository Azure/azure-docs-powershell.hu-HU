---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185517"
---
# <span data-ttu-id="bd4b2-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="bd4b2-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="bd4b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4b2-103">Szerezzen be egy eszköz-beiratkozási rekordot.</span><span class="sxs-lookup"><span data-stu-id="bd4b2-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="bd4b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd4b2-104">SYNTAX</span></span>

### <span data-ttu-id="bd4b2-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd4b2-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd4b2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd4b2-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd4b2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bd4b2-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd4b2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd4b2-108">DESCRIPTION</span></span>
<span data-ttu-id="bd4b2-109">Az eszköz-beiktatási adatok beszerzése vagy a lista eszköz-beiktatása az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="bd4b2-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="bd4b2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bd4b2-110">EXAMPLES</span></span>

### <span data-ttu-id="bd4b2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd4b2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="bd4b2-112">Eszköztelepítési adatok beszerzése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="bd4b2-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="bd4b2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bd4b2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="bd4b2-114">Eszköz-igénylések listázása az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="bd4b2-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="bd4b2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd4b2-115">PARAMETERS</span></span>

### <span data-ttu-id="bd4b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4b2-116">-DefaultProfile</span></span>
<span data-ttu-id="bd4b2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd4b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd4b2-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="bd4b2-118">-DpsName</span></span>
<span data-ttu-id="bd4b2-119">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="bd4b2-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bd4b2-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="bd4b2-120">-DpsObject</span></span>
<span data-ttu-id="bd4b2-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="bd4b2-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="bd4b2-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="bd4b2-122">-RegistrationId</span></span>
<span data-ttu-id="bd4b2-123">Egyéni beiratkozási regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="bd4b2-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="bd4b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd4b2-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bd4b2-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bd4b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd4b2-126">-ResourceId</span></span>
<span data-ttu-id="bd4b2-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bd4b2-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bd4b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4b2-128">CommonParameters</span></span>
<span data-ttu-id="bd4b2-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd4b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4b2-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4b2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4b2-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd4b2-131">INPUTS</span></span>

### <span data-ttu-id="bd4b2-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bd4b2-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="bd4b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bd4b2-133">System.String</span></span>

## <span data-ttu-id="bd4b2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd4b2-134">OUTPUTS</span></span>

### <span data-ttu-id="bd4b2-135">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="bd4b2-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="bd4b2-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="bd4b2-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="bd4b2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd4b2-137">NOTES</span></span>

## <span data-ttu-id="bd4b2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd4b2-138">RELATED LINKS</span></span>
