---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328799"
---
# <span data-ttu-id="ca5f2-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca5f2-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="ca5f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5f2-103">Vegyen fel egy új megosztott hozzáférési házirendet egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ca5f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca5f2-104">SYNTAX</span></span>

### <span data-ttu-id="ca5f2-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca5f2-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca5f2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca5f2-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca5f2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca5f2-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca5f2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca5f2-108">DESCRIPTION</span></span>
<span data-ttu-id="ca5f2-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ca5f2-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ca5f2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca5f2-110">EXAMPLES</span></span>

### <span data-ttu-id="ca5f2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ca5f2-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="ca5f2-112">Vegyen fel egy új megosztott hozzáférési házirendet egy Azure IoT-központ eszköz kiépítési szolgáltatásában a EnrollmentWrite és a ServiceConfig jogosultságokkal.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="ca5f2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ca5f2-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="ca5f2-114">Vegyen fel egy új megosztott hozzáférési házirendet egy Azure IoT-központ eszköz kiépítési szolgáltatásában a EnrollmentRead jobb oldalon.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="ca5f2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca5f2-115">PARAMETERS</span></span>

### <span data-ttu-id="ca5f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5f2-116">-DefaultProfile</span></span>
<span data-ttu-id="ca5f2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca5f2-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ca5f2-118">-DpsObject</span></span>
<span data-ttu-id="ca5f2-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="ca5f2-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ca5f2-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ca5f2-120">-KeyName</span></span>
<span data-ttu-id="ca5f2-121">IoT-eszköz kiépítési szolgáltatás hozzáférési házirendkulcsának neve</span><span class="sxs-lookup"><span data-stu-id="ca5f2-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="ca5f2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ca5f2-122">-Name</span></span>
<span data-ttu-id="ca5f2-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="ca5f2-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ca5f2-124">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="ca5f2-124">-Permissions</span></span>
<span data-ttu-id="ca5f2-125">IoT-eszköz kiépítési szolgáltatás hozzáférési házirend-engedélyei</span><span class="sxs-lookup"><span data-stu-id="ca5f2-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="ca5f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca5f2-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ca5f2-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca5f2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca5f2-128">-ResourceId</span></span>
<span data-ttu-id="ca5f2-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca5f2-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ca5f2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca5f2-130">-Confirm</span></span>
<span data-ttu-id="ca5f2-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca5f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5f2-132">-WhatIf</span></span>
<span data-ttu-id="ca5f2-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5f2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca5f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5f2-135">CommonParameters</span></span>
<span data-ttu-id="ca5f2-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5f2-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca5f2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5f2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca5f2-138">INPUTS</span></span>

### <span data-ttu-id="ca5f2-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ca5f2-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ca5f2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ca5f2-140">System.String</span></span>

## <span data-ttu-id="ca5f2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca5f2-141">OUTPUTS</span></span>

### <span data-ttu-id="ca5f2-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="ca5f2-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="ca5f2-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca5f2-143">NOTES</span></span>

## <span data-ttu-id="ca5f2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca5f2-144">RELATED LINKS</span></span>
