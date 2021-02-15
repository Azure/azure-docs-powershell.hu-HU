---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152843"
---
# <span data-ttu-id="c4ab2-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="c4ab2-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="c4ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ab2-103">Azure IoT-központbeli tanúsítványt ellenőriz.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="c4ab2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4ab2-104">SYNTAX</span></span>

### <span data-ttu-id="c4ab2-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4ab2-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4ab2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4ab2-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ab2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c4ab2-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4ab2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4ab2-108">DESCRIPTION</span></span>
<span data-ttu-id="c4ab2-109">Tanúsítványt ellenőriz a Get-AzIotHubCertificateVerificationCode parancsmag által kapott ellenőrzőkódot tartalmazó ellenőrző tanúsítvány feltöltésével.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="c4ab2-110">Ez az eljárás igazolásának utolsó lépése.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="c4ab2-111">Az Azure IoT-központban található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát az https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c4ab2-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c4ab2-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4ab2-112">EXAMPLES</span></span>

### <span data-ttu-id="c4ab2-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4ab2-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="c4ab2-114">Ellenőrzi a MyCertificate privát kulcs tulajdonjogát.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="c4ab2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4ab2-115">PARAMETERS</span></span>

### <span data-ttu-id="c4ab2-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c4ab2-116">-CertificateName</span></span>
<span data-ttu-id="c4ab2-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="c4ab2-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c4ab2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ab2-118">-DefaultProfile</span></span>
<span data-ttu-id="c4ab2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4ab2-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="c4ab2-120">-Etag</span></span>
<span data-ttu-id="c4ab2-121">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="c4ab2-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c4ab2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4ab2-122">-InputObject</span></span>
<span data-ttu-id="c4ab2-123">Tanúsítványobjektum</span><span class="sxs-lookup"><span data-stu-id="c4ab2-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ab2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ab2-124">-Name</span></span>
<span data-ttu-id="c4ab2-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="c4ab2-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ab2-126">-Path</span><span class="sxs-lookup"><span data-stu-id="c4ab2-126">-Path</span></span>
<span data-ttu-id="c4ab2-127">base-64 representation of X509 certificate .cer file or .pem file path.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="c4ab2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ab2-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4ab2-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c4ab2-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ab2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ab2-130">-ResourceId</span></span>
<span data-ttu-id="c4ab2-131">Tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c4ab2-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="c4ab2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4ab2-132">-Confirm</span></span>
<span data-ttu-id="c4ab2-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ab2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ab2-134">-WhatIf</span></span>
<span data-ttu-id="c4ab2-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ab2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ab2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ab2-137">CommonParameters</span></span>
<span data-ttu-id="c4ab2-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ab2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ab2-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ab2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ab2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4ab2-140">INPUTS</span></span>

### <span data-ttu-id="c4ab2-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="c4ab2-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="c4ab2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c4ab2-142">System.String</span></span>

## <span data-ttu-id="c4ab2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ab2-143">OUTPUTS</span></span>

### <span data-ttu-id="c4ab2-144">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="c4ab2-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="c4ab2-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4ab2-145">NOTES</span></span>

## <span data-ttu-id="c4ab2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4ab2-146">RELATED LINKS</span></span>
