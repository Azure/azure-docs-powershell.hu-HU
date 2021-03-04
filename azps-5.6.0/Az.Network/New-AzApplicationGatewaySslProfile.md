---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 4e58ee2c2f9b7854234913f0cf6ce7c6923f3345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927866"
---
# <span data-ttu-id="53085-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="53085-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="53085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53085-102">SYNOPSIS</span></span>
<span data-ttu-id="53085-103">SSL-profilt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="53085-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="53085-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53085-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53085-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53085-105">DESCRIPTION</span></span>
<span data-ttu-id="53085-106">A **New-AzApplicationGatewaySslProfile** parancsmag SSL-profilt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="53085-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="53085-107">Az ssl-profil konfigurálva van a HTTPS-figyelőkben.</span><span class="sxs-lookup"><span data-stu-id="53085-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="53085-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53085-108">EXAMPLES</span></span>

### <span data-ttu-id="53085-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="53085-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="53085-110">Az első parancs létrehoz egy új SSL-házirendet, és azt a $sslPolicy tárolja.</span><span class="sxs-lookup"><span data-stu-id="53085-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="53085-111">A második parancs egy megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot hoz létre, és a $ClientCert 01 változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="53085-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="53085-112">A harmadik parancs létrehoz egy új SSL-profilt az ssl-házirend és a megbízható ügyfél-hitelesítésszolgáltatói tanúsítványlánc segítségével.</span><span class="sxs-lookup"><span data-stu-id="53085-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="53085-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53085-113">PARAMETERS</span></span>

### <span data-ttu-id="53085-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="53085-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="53085-115">Ügyfél-hitelesítés konfigurációs beállításai</span><span class="sxs-lookup"><span data-stu-id="53085-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53085-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53085-116">-DefaultProfile</span></span>
<span data-ttu-id="53085-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53085-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53085-118">-Name</span><span class="sxs-lookup"><span data-stu-id="53085-118">-Name</span></span>
<span data-ttu-id="53085-119">Az SSL-profil neve</span><span class="sxs-lookup"><span data-stu-id="53085-119">The name of the SSL profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53085-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="53085-120">-SslPolicy</span></span>
<span data-ttu-id="53085-121">SSL-házirend</span><span class="sxs-lookup"><span data-stu-id="53085-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53085-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="53085-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="53085-123">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncai</span><span class="sxs-lookup"><span data-stu-id="53085-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53085-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53085-124">CommonParameters</span></span>
<span data-ttu-id="53085-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53085-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53085-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53085-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53085-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53085-127">INPUTS</span></span>

### <span data-ttu-id="53085-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="53085-128">None</span></span>

## <span data-ttu-id="53085-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53085-129">OUTPUTS</span></span>

### <span data-ttu-id="53085-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="53085-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="53085-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53085-131">NOTES</span></span>

## <span data-ttu-id="53085-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53085-132">RELATED LINKS</span></span>

[<span data-ttu-id="53085-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="53085-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="53085-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="53085-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="53085-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="53085-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="53085-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="53085-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)