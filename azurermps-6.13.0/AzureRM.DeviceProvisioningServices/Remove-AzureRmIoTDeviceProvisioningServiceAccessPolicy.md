---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499531"
---
# <span data-ttu-id="fab5b-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fab5b-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="fab5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fab5b-102">SYNOPSIS</span></span>
<span data-ttu-id="fab5b-103">Megosztott hozzáférésű házirendek törlése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="fab5b-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fab5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fab5b-104">SYNTAX</span></span>

### <span data-ttu-id="fab5b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fab5b-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fab5b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fab5b-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab5b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fab5b-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab5b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fab5b-108">DESCRIPTION</span></span>
<span data-ttu-id="fab5b-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fab5b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fab5b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fab5b-110">EXAMPLES</span></span>

### <span data-ttu-id="fab5b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fab5b-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="fab5b-112">Törölje a "mypolicy" megosztott elérési házirendet az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="fab5b-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="fab5b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fab5b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="fab5b-114">Törölje a "mypolicy" megosztott elérési házirendet egy Azure IoT hub-eszköz kiépítési szolgáltatásához a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="fab5b-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="fab5b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fab5b-115">PARAMETERS</span></span>

### <span data-ttu-id="fab5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab5b-116">-DefaultProfile</span></span>
<span data-ttu-id="fab5b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fab5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab5b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab5b-118">-InputObject</span></span>
<span data-ttu-id="fab5b-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="fab5b-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fab5b-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="fab5b-120">-KeyName</span></span>
<span data-ttu-id="fab5b-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="fab5b-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="fab5b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fab5b-122">-Name</span></span>
<span data-ttu-id="fab5b-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="fab5b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fab5b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fab5b-124">-PassThru</span></span>
<span data-ttu-id="fab5b-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fab5b-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab5b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab5b-126">-ResourceGroupName</span></span>
<span data-ttu-id="fab5b-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fab5b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fab5b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fab5b-128">-ResourceId</span></span>
<span data-ttu-id="fab5b-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fab5b-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fab5b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fab5b-130">-Confirm</span></span>
<span data-ttu-id="fab5b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fab5b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab5b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab5b-132">-WhatIf</span></span>
<span data-ttu-id="fab5b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fab5b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab5b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fab5b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab5b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab5b-135">CommonParameters</span></span>
<span data-ttu-id="fab5b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fab5b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab5b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab5b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab5b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fab5b-138">INPUTS</span></span>

### <span data-ttu-id="fab5b-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="fab5b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="fab5b-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fab5b-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fab5b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fab5b-141">System.String</span></span>

## <span data-ttu-id="fab5b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fab5b-142">OUTPUTS</span></span>

### <span data-ttu-id="fab5b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fab5b-143">System.Boolean</span></span>

## <span data-ttu-id="fab5b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fab5b-144">NOTES</span></span>

## <span data-ttu-id="fab5b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fab5b-145">RELATED LINKS</span></span>
