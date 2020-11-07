---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f5d750dc795619f32f6c4f16a5fe1e3b5e111106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680370"
---
# <span data-ttu-id="7eb80-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7eb80-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="7eb80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7eb80-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb80-103">Megosztott hozzáférésű házirend frissítése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7eb80-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7eb80-104">SYNTAX</span></span>

### <span data-ttu-id="7eb80-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7eb80-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eb80-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7eb80-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb80-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7eb80-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb80-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7eb80-108">DESCRIPTION</span></span>
<span data-ttu-id="7eb80-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7eb80-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7eb80-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7eb80-110">EXAMPLES</span></span>

### <span data-ttu-id="7eb80-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7eb80-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="7eb80-112">Frissítse a "mypolicy" Access-házirendet egy Azure IoT hub-eszköz kiépítési szolgáltatásban a EnrollmentWrite jobbra.</span><span class="sxs-lookup"><span data-stu-id="7eb80-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="7eb80-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7eb80-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzureRmIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="7eb80-114">Frissítse a "mypolicy" Access-házirendet egy Azure IoT hub-eszköz kiépítési szolgáltatásban, a EnrollmentWrite jobbra a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="7eb80-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="7eb80-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7eb80-115">PARAMETERS</span></span>

### <span data-ttu-id="7eb80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb80-116">-DefaultProfile</span></span>
<span data-ttu-id="7eb80-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7eb80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb80-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb80-118">-InputObject</span></span>
<span data-ttu-id="7eb80-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="7eb80-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7eb80-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="7eb80-120">-KeyName</span></span>
<span data-ttu-id="7eb80-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="7eb80-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="7eb80-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7eb80-122">-Name</span></span>
<span data-ttu-id="7eb80-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="7eb80-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7eb80-124">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="7eb80-124">-Permissions</span></span>
<span data-ttu-id="7eb80-125">IoT-eszközök kiépítése szolgáltatás-hozzáférési házirend engedélyei</span><span class="sxs-lookup"><span data-stu-id="7eb80-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="7eb80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb80-126">-ResourceGroupName</span></span>
<span data-ttu-id="7eb80-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7eb80-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7eb80-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eb80-128">-ResourceId</span></span>
<span data-ttu-id="7eb80-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7eb80-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7eb80-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7eb80-130">-Confirm</span></span>
<span data-ttu-id="7eb80-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7eb80-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb80-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb80-132">-WhatIf</span></span>
<span data-ttu-id="7eb80-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7eb80-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb80-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7eb80-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb80-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb80-135">CommonParameters</span></span>
<span data-ttu-id="7eb80-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7eb80-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb80-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb80-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb80-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eb80-138">INPUTS</span></span>

### <span data-ttu-id="7eb80-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="7eb80-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="7eb80-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7eb80-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7eb80-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb80-141">System.String</span></span>

## <span data-ttu-id="7eb80-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eb80-142">OUTPUTS</span></span>

### <span data-ttu-id="7eb80-143">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="7eb80-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="7eb80-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7eb80-144">NOTES</span></span>

## <span data-ttu-id="7eb80-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7eb80-145">RELATED LINKS</span></span>
