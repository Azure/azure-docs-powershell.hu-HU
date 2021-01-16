---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fbab2b1b9887fa7a5d509b46909f29eb741959bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468242"
---
# <span data-ttu-id="5428b-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5428b-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5428b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5428b-102">SYNOPSIS</span></span>
<span data-ttu-id="5428b-103">Hitelesítési tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5428b-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5428b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5428b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5428b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5428b-105">DESCRIPTION</span></span>
<span data-ttu-id="5428b-106">A **Get-AzApplicationGatewayAuthenticationCertificate parancsmag** kap egy hitelesítési tanúsítványt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5428b-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5428b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5428b-107">EXAMPLES</span></span>

### <span data-ttu-id="5428b-108">1. példa: Megadott hitelesítési tanúsítvány lekérve</span><span class="sxs-lookup"><span data-stu-id="5428b-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="5428b-109">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5428b-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="5428b-110">A második parancs lekéri a pool01 nevű hitelesítési tanúsítványt, és a $pool tárolja.</span><span class="sxs-lookup"><span data-stu-id="5428b-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="5428b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5428b-111">PARAMETERS</span></span>

### <span data-ttu-id="5428b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5428b-112">-ApplicationGateway</span></span>
<span data-ttu-id="5428b-113">Megadja annak az alkalmazás-átjárónak a nevét, amelyhez ez a parancsmag hitelesítési tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="5428b-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="5428b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5428b-114">-DefaultProfile</span></span>
<span data-ttu-id="5428b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5428b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5428b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5428b-116">-Name</span></span>
<span data-ttu-id="5428b-117">Annak a hitelesítési tanúsítványnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5428b-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5428b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5428b-118">CommonParameters</span></span>
<span data-ttu-id="5428b-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5428b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5428b-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5428b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5428b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5428b-121">INPUTS</span></span>

### <span data-ttu-id="5428b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5428b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5428b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5428b-123">OUTPUTS</span></span>

### <span data-ttu-id="5428b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5428b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5428b-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5428b-125">NOTES</span></span>
* <span data-ttu-id="5428b-126">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="5428b-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5428b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5428b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5428b-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5428b-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5428b-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5428b-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5428b-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5428b-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5428b-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5428b-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


