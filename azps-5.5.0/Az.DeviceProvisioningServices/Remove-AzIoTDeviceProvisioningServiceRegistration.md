---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163610"
---
# <span data-ttu-id="afb56-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="afb56-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="afb56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb56-102">SYNOPSIS</span></span>
<span data-ttu-id="afb56-103">Törli az eszköz regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="afb56-103">Deletes the device registration.</span></span>

## <span data-ttu-id="afb56-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="afb56-104">SYNTAX</span></span>

### <span data-ttu-id="afb56-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="afb56-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afb56-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afb56-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afb56-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afb56-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb56-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="afb56-108">DESCRIPTION</span></span>
<span data-ttu-id="afb56-109">Eszközregisztráció törlése egy Azure IoT-központ eszközépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="afb56-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="afb56-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="afb56-110">EXAMPLES</span></span>

### <span data-ttu-id="afb56-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="afb56-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="afb56-112">Eszközregisztráció törlése egy Azure IoT-központ eszközépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="afb56-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="afb56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb56-113">PARAMETERS</span></span>

### <span data-ttu-id="afb56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb56-114">-DefaultProfile</span></span>
<span data-ttu-id="afb56-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afb56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb56-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="afb56-116">-DpsName</span></span>
<span data-ttu-id="afb56-117">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="afb56-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="afb56-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="afb56-118">-DpsObject</span></span>
<span data-ttu-id="afb56-119">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="afb56-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="afb56-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afb56-120">-PassThru</span></span>
<span data-ttu-id="afb56-121">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="afb56-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="afb56-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="afb56-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="afb56-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="afb56-123">-RegistrationId</span></span>
<span data-ttu-id="afb56-124">Az eszközregisztráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="afb56-124">ID of device registration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb56-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb56-125">-ResourceGroupName</span></span>
<span data-ttu-id="afb56-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="afb56-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="afb56-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afb56-127">-ResourceId</span></span>
<span data-ttu-id="afb56-128">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="afb56-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="afb56-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afb56-129">-Confirm</span></span>
<span data-ttu-id="afb56-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="afb56-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb56-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb56-131">-WhatIf</span></span>
<span data-ttu-id="afb56-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="afb56-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb56-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="afb56-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb56-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb56-134">CommonParameters</span></span>
<span data-ttu-id="afb56-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb56-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb56-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb56-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb56-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afb56-137">INPUTS</span></span>

### <span data-ttu-id="afb56-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="afb56-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="afb56-139">System.String</span><span class="sxs-lookup"><span data-stu-id="afb56-139">System.String</span></span>

## <span data-ttu-id="afb56-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afb56-140">OUTPUTS</span></span>

### <span data-ttu-id="afb56-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afb56-141">System.Boolean</span></span>

## <span data-ttu-id="afb56-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="afb56-142">NOTES</span></span>

## <span data-ttu-id="afb56-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afb56-143">RELATED LINKS</span></span>
