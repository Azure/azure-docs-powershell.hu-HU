---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376989"
---
# <span data-ttu-id="e6922-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6922-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="e6922-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6922-102">SYNOPSIS</span></span>
<span data-ttu-id="e6922-103">Megosztott hozzáférési házirendek törlése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="e6922-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e6922-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6922-104">SYNTAX</span></span>

### <span data-ttu-id="e6922-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6922-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6922-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6922-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6922-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e6922-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6922-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6922-108">DESCRIPTION</span></span>
<span data-ttu-id="e6922-109">Az Azure IoT Hub eszköztelepítési szolgáltatásának bemutatása: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e6922-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e6922-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6922-110">EXAMPLES</span></span>

### <span data-ttu-id="e6922-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6922-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="e6922-112">A megosztott hozzáférési házirend "mypolicy" törlése egy Azure IoT Hub-eszköz kiépítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e6922-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="e6922-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6922-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="e6922-114">A megosztott hozzáférési házirend "mypolicy" törlése egy Azure IoT-központbeli eszköz kiépítési szolgáltatásában egy folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="e6922-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="e6922-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6922-115">PARAMETERS</span></span>

### <span data-ttu-id="e6922-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6922-116">-DefaultProfile</span></span>
<span data-ttu-id="e6922-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6922-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6922-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6922-118">-InputObject</span></span>
<span data-ttu-id="e6922-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="e6922-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e6922-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e6922-120">-KeyName</span></span>
<span data-ttu-id="e6922-121">IoT-eszköz kiépítési szolgáltatás hozzáférési házirendkulcsának neve</span><span class="sxs-lookup"><span data-stu-id="e6922-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="e6922-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e6922-122">-Name</span></span>
<span data-ttu-id="e6922-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="e6922-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e6922-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6922-124">-PassThru</span></span>
<span data-ttu-id="e6922-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e6922-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e6922-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6922-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6922-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e6922-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e6922-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6922-128">-ResourceId</span></span>
<span data-ttu-id="e6922-129">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e6922-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e6922-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6922-130">-Confirm</span></span>
<span data-ttu-id="e6922-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6922-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6922-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6922-132">-WhatIf</span></span>
<span data-ttu-id="e6922-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6922-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6922-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6922-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6922-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6922-135">CommonParameters</span></span>
<span data-ttu-id="e6922-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6922-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6922-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6922-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6922-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6922-138">INPUTS</span></span>

### <span data-ttu-id="e6922-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="e6922-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="e6922-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e6922-140">System.String</span></span>

## <span data-ttu-id="e6922-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6922-141">OUTPUTS</span></span>

### <span data-ttu-id="e6922-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6922-142">System.Boolean</span></span>

## <span data-ttu-id="e6922-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6922-143">NOTES</span></span>

## <span data-ttu-id="e6922-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6922-144">RELATED LINKS</span></span>
