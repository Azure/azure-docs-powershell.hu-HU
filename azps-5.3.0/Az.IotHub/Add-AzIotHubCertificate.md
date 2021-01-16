---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480183"
---
# <span data-ttu-id="468ac-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="468ac-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="468ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="468ac-102">SYNOPSIS</span></span>
<span data-ttu-id="468ac-103">Azure IoT-központbeli tanúsítvány létrehozása/frissítése.</span><span class="sxs-lookup"><span data-stu-id="468ac-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="468ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="468ac-104">SYNTAX</span></span>

### <span data-ttu-id="468ac-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="468ac-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="468ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="468ac-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="468ac-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="468ac-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="468ac-108">DESCRIPTION</span></span>
<span data-ttu-id="468ac-109">Feltölt egy új tanúsítványt, vagy lecseréli a meglévő tanúsítványt ugyanazra a névre.</span><span class="sxs-lookup"><span data-stu-id="468ac-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="468ac-110">Az Azure IoT-központban található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát az https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="468ac-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="468ac-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="468ac-111">EXAMPLES</span></span>

### <span data-ttu-id="468ac-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="468ac-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="468ac-113">Hitelesítésszolgáltatói tanúsítvány CER-fájlját tölti fel egy IoT-központba.</span><span class="sxs-lookup"><span data-stu-id="468ac-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="468ac-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="468ac-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="468ac-115">Egy új CER-fájl feltöltésével frissíti a hitelesítésszolgáltatói tanúsítványt egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="468ac-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="468ac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="468ac-116">PARAMETERS</span></span>

### <span data-ttu-id="468ac-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="468ac-117">-CertificateName</span></span>
<span data-ttu-id="468ac-118">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="468ac-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="468ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468ac-119">-DefaultProfile</span></span>
<span data-ttu-id="468ac-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="468ac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="468ac-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="468ac-121">-Etag</span></span>
<span data-ttu-id="468ac-122">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="468ac-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="468ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="468ac-123">-InputObject</span></span>
<span data-ttu-id="468ac-124">Tanúsítványobjektum</span><span class="sxs-lookup"><span data-stu-id="468ac-124">Certificate Object</span></span>

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

### <span data-ttu-id="468ac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="468ac-125">-Name</span></span>
<span data-ttu-id="468ac-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="468ac-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="468ac-127">-Path</span><span class="sxs-lookup"><span data-stu-id="468ac-127">-Path</span></span>
<span data-ttu-id="468ac-128">base-64 representation of X509 certificate .cer file or .pem file path.</span><span class="sxs-lookup"><span data-stu-id="468ac-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="468ac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468ac-129">-ResourceGroupName</span></span>
<span data-ttu-id="468ac-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="468ac-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="468ac-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="468ac-131">-ResourceId</span></span>
<span data-ttu-id="468ac-132">Tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="468ac-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="468ac-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="468ac-133">-Confirm</span></span>
<span data-ttu-id="468ac-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="468ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="468ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="468ac-135">-WhatIf</span></span>
<span data-ttu-id="468ac-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="468ac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="468ac-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="468ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="468ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468ac-138">CommonParameters</span></span>
<span data-ttu-id="468ac-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468ac-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="468ac-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468ac-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="468ac-141">INPUTS</span></span>

### <span data-ttu-id="468ac-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="468ac-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="468ac-143">System.String</span><span class="sxs-lookup"><span data-stu-id="468ac-143">System.String</span></span>

## <span data-ttu-id="468ac-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="468ac-144">OUTPUTS</span></span>

### <span data-ttu-id="468ac-145">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="468ac-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="468ac-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="468ac-146">NOTES</span></span>

## <span data-ttu-id="468ac-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="468ac-147">RELATED LINKS</span></span>
