---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7b5f37cb42d128cbf44294520419c8f4d09124fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837871"
---
# <span data-ttu-id="9a301-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a301-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9a301-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a301-102">SYNOPSIS</span></span>
<span data-ttu-id="9a301-103">Az Azure Application Gateway-től származó SSL-tanúsítványok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9a301-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="9a301-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a301-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a301-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a301-105">DESCRIPTION</span></span>
<span data-ttu-id="9a301-106">A **Remove-AzApplicationGatewaySslCertificate** parancsmag a Secure Sockets Layer (SSL) tanúsítványt egy Azure Application Gateway-ből távolítja el.</span><span class="sxs-lookup"><span data-stu-id="9a301-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="9a301-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a301-107">EXAMPLES</span></span>

### <span data-ttu-id="9a301-108">1. példa: az SSL-tanúsítványok eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="9a301-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="9a301-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a301-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="9a301-110">A második parancs eltávolítja a Cert02 nevű SSL-tanúsítványt a $AppGW változóban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="9a301-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="9a301-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a301-111">PARAMETERS</span></span>

### <span data-ttu-id="9a301-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a301-112">-ApplicationGateway</span></span>
<span data-ttu-id="9a301-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="9a301-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="9a301-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a301-114">-DefaultProfile</span></span>
<span data-ttu-id="9a301-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a301-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a301-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a301-116">-Name</span></span>
<span data-ttu-id="9a301-117">A parancsmag által eltávolított SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a301-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9a301-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a301-118">CommonParameters</span></span>
<span data-ttu-id="9a301-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a301-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a301-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a301-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a301-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a301-121">INPUTS</span></span>

### <span data-ttu-id="9a301-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a301-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9a301-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a301-123">OUTPUTS</span></span>

### <span data-ttu-id="9a301-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a301-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9a301-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a301-125">NOTES</span></span>

## <span data-ttu-id="9a301-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a301-126">RELATED LINKS</span></span>

[<span data-ttu-id="9a301-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a301-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9a301-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a301-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9a301-129">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a301-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9a301-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a301-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


