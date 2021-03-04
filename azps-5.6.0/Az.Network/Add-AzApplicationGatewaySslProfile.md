---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 469b490b0f0c2bd37f7f58265108278322cbca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933857"
---
# <span data-ttu-id="2c9f5-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f5-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2c9f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9f5-103">SSL-profil hozzáadása egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="2c9f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c9f5-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9f5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c9f5-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9f5-106">Az **Add-AzApplicationGatewaySslProfile** parancsmag hozzáad egy SSL-profilt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="2c9f5-107">Az SSL-profil a HTTPS-figyelőkre van alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="2c9f5-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c9f5-108">EXAMPLES</span></span>

### <span data-ttu-id="2c9f5-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c9f5-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="2c9f5-110">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2c9f5-111">A második parancs létrehoz egy új SSL-házirendet, és azt a $sslPolicy tárolja.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="2c9f5-112">A harmadik és negyedik parancs két új megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot hoz létre, és azokat a $ClientCert 01 és $ClientCert 02 változókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="2c9f5-113">Az ötödik parancs hozzáadja az SSL-profilt az ssl-házirend és a megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncokkal együtt az $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="2c9f5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c9f5-114">PARAMETERS</span></span>

### <span data-ttu-id="2c9f5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c9f5-115">-ApplicationGateway</span></span>
<span data-ttu-id="2c9f5-116">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c9f5-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f5-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c9f5-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="2c9f5-118">Ügyfél-hitelesítés konfigurációs beállításai</span><span class="sxs-lookup"><span data-stu-id="2c9f5-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="2c9f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f5-119">-DefaultProfile</span></span>
<span data-ttu-id="2c9f5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c9f5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2c9f5-121">-Name</span></span>
<span data-ttu-id="2c9f5-122">Az SSL-profil neve</span><span class="sxs-lookup"><span data-stu-id="2c9f5-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="2c9f5-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c9f5-123">-SslPolicy</span></span>
<span data-ttu-id="2c9f5-124">SSL-házirend</span><span class="sxs-lookup"><span data-stu-id="2c9f5-124">SSL policy</span></span>

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

### <span data-ttu-id="2c9f5-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="2c9f5-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="2c9f5-126">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncai</span><span class="sxs-lookup"><span data-stu-id="2c9f5-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="2c9f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9f5-127">CommonParameters</span></span>
<span data-ttu-id="2c9f5-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9f5-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c9f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9f5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c9f5-130">INPUTS</span></span>

### <span data-ttu-id="2c9f5-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c9f5-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c9f5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c9f5-132">OUTPUTS</span></span>

### <span data-ttu-id="2c9f5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c9f5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c9f5-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c9f5-134">NOTES</span></span>

## <span data-ttu-id="2c9f5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c9f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c9f5-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f5-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2c9f5-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f5-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2c9f5-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f5-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2c9f5-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f5-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)