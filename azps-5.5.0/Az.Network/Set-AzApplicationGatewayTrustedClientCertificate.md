---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154122"
---
# <span data-ttu-id="c3312-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c3312-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="c3312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3312-102">SYNOPSIS</span></span>
<span data-ttu-id="c3312-103">Módosítja egy alkalmazás-átjáró megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncát.</span><span class="sxs-lookup"><span data-stu-id="c3312-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="c3312-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3312-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3312-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3312-105">DESCRIPTION</span></span>
<span data-ttu-id="c3312-106">A **Set-AzApplicationGatewayTrustedClientCertificate** parancsmag módosítja egy alkalmazás-átjáró megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncát.</span><span class="sxs-lookup"><span data-stu-id="c3312-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="c3312-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3312-107">EXAMPLES</span></span>

### <span data-ttu-id="c3312-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3312-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c3312-109">A fenti példa azt mutatja be, hogy miként frissíthet egy megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát.</span><span class="sxs-lookup"><span data-stu-id="c3312-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="c3312-110">Az első parancs egy alkalmazás-átjárót kap, és a $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="c3312-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="c3312-111">A második parancs módosítja a már meglévő megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát egy új hitelesítésszolgáltatói tanúsítványláncfájllal.</span><span class="sxs-lookup"><span data-stu-id="c3312-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="c3312-112">A harmadik parancs frissíti az alkalmazás-átjárót az Azure-on.</span><span class="sxs-lookup"><span data-stu-id="c3312-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c3312-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3312-113">PARAMETERS</span></span>

### <span data-ttu-id="c3312-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3312-114">-ApplicationGateway</span></span>
<span data-ttu-id="c3312-115">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3312-115">The applicationGateway</span></span>

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

### <span data-ttu-id="c3312-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c3312-116">-CertificateFile</span></span>
<span data-ttu-id="c3312-117">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncfájlja elérési útja</span><span class="sxs-lookup"><span data-stu-id="c3312-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="c3312-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3312-118">-DefaultProfile</span></span>
<span data-ttu-id="c3312-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3312-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3312-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c3312-120">-Name</span></span>
<span data-ttu-id="c3312-121">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="c3312-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="c3312-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3312-122">-Confirm</span></span>
<span data-ttu-id="c3312-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3312-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3312-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3312-124">-WhatIf</span></span>
<span data-ttu-id="c3312-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3312-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3312-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3312-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3312-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3312-127">CommonParameters</span></span>
<span data-ttu-id="c3312-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3312-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3312-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3312-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3312-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3312-130">INPUTS</span></span>

### <span data-ttu-id="c3312-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3312-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3312-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3312-132">OUTPUTS</span></span>

### <span data-ttu-id="c3312-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3312-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3312-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3312-134">NOTES</span></span>

## <span data-ttu-id="c3312-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3312-135">RELATED LINKS</span></span>

[<span data-ttu-id="c3312-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c3312-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c3312-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c3312-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c3312-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c3312-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c3312-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c3312-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)