---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011898"
---
# <span data-ttu-id="d0eb5-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0eb5-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d0eb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d0eb5-103">Megosztott hozzáférésű házirend frissítése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d0eb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0eb5-104">SYNTAX</span></span>

### <span data-ttu-id="d0eb5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0eb5-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0eb5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0eb5-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0eb5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0eb5-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0eb5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="d0eb5-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d0eb5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d0eb5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d0eb5-110">EXAMPLES</span></span>

### <span data-ttu-id="d0eb5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0eb5-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="d0eb5-112">Frissítse a "mypolicy" Access-házirendet egy Azure IoT hub-eszköz kiépítési szolgáltatásban a EnrollmentWrite jobbra.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="d0eb5-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0eb5-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="d0eb5-114">Frissítse a "mypolicy" Access-házirendet egy Azure IoT hub-eszköz kiépítési szolgáltatásban, a EnrollmentWrite jobbra a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="d0eb5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0eb5-115">PARAMETERS</span></span>

### <span data-ttu-id="d0eb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0eb5-116">-DefaultProfile</span></span>
<span data-ttu-id="d0eb5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0eb5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0eb5-118">-InputObject</span></span>
<span data-ttu-id="d0eb5-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="d0eb5-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d0eb5-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="d0eb5-120">-KeyName</span></span>
<span data-ttu-id="d0eb5-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="d0eb5-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="d0eb5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0eb5-122">-Name</span></span>
<span data-ttu-id="d0eb5-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="d0eb5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d0eb5-124">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="d0eb5-124">-Permissions</span></span>
<span data-ttu-id="d0eb5-125">IoT-eszközök kiépítése szolgáltatás-hozzáférési házirend engedélyei</span><span class="sxs-lookup"><span data-stu-id="d0eb5-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="d0eb5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0eb5-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0eb5-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d0eb5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0eb5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0eb5-128">-ResourceId</span></span>
<span data-ttu-id="d0eb5-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d0eb5-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d0eb5-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0eb5-130">-Confirm</span></span>
<span data-ttu-id="d0eb5-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0eb5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0eb5-132">-WhatIf</span></span>
<span data-ttu-id="d0eb5-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0eb5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0eb5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0eb5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0eb5-135">CommonParameters</span></span>
<span data-ttu-id="d0eb5-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0eb5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0eb5-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0eb5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0eb5-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0eb5-138">INPUTS</span></span>

### <span data-ttu-id="d0eb5-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="d0eb5-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="d0eb5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d0eb5-140">System.String</span></span>

## <span data-ttu-id="d0eb5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0eb5-141">OUTPUTS</span></span>

### <span data-ttu-id="d0eb5-142">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="d0eb5-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="d0eb5-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0eb5-143">NOTES</span></span>

## <span data-ttu-id="d0eb5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0eb5-144">RELATED LINKS</span></span>
