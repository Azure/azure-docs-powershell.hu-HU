---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 59445c2e162a7cbfce5cff26bac91d133c8928a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493694"
---
# <span data-ttu-id="7b0e3-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="7b0e3-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="7b0e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0e3-103">Hitelesítő kód létrehozása az Azure IoT hub-eszközök kiépítési szolgáltatási tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b0e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b0e3-104">SYNTAX</span></span>

### <span data-ttu-id="7b0e3-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b0e3-105">ResourceSet (Default)</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String>
 [-Name] <String> [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b0e3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7b0e3-106">InputObjectSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b0e3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7b0e3-107">ResourceIdSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b0e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b0e3-108">DESCRIPTION</span></span>
<span data-ttu-id="7b0e3-109">Ez az ellenőrző kód a tanúsítványok birtoklási lépésének igazolását fejezi ki.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="7b0e3-110">Ezt az ellenőrző kódot használja egy új, a főtanúsítványokat tartalmazó titkos kulccsal aláírt tanúsítvány CN-ként.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="7b0e3-111">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="7b0e3-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="7b0e3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7b0e3-112">EXAMPLES</span></span>

### <span data-ttu-id="7b0e3-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b0e3-113">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="7b0e3-114">Hitelesítő kód létrehozása a "mycertificate" kifejezéshez.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="7b0e3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="7b0e3-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzureRmIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="7b0e3-116">Hitelesítő kód létrehozása a "mycertificate"-hoz csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="7b0e3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b0e3-117">PARAMETERS</span></span>

### <span data-ttu-id="7b0e3-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7b0e3-118">-CertificateName</span></span>
<span data-ttu-id="7b0e3-119">A IOT-eszköz kiépítési szolgáltatási tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="7b0e3-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="7b0e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0e3-120">-DefaultProfile</span></span>
<span data-ttu-id="7b0e3-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b0e3-122">-ETAG</span><span class="sxs-lookup"><span data-stu-id="7b0e3-122">-Etag</span></span>
<span data-ttu-id="7b0e3-123">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="7b0e3-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="7b0e3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b0e3-124">-InputObject</span></span>
<span data-ttu-id="7b0e3-125">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="7b0e3-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="7b0e3-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b0e3-126">-Name</span></span>
<span data-ttu-id="7b0e3-127">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="7b0e3-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7b0e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="7b0e3-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7b0e3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7b0e3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0e3-130">-ResourceId</span></span>
<span data-ttu-id="7b0e3-131">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7b0e3-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="7b0e3-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b0e3-132">-Confirm</span></span>
<span data-ttu-id="7b0e3-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b0e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b0e3-134">-WhatIf</span></span>
<span data-ttu-id="7b0e3-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b0e3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b0e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0e3-137">CommonParameters</span></span>
<span data-ttu-id="7b0e3-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b0e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0e3-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0e3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0e3-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b0e3-140">INPUTS</span></span>

### <span data-ttu-id="7b0e3-141">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7b0e3-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="7b0e3-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b0e3-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7b0e3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7b0e3-143">System.String</span></span>

## <span data-ttu-id="7b0e3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b0e3-144">OUTPUTS</span></span>

### <span data-ttu-id="7b0e3-145">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="7b0e3-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="7b0e3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b0e3-146">NOTES</span></span>

## <span data-ttu-id="7b0e3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b0e3-147">RELATED LINKS</span></span>
