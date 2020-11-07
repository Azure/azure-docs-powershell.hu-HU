---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670913"
---
# <span data-ttu-id="07a35-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="07a35-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="07a35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07a35-102">SYNOPSIS</span></span>
<span data-ttu-id="07a35-103">Azure IoT hub-eszköz kiépítési szolgáltatási tanúsítványának törlése</span><span class="sxs-lookup"><span data-stu-id="07a35-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="07a35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07a35-104">SYNTAX</span></span>

### <span data-ttu-id="07a35-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07a35-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a35-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="07a35-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a35-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="07a35-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a35-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="07a35-108">DESCRIPTION</span></span>
<span data-ttu-id="07a35-109">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="07a35-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="07a35-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07a35-110">EXAMPLES</span></span>

### <span data-ttu-id="07a35-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07a35-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="07a35-112">Törölje a "mycertificate" kifejezést egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="07a35-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="07a35-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07a35-113">PARAMETERS</span></span>

### <span data-ttu-id="07a35-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="07a35-114">-CertificateName</span></span>
<span data-ttu-id="07a35-115">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="07a35-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="07a35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a35-116">-DefaultProfile</span></span>
<span data-ttu-id="07a35-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07a35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a35-118">-ETAG</span><span class="sxs-lookup"><span data-stu-id="07a35-118">-Etag</span></span>
<span data-ttu-id="07a35-119">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="07a35-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="07a35-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07a35-120">-InputObject</span></span>
<span data-ttu-id="07a35-121">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="07a35-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="07a35-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07a35-122">-Name</span></span>
<span data-ttu-id="07a35-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="07a35-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="07a35-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07a35-124">-PassThru</span></span>
<span data-ttu-id="07a35-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="07a35-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="07a35-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a35-126">-ResourceGroupName</span></span>
<span data-ttu-id="07a35-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="07a35-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="07a35-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a35-128">-ResourceId</span></span>
<span data-ttu-id="07a35-129">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="07a35-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="07a35-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07a35-130">-Confirm</span></span>
<span data-ttu-id="07a35-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07a35-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a35-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a35-132">-WhatIf</span></span>
<span data-ttu-id="07a35-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07a35-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a35-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07a35-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a35-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a35-135">CommonParameters</span></span>
<span data-ttu-id="07a35-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07a35-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a35-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a35-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a35-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a35-138">INPUTS</span></span>

### <span data-ttu-id="07a35-139">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="07a35-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="07a35-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07a35-140">System.String</span></span>

## <span data-ttu-id="07a35-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a35-141">OUTPUTS</span></span>

### <span data-ttu-id="07a35-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07a35-142">System.Boolean</span></span>

## <span data-ttu-id="07a35-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07a35-143">NOTES</span></span>

## <span data-ttu-id="07a35-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07a35-144">RELATED LINKS</span></span>
