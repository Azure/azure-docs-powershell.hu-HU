---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202634"
---
# <span data-ttu-id="91e91-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91e91-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="91e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e91-102">SYNOPSIS</span></span>
<span data-ttu-id="91e91-103">Eltávolítja egy meglévő alkalmazás-átjáró állapotát.</span><span class="sxs-lookup"><span data-stu-id="91e91-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="91e91-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91e91-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e91-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91e91-105">DESCRIPTION</span></span>
<span data-ttu-id="91e91-106">A Remove-AzApplicationGatewayProbeConfig parancsmag eltávolítja a hőveszteséget egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="91e91-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="91e91-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91e91-107">EXAMPLES</span></span>

### <span data-ttu-id="91e91-108">1. példa: Állapot állapotának eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="91e91-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="91e91-109">Ezzel a paranccsal eltávolítja az Átjáró nevű alkalmazás-átjáróból az 1111114-es nevű állapotkezelő nevet.</span><span class="sxs-lookup"><span data-stu-id="91e91-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="91e91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91e91-110">PARAMETERS</span></span>

### <span data-ttu-id="91e91-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91e91-111">-ApplicationGateway</span></span>
<span data-ttu-id="91e91-112">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag eltávolítja az adatsértőt.</span><span class="sxs-lookup"><span data-stu-id="91e91-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="91e91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e91-113">-DefaultProfile</span></span>
<span data-ttu-id="91e91-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91e91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91e91-115">-Name</span><span class="sxs-lookup"><span data-stu-id="91e91-115">-Name</span></span>
<span data-ttu-id="91e91-116">Annak a parancsmagnak a nevét adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="91e91-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="91e91-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e91-117">CommonParameters</span></span>
<span data-ttu-id="91e91-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e91-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e91-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e91-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e91-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91e91-120">INPUTS</span></span>

### <span data-ttu-id="91e91-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91e91-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91e91-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91e91-122">OUTPUTS</span></span>

### <span data-ttu-id="91e91-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91e91-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91e91-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91e91-124">NOTES</span></span>

## <span data-ttu-id="91e91-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91e91-125">RELATED LINKS</span></span>

[<span data-ttu-id="91e91-126">Eltávolítás meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="91e91-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="91e91-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91e91-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="91e91-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91e91-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="91e91-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91e91-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="91e91-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91e91-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

