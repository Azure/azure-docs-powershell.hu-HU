---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 00d5d84f3f9895aec42f9728de6eec1bf2ff9b06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157154"
---
# <span data-ttu-id="ba8fc-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba8fc-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ba8fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8fc-103">Hitelesítési tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="ba8fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba8fc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8fc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba8fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8fc-106">A **Get-AzApplicationGatewayAuthenticationCertificate parancsmag egy Azure-alkalmazás** átjáróhoz kap egy hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ba8fc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba8fc-107">EXAMPLES</span></span>

### <span data-ttu-id="ba8fc-108">1. példa: Megadott hitelesítési tanúsítvány lekérve</span><span class="sxs-lookup"><span data-stu-id="ba8fc-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="ba8fc-109">Az első parancs lekérte az appGwName nevű alkalmazás-átjárót, és a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="ba8fc-110">A második parancs lekéri a cert01 nevű hitelesítési tanúsítványt, és a hitelesítő $cert tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="ba8fc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba8fc-111">PARAMETERS</span></span>

### <span data-ttu-id="ba8fc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba8fc-112">-ApplicationGateway</span></span>
<span data-ttu-id="ba8fc-113">Megadja annak az alkalmazás-átjárónak a nevét, amelyhez ez a parancsmag hitelesítési tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="ba8fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8fc-114">-DefaultProfile</span></span>
<span data-ttu-id="ba8fc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba8fc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ba8fc-116">-Name</span></span>
<span data-ttu-id="ba8fc-117">Annak a hitelesítési tanúsítványnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ba8fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8fc-118">CommonParameters</span></span>
<span data-ttu-id="ba8fc-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8fc-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba8fc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8fc-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba8fc-121">INPUTS</span></span>

### <span data-ttu-id="ba8fc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba8fc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ba8fc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba8fc-123">OUTPUTS</span></span>

### <span data-ttu-id="ba8fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba8fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ba8fc-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba8fc-125">NOTES</span></span>
* <span data-ttu-id="ba8fc-126">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="ba8fc-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ba8fc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba8fc-127">RELATED LINKS</span></span>

[<span data-ttu-id="ba8fc-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba8fc-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ba8fc-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba8fc-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ba8fc-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba8fc-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ba8fc-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba8fc-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


