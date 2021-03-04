---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936146"
---
# <span data-ttu-id="e2c6f-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2c6f-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e2c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c6f-103">Eltávolít egy SSL-tanúsítványt egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e2c6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2c6f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2c6f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c6f-106">A **Remove-AzApplicationGatewaySslCertificate** parancsmag eltávolít egy SSL-tanúsítványt egy Azure-alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e2c6f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2c6f-107">EXAMPLES</span></span>

### <span data-ttu-id="e2c6f-108">1. példa: SSL-tanúsítvány eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="e2c6f-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="e2c6f-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e2c6f-110">A második parancs eltávolítja a Cert02 nevű SSL-tanúsítványt a $AppGW átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="e2c6f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2c6f-111">PARAMETERS</span></span>

### <span data-ttu-id="e2c6f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2c6f-112">-ApplicationGateway</span></span>
<span data-ttu-id="e2c6f-113">Azt az alkalmazás-átjárót adja meg, amelyből a parancsmag eltávolít egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="e2c6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c6f-114">-DefaultProfile</span></span>
<span data-ttu-id="e2c6f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2c6f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e2c6f-116">-Name</span></span>
<span data-ttu-id="e2c6f-117">Annak az SSL-tanúsítványnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2c6f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c6f-118">CommonParameters</span></span>
<span data-ttu-id="e2c6f-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c6f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c6f-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c6f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c6f-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2c6f-121">INPUTS</span></span>

### <span data-ttu-id="e2c6f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2c6f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2c6f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2c6f-123">OUTPUTS</span></span>

### <span data-ttu-id="e2c6f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2c6f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2c6f-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2c6f-125">NOTES</span></span>

## <span data-ttu-id="e2c6f-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2c6f-126">RELATED LINKS</span></span>

[<span data-ttu-id="e2c6f-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2c6f-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e2c6f-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2c6f-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e2c6f-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2c6f-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e2c6f-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2c6f-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


