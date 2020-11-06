---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 271eaf702165c3c1e80243efa080b3e4d981390d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499991"
---
# <span data-ttu-id="f84e2-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f84e2-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f84e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f84e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f84e2-103">Hitelesítési tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="f84e2-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f84e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f84e2-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f84e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f84e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f84e2-106">Az **Add-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag hitelesítő tanúsítványt ad az Azure Application Gateway programhoz.</span><span class="sxs-lookup"><span data-stu-id="f84e2-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="f84e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f84e2-107">EXAMPLES</span></span>

## <span data-ttu-id="f84e2-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f84e2-108">PARAMETERS</span></span>

### <span data-ttu-id="f84e2-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f84e2-109">-ApplicationGateway</span></span>
<span data-ttu-id="f84e2-110">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag egy hitelesítési tanúsítványt ad.</span><span class="sxs-lookup"><span data-stu-id="f84e2-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="f84e2-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f84e2-111">-CertificateFile</span></span>
<span data-ttu-id="f84e2-112">A parancsmag által hozzáadott hitelesítési tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f84e2-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f84e2-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f84e2-113">-Name</span></span>
<span data-ttu-id="f84e2-114">Annak a tanúsítványnak a nevét adja meg, amelyre a parancsmag hozzáadja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="f84e2-114">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="f84e2-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f84e2-115">-Confirm</span></span>
<span data-ttu-id="f84e2-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f84e2-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84e2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84e2-117">-WhatIf</span></span>
<span data-ttu-id="f84e2-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f84e2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84e2-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f84e2-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84e2-120">-DefaultProfile</span></span>
<span data-ttu-id="f84e2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f84e2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84e2-122">CommonParameters</span></span>
<span data-ttu-id="f84e2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f84e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84e2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84e2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84e2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f84e2-125">INPUTS</span></span>

### <span data-ttu-id="f84e2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f84e2-126">System.String</span></span>

## <span data-ttu-id="f84e2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f84e2-127">OUTPUTS</span></span>

### <span data-ttu-id="f84e2-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f84e2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f84e2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f84e2-129">NOTES</span></span>
* <span data-ttu-id="f84e2-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="f84e2-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f84e2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f84e2-131">RELATED LINKS</span></span>

[<span data-ttu-id="f84e2-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f84e2-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f84e2-133">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f84e2-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f84e2-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f84e2-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f84e2-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f84e2-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


