---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360988"
---
# <span data-ttu-id="cbb21-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb21-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cbb21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb21-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb21-103">Megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cbb21-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="cbb21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbb21-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbb21-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbb21-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb21-106">A New-AzApplicationGatewayTrustedClientCertificate parancsmag létrehoz egy megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cbb21-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="cbb21-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbb21-107">EXAMPLES</span></span>

### <span data-ttu-id="cbb21-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbb21-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="cbb21-109">A parancs egy új megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát hozza létre, amely az ügyfél-hitelesítésszolgáltató tanúsítványának beviteli útvonalát veszi fel.</span><span class="sxs-lookup"><span data-stu-id="cbb21-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="cbb21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbb21-110">PARAMETERS</span></span>

### <span data-ttu-id="cbb21-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cbb21-111">-CertificateFile</span></span>
<span data-ttu-id="cbb21-112">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncfájlja elérési útja</span><span class="sxs-lookup"><span data-stu-id="cbb21-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="cbb21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb21-113">-DefaultProfile</span></span>
<span data-ttu-id="cbb21-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbb21-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbb21-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cbb21-115">-Name</span></span>
<span data-ttu-id="cbb21-116">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="cbb21-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="cbb21-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbb21-117">-Confirm</span></span>
<span data-ttu-id="cbb21-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cbb21-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbb21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbb21-119">-WhatIf</span></span>
<span data-ttu-id="cbb21-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cbb21-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbb21-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbb21-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbb21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb21-122">CommonParameters</span></span>
<span data-ttu-id="cbb21-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb21-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbb21-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb21-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbb21-125">INPUTS</span></span>

### <span data-ttu-id="cbb21-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="cbb21-126">None</span></span>

## <span data-ttu-id="cbb21-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbb21-127">OUTPUTS</span></span>

### <span data-ttu-id="cbb21-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb21-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cbb21-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbb21-129">NOTES</span></span>

## <span data-ttu-id="cbb21-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbb21-130">RELATED LINKS</span></span>

[<span data-ttu-id="cbb21-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb21-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cbb21-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb21-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cbb21-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb21-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cbb21-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb21-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)