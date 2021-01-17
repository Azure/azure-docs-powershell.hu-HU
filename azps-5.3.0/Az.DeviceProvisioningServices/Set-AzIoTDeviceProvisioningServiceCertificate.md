---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467786"
---
# <span data-ttu-id="74f9f-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="74f9f-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="74f9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="74f9f-103">Ellenőrizze az Azure IoT Hub eszköz-kiépítési szolgáltatás tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="74f9f-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="74f9f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74f9f-104">SYNTAX</span></span>

### <span data-ttu-id="74f9f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74f9f-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f9f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74f9f-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f9f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="74f9f-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f9f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74f9f-108">DESCRIPTION</span></span>
<span data-ttu-id="74f9f-109">A tanúsítvány ellenőrzéséhez töltsön fel egy ellenőrző tanúsítványt, amely tartalmazza a generált ellenőrző kód hívása során kapott ellenőrző kódot.</span><span class="sxs-lookup"><span data-stu-id="74f9f-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="74f9f-110">Ez az eljárás igazolásának utolsó lépése.</span><span class="sxs-lookup"><span data-stu-id="74f9f-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="74f9f-111">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát lásd: https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="74f9f-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="74f9f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74f9f-112">EXAMPLES</span></span>

### <span data-ttu-id="74f9f-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="74f9f-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="74f9f-114">Ellenőrizze a "mycertificate" privát kulcs tulajdonjogát.</span><span class="sxs-lookup"><span data-stu-id="74f9f-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="74f9f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="74f9f-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="74f9f-116">A mycertificate privát kulcs tulajdonjogának igazolása folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="74f9f-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="74f9f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f9f-117">PARAMETERS</span></span>

### <span data-ttu-id="74f9f-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="74f9f-118">-CertificateName</span></span>
<span data-ttu-id="74f9f-119">Az Iot-eszköz kiépítési szolgáltatás tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="74f9f-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="74f9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f9f-120">-DefaultProfile</span></span>
<span data-ttu-id="74f9f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74f9f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f9f-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="74f9f-122">-Etag</span></span>
<span data-ttu-id="74f9f-123">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="74f9f-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="74f9f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74f9f-124">-InputObject</span></span>
<span data-ttu-id="74f9f-125">IoT-eszköz kiépítési szolgáltatás tanúsítványobjektuma</span><span class="sxs-lookup"><span data-stu-id="74f9f-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="74f9f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="74f9f-126">-Name</span></span>
<span data-ttu-id="74f9f-127">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="74f9f-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="74f9f-128">-Path</span><span class="sxs-lookup"><span data-stu-id="74f9f-128">-Path</span></span>
<span data-ttu-id="74f9f-129">Base-64 representation of X509 certificate .cer file or .pem file path</span><span class="sxs-lookup"><span data-stu-id="74f9f-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="74f9f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f9f-130">-ResourceGroupName</span></span>
<span data-ttu-id="74f9f-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="74f9f-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="74f9f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74f9f-132">-ResourceId</span></span>
<span data-ttu-id="74f9f-133">IoT-eszköz kiépítési szolgáltatás tanúsítványának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="74f9f-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="74f9f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74f9f-134">-Confirm</span></span>
<span data-ttu-id="74f9f-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74f9f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f9f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f9f-136">-WhatIf</span></span>
<span data-ttu-id="74f9f-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74f9f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f9f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74f9f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f9f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f9f-139">CommonParameters</span></span>
<span data-ttu-id="74f9f-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f9f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f9f-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f9f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f9f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74f9f-142">INPUTS</span></span>

### <span data-ttu-id="74f9f-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="74f9f-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="74f9f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="74f9f-144">System.String</span></span>

## <span data-ttu-id="74f9f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74f9f-145">OUTPUTS</span></span>

### <span data-ttu-id="74f9f-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="74f9f-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="74f9f-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74f9f-147">NOTES</span></span>

## <span data-ttu-id="74f9f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74f9f-148">RELATED LINKS</span></span>
