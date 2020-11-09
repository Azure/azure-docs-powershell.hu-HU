---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303148"
---
# <span data-ttu-id="b6e88-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6e88-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b6e88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6e88-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e88-103">Egy megbízható főtanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="b6e88-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="b6e88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6e88-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e88-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6e88-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e88-106">A **Remove-AzApplicationGatewayTrustedRootCertificate** parancsmag egy meglévő alkalmazás-átjárótól eltávolítja a megbízható legfelső szintű tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="b6e88-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="b6e88-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6e88-107">EXAMPLES</span></span>

### <span data-ttu-id="b6e88-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6e88-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b6e88-109">Az első parancs beolvassa az Application Gatewayt, és a $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b6e88-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="b6e88-110">A második parancs eltávolítja a myRootCA nevű megbízható főtanúsítványt az $gw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b6e88-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="b6e88-111">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="b6e88-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b6e88-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6e88-112">PARAMETERS</span></span>

### <span data-ttu-id="b6e88-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6e88-113">-ApplicationGateway</span></span>
<span data-ttu-id="b6e88-114">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6e88-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e88-115">-DefaultProfile</span></span>
<span data-ttu-id="b6e88-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6e88-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e88-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6e88-117">-Name</span></span>
<span data-ttu-id="b6e88-118">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="b6e88-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e88-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6e88-119">-Confirm</span></span>
<span data-ttu-id="b6e88-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6e88-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e88-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e88-121">-WhatIf</span></span>
<span data-ttu-id="b6e88-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6e88-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e88-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6e88-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e88-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e88-124">CommonParameters</span></span>
<span data-ttu-id="b6e88-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6e88-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e88-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e88-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e88-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e88-127">INPUTS</span></span>

### <span data-ttu-id="b6e88-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6e88-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6e88-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e88-129">OUTPUTS</span></span>

### <span data-ttu-id="b6e88-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6e88-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6e88-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6e88-131">NOTES</span></span>

## <span data-ttu-id="b6e88-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6e88-132">RELATED LINKS</span></span>

[<span data-ttu-id="b6e88-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6e88-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b6e88-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6e88-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b6e88-135">Új – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6e88-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b6e88-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6e88-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
