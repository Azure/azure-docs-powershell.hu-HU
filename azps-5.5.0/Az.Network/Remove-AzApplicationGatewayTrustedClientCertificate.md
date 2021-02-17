---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154218"
---
# <span data-ttu-id="6175a-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6175a-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="6175a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6175a-102">SYNOPSIS</span></span>
<span data-ttu-id="6175a-103">Eltávolítja a megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="6175a-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="6175a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6175a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6175a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6175a-105">DESCRIPTION</span></span>
<span data-ttu-id="6175a-106">A **Remove-AzApplicationGatewayTrustedClientCertificate** parancsmag eltávolítja a megbízható ügyfél-hitelesítésszolgáltató tanúsítványlánc-objektumát egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="6175a-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="6175a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6175a-107">EXAMPLES</span></span>

### <span data-ttu-id="6175a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6175a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="6175a-109">Az első parancs egy alkalmazás-átjárót kap, és a $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="6175a-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="6175a-110">A második parancs eltávolítja a "TrustedClientCertificate01" nevű megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot a $gw.</span><span class="sxs-lookup"><span data-stu-id="6175a-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="6175a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6175a-111">PARAMETERS</span></span>

### <span data-ttu-id="6175a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6175a-112">-ApplicationGateway</span></span>
<span data-ttu-id="6175a-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6175a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6175a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6175a-114">-DefaultProfile</span></span>
<span data-ttu-id="6175a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6175a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6175a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6175a-116">-Name</span></span>
<span data-ttu-id="6175a-117">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="6175a-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="6175a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6175a-118">-Confirm</span></span>
<span data-ttu-id="6175a-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6175a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6175a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6175a-120">-WhatIf</span></span>
<span data-ttu-id="6175a-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6175a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6175a-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6175a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6175a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6175a-123">CommonParameters</span></span>
<span data-ttu-id="6175a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6175a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6175a-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6175a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6175a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6175a-126">INPUTS</span></span>

### <span data-ttu-id="6175a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6175a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6175a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6175a-128">OUTPUTS</span></span>

### <span data-ttu-id="6175a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6175a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6175a-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6175a-130">NOTES</span></span>

## <span data-ttu-id="6175a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6175a-131">RELATED LINKS</span></span>

[<span data-ttu-id="6175a-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6175a-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="6175a-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6175a-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="6175a-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6175a-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="6175a-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6175a-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)