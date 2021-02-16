---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160907"
---
# <span data-ttu-id="9936d-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9936d-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="9936d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9936d-102">SYNOPSIS</span></span>
<span data-ttu-id="9936d-103">Megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9936d-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="9936d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9936d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9936d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9936d-105">DESCRIPTION</span></span>
<span data-ttu-id="9936d-106">A New-AzApplicationGatewayTrustedClientCertificate parancsmag létrehoz egy megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9936d-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="9936d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9936d-107">EXAMPLES</span></span>

### <span data-ttu-id="9936d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9936d-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="9936d-109">A parancs egy új megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát hozza létre, amely az ügyfél-hitelesítésszolgáltató tanúsítványának beviteli útvonalát veszi fel.</span><span class="sxs-lookup"><span data-stu-id="9936d-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="9936d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9936d-110">PARAMETERS</span></span>

### <span data-ttu-id="9936d-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9936d-111">-CertificateFile</span></span>
<span data-ttu-id="9936d-112">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncfájlja elérési útja</span><span class="sxs-lookup"><span data-stu-id="9936d-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="9936d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9936d-113">-DefaultProfile</span></span>
<span data-ttu-id="9936d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9936d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9936d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9936d-115">-Name</span></span>
<span data-ttu-id="9936d-116">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="9936d-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="9936d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9936d-117">-Confirm</span></span>
<span data-ttu-id="9936d-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9936d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9936d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9936d-119">-WhatIf</span></span>
<span data-ttu-id="9936d-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9936d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9936d-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9936d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9936d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9936d-122">CommonParameters</span></span>
<span data-ttu-id="9936d-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9936d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9936d-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9936d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9936d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9936d-125">INPUTS</span></span>

### <span data-ttu-id="9936d-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9936d-126">None</span></span>

## <span data-ttu-id="9936d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9936d-127">OUTPUTS</span></span>

### <span data-ttu-id="9936d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9936d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="9936d-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9936d-129">NOTES</span></span>

## <span data-ttu-id="9936d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9936d-130">RELATED LINKS</span></span>

[<span data-ttu-id="9936d-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9936d-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9936d-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9936d-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9936d-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9936d-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9936d-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9936d-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)