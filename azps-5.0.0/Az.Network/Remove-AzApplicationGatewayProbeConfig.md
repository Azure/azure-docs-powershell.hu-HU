---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185970"
---
# <span data-ttu-id="801e5-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="801e5-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="801e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="801e5-102">SYNOPSIS</span></span>
<span data-ttu-id="801e5-103">Egy meglévő alkalmazás-átjárótól eltávolítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="801e5-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="801e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="801e5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="801e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="801e5-105">DESCRIPTION</span></span>
<span data-ttu-id="801e5-106">A Remove-AzApplicationGatewayProbeConfig parancsmag eltávolítja a Heath-szondát egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="801e5-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="801e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="801e5-107">EXAMPLES</span></span>

### <span data-ttu-id="801e5-108">1. példa: biztonságiállapot-szonda eltávolítása meglévő alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="801e5-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="801e5-109">Ez a parancs eltávolítja a Probe04 nevű biztonságiállapot-szondat az átjáró nevű alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="801e5-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="801e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="801e5-110">PARAMETERS</span></span>

### <span data-ttu-id="801e5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="801e5-111">-ApplicationGateway</span></span>
<span data-ttu-id="801e5-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja a szondát.</span><span class="sxs-lookup"><span data-stu-id="801e5-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="801e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801e5-113">-DefaultProfile</span></span>
<span data-ttu-id="801e5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="801e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="801e5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="801e5-115">-Name</span></span>
<span data-ttu-id="801e5-116">Annak a szondanak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="801e5-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="801e5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801e5-117">CommonParameters</span></span>
<span data-ttu-id="801e5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="801e5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801e5-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="801e5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801e5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="801e5-120">INPUTS</span></span>

### <span data-ttu-id="801e5-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="801e5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="801e5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="801e5-122">OUTPUTS</span></span>

### <span data-ttu-id="801e5-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="801e5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="801e5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="801e5-124">NOTES</span></span>

## <span data-ttu-id="801e5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="801e5-125">RELATED LINKS</span></span>

[<span data-ttu-id="801e5-126">Szonda eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="801e5-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="801e5-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="801e5-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="801e5-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="801e5-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="801e5-129">Új – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="801e5-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="801e5-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="801e5-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

