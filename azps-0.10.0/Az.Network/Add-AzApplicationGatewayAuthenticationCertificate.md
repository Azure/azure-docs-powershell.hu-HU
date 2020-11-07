---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841890"
---
# <span data-ttu-id="a8229-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8229-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a8229-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8229-102">SYNOPSIS</span></span>
<span data-ttu-id="a8229-103">Hitelesítési tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a8229-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="a8229-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8229-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8229-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8229-105">DESCRIPTION</span></span>
<span data-ttu-id="a8229-106">Az **Add-AzApplicationGatewayAuthenticationCertificate** parancsmag hitelesítő tanúsítványt ad az Azure Application Gateway programhoz.</span><span class="sxs-lookup"><span data-stu-id="a8229-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="a8229-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8229-107">EXAMPLES</span></span>

### <span data-ttu-id="a8229-108">1:</span><span class="sxs-lookup"><span data-stu-id="a8229-108">1:</span></span>
```

```

## <span data-ttu-id="a8229-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8229-109">PARAMETERS</span></span>

### <span data-ttu-id="a8229-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8229-110">-ApplicationGateway</span></span>
<span data-ttu-id="a8229-111">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag egy hitelesítési tanúsítványt ad.</span><span class="sxs-lookup"><span data-stu-id="a8229-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="a8229-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a8229-112">-CertificateFile</span></span>
<span data-ttu-id="a8229-113">A parancsmag által hozzáadott hitelesítési tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8229-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8229-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8229-114">-DefaultProfile</span></span>
<span data-ttu-id="a8229-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8229-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8229-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8229-116">-Name</span></span>
<span data-ttu-id="a8229-117">Annak a tanúsítványnak a nevét adja meg, amelyre a parancsmag hozzáadja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="a8229-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8229-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8229-118">-Confirm</span></span>
<span data-ttu-id="a8229-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8229-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8229-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8229-120">-WhatIf</span></span>
<span data-ttu-id="a8229-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8229-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8229-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8229-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8229-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8229-123">CommonParameters</span></span>
<span data-ttu-id="a8229-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8229-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8229-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8229-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8229-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8229-126">INPUTS</span></span>

### <span data-ttu-id="a8229-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a8229-127">System.String</span></span>

## <span data-ttu-id="a8229-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8229-128">OUTPUTS</span></span>

### <span data-ttu-id="a8229-129">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8229-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8229-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8229-130">NOTES</span></span>
* <span data-ttu-id="a8229-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="a8229-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a8229-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8229-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8229-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8229-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a8229-134">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8229-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a8229-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8229-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a8229-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a8229-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


