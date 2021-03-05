---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 999fa5d697feb8eab6edb83816763ed6cf49523c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004166"
---
# <span data-ttu-id="5a371-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="5a371-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="5a371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a371-102">SYNOPSIS</span></span>
<span data-ttu-id="5a371-103">Ellenőrzőkódot generál egy Azure IoT Hub eszköz kiépítési szolgáltatás tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="5a371-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="5a371-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a371-104">SYNTAX</span></span>

### <span data-ttu-id="5a371-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a371-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a371-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a371-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a371-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5a371-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a371-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a371-108">DESCRIPTION</span></span>
<span data-ttu-id="5a371-109">Ezt az ellenőrző kódot egy tanúsítvány igazolásának befejezéséhez használjuk.</span><span class="sxs-lookup"><span data-stu-id="5a371-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="5a371-110">Ezt az ellenőrző kódot használhatja a főtanúsítványok titkos kulcsával aláírt új tanúsítvány CN-kódjaként.</span><span class="sxs-lookup"><span data-stu-id="5a371-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="5a371-111">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates lásd: .</span><span class="sxs-lookup"><span data-stu-id="5a371-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="5a371-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a371-112">EXAMPLES</span></span>

### <span data-ttu-id="5a371-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="5a371-113">Example 1</span></span>
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

<span data-ttu-id="5a371-114">Ellenőrző kód létrehozása a "mycertificate" számára.</span><span class="sxs-lookup"><span data-stu-id="5a371-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="5a371-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="5a371-115">Example 2</span></span>
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

<span data-ttu-id="5a371-116">Ellenőrző kód létrehozása a "mycertificate" folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="5a371-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="5a371-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a371-117">PARAMETERS</span></span>

### <span data-ttu-id="5a371-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5a371-118">-CertificateName</span></span>
<span data-ttu-id="5a371-119">Az Iot-eszköz kiépítési szolgáltatás tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="5a371-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="5a371-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a371-120">-DefaultProfile</span></span>
<span data-ttu-id="5a371-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a371-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a371-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="5a371-122">-Etag</span></span>
<span data-ttu-id="5a371-123">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="5a371-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="5a371-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a371-124">-InputObject</span></span>
<span data-ttu-id="5a371-125">IoT-eszköz kiépítési szolgáltatás tanúsítványobjektuma</span><span class="sxs-lookup"><span data-stu-id="5a371-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="5a371-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5a371-126">-Name</span></span>
<span data-ttu-id="5a371-127">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="5a371-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5a371-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a371-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a371-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5a371-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5a371-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a371-130">-ResourceId</span></span>
<span data-ttu-id="5a371-131">IoT-eszköz kiépítési szolgáltatás tanúsítványának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5a371-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="5a371-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a371-132">-Confirm</span></span>
<span data-ttu-id="5a371-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a371-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a371-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a371-134">-WhatIf</span></span>
<span data-ttu-id="5a371-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a371-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a371-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a371-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a371-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a371-137">CommonParameters</span></span>
<span data-ttu-id="5a371-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a371-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a371-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a371-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a371-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a371-140">INPUTS</span></span>

### <span data-ttu-id="5a371-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="5a371-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="5a371-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5a371-142">System.String</span></span>

## <span data-ttu-id="5a371-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a371-143">OUTPUTS</span></span>

### <span data-ttu-id="5a371-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="5a371-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="5a371-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a371-145">NOTES</span></span>

## <span data-ttu-id="5a371-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a371-146">RELATED LINKS</span></span>
