---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841762"
---
# <span data-ttu-id="2578c-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2578c-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2578c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2578c-102">SYNOPSIS</span></span>
<span data-ttu-id="2578c-103">Hitelesítési tanúsítvány kérése az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2578c-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="2578c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2578c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2578c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2578c-105">DESCRIPTION</span></span>
<span data-ttu-id="2578c-106">A **Get-AzApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát kapja.</span><span class="sxs-lookup"><span data-stu-id="2578c-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2578c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2578c-107">EXAMPLES</span></span>

### <span data-ttu-id="2578c-108">1:</span><span class="sxs-lookup"><span data-stu-id="2578c-108">1:</span></span>
```

```

## <span data-ttu-id="2578c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2578c-109">PARAMETERS</span></span>

### <span data-ttu-id="2578c-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2578c-110">-ApplicationGateway</span></span>
<span data-ttu-id="2578c-111">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag hitelesítő tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="2578c-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2578c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2578c-112">-DefaultProfile</span></span>
<span data-ttu-id="2578c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2578c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2578c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2578c-114">-Name</span></span>
<span data-ttu-id="2578c-115">Annak a hitelesítési tanúsítványnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="2578c-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2578c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2578c-116">CommonParameters</span></span>
<span data-ttu-id="2578c-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2578c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2578c-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2578c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2578c-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2578c-119">INPUTS</span></span>

### <span data-ttu-id="2578c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2578c-120">System.String</span></span>

## <span data-ttu-id="2578c-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2578c-121">OUTPUTS</span></span>

### <span data-ttu-id="2578c-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2578c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2578c-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2578c-123">NOTES</span></span>
* <span data-ttu-id="2578c-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="2578c-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2578c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2578c-125">RELATED LINKS</span></span>

[<span data-ttu-id="2578c-126">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2578c-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2578c-127">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2578c-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2578c-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2578c-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2578c-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2578c-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


