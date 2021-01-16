---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362947"
---
# <span data-ttu-id="e0438-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e0438-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="e0438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0438-102">SYNOPSIS</span></span>
<span data-ttu-id="e0438-103">SSL-profil hozzáadása egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e0438-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="e0438-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0438-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0438-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0438-105">DESCRIPTION</span></span>
<span data-ttu-id="e0438-106">Az **Add-AzApplicationGatewaySslProfile** parancsmag hozzáad egy SSL-profilt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e0438-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="e0438-107">Az SSL-profil a HTTPS-figyelőkre van alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="e0438-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="e0438-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0438-108">EXAMPLES</span></span>

### <span data-ttu-id="e0438-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0438-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="e0438-110">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0438-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e0438-111">A második parancs létrehoz egy új SSL-házirendet, és azt a $sslPolicy tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0438-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="e0438-112">A harmadik és negyedik parancs két új megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot hoz létre, és azokat a $ClientCert 01 és $ClientCert 02 változókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0438-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="e0438-113">Az ötödik parancs hozzáadja az SSL-profilt az ssl-házirend és a megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncokkal együtt az $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e0438-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="e0438-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0438-114">PARAMETERS</span></span>

### <span data-ttu-id="e0438-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0438-115">-ApplicationGateway</span></span>
<span data-ttu-id="e0438-116">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0438-116">The applicationGateway</span></span>

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

### <span data-ttu-id="e0438-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0438-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="e0438-118">Ügyfél-hitelesítés konfigurációs beállításai</span><span class="sxs-lookup"><span data-stu-id="e0438-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="e0438-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0438-119">-DefaultProfile</span></span>
<span data-ttu-id="e0438-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0438-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0438-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e0438-121">-Name</span></span>
<span data-ttu-id="e0438-122">Az SSL-profil neve</span><span class="sxs-lookup"><span data-stu-id="e0438-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="e0438-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="e0438-123">-SslPolicy</span></span>
<span data-ttu-id="e0438-124">SSL-házirend</span><span class="sxs-lookup"><span data-stu-id="e0438-124">SSL policy</span></span>

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

### <span data-ttu-id="e0438-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="e0438-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="e0438-126">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncai</span><span class="sxs-lookup"><span data-stu-id="e0438-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="e0438-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0438-127">CommonParameters</span></span>
<span data-ttu-id="e0438-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0438-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0438-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0438-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0438-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0438-130">INPUTS</span></span>

### <span data-ttu-id="e0438-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0438-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0438-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0438-132">OUTPUTS</span></span>

### <span data-ttu-id="e0438-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0438-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0438-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0438-134">NOTES</span></span>

## <span data-ttu-id="e0438-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0438-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0438-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e0438-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="e0438-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e0438-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="e0438-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e0438-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="e0438-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e0438-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)