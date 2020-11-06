---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 23d9e40fe6d25fbd2a6bb3e23959d1a4bf087af2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502112"
---
# <span data-ttu-id="8ce23-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ce23-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="8ce23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ce23-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce23-103">Új megosztott hozzáférési házirend hozzáadása az Azure IoT hub-eszközök kiépítési szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="8ce23-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ce23-104">SYNTAX</span></span>

### <span data-ttu-id="8ce23-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ce23-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ce23-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ce23-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ce23-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8ce23-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce23-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ce23-108">DESCRIPTION</span></span>
<span data-ttu-id="8ce23-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8ce23-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8ce23-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8ce23-110">EXAMPLES</span></span>

### <span data-ttu-id="8ce23-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8ce23-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="8ce23-112">Új megosztott hozzáférési házirend hozzáadása az Azure IoT hub eszköz kiépítési szolgáltatásához a EnrollmentWrite és a ServiceConfig jogosultságokkal.</span><span class="sxs-lookup"><span data-stu-id="8ce23-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="8ce23-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8ce23-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="8ce23-114">Új, megosztott hozzáférési házirend hozzáadása az Azure IoT hub eszköz kiépítési szolgáltatásához a EnrollmentRead jobb oldalán.</span><span class="sxs-lookup"><span data-stu-id="8ce23-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="8ce23-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ce23-115">PARAMETERS</span></span>

### <span data-ttu-id="8ce23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce23-116">-DefaultProfile</span></span>
<span data-ttu-id="8ce23-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ce23-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ce23-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8ce23-118">-DpsObject</span></span>
<span data-ttu-id="8ce23-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="8ce23-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8ce23-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="8ce23-120">-KeyName</span></span>
<span data-ttu-id="8ce23-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="8ce23-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce23-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ce23-122">-Name</span></span>
<span data-ttu-id="8ce23-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="8ce23-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8ce23-124">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="8ce23-124">-Permissions</span></span>
<span data-ttu-id="8ce23-125">IoT-eszközök kiépítése szolgáltatás-hozzáférési házirend engedélyei</span><span class="sxs-lookup"><span data-stu-id="8ce23-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="8ce23-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce23-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ce23-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8ce23-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8ce23-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ce23-128">-ResourceId</span></span>
<span data-ttu-id="8ce23-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8ce23-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8ce23-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ce23-130">-Confirm</span></span>
<span data-ttu-id="8ce23-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ce23-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce23-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce23-132">-WhatIf</span></span>
<span data-ttu-id="8ce23-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ce23-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce23-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ce23-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce23-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce23-135">CommonParameters</span></span>
<span data-ttu-id="8ce23-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ce23-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce23-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce23-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce23-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce23-138">INPUTS</span></span>

### <span data-ttu-id="8ce23-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8ce23-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="8ce23-140">Paraméterek: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ce23-140">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="8ce23-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8ce23-141">System.String</span></span>

## <span data-ttu-id="8ce23-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce23-142">OUTPUTS</span></span>

### <span data-ttu-id="8ce23-143">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="8ce23-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="8ce23-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ce23-144">NOTES</span></span>

## <span data-ttu-id="8ce23-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ce23-145">RELATED LINKS</span></span>
