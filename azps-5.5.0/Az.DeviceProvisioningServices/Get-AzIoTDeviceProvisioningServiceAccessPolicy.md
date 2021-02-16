---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167658"
---
# <span data-ttu-id="841ec-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="841ec-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="841ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="841ec-102">SYNOPSIS</span></span>
<span data-ttu-id="841ec-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span><span class="sxs-lookup"><span data-stu-id="841ec-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="841ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="841ec-104">SYNTAX</span></span>

### <span data-ttu-id="841ec-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="841ec-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="841ec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="841ec-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="841ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="841ec-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="841ec-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="841ec-108">DESCRIPTION</span></span>
<span data-ttu-id="841ec-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="841ec-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="841ec-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="841ec-110">EXAMPLES</span></span>

### <span data-ttu-id="841ec-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="841ec-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="841ec-112">List all shared access policies in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="841ec-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="841ec-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="841ec-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="841ec-114">A megosztott hozzáférési házirendek "mypolicy" részleteinek megjelenítése az Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="841ec-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="841ec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="841ec-115">PARAMETERS</span></span>

### <span data-ttu-id="841ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841ec-116">-DefaultProfile</span></span>
<span data-ttu-id="841ec-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="841ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="841ec-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="841ec-118">-DpsObject</span></span>
<span data-ttu-id="841ec-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="841ec-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="841ec-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="841ec-120">-KeyName</span></span>
<span data-ttu-id="841ec-121">IoT-eszköz kiépítési szolgáltatás hozzáférési házirendkulcsának neve</span><span class="sxs-lookup"><span data-stu-id="841ec-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="841ec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="841ec-122">-Name</span></span>
<span data-ttu-id="841ec-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="841ec-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="841ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="841ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="841ec-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="841ec-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="841ec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="841ec-126">-ResourceId</span></span>
<span data-ttu-id="841ec-127">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="841ec-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="841ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841ec-128">CommonParameters</span></span>
<span data-ttu-id="841ec-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841ec-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841ec-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841ec-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="841ec-131">INPUTS</span></span>

### <span data-ttu-id="841ec-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="841ec-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="841ec-133">System.String</span><span class="sxs-lookup"><span data-stu-id="841ec-133">System.String</span></span>

## <span data-ttu-id="841ec-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="841ec-134">OUTPUTS</span></span>

### <span data-ttu-id="841ec-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="841ec-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="841ec-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="841ec-136">NOTES</span></span>

## <span data-ttu-id="841ec-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="841ec-137">RELATED LINKS</span></span>
