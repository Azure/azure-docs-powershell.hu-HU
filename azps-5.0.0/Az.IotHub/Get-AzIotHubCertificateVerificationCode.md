---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187762"
---
# <span data-ttu-id="a0d07-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="a0d07-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="a0d07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0d07-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d07-103">Hitelesítő kódot hoz létre az Azure IoT hub tanúsítványához.</span><span class="sxs-lookup"><span data-stu-id="a0d07-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="a0d07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0d07-104">SYNTAX</span></span>

### <span data-ttu-id="a0d07-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0d07-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0d07-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a0d07-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0d07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a0d07-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0d07-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0d07-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d07-109">Ez az ellenőrző kód a tanúsítványok birtoklási lépésének igazolását fejezi ki.</span><span class="sxs-lookup"><span data-stu-id="a0d07-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="a0d07-110">Ezt az ellenőrző kódot használja egy új, a főtanúsítványokat tartalmazó titkos kulccsal aláírt tanúsítvány CN-ként.</span><span class="sxs-lookup"><span data-stu-id="a0d07-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="a0d07-111">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="a0d07-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="a0d07-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a0d07-112">EXAMPLES</span></span>

### <span data-ttu-id="a0d07-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a0d07-113">Example 1</span></span>
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

<span data-ttu-id="a0d07-114">Hitelesítő kód létrehozása a MyCertificate-hoz</span><span class="sxs-lookup"><span data-stu-id="a0d07-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="a0d07-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0d07-115">PARAMETERS</span></span>

### <span data-ttu-id="a0d07-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a0d07-116">-CertificateName</span></span>
<span data-ttu-id="a0d07-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="a0d07-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a0d07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d07-118">-DefaultProfile</span></span>
<span data-ttu-id="a0d07-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0d07-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d07-120">-ETAG</span><span class="sxs-lookup"><span data-stu-id="a0d07-120">-Etag</span></span>
<span data-ttu-id="a0d07-121">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="a0d07-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a0d07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0d07-122">-InputObject</span></span>
<span data-ttu-id="a0d07-123">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="a0d07-123">Certificate Object</span></span>

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

### <span data-ttu-id="a0d07-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0d07-124">-Name</span></span>
<span data-ttu-id="a0d07-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="a0d07-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a0d07-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d07-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0d07-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a0d07-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a0d07-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0d07-128">-ResourceId</span></span>
<span data-ttu-id="a0d07-129">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a0d07-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="a0d07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d07-130">CommonParameters</span></span>
<span data-ttu-id="a0d07-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0d07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d07-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d07-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d07-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0d07-133">INPUTS</span></span>

### <span data-ttu-id="a0d07-134">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="a0d07-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="a0d07-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a0d07-135">System.String</span></span>

## <span data-ttu-id="a0d07-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0d07-136">OUTPUTS</span></span>

### <span data-ttu-id="a0d07-137">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="a0d07-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="a0d07-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0d07-138">NOTES</span></span>

## <span data-ttu-id="a0d07-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0d07-139">RELATED LINKS</span></span>