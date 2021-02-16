---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161699"
---
# <span data-ttu-id="11239-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11239-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="11239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11239-102">SYNOPSIS</span></span>
<span data-ttu-id="11239-103">Megosztott hozzáférési házirend frissítése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="11239-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="11239-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11239-104">SYNTAX</span></span>

### <span data-ttu-id="11239-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11239-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11239-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11239-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11239-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11239-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11239-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11239-108">DESCRIPTION</span></span>
<span data-ttu-id="11239-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="11239-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="11239-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11239-110">EXAMPLES</span></span>

### <span data-ttu-id="11239-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="11239-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="11239-112">Frissítse a hozzáférési házirend "mypolicy" egy Azure IoT Hub eszköz kiépítési szolgáltatásában a EnrollmentWrite jogosultsággal.</span><span class="sxs-lookup"><span data-stu-id="11239-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="11239-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="11239-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="11239-114">Frissítse a hozzáférési házirend "mypolicy" egy Azure IoT-központ eszköz kiépítési szolgáltatásában a EnrollmentWrite-et közvetlenül a folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="11239-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="11239-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11239-115">PARAMETERS</span></span>

### <span data-ttu-id="11239-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11239-116">-DefaultProfile</span></span>
<span data-ttu-id="11239-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11239-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11239-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11239-118">-InputObject</span></span>
<span data-ttu-id="11239-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="11239-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11239-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="11239-120">-KeyName</span></span>
<span data-ttu-id="11239-121">IoT-eszköz kiépítési szolgáltatás hozzáférési házirendkulcsának neve</span><span class="sxs-lookup"><span data-stu-id="11239-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11239-122">-Name</span><span class="sxs-lookup"><span data-stu-id="11239-122">-Name</span></span>
<span data-ttu-id="11239-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="11239-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="11239-124">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="11239-124">-Permissions</span></span>
<span data-ttu-id="11239-125">IoT-eszköz kiépítési szolgáltatás hozzáférési házirend-engedélyei</span><span class="sxs-lookup"><span data-stu-id="11239-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11239-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11239-126">-ResourceGroupName</span></span>
<span data-ttu-id="11239-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="11239-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11239-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11239-128">-ResourceId</span></span>
<span data-ttu-id="11239-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="11239-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="11239-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11239-130">-Confirm</span></span>
<span data-ttu-id="11239-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11239-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11239-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11239-132">-WhatIf</span></span>
<span data-ttu-id="11239-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11239-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11239-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11239-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11239-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11239-135">CommonParameters</span></span>
<span data-ttu-id="11239-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11239-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11239-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11239-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11239-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11239-138">INPUTS</span></span>

### <span data-ttu-id="11239-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="11239-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="11239-140">System.String</span><span class="sxs-lookup"><span data-stu-id="11239-140">System.String</span></span>

## <span data-ttu-id="11239-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11239-141">OUTPUTS</span></span>

### <span data-ttu-id="11239-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="11239-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="11239-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11239-143">NOTES</span></span>

## <span data-ttu-id="11239-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11239-144">RELATED LINKS</span></span>
