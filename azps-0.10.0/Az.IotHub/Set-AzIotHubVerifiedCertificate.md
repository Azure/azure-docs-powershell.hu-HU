---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 17149af8eb279f95631aafc50d3c0b21857fec98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843925"
---
# <span data-ttu-id="91131-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="91131-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="91131-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91131-102">SYNOPSIS</span></span>
<span data-ttu-id="91131-103">Ellenőrzi az Azure IoT hub tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="91131-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="91131-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91131-104">SYNTAX</span></span>

### <span data-ttu-id="91131-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91131-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91131-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91131-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91131-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91131-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91131-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91131-108">DESCRIPTION</span></span>
<span data-ttu-id="91131-109">Igazolja a tanúsítványt, ha olyan ellenőrző tanúsítványt tölt fel, amely tartalmazza a AzIotHubCertificateVerificationCode parancsmaggal kapott ellenőrző kódot.</span><span class="sxs-lookup"><span data-stu-id="91131-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="91131-110">Ez az utolsó lépés a birtoklási folyamat igazolásakor.</span><span class="sxs-lookup"><span data-stu-id="91131-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="91131-111">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="91131-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="91131-112">Példák</span><span class="sxs-lookup"><span data-stu-id="91131-112">EXAMPLES</span></span>

### <span data-ttu-id="91131-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91131-113">Example 1</span></span>
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

<span data-ttu-id="91131-114">Ellenőrzi a MyCertificate titkos kulcs tulajdonjogát.</span><span class="sxs-lookup"><span data-stu-id="91131-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="91131-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91131-115">PARAMETERS</span></span>

### <span data-ttu-id="91131-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="91131-116">-CertificateName</span></span>
<span data-ttu-id="91131-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="91131-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="91131-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91131-118">-DefaultProfile</span></span>
<span data-ttu-id="91131-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91131-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91131-120">-ETAG</span><span class="sxs-lookup"><span data-stu-id="91131-120">-Etag</span></span>
<span data-ttu-id="91131-121">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="91131-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="91131-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91131-122">-InputObject</span></span>
<span data-ttu-id="91131-123">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="91131-123">Certificate Object</span></span>

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

### <span data-ttu-id="91131-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91131-124">-Name</span></span>
<span data-ttu-id="91131-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="91131-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="91131-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="91131-126">-Path</span></span>
<span data-ttu-id="91131-127">a X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="91131-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="91131-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91131-128">-ResourceGroupName</span></span>
<span data-ttu-id="91131-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="91131-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91131-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91131-130">-ResourceId</span></span>
<span data-ttu-id="91131-131">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="91131-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="91131-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91131-132">-Confirm</span></span>
<span data-ttu-id="91131-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91131-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91131-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91131-134">-WhatIf</span></span>
<span data-ttu-id="91131-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91131-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91131-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91131-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91131-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91131-137">CommonParameters</span></span>
<span data-ttu-id="91131-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91131-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91131-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91131-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91131-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91131-140">INPUTS</span></span>

### <span data-ttu-id="91131-141">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="91131-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="91131-142">System. String</span><span class="sxs-lookup"><span data-stu-id="91131-142">System.String</span></span>

## <span data-ttu-id="91131-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91131-143">OUTPUTS</span></span>

### <span data-ttu-id="91131-144">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="91131-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="91131-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91131-145">NOTES</span></span>

## <span data-ttu-id="91131-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91131-146">RELATED LINKS</span></span>
