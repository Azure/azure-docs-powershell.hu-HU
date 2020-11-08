---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184549"
---
# <span data-ttu-id="e2ecd-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="e2ecd-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="e2ecd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ecd-103">Hitelesítő kód létrehozása az Azure IoT hub-eszközök kiépítési szolgáltatási tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="e2ecd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2ecd-104">SYNTAX</span></span>

### <span data-ttu-id="e2ecd-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2ecd-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2ecd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2ecd-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2ecd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e2ecd-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ecd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2ecd-108">DESCRIPTION</span></span>
<span data-ttu-id="e2ecd-109">Ez az ellenőrző kód a tanúsítványok birtoklási lépésének igazolását fejezi ki.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="e2ecd-110">Ezt az ellenőrző kódot használja egy új, a főtanúsítványokat tartalmazó titkos kulccsal aláírt tanúsítvány CN-ként.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="e2ecd-111">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="e2ecd-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="e2ecd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e2ecd-112">EXAMPLES</span></span>

### <span data-ttu-id="e2ecd-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2ecd-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="e2ecd-114">Hitelesítő kód létrehozása a "mycertificate" kifejezéshez.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="e2ecd-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="e2ecd-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

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

<span data-ttu-id="e2ecd-116">Hitelesítő kód létrehozása a "mycertificate"-hoz csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="e2ecd-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2ecd-117">PARAMETERS</span></span>

### <span data-ttu-id="e2ecd-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e2ecd-118">-CertificateName</span></span>
<span data-ttu-id="e2ecd-119">A IOT-eszköz kiépítési szolgáltatási tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="e2ecd-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="e2ecd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ecd-120">-DefaultProfile</span></span>
<span data-ttu-id="e2ecd-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ecd-122">-ETAG</span><span class="sxs-lookup"><span data-stu-id="e2ecd-122">-Etag</span></span>
<span data-ttu-id="e2ecd-123">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="e2ecd-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="e2ecd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ecd-124">-InputObject</span></span>
<span data-ttu-id="e2ecd-125">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="e2ecd-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="e2ecd-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2ecd-126">-Name</span></span>
<span data-ttu-id="e2ecd-127">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="e2ecd-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e2ecd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ecd-128">-ResourceGroupName</span></span>
<span data-ttu-id="e2ecd-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e2ecd-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e2ecd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2ecd-130">-ResourceId</span></span>
<span data-ttu-id="e2ecd-131">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e2ecd-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="e2ecd-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2ecd-132">-Confirm</span></span>
<span data-ttu-id="e2ecd-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ecd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ecd-134">-WhatIf</span></span>
<span data-ttu-id="e2ecd-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ecd-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ecd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ecd-137">CommonParameters</span></span>
<span data-ttu-id="e2ecd-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2ecd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ecd-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ecd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ecd-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2ecd-140">INPUTS</span></span>

### <span data-ttu-id="e2ecd-141">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="e2ecd-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="e2ecd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e2ecd-142">System.String</span></span>

## <span data-ttu-id="e2ecd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2ecd-143">OUTPUTS</span></span>

### <span data-ttu-id="e2ecd-144">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="e2ecd-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="e2ecd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2ecd-145">NOTES</span></span>

## <span data-ttu-id="e2ecd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2ecd-146">RELATED LINKS</span></span>
