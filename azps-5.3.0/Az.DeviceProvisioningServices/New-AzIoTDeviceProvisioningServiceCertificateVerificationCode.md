---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467785"
---
# <span data-ttu-id="77eb3-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="77eb3-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="77eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="77eb3-103">Ellenőrzőkódot generál egy Azure IoT Hub eszköz kiépítési szolgáltatás tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="77eb3-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="77eb3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77eb3-104">SYNTAX</span></span>

### <span data-ttu-id="77eb3-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77eb3-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77eb3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77eb3-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77eb3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="77eb3-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77eb3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77eb3-108">DESCRIPTION</span></span>
<span data-ttu-id="77eb3-109">Ezt az ellenőrző kódot egy tanúsítvány igazolásának befejezéséhez használjuk.</span><span class="sxs-lookup"><span data-stu-id="77eb3-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="77eb3-110">Ezt az ellenőrző kódot használhatja a főtanúsítványok titkos kulcsával aláírt új tanúsítvány CN-kódjaként.</span><span class="sxs-lookup"><span data-stu-id="77eb3-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="77eb3-111">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates lásd: .</span><span class="sxs-lookup"><span data-stu-id="77eb3-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="77eb3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77eb3-112">EXAMPLES</span></span>

### <span data-ttu-id="77eb3-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="77eb3-113">Example 1</span></span>
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

<span data-ttu-id="77eb3-114">Ellenőrző kód létrehozása a "mycertificate" számára.</span><span class="sxs-lookup"><span data-stu-id="77eb3-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="77eb3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="77eb3-115">Example 2</span></span>
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

<span data-ttu-id="77eb3-116">Ellenőrző kód létrehozása a "mycertificate" folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="77eb3-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="77eb3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77eb3-117">PARAMETERS</span></span>

### <span data-ttu-id="77eb3-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="77eb3-118">-CertificateName</span></span>
<span data-ttu-id="77eb3-119">Az Iot-eszköz kiépítési szolgáltatás tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="77eb3-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="77eb3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77eb3-120">-DefaultProfile</span></span>
<span data-ttu-id="77eb3-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77eb3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77eb3-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="77eb3-122">-Etag</span></span>
<span data-ttu-id="77eb3-123">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="77eb3-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="77eb3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77eb3-124">-InputObject</span></span>
<span data-ttu-id="77eb3-125">IoT-eszköz kiépítési szolgáltatás tanúsítványobjektuma</span><span class="sxs-lookup"><span data-stu-id="77eb3-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="77eb3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="77eb3-126">-Name</span></span>
<span data-ttu-id="77eb3-127">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="77eb3-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="77eb3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77eb3-128">-ResourceGroupName</span></span>
<span data-ttu-id="77eb3-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="77eb3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="77eb3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77eb3-130">-ResourceId</span></span>
<span data-ttu-id="77eb3-131">IoT-eszköz kiépítési szolgáltatás tanúsítványának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="77eb3-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="77eb3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77eb3-132">-Confirm</span></span>
<span data-ttu-id="77eb3-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="77eb3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77eb3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77eb3-134">-WhatIf</span></span>
<span data-ttu-id="77eb3-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="77eb3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77eb3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77eb3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77eb3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77eb3-137">CommonParameters</span></span>
<span data-ttu-id="77eb3-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77eb3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77eb3-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77eb3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77eb3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77eb3-140">INPUTS</span></span>

### <span data-ttu-id="77eb3-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="77eb3-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="77eb3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="77eb3-142">System.String</span></span>

## <span data-ttu-id="77eb3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77eb3-143">OUTPUTS</span></span>

### <span data-ttu-id="77eb3-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="77eb3-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="77eb3-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77eb3-145">NOTES</span></span>

## <span data-ttu-id="77eb3-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77eb3-146">RELATED LINKS</span></span>
