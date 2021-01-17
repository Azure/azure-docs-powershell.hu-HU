---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466198"
---
# <span data-ttu-id="16c65-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="16c65-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="16c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c65-102">SYNOPSIS</span></span>
<span data-ttu-id="16c65-103">Töröljön egy Azure IoT Hub-eszköz kiépítési szolgáltatás tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="16c65-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="16c65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16c65-104">SYNTAX</span></span>

### <span data-ttu-id="16c65-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16c65-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c65-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16c65-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c65-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16c65-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c65-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16c65-108">DESCRIPTION</span></span>
<span data-ttu-id="16c65-109">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates lásd: .</span><span class="sxs-lookup"><span data-stu-id="16c65-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="16c65-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16c65-110">EXAMPLES</span></span>

### <span data-ttu-id="16c65-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="16c65-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="16c65-112">Törölje a "mycertificate" parancsot egy Azure IoT Hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="16c65-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="16c65-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c65-113">PARAMETERS</span></span>

### <span data-ttu-id="16c65-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="16c65-114">-CertificateName</span></span>
<span data-ttu-id="16c65-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="16c65-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c65-116">-DefaultProfile</span></span>
<span data-ttu-id="16c65-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16c65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c65-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="16c65-118">-Etag</span></span>
<span data-ttu-id="16c65-119">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="16c65-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="16c65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c65-120">-InputObject</span></span>
<span data-ttu-id="16c65-121">IoT-eszköz kiépítési szolgáltatás tanúsítványobjektuma</span><span class="sxs-lookup"><span data-stu-id="16c65-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16c65-122">-Name</span><span class="sxs-lookup"><span data-stu-id="16c65-122">-Name</span></span>
<span data-ttu-id="16c65-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="16c65-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="16c65-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16c65-124">-PassThru</span></span>
<span data-ttu-id="16c65-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="16c65-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="16c65-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c65-126">-ResourceGroupName</span></span>
<span data-ttu-id="16c65-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="16c65-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16c65-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16c65-128">-ResourceId</span></span>
<span data-ttu-id="16c65-129">IoT-eszköz kiépítési szolgáltatás tanúsítványának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="16c65-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="16c65-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16c65-130">-Confirm</span></span>
<span data-ttu-id="16c65-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="16c65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c65-132">-WhatIf</span></span>
<span data-ttu-id="16c65-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="16c65-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c65-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16c65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c65-135">CommonParameters</span></span>
<span data-ttu-id="16c65-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c65-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c65-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c65-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16c65-138">INPUTS</span></span>

### <span data-ttu-id="16c65-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="16c65-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="16c65-140">System.String</span><span class="sxs-lookup"><span data-stu-id="16c65-140">System.String</span></span>

## <span data-ttu-id="16c65-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16c65-141">OUTPUTS</span></span>

### <span data-ttu-id="16c65-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16c65-142">System.Boolean</span></span>

## <span data-ttu-id="16c65-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16c65-143">NOTES</span></span>

## <span data-ttu-id="16c65-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16c65-144">RELATED LINKS</span></span>
