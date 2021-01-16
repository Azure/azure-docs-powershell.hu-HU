---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328701"
---
# <span data-ttu-id="c5938-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="c5938-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="c5938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5938-102">SYNOPSIS</span></span>
<span data-ttu-id="c5938-103">Eszközregisztrációs csoport törlése.</span><span class="sxs-lookup"><span data-stu-id="c5938-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="c5938-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5938-104">SYNTAX</span></span>

### <span data-ttu-id="c5938-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5938-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5938-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5938-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5938-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c5938-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5938-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5938-108">DESCRIPTION</span></span>
<span data-ttu-id="c5938-109">Törölhet egy regisztrációs csoportot egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="c5938-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c5938-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5938-110">EXAMPLES</span></span>

### <span data-ttu-id="c5938-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5938-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="c5938-112">Egy megadott regisztrációs csoport törlése.</span><span class="sxs-lookup"><span data-stu-id="c5938-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="c5938-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c5938-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="c5938-114">Törölje az összes regisztrációs csoportot.</span><span class="sxs-lookup"><span data-stu-id="c5938-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="c5938-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5938-115">PARAMETERS</span></span>

### <span data-ttu-id="c5938-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5938-116">-DefaultProfile</span></span>
<span data-ttu-id="c5938-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5938-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5938-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c5938-118">-DpsName</span></span>
<span data-ttu-id="c5938-119">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="c5938-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c5938-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c5938-120">-DpsObject</span></span>
<span data-ttu-id="c5938-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="c5938-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c5938-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c5938-122">-Name</span></span>
<span data-ttu-id="c5938-123">A regisztrációs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5938-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="c5938-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5938-124">-PassThru</span></span>
<span data-ttu-id="c5938-125">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="c5938-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="c5938-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c5938-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c5938-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5938-127">-ResourceGroupName</span></span>
<span data-ttu-id="c5938-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c5938-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c5938-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5938-129">-ResourceId</span></span>
<span data-ttu-id="c5938-130">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c5938-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c5938-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5938-131">-Confirm</span></span>
<span data-ttu-id="c5938-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5938-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5938-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5938-133">-WhatIf</span></span>
<span data-ttu-id="c5938-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5938-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5938-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5938-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5938-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5938-136">CommonParameters</span></span>
<span data-ttu-id="c5938-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5938-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5938-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5938-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5938-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5938-139">INPUTS</span></span>

### <span data-ttu-id="c5938-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c5938-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c5938-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c5938-141">System.String</span></span>

## <span data-ttu-id="c5938-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5938-142">OUTPUTS</span></span>

### <span data-ttu-id="c5938-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5938-143">System.Boolean</span></span>

## <span data-ttu-id="c5938-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5938-144">NOTES</span></span>

## <span data-ttu-id="c5938-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5938-145">RELATED LINKS</span></span>
