---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185499"
---
# <span data-ttu-id="54fc6-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="54fc6-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="54fc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="54fc6-103">Eszköz-beiktatási rekord törlése</span><span class="sxs-lookup"><span data-stu-id="54fc6-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="54fc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54fc6-104">SYNTAX</span></span>

### <span data-ttu-id="54fc6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54fc6-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54fc6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54fc6-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54fc6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54fc6-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fc6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="54fc6-108">DESCRIPTION</span></span>
<span data-ttu-id="54fc6-109">Eszköz-igénylés törlése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="54fc6-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="54fc6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="54fc6-110">EXAMPLES</span></span>

### <span data-ttu-id="54fc6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54fc6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="54fc6-112">A megadott tanúsítványigénylési rekord törlése</span><span class="sxs-lookup"><span data-stu-id="54fc6-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="54fc6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="54fc6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="54fc6-114">Törölje az összes beiratkozási rekordot.</span><span class="sxs-lookup"><span data-stu-id="54fc6-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="54fc6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54fc6-115">PARAMETERS</span></span>

### <span data-ttu-id="54fc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fc6-116">-DefaultProfile</span></span>
<span data-ttu-id="54fc6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54fc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54fc6-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="54fc6-118">-DpsName</span></span>
<span data-ttu-id="54fc6-119">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="54fc6-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="54fc6-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="54fc6-120">-DpsObject</span></span>
<span data-ttu-id="54fc6-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="54fc6-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="54fc6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54fc6-122">-PassThru</span></span>
<span data-ttu-id="54fc6-123">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="54fc6-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="54fc6-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="54fc6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54fc6-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="54fc6-125">-RegistrationId</span></span>
<span data-ttu-id="54fc6-126">Egyéni beiratkozási regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="54fc6-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="54fc6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fc6-127">-ResourceGroupName</span></span>
<span data-ttu-id="54fc6-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="54fc6-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54fc6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54fc6-129">-ResourceId</span></span>
<span data-ttu-id="54fc6-130">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="54fc6-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="54fc6-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54fc6-131">-Confirm</span></span>
<span data-ttu-id="54fc6-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54fc6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fc6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fc6-133">-WhatIf</span></span>
<span data-ttu-id="54fc6-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54fc6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fc6-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54fc6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fc6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fc6-136">CommonParameters</span></span>
<span data-ttu-id="54fc6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54fc6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fc6-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fc6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fc6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54fc6-139">INPUTS</span></span>

### <span data-ttu-id="54fc6-140">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="54fc6-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="54fc6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="54fc6-141">System.String</span></span>

## <span data-ttu-id="54fc6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54fc6-142">OUTPUTS</span></span>

### <span data-ttu-id="54fc6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54fc6-143">System.Boolean</span></span>

## <span data-ttu-id="54fc6-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54fc6-144">NOTES</span></span>

## <span data-ttu-id="54fc6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54fc6-145">RELATED LINKS</span></span>