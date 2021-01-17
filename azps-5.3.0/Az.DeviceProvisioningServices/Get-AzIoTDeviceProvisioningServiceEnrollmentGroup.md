---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467810"
---
# <span data-ttu-id="27993-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="27993-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="27993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27993-102">SYNOPSIS</span></span>
<span data-ttu-id="27993-103">Eszközregisztrációs csoport igénylése.</span><span class="sxs-lookup"><span data-stu-id="27993-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="27993-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27993-104">SYNTAX</span></span>

### <span data-ttu-id="27993-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27993-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27993-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27993-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27993-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27993-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27993-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27993-108">DESCRIPTION</span></span>
<span data-ttu-id="27993-109">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található regisztrációs csoportok részleteinek leigénylése vagy az összes regisztrációs csoport felsorolása.</span><span class="sxs-lookup"><span data-stu-id="27993-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="27993-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27993-110">EXAMPLES</span></span>

### <span data-ttu-id="27993-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="27993-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="27993-112">Eszközregisztrációs csoport lekérte egy Azure IoT-központ eszközépítési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="27993-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="27993-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="27993-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="27993-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="27993-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="27993-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27993-115">PARAMETERS</span></span>

### <span data-ttu-id="27993-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27993-116">-DefaultProfile</span></span>
<span data-ttu-id="27993-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27993-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27993-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="27993-118">-DpsName</span></span>
<span data-ttu-id="27993-119">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="27993-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="27993-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="27993-120">-DpsObject</span></span>
<span data-ttu-id="27993-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="27993-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="27993-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27993-122">-Name</span></span>
<span data-ttu-id="27993-123">A regisztrációs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="27993-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="27993-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27993-124">-ResourceGroupName</span></span>
<span data-ttu-id="27993-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="27993-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27993-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27993-126">-ResourceId</span></span>
<span data-ttu-id="27993-127">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="27993-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="27993-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27993-128">CommonParameters</span></span>
<span data-ttu-id="27993-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27993-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27993-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27993-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27993-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27993-131">INPUTS</span></span>

### <span data-ttu-id="27993-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="27993-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="27993-133">System.String</span><span class="sxs-lookup"><span data-stu-id="27993-133">System.String</span></span>

## <span data-ttu-id="27993-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27993-134">OUTPUTS</span></span>

### <span data-ttu-id="27993-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="27993-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="27993-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="27993-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="27993-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27993-137">NOTES</span></span>

## <span data-ttu-id="27993-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27993-138">RELATED LINKS</span></span>
