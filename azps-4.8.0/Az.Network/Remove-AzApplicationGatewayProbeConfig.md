---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024593"
---
# <span data-ttu-id="82a38-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="82a38-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="82a38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82a38-102">SYNOPSIS</span></span>
<span data-ttu-id="82a38-103">Egy meglévő alkalmazás-átjárótól eltávolítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="82a38-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="82a38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82a38-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82a38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82a38-105">DESCRIPTION</span></span>
<span data-ttu-id="82a38-106">A Remove-AzApplicationGatewayProbeConfig parancsmag eltávolítja a Heath-szondát egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="82a38-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="82a38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="82a38-107">EXAMPLES</span></span>

### <span data-ttu-id="82a38-108">1. példa: biztonságiállapot-szonda eltávolítása meglévő alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="82a38-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="82a38-109">Ez a parancs eltávolítja a Probe04 nevű biztonságiállapot-szondat az átjáró nevű alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="82a38-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="82a38-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82a38-110">PARAMETERS</span></span>

### <span data-ttu-id="82a38-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82a38-111">-ApplicationGateway</span></span>
<span data-ttu-id="82a38-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja a szondát.</span><span class="sxs-lookup"><span data-stu-id="82a38-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="82a38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a38-113">-DefaultProfile</span></span>
<span data-ttu-id="82a38-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82a38-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82a38-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82a38-115">-Name</span></span>
<span data-ttu-id="82a38-116">Annak a szondanak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="82a38-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="82a38-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a38-117">CommonParameters</span></span>
<span data-ttu-id="82a38-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82a38-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a38-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a38-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a38-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82a38-120">INPUTS</span></span>

### <span data-ttu-id="82a38-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82a38-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82a38-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82a38-122">OUTPUTS</span></span>

### <span data-ttu-id="82a38-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82a38-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82a38-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82a38-124">NOTES</span></span>

## <span data-ttu-id="82a38-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82a38-125">RELATED LINKS</span></span>

[<span data-ttu-id="82a38-126">Szonda eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="82a38-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="82a38-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="82a38-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="82a38-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="82a38-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="82a38-129">Új – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="82a38-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="82a38-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="82a38-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

