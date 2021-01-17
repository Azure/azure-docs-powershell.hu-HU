---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479965"
---
# <span data-ttu-id="579a0-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="579a0-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="579a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="579a0-102">SYNOPSIS</span></span>
<span data-ttu-id="579a0-103">Eltávolítja egy meglévő alkalmazás-átjáró állapotát.</span><span class="sxs-lookup"><span data-stu-id="579a0-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="579a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="579a0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579a0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="579a0-105">DESCRIPTION</span></span>
<span data-ttu-id="579a0-106">A Remove-AzApplicationGatewayProbeConfig parancsmag eltávolítja a hőveszteséget egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="579a0-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="579a0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="579a0-107">EXAMPLES</span></span>

### <span data-ttu-id="579a0-108">1. példa: Állapot állapotának eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="579a0-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="579a0-109">Ezzel a paranccsal eltávolítja az "1104" nevű állapotkezelő nevet az Átjáró nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="579a0-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="579a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="579a0-110">PARAMETERS</span></span>

### <span data-ttu-id="579a0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="579a0-111">-ApplicationGateway</span></span>
<span data-ttu-id="579a0-112">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag eltávolítja az adatsértőt.</span><span class="sxs-lookup"><span data-stu-id="579a0-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="579a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579a0-113">-DefaultProfile</span></span>
<span data-ttu-id="579a0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="579a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579a0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="579a0-115">-Name</span></span>
<span data-ttu-id="579a0-116">Annak a parancsmagnak a nevét adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="579a0-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="579a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579a0-117">CommonParameters</span></span>
<span data-ttu-id="579a0-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579a0-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="579a0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579a0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="579a0-120">INPUTS</span></span>

### <span data-ttu-id="579a0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="579a0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="579a0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="579a0-122">OUTPUTS</span></span>

### <span data-ttu-id="579a0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="579a0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="579a0-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="579a0-124">NOTES</span></span>

## <span data-ttu-id="579a0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="579a0-125">RELATED LINKS</span></span>

[<span data-ttu-id="579a0-126">Eltávolítás meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="579a0-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="579a0-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="579a0-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="579a0-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="579a0-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="579a0-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="579a0-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="579a0-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="579a0-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

