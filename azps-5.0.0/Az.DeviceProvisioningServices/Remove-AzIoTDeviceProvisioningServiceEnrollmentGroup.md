---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187477"
---
# <span data-ttu-id="29534-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="29534-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="29534-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29534-102">SYNOPSIS</span></span>
<span data-ttu-id="29534-103">Eszköz-beiktatási csoport törlése</span><span class="sxs-lookup"><span data-stu-id="29534-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="29534-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29534-104">SYNTAX</span></span>

### <span data-ttu-id="29534-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29534-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29534-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29534-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29534-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29534-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29534-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29534-108">DESCRIPTION</span></span>
<span data-ttu-id="29534-109">A tanúsítványigénylési csoport törlése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="29534-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="29534-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29534-110">EXAMPLES</span></span>

### <span data-ttu-id="29534-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29534-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="29534-112">A megadott tanúsítványigénylési csoport törlése</span><span class="sxs-lookup"><span data-stu-id="29534-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="29534-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="29534-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="29534-114">Az összes tanúsítványigénylési csoport törlése</span><span class="sxs-lookup"><span data-stu-id="29534-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="29534-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29534-115">PARAMETERS</span></span>

### <span data-ttu-id="29534-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29534-116">-DefaultProfile</span></span>
<span data-ttu-id="29534-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29534-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29534-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="29534-118">-DpsName</span></span>
<span data-ttu-id="29534-119">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="29534-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="29534-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="29534-120">-DpsObject</span></span>
<span data-ttu-id="29534-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="29534-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="29534-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29534-122">-Name</span></span>
<span data-ttu-id="29534-123">A beiratkozási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="29534-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="29534-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29534-124">-PassThru</span></span>
<span data-ttu-id="29534-125">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="29534-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="29534-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="29534-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29534-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29534-127">-ResourceGroupName</span></span>
<span data-ttu-id="29534-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="29534-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29534-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29534-129">-ResourceId</span></span>
<span data-ttu-id="29534-130">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="29534-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="29534-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29534-131">-Confirm</span></span>
<span data-ttu-id="29534-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29534-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29534-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29534-133">-WhatIf</span></span>
<span data-ttu-id="29534-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29534-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29534-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29534-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29534-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29534-136">CommonParameters</span></span>
<span data-ttu-id="29534-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29534-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29534-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29534-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29534-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29534-139">INPUTS</span></span>

### <span data-ttu-id="29534-140">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="29534-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="29534-141">System. String</span><span class="sxs-lookup"><span data-stu-id="29534-141">System.String</span></span>

## <span data-ttu-id="29534-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29534-142">OUTPUTS</span></span>

### <span data-ttu-id="29534-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29534-143">System.Boolean</span></span>

## <span data-ttu-id="29534-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29534-144">NOTES</span></span>

## <span data-ttu-id="29534-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29534-145">RELATED LINKS</span></span>
