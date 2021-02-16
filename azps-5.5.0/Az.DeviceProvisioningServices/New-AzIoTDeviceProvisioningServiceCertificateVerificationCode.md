---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147987"
---
# <span data-ttu-id="dfebf-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="dfebf-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="dfebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfebf-102">SYNOPSIS</span></span>
<span data-ttu-id="dfebf-103">Ellenőrzőkódot generál egy Azure IoT Hub eszköz kiépítési szolgáltatás tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="dfebf-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="dfebf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dfebf-104">SYNTAX</span></span>

### <span data-ttu-id="dfebf-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dfebf-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfebf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dfebf-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfebf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dfebf-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfebf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dfebf-108">DESCRIPTION</span></span>
<span data-ttu-id="dfebf-109">Ezt az ellenőrző kódot egy tanúsítvány igazolásának befejezéséhez használjuk.</span><span class="sxs-lookup"><span data-stu-id="dfebf-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="dfebf-110">Ezt az ellenőrző kódot használhatja a főtanúsítványok titkos kulcsával aláírt új tanúsítvány CN-kódjaként.</span><span class="sxs-lookup"><span data-stu-id="dfebf-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="dfebf-111">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates lásd: .</span><span class="sxs-lookup"><span data-stu-id="dfebf-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="dfebf-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dfebf-112">EXAMPLES</span></span>

### <span data-ttu-id="dfebf-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="dfebf-113">Example 1</span></span>
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

<span data-ttu-id="dfebf-114">Ellenőrző kód létrehozása a "mycertificate" számára.</span><span class="sxs-lookup"><span data-stu-id="dfebf-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="dfebf-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="dfebf-115">Example 2</span></span>
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

<span data-ttu-id="dfebf-116">Ellenőrző kód létrehozása a "mycertificate" folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="dfebf-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="dfebf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfebf-117">PARAMETERS</span></span>

### <span data-ttu-id="dfebf-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="dfebf-118">-CertificateName</span></span>
<span data-ttu-id="dfebf-119">Az Iot-eszköz kiépítési szolgáltatás tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="dfebf-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="dfebf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfebf-120">-DefaultProfile</span></span>
<span data-ttu-id="dfebf-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfebf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfebf-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="dfebf-122">-Etag</span></span>
<span data-ttu-id="dfebf-123">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="dfebf-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="dfebf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfebf-124">-InputObject</span></span>
<span data-ttu-id="dfebf-125">IoT-eszköz kiépítési szolgáltatás tanúsítványobjektuma</span><span class="sxs-lookup"><span data-stu-id="dfebf-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="dfebf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="dfebf-126">-Name</span></span>
<span data-ttu-id="dfebf-127">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="dfebf-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dfebf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfebf-128">-ResourceGroupName</span></span>
<span data-ttu-id="dfebf-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dfebf-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dfebf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfebf-130">-ResourceId</span></span>
<span data-ttu-id="dfebf-131">IoT-eszköz kiépítési szolgáltatás tanúsítványának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="dfebf-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="dfebf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfebf-132">-Confirm</span></span>
<span data-ttu-id="dfebf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dfebf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfebf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfebf-134">-WhatIf</span></span>
<span data-ttu-id="dfebf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dfebf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfebf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfebf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfebf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfebf-137">CommonParameters</span></span>
<span data-ttu-id="dfebf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfebf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfebf-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfebf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfebf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfebf-140">INPUTS</span></span>

### <span data-ttu-id="dfebf-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="dfebf-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="dfebf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dfebf-142">System.String</span></span>

## <span data-ttu-id="dfebf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfebf-143">OUTPUTS</span></span>

### <span data-ttu-id="dfebf-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="dfebf-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="dfebf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dfebf-145">NOTES</span></span>

## <span data-ttu-id="dfebf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfebf-146">RELATED LINKS</span></span>
