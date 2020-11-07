---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 28c37988f25418e36b99b752a3be2e2ff923bbc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666598"
---
# <span data-ttu-id="092eb-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="092eb-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="092eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="092eb-102">SYNOPSIS</span></span>
<span data-ttu-id="092eb-103">Azure IoT hub-eszköz kiépítési szolgáltatási tanúsítványának létrehozása/frissítése</span><span class="sxs-lookup"><span data-stu-id="092eb-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="092eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="092eb-104">SYNTAX</span></span>

### <span data-ttu-id="092eb-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="092eb-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="092eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="092eb-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="092eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="092eb-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="092eb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="092eb-108">DESCRIPTION</span></span>
<span data-ttu-id="092eb-109">Új tanúsítvány feltöltése vagy a meglévő tanúsítvány cseréje ugyanazzal a névvel.</span><span class="sxs-lookup"><span data-stu-id="092eb-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="092eb-110">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="092eb-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="092eb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="092eb-111">EXAMPLES</span></span>

### <span data-ttu-id="092eb-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="092eb-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="092eb-113">Töltse fel a HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány CER-fájlját egy Azure IoT hub-eszköz kiépítési szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="092eb-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="092eb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="092eb-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="092eb-115">Egy új CER-fájl feltöltésével frissíti a HITELESÍTÉSSZOLGÁLTATÓI tanúsítványt egy IoT-hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="092eb-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="092eb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="092eb-116">PARAMETERS</span></span>

### <span data-ttu-id="092eb-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="092eb-117">-CertificateName</span></span>
<span data-ttu-id="092eb-118">A IOT-eszköz kiépítési szolgáltatási tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="092eb-118">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="092eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="092eb-119">-DefaultProfile</span></span>
<span data-ttu-id="092eb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="092eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="092eb-121">-ETAG</span><span class="sxs-lookup"><span data-stu-id="092eb-121">-Etag</span></span>
<span data-ttu-id="092eb-122">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="092eb-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="092eb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="092eb-123">-InputObject</span></span>
<span data-ttu-id="092eb-124">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="092eb-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="092eb-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="092eb-125">-Name</span></span>
<span data-ttu-id="092eb-126">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="092eb-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="092eb-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="092eb-127">-Path</span></span>
<span data-ttu-id="092eb-128">a X509. cer fájl vagy a. PEM fájl elérési útjának a 64-alapú megjelenítése</span><span class="sxs-lookup"><span data-stu-id="092eb-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="092eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="092eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="092eb-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="092eb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="092eb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="092eb-131">-ResourceId</span></span>
<span data-ttu-id="092eb-132">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="092eb-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="092eb-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="092eb-133">-Confirm</span></span>
<span data-ttu-id="092eb-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="092eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="092eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="092eb-135">-WhatIf</span></span>
<span data-ttu-id="092eb-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="092eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="092eb-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="092eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="092eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="092eb-138">CommonParameters</span></span>
<span data-ttu-id="092eb-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="092eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="092eb-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="092eb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="092eb-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="092eb-141">INPUTS</span></span>

### <span data-ttu-id="092eb-142">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="092eb-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="092eb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="092eb-143">System.String</span></span>

## <span data-ttu-id="092eb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="092eb-144">OUTPUTS</span></span>

### <span data-ttu-id="092eb-145">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="092eb-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="092eb-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="092eb-146">NOTES</span></span>

## <span data-ttu-id="092eb-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="092eb-147">RELATED LINKS</span></span>
