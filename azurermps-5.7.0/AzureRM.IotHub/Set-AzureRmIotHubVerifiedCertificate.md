---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: a241905b204de1bd7d0d372cdcafc6e321b8c98d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504551"
---
# <span data-ttu-id="d9a16-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="d9a16-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="d9a16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9a16-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a16-103">Ellenőrzi az Azure IoT hub tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="d9a16-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9a16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9a16-104">SYNTAX</span></span>

### <span data-ttu-id="d9a16-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9a16-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9a16-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9a16-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a16-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9a16-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a16-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9a16-108">DESCRIPTION</span></span>
<span data-ttu-id="d9a16-109">Igazolja a tanúsítványt, ha olyan ellenőrző tanúsítványt tölt fel, amely tartalmazza a AzureRmIotHubCertificateVerificationCode parancsmaggal kapott ellenőrző kódot.</span><span class="sxs-lookup"><span data-stu-id="d9a16-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="d9a16-110">Ez az utolsó lépés a birtoklási folyamat igazolásakor.</span><span class="sxs-lookup"><span data-stu-id="d9a16-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="d9a16-111">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="d9a16-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="d9a16-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d9a16-112">EXAMPLES</span></span>

### <span data-ttu-id="d9a16-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d9a16-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="d9a16-114">Ellenőrzi a MyCertificate titkos kulcs tulajdonjogát.</span><span class="sxs-lookup"><span data-stu-id="d9a16-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="d9a16-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9a16-115">PARAMETERS</span></span>

### <span data-ttu-id="d9a16-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d9a16-116">-CertificateName</span></span>
<span data-ttu-id="d9a16-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="d9a16-117">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a16-118">-DefaultProfile</span></span>
<span data-ttu-id="d9a16-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9a16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-120">-ETAG</span><span class="sxs-lookup"><span data-stu-id="d9a16-120">-Etag</span></span>
<span data-ttu-id="d9a16-121">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="d9a16-121">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a16-122">-InputObject</span></span>
<span data-ttu-id="d9a16-123">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="d9a16-123">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9a16-124">-Name</span></span>
<span data-ttu-id="d9a16-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="d9a16-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d9a16-126">-Path</span></span>
<span data-ttu-id="d9a16-127">a X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="d9a16-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a16-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9a16-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d9a16-129">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9a16-130">-ResourceId</span></span>
<span data-ttu-id="d9a16-131">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="d9a16-131">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9a16-132">-Confirm</span></span>
<span data-ttu-id="d9a16-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9a16-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a16-134">-WhatIf</span></span>
<span data-ttu-id="d9a16-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9a16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a16-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9a16-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a16-137">CommonParameters</span></span>
<span data-ttu-id="d9a16-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9a16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a16-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a16-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a16-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9a16-140">INPUTS</span></span>

### <span data-ttu-id="d9a16-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d9a16-141">System.String</span></span>

## <span data-ttu-id="d9a16-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9a16-142">OUTPUTS</span></span>

### <span data-ttu-id="d9a16-143">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="d9a16-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="d9a16-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9a16-144">NOTES</span></span>

## <span data-ttu-id="d9a16-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9a16-145">RELATED LINKS</span></span>

