---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480168"
---
# <span data-ttu-id="72cbc-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="72cbc-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="72cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="72cbc-103">Ellenőrzőkódot hoz létre egy Azure IoT-központbeli tanúsítványhoz.</span><span class="sxs-lookup"><span data-stu-id="72cbc-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="72cbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72cbc-104">SYNTAX</span></span>

### <span data-ttu-id="72cbc-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72cbc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72cbc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72cbc-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72cbc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72cbc-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72cbc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="72cbc-109">Ezt az ellenőrző kódot egy tanúsítvány igazolásának befejezéséhez használjuk.</span><span class="sxs-lookup"><span data-stu-id="72cbc-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="72cbc-110">Ezt az ellenőrző kódot használhatja a főtanúsítványok titkos kulcsával aláírt új tanúsítvány CN-kódjaként.</span><span class="sxs-lookup"><span data-stu-id="72cbc-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="72cbc-111">Az Azure IoT-központban található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát az https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="72cbc-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="72cbc-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72cbc-112">EXAMPLES</span></span>

### <span data-ttu-id="72cbc-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="72cbc-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="72cbc-114">Ellenőrzőkódot hoz létre a MyCertificate számára</span><span class="sxs-lookup"><span data-stu-id="72cbc-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="72cbc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72cbc-115">PARAMETERS</span></span>

### <span data-ttu-id="72cbc-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="72cbc-116">-CertificateName</span></span>
<span data-ttu-id="72cbc-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="72cbc-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="72cbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cbc-118">-DefaultProfile</span></span>
<span data-ttu-id="72cbc-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72cbc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72cbc-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="72cbc-120">-Etag</span></span>
<span data-ttu-id="72cbc-121">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="72cbc-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="72cbc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72cbc-122">-InputObject</span></span>
<span data-ttu-id="72cbc-123">Tanúsítványobjektum</span><span class="sxs-lookup"><span data-stu-id="72cbc-123">Certificate Object</span></span>

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

### <span data-ttu-id="72cbc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="72cbc-124">-Name</span></span>
<span data-ttu-id="72cbc-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="72cbc-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="72cbc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72cbc-126">-ResourceGroupName</span></span>
<span data-ttu-id="72cbc-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="72cbc-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="72cbc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72cbc-128">-ResourceId</span></span>
<span data-ttu-id="72cbc-129">Tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="72cbc-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="72cbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cbc-130">CommonParameters</span></span>
<span data-ttu-id="72cbc-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cbc-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cbc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cbc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72cbc-133">INPUTS</span></span>

### <span data-ttu-id="72cbc-134">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="72cbc-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="72cbc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="72cbc-135">System.String</span></span>

## <span data-ttu-id="72cbc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72cbc-136">OUTPUTS</span></span>

### <span data-ttu-id="72cbc-137">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="72cbc-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="72cbc-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72cbc-138">NOTES</span></span>

## <span data-ttu-id="72cbc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72cbc-139">RELATED LINKS</span></span>
