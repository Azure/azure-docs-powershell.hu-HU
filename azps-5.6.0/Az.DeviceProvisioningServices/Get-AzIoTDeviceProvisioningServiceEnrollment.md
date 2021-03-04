---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 56aadda2d7f1dccb77795d5226fb79c8a0fc65ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921977"
---
# <span data-ttu-id="f252b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="f252b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="f252b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f252b-102">SYNOPSIS</span></span>
<span data-ttu-id="f252b-103">Eszközregisztrációs rekord igénylése.</span><span class="sxs-lookup"><span data-stu-id="f252b-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="f252b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f252b-104">SYNTAX</span></span>

### <span data-ttu-id="f252b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f252b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f252b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f252b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f252b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f252b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f252b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f252b-108">DESCRIPTION</span></span>
<span data-ttu-id="f252b-109">Eszközbeiratkozási adatokat vagy eszközregisztrációs listaelemeket olvashat az Azure IoT Hub eszközépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="f252b-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f252b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f252b-110">EXAMPLES</span></span>

### <span data-ttu-id="f252b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f252b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="f252b-112">Eszközregisztrációs adatok lekérte egy Azure IoT-központ eszközépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="f252b-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="f252b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f252b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="f252b-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="f252b-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f252b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f252b-115">PARAMETERS</span></span>

### <span data-ttu-id="f252b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f252b-116">-DefaultProfile</span></span>
<span data-ttu-id="f252b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f252b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f252b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f252b-118">-DpsName</span></span>
<span data-ttu-id="f252b-119">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f252b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f252b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f252b-120">-DpsObject</span></span>
<span data-ttu-id="f252b-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="f252b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f252b-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="f252b-122">-RegistrationId</span></span>
<span data-ttu-id="f252b-123">Egyéni regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="f252b-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="f252b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f252b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f252b-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f252b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f252b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f252b-126">-ResourceId</span></span>
<span data-ttu-id="f252b-127">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f252b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f252b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f252b-128">CommonParameters</span></span>
<span data-ttu-id="f252b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f252b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f252b-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f252b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f252b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f252b-131">INPUTS</span></span>

### <span data-ttu-id="f252b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f252b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f252b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f252b-133">System.String</span></span>

## <span data-ttu-id="f252b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f252b-134">OUTPUTS</span></span>

### <span data-ttu-id="f252b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="f252b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="f252b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="f252b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="f252b-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f252b-137">NOTES</span></span>

## <span data-ttu-id="f252b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f252b-138">RELATED LINKS</span></span>
