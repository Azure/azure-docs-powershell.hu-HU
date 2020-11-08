---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184551"
---
# <span data-ttu-id="4c566-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="4c566-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="4c566-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c566-102">SYNOPSIS</span></span>
<span data-ttu-id="4c566-103">Az eszközök tanúsítványigénylési csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4c566-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="4c566-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c566-104">SYNTAX</span></span>

### <span data-ttu-id="4c566-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c566-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c566-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c566-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c566-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4c566-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c566-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c566-108">DESCRIPTION</span></span>
<span data-ttu-id="4c566-109">Megtudhatja, hogy milyen adatokat kell beszereznie a tanúsítványigénylési csoporttól, vagy listázhatja az összes beiratkozási csoportot egy Azure IoT hub-eszköz kiépítési szolgáltatása</span><span class="sxs-lookup"><span data-stu-id="4c566-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4c566-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c566-110">EXAMPLES</span></span>

### <span data-ttu-id="4c566-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c566-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="4c566-112">Eszköztelepítési csoport beszerzése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="4c566-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="4c566-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c566-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="4c566-114">Az összes eszköz-igénylési csoport listázása az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="4c566-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4c566-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c566-115">PARAMETERS</span></span>

### <span data-ttu-id="4c566-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c566-116">-DefaultProfile</span></span>
<span data-ttu-id="4c566-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c566-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c566-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4c566-118">-DpsName</span></span>
<span data-ttu-id="4c566-119">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="4c566-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4c566-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4c566-120">-DpsObject</span></span>
<span data-ttu-id="4c566-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="4c566-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4c566-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c566-122">-Name</span></span>
<span data-ttu-id="4c566-123">A beiratkozási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4c566-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="4c566-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c566-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c566-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4c566-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4c566-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c566-126">-ResourceId</span></span>
<span data-ttu-id="4c566-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4c566-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4c566-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c566-128">CommonParameters</span></span>
<span data-ttu-id="4c566-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c566-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c566-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c566-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c566-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c566-131">INPUTS</span></span>

### <span data-ttu-id="4c566-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4c566-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4c566-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4c566-133">System.String</span></span>

## <span data-ttu-id="4c566-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c566-134">OUTPUTS</span></span>

### <span data-ttu-id="4c566-135">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="4c566-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="4c566-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="4c566-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="4c566-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c566-137">NOTES</span></span>

## <span data-ttu-id="4c566-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c566-138">RELATED LINKS</span></span>
