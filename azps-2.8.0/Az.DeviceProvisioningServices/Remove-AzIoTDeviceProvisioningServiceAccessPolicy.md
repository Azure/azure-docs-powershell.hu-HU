---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 1efd429489be41f619454fd2b772c7cbb1ebc5c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666579"
---
# <span data-ttu-id="320d7-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="320d7-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="320d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="320d7-102">SYNOPSIS</span></span>
<span data-ttu-id="320d7-103">Megosztott hozzáférésű házirendek törlése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="320d7-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="320d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="320d7-104">SYNTAX</span></span>

### <span data-ttu-id="320d7-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="320d7-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="320d7-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="320d7-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320d7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="320d7-108">DESCRIPTION</span></span>
<span data-ttu-id="320d7-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="320d7-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="320d7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="320d7-110">EXAMPLES</span></span>

### <span data-ttu-id="320d7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="320d7-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="320d7-112">Törölje a "mypolicy" megosztott elérési házirendet az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="320d7-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="320d7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="320d7-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="320d7-114">Törölje a "mypolicy" megosztott elérési házirendet egy Azure IoT hub-eszköz kiépítési szolgáltatásához a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="320d7-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="320d7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="320d7-115">PARAMETERS</span></span>

### <span data-ttu-id="320d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320d7-116">-DefaultProfile</span></span>
<span data-ttu-id="320d7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="320d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="320d7-118">-InputObject</span></span>
<span data-ttu-id="320d7-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="320d7-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="320d7-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="320d7-120">-KeyName</span></span>
<span data-ttu-id="320d7-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="320d7-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="320d7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="320d7-122">-Name</span></span>
<span data-ttu-id="320d7-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="320d7-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="320d7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="320d7-124">-PassThru</span></span>
<span data-ttu-id="320d7-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="320d7-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="320d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="320d7-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="320d7-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="320d7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="320d7-128">-ResourceId</span></span>
<span data-ttu-id="320d7-129">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="320d7-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="320d7-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="320d7-130">-Confirm</span></span>
<span data-ttu-id="320d7-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="320d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320d7-132">-WhatIf</span></span>
<span data-ttu-id="320d7-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="320d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320d7-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="320d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320d7-135">CommonParameters</span></span>
<span data-ttu-id="320d7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="320d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320d7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320d7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320d7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="320d7-138">INPUTS</span></span>

### <span data-ttu-id="320d7-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="320d7-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="320d7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="320d7-140">System.String</span></span>

## <span data-ttu-id="320d7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="320d7-141">OUTPUTS</span></span>

### <span data-ttu-id="320d7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="320d7-142">System.Boolean</span></span>

## <span data-ttu-id="320d7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="320d7-143">NOTES</span></span>

## <span data-ttu-id="320d7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="320d7-144">RELATED LINKS</span></span>
