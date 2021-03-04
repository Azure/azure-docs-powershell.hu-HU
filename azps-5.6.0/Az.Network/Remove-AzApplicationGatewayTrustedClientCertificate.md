---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: c7fdf250ad7c322e47c26e023f04689a12a8eee5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930953"
---
# <span data-ttu-id="9c0d6-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9c0d6-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="9c0d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0d6-103">Eltávolítja a megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="9c0d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c0d6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c0d6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c0d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9c0d6-106">A **Remove-AzApplicationGatewayTrustedClientCertificate** parancsmag eltávolítja a megbízható ügyfél-hitelesítésszolgáltató tanúsítványlánc-objektumát egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="9c0d6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c0d6-107">EXAMPLES</span></span>

### <span data-ttu-id="9c0d6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9c0d6-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="9c0d6-109">Az első parancs egy alkalmazás-átjárót kap, és a $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="9c0d6-110">A második parancs eltávolítja a "TrustedClientCertificate01" nevű megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot a $gw.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="9c0d6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c0d6-111">PARAMETERS</span></span>

### <span data-ttu-id="9c0d6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c0d6-112">-ApplicationGateway</span></span>
<span data-ttu-id="9c0d6-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c0d6-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9c0d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c0d6-114">-DefaultProfile</span></span>
<span data-ttu-id="9c0d6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c0d6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9c0d6-116">-Name</span></span>
<span data-ttu-id="9c0d6-117">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="9c0d6-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="9c0d6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c0d6-118">-Confirm</span></span>
<span data-ttu-id="9c0d6-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c0d6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c0d6-120">-WhatIf</span></span>
<span data-ttu-id="9c0d6-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c0d6-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c0d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0d6-123">CommonParameters</span></span>
<span data-ttu-id="9c0d6-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0d6-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c0d6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0d6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c0d6-126">INPUTS</span></span>

### <span data-ttu-id="9c0d6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c0d6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c0d6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c0d6-128">OUTPUTS</span></span>

### <span data-ttu-id="9c0d6-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c0d6-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c0d6-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c0d6-130">NOTES</span></span>

## <span data-ttu-id="9c0d6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c0d6-131">RELATED LINKS</span></span>

[<span data-ttu-id="9c0d6-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9c0d6-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9c0d6-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9c0d6-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9c0d6-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9c0d6-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9c0d6-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9c0d6-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)