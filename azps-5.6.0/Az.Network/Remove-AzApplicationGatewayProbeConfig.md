---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 8ee58ee3f6c7a92fac0cb3c92f0a45966e4e875e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938594"
---
# <span data-ttu-id="6b023-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b023-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6b023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b023-102">SYNOPSIS</span></span>
<span data-ttu-id="6b023-103">Eltávolítja a meglévő alkalmazásátjárók állapot-állapotát.</span><span class="sxs-lookup"><span data-stu-id="6b023-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="6b023-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b023-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b023-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b023-105">DESCRIPTION</span></span>
<span data-ttu-id="6b023-106">A Remove-AzApplicationGatewayProbeConfig parancsmag eltávolítja a hőveszteséget egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="6b023-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="6b023-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b023-107">EXAMPLES</span></span>

### <span data-ttu-id="6b023-108">1. példa: Állapoti problémák eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="6b023-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="6b023-109">Ezzel a paranccsal eltávolítja az Átjáró nevű alkalmazás-átjáróból az 1111114-es nevű állapotkezelő nevet.</span><span class="sxs-lookup"><span data-stu-id="6b023-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="6b023-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b023-110">PARAMETERS</span></span>

### <span data-ttu-id="6b023-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b023-111">-ApplicationGateway</span></span>
<span data-ttu-id="6b023-112">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag eltávolítja az adatsértőt.</span><span class="sxs-lookup"><span data-stu-id="6b023-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="6b023-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b023-113">-DefaultProfile</span></span>
<span data-ttu-id="6b023-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b023-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b023-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6b023-115">-Name</span></span>
<span data-ttu-id="6b023-116">Annak a parancsmagnak a nevét adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="6b023-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b023-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b023-117">CommonParameters</span></span>
<span data-ttu-id="6b023-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b023-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b023-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b023-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b023-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b023-120">INPUTS</span></span>

### <span data-ttu-id="6b023-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b023-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b023-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b023-122">OUTPUTS</span></span>

### <span data-ttu-id="6b023-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b023-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b023-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b023-124">NOTES</span></span>

## <span data-ttu-id="6b023-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b023-125">RELATED LINKS</span></span>

[<span data-ttu-id="6b023-126">Eltávolítás meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="6b023-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="6b023-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b023-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6b023-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b023-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6b023-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b023-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6b023-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b023-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

