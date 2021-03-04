---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: ac4da06b2f90f9d7bb5c3cbccbde98c8c65db481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933850"
---
# <span data-ttu-id="14816-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="14816-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="14816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14816-102">SYNOPSIS</span></span>
<span data-ttu-id="14816-103">Hozzáad egy megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="14816-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="14816-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14816-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14816-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14816-105">DESCRIPTION</span></span>
<span data-ttu-id="14816-106">Az **Add-AzApplicationGatewayTrustedClientCertificate** parancsmag hozzáad egy megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="14816-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="14816-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14816-107">EXAMPLES</span></span>

### <span data-ttu-id="14816-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="14816-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="14816-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="14816-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="14816-110">A második parancs egy új megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncot hoz létre, amely az ügyfél-hitelesítésszolgáltató tanúsítványának beviteli útvonalát veszi fel.</span><span class="sxs-lookup"><span data-stu-id="14816-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="14816-111">A harmadik parancs egy SSL-profilt hoz létre megbízható ügyfél tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="14816-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="14816-112">A negyedik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="14816-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="14816-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14816-113">PARAMETERS</span></span>

### <span data-ttu-id="14816-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14816-114">-ApplicationGateway</span></span>
<span data-ttu-id="14816-115">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="14816-115">The applicationGateway</span></span>

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

### <span data-ttu-id="14816-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="14816-116">-CertificateFile</span></span>
<span data-ttu-id="14816-117">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncfájlja elérési útja</span><span class="sxs-lookup"><span data-stu-id="14816-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="14816-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14816-118">-DefaultProfile</span></span>
<span data-ttu-id="14816-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14816-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14816-120">-Name</span><span class="sxs-lookup"><span data-stu-id="14816-120">-Name</span></span>
<span data-ttu-id="14816-121">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="14816-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="14816-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14816-122">-Confirm</span></span>
<span data-ttu-id="14816-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="14816-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14816-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14816-124">-WhatIf</span></span>
<span data-ttu-id="14816-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="14816-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14816-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14816-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14816-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14816-127">CommonParameters</span></span>
<span data-ttu-id="14816-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14816-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14816-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14816-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14816-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14816-130">INPUTS</span></span>

### <span data-ttu-id="14816-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14816-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14816-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14816-132">OUTPUTS</span></span>

### <span data-ttu-id="14816-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14816-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14816-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14816-134">NOTES</span></span>

## <span data-ttu-id="14816-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14816-135">RELATED LINKS</span></span>

[<span data-ttu-id="14816-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="14816-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="14816-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="14816-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="14816-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="14816-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="14816-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="14816-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)