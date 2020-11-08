---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185495"
---
# <span data-ttu-id="b345f-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="b345f-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="b345f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b345f-102">SYNOPSIS</span></span>
<span data-ttu-id="b345f-103">Törli az eszköz regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="b345f-103">Deletes the device registration.</span></span>

## <span data-ttu-id="b345f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b345f-104">SYNTAX</span></span>

### <span data-ttu-id="b345f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b345f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b345f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b345f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b345f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b345f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b345f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b345f-108">DESCRIPTION</span></span>
<span data-ttu-id="b345f-109">Eszköz-Regisztráció törlése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="b345f-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="b345f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b345f-110">EXAMPLES</span></span>

### <span data-ttu-id="b345f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b345f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="b345f-112">Eszköz-Regisztráció törlése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="b345f-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="b345f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b345f-113">PARAMETERS</span></span>

### <span data-ttu-id="b345f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b345f-114">-DefaultProfile</span></span>
<span data-ttu-id="b345f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b345f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b345f-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="b345f-116">-DpsName</span></span>
<span data-ttu-id="b345f-117">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="b345f-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b345f-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="b345f-118">-DpsObject</span></span>
<span data-ttu-id="b345f-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="b345f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b345f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b345f-120">-PassThru</span></span>
<span data-ttu-id="b345f-121">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="b345f-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="b345f-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b345f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b345f-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="b345f-123">-RegistrationId</span></span>
<span data-ttu-id="b345f-124">Az eszköz regisztrációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b345f-124">ID of device registration.</span></span>

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

### <span data-ttu-id="b345f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b345f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b345f-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b345f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b345f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b345f-127">-ResourceId</span></span>
<span data-ttu-id="b345f-128">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b345f-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b345f-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b345f-129">-Confirm</span></span>
<span data-ttu-id="b345f-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b345f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b345f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b345f-131">-WhatIf</span></span>
<span data-ttu-id="b345f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b345f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b345f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b345f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b345f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b345f-134">CommonParameters</span></span>
<span data-ttu-id="b345f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b345f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b345f-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b345f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b345f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b345f-137">INPUTS</span></span>

### <span data-ttu-id="b345f-138">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b345f-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b345f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b345f-139">System.String</span></span>

## <span data-ttu-id="b345f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b345f-140">OUTPUTS</span></span>

### <span data-ttu-id="b345f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b345f-141">System.Boolean</span></span>

## <span data-ttu-id="b345f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b345f-142">NOTES</span></span>

## <span data-ttu-id="b345f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b345f-143">RELATED LINKS</span></span>
