---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cd88a6ddf591ec4bace75fec1cb51bf1b4769583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495537"
---
# <span data-ttu-id="09713-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09713-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="09713-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09713-102">SYNOPSIS</span></span>
<span data-ttu-id="09713-103">Az Azure Application Gateway-től származó SSL-tanúsítványok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="09713-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09713-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09713-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09713-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09713-105">DESCRIPTION</span></span>
<span data-ttu-id="09713-106">A **Remove-AzureRmApplicationGatewaySslCertificate** parancsmag a Secure Sockets Layer (SSL) tanúsítványt egy Azure Application Gateway-ből távolítja el.</span><span class="sxs-lookup"><span data-stu-id="09713-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="09713-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09713-107">EXAMPLES</span></span>

### <span data-ttu-id="09713-108">1. példa: az SSL-tanúsítványok eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="09713-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="09713-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09713-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="09713-110">A második parancs eltávolítja a Cert02 nevű SSL-tanúsítványt a $AppGW változóban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="09713-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="09713-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09713-111">PARAMETERS</span></span>

### <span data-ttu-id="09713-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09713-112">-ApplicationGateway</span></span>
<span data-ttu-id="09713-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="09713-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="09713-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09713-114">-Name</span></span>
<span data-ttu-id="09713-115">A parancsmag által eltávolított SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09713-115">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09713-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09713-116">-DefaultProfile</span></span>
<span data-ttu-id="09713-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09713-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09713-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09713-118">CommonParameters</span></span>
<span data-ttu-id="09713-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09713-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09713-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09713-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09713-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09713-121">INPUTS</span></span>

### <span data-ttu-id="09713-122">System. String</span><span class="sxs-lookup"><span data-stu-id="09713-122">System.String</span></span>

## <span data-ttu-id="09713-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09713-123">OUTPUTS</span></span>

### <span data-ttu-id="09713-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09713-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09713-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09713-125">NOTES</span></span>

## <span data-ttu-id="09713-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09713-126">RELATED LINKS</span></span>

[<span data-ttu-id="09713-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09713-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="09713-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09713-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="09713-129">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09713-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="09713-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09713-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


