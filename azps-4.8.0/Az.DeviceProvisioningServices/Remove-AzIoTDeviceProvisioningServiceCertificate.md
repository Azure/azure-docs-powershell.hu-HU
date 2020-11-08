---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184997"
---
# <span data-ttu-id="dfbd5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="dfbd5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="dfbd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbd5-103">Azure IoT hub-eszköz kiépítési szolgáltatási tanúsítványának törlése</span><span class="sxs-lookup"><span data-stu-id="dfbd5-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="dfbd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfbd5-104">SYNTAX</span></span>

### <span data-ttu-id="dfbd5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dfbd5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbd5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dfbd5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbd5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dfbd5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfbd5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfbd5-108">DESCRIPTION</span></span>
<span data-ttu-id="dfbd5-109">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="dfbd5-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="dfbd5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dfbd5-110">EXAMPLES</span></span>

### <span data-ttu-id="dfbd5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dfbd5-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="dfbd5-112">Törölje a "mycertificate" kifejezést egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="dfbd5-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="dfbd5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfbd5-113">PARAMETERS</span></span>

### <span data-ttu-id="dfbd5-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="dfbd5-114">-CertificateName</span></span>
<span data-ttu-id="dfbd5-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="dfbd5-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="dfbd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbd5-116">-DefaultProfile</span></span>
<span data-ttu-id="dfbd5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfbd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfbd5-118">-ETAG</span><span class="sxs-lookup"><span data-stu-id="dfbd5-118">-Etag</span></span>
<span data-ttu-id="dfbd5-119">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="dfbd5-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="dfbd5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfbd5-120">-InputObject</span></span>
<span data-ttu-id="dfbd5-121">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="dfbd5-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="dfbd5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfbd5-122">-Name</span></span>
<span data-ttu-id="dfbd5-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="dfbd5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dfbd5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfbd5-124">-PassThru</span></span>
<span data-ttu-id="dfbd5-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dfbd5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dfbd5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbd5-126">-ResourceGroupName</span></span>
<span data-ttu-id="dfbd5-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dfbd5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dfbd5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfbd5-128">-ResourceId</span></span>
<span data-ttu-id="dfbd5-129">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="dfbd5-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="dfbd5-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfbd5-130">-Confirm</span></span>
<span data-ttu-id="dfbd5-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfbd5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbd5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbd5-132">-WhatIf</span></span>
<span data-ttu-id="dfbd5-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dfbd5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfbd5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfbd5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbd5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbd5-135">CommonParameters</span></span>
<span data-ttu-id="dfbd5-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfbd5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbd5-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbd5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbd5-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfbd5-138">INPUTS</span></span>

### <span data-ttu-id="dfbd5-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="dfbd5-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="dfbd5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dfbd5-140">System.String</span></span>

## <span data-ttu-id="dfbd5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfbd5-141">OUTPUTS</span></span>

### <span data-ttu-id="dfbd5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfbd5-142">System.Boolean</span></span>

## <span data-ttu-id="dfbd5-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfbd5-143">NOTES</span></span>

## <span data-ttu-id="dfbd5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfbd5-144">RELATED LINKS</span></span>
