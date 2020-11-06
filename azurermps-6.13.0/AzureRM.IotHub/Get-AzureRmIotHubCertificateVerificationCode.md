---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: a2c4c72f93597f3275e9edb1fecb6139eafbeb50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503668"
---
# <span data-ttu-id="94e60-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="94e60-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="94e60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94e60-102">SYNOPSIS</span></span>
<span data-ttu-id="94e60-103">Hitelesítő kódot hoz létre az Azure IoT hub tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="94e60-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94e60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94e60-104">SYNTAX</span></span>

### <span data-ttu-id="94e60-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94e60-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94e60-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94e60-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94e60-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94e60-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94e60-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="94e60-108">DESCRIPTION</span></span>
<span data-ttu-id="94e60-109">Ez az ellenőrző kód a tanúsítványok birtoklási lépésének igazolását fejezi ki.</span><span class="sxs-lookup"><span data-stu-id="94e60-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="94e60-110">Ezt az ellenőrző kódot használja egy új, a főtanúsítványokat tartalmazó titkos kulccsal aláírt tanúsítvány CN-ként.</span><span class="sxs-lookup"><span data-stu-id="94e60-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="94e60-111">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="94e60-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="94e60-112">Példák</span><span class="sxs-lookup"><span data-stu-id="94e60-112">EXAMPLES</span></span>

### <span data-ttu-id="94e60-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94e60-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="94e60-114">Hitelesítő kód létrehozása a MyCertificate-hoz</span><span class="sxs-lookup"><span data-stu-id="94e60-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="94e60-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94e60-115">PARAMETERS</span></span>

### <span data-ttu-id="94e60-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="94e60-116">-CertificateName</span></span>
<span data-ttu-id="94e60-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="94e60-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="94e60-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e60-118">-DefaultProfile</span></span>
<span data-ttu-id="94e60-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94e60-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e60-120">-ETAG</span><span class="sxs-lookup"><span data-stu-id="94e60-120">-Etag</span></span>
<span data-ttu-id="94e60-121">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="94e60-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="94e60-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e60-122">-InputObject</span></span>
<span data-ttu-id="94e60-123">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="94e60-123">Certificate Object</span></span>

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

### <span data-ttu-id="94e60-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94e60-124">-Name</span></span>
<span data-ttu-id="94e60-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="94e60-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="94e60-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e60-126">-ResourceGroupName</span></span>
<span data-ttu-id="94e60-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="94e60-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="94e60-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94e60-128">-ResourceId</span></span>
<span data-ttu-id="94e60-129">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="94e60-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="94e60-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e60-130">CommonParameters</span></span>
<span data-ttu-id="94e60-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94e60-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e60-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e60-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e60-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94e60-133">INPUTS</span></span>

### <span data-ttu-id="94e60-134">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="94e60-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="94e60-135">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94e60-135">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="94e60-136">System. String</span><span class="sxs-lookup"><span data-stu-id="94e60-136">System.String</span></span>

## <span data-ttu-id="94e60-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94e60-137">OUTPUTS</span></span>

### <span data-ttu-id="94e60-138">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="94e60-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="94e60-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94e60-139">NOTES</span></span>

## <span data-ttu-id="94e60-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94e60-140">RELATED LINKS</span></span>