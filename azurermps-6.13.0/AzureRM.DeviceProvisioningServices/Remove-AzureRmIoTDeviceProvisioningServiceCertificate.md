---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672946"
---
# <span data-ttu-id="5ab8b-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="5ab8b-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="5ab8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ab8b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab8b-103">Azure IoT hub-eszköz kiépítési szolgáltatási tanúsítványának törlése</span><span class="sxs-lookup"><span data-stu-id="5ab8b-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ab8b-104">SYNTAX</span></span>

### <span data-ttu-id="5ab8b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ab8b-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab8b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ab8b-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab8b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ab8b-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab8b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ab8b-108">DESCRIPTION</span></span>
<span data-ttu-id="5ab8b-109">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="5ab8b-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="5ab8b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5ab8b-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab8b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5ab8b-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="5ab8b-112">Törölje a "mycertificate" kifejezést egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="5ab8b-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5ab8b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ab8b-113">PARAMETERS</span></span>

### <span data-ttu-id="5ab8b-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5ab8b-114">-CertificateName</span></span>
<span data-ttu-id="5ab8b-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="5ab8b-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="5ab8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab8b-116">-DefaultProfile</span></span>
<span data-ttu-id="5ab8b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ab8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab8b-118">-ETAG</span><span class="sxs-lookup"><span data-stu-id="5ab8b-118">-Etag</span></span>
<span data-ttu-id="5ab8b-119">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="5ab8b-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="5ab8b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ab8b-120">-InputObject</span></span>
<span data-ttu-id="5ab8b-121">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="5ab8b-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="5ab8b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ab8b-122">-Name</span></span>
<span data-ttu-id="5ab8b-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="5ab8b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5ab8b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ab8b-124">-PassThru</span></span>
<span data-ttu-id="5ab8b-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ab8b-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ab8b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab8b-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ab8b-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5ab8b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5ab8b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ab8b-128">-ResourceId</span></span>
<span data-ttu-id="5ab8b-129">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5ab8b-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="5ab8b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ab8b-130">-Confirm</span></span>
<span data-ttu-id="5ab8b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ab8b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab8b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab8b-132">-WhatIf</span></span>
<span data-ttu-id="5ab8b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ab8b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab8b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ab8b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab8b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab8b-135">CommonParameters</span></span>
<span data-ttu-id="5ab8b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ab8b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab8b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab8b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab8b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab8b-138">INPUTS</span></span>

### <span data-ttu-id="5ab8b-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="5ab8b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="5ab8b-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ab8b-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5ab8b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab8b-141">System.String</span></span>

## <span data-ttu-id="5ab8b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab8b-142">OUTPUTS</span></span>

### <span data-ttu-id="5ab8b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ab8b-143">System.Boolean</span></span>

## <span data-ttu-id="5ab8b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ab8b-144">NOTES</span></span>

## <span data-ttu-id="5ab8b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ab8b-145">RELATED LINKS</span></span>
