---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 098689074debe4b9cf5be4d682023186b123d504
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680371"
---
# <span data-ttu-id="7bdf2-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="7bdf2-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="7bdf2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdf2-103">Azure IoT hub-eszköz kiépítési szolgáltatási tanúsítványának létrehozása/frissítése</span><span class="sxs-lookup"><span data-stu-id="7bdf2-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bdf2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bdf2-104">SYNTAX</span></span>

### <span data-ttu-id="7bdf2-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7bdf2-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bdf2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7bdf2-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bdf2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7bdf2-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bdf2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bdf2-108">DESCRIPTION</span></span>
<span data-ttu-id="7bdf2-109">Új tanúsítvány feltöltése vagy a meglévő tanúsítvány cseréje ugyanazzal a névvel.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="7bdf2-110">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="7bdf2-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="7bdf2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7bdf2-111">EXAMPLES</span></span>

### <span data-ttu-id="7bdf2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7bdf2-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="7bdf2-113">Töltse fel a HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány CER-fájlját egy Azure IoT hub-eszköz kiépítési szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7bdf2-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="7bdf2-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

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

<span data-ttu-id="7bdf2-115">Egy új CER-fájl feltöltésével frissíti a HITELESÍTÉSSZOLGÁLTATÓI tanúsítványt egy IoT-hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="7bdf2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bdf2-116">PARAMETERS</span></span>

### <span data-ttu-id="7bdf2-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7bdf2-117">-CertificateName</span></span>
<span data-ttu-id="7bdf2-118">A IOT-eszköz kiépítési szolgáltatási tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="7bdf2-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="7bdf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdf2-119">-DefaultProfile</span></span>
<span data-ttu-id="7bdf2-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bdf2-121">-ETAG</span><span class="sxs-lookup"><span data-stu-id="7bdf2-121">-Etag</span></span>
<span data-ttu-id="7bdf2-122">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="7bdf2-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="7bdf2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bdf2-123">-InputObject</span></span>
<span data-ttu-id="7bdf2-124">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="7bdf2-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="7bdf2-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7bdf2-125">-Name</span></span>
<span data-ttu-id="7bdf2-126">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="7bdf2-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7bdf2-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="7bdf2-127">-Path</span></span>
<span data-ttu-id="7bdf2-128">a X509. cer fájl vagy a. PEM fájl elérési útjának a 64-alapú megjelenítése</span><span class="sxs-lookup"><span data-stu-id="7bdf2-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="7bdf2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bdf2-129">-ResourceGroupName</span></span>
<span data-ttu-id="7bdf2-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7bdf2-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7bdf2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bdf2-131">-ResourceId</span></span>
<span data-ttu-id="7bdf2-132">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7bdf2-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="7bdf2-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7bdf2-133">-Confirm</span></span>
<span data-ttu-id="7bdf2-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bdf2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bdf2-135">-WhatIf</span></span>
<span data-ttu-id="7bdf2-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bdf2-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bdf2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bdf2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdf2-138">CommonParameters</span></span>
<span data-ttu-id="7bdf2-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bdf2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdf2-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bdf2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdf2-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bdf2-141">INPUTS</span></span>

### <span data-ttu-id="7bdf2-142">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7bdf2-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="7bdf2-143">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7bdf2-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7bdf2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7bdf2-144">System.String</span></span>

## <span data-ttu-id="7bdf2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bdf2-145">OUTPUTS</span></span>

### <span data-ttu-id="7bdf2-146">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7bdf2-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="7bdf2-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bdf2-147">NOTES</span></span>

## <span data-ttu-id="7bdf2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bdf2-148">RELATED LINKS</span></span>
