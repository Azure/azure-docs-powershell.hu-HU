---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167618"
---
# <span data-ttu-id="2b33b-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="2b33b-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="2b33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b33b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b33b-103">Eszközregisztrációs rekord törlése</span><span class="sxs-lookup"><span data-stu-id="2b33b-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="2b33b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b33b-104">SYNTAX</span></span>

### <span data-ttu-id="2b33b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b33b-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b33b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b33b-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b33b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b33b-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b33b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b33b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b33b-109">Eszköz-regisztráció törlése egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="2b33b-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2b33b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b33b-110">EXAMPLES</span></span>

### <span data-ttu-id="2b33b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2b33b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="2b33b-112">Törölhet egy megadott regisztrációs rekordot.</span><span class="sxs-lookup"><span data-stu-id="2b33b-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="2b33b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2b33b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="2b33b-114">Törölje az összes regisztrációs rekordot.</span><span class="sxs-lookup"><span data-stu-id="2b33b-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="2b33b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b33b-115">PARAMETERS</span></span>

### <span data-ttu-id="2b33b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b33b-116">-DefaultProfile</span></span>
<span data-ttu-id="2b33b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b33b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b33b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2b33b-118">-DpsName</span></span>
<span data-ttu-id="2b33b-119">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="2b33b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2b33b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2b33b-120">-DpsObject</span></span>
<span data-ttu-id="2b33b-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="2b33b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2b33b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b33b-122">-PassThru</span></span>
<span data-ttu-id="2b33b-123">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="2b33b-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="2b33b-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2b33b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b33b-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="2b33b-125">-RegistrationId</span></span>
<span data-ttu-id="2b33b-126">Egyéni regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="2b33b-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="2b33b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b33b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b33b-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2b33b-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2b33b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b33b-129">-ResourceId</span></span>
<span data-ttu-id="2b33b-130">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2b33b-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2b33b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b33b-131">-Confirm</span></span>
<span data-ttu-id="2b33b-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2b33b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b33b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b33b-133">-WhatIf</span></span>
<span data-ttu-id="2b33b-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2b33b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b33b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b33b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b33b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b33b-136">CommonParameters</span></span>
<span data-ttu-id="2b33b-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b33b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b33b-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b33b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b33b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b33b-139">INPUTS</span></span>

### <span data-ttu-id="2b33b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2b33b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2b33b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2b33b-141">System.String</span></span>

## <span data-ttu-id="2b33b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b33b-142">OUTPUTS</span></span>

### <span data-ttu-id="2b33b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b33b-143">System.Boolean</span></span>

## <span data-ttu-id="2b33b-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b33b-144">NOTES</span></span>

## <span data-ttu-id="2b33b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b33b-145">RELATED LINKS</span></span>
