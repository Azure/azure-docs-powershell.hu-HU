---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025243"
---
# <span data-ttu-id="4a144-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4a144-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4a144-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a144-102">SYNOPSIS</span></span>
<span data-ttu-id="4a144-103">Hitelesítési tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4a144-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="4a144-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a144-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a144-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a144-105">DESCRIPTION</span></span>
<span data-ttu-id="4a144-106">Az **Add-AzApplicationGatewayAuthenticationCertificate** parancsmag hitelesítő tanúsítványt ad az Azure Application Gateway programhoz.</span><span class="sxs-lookup"><span data-stu-id="4a144-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="4a144-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a144-107">EXAMPLES</span></span>

### <span data-ttu-id="4a144-108">1. példa: hitelesítési tanúsítvány hozzáadása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="4a144-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4a144-109">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és $appgw változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="4a144-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="4a144-110">A második parancs hozzáadja a cert01 nevű hitelesítési tanúsítványt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4a144-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="4a144-111">A harmadik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="4a144-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="4a144-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a144-112">PARAMETERS</span></span>

### <span data-ttu-id="4a144-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a144-113">-ApplicationGateway</span></span>
<span data-ttu-id="4a144-114">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag egy hitelesítési tanúsítványt ad.</span><span class="sxs-lookup"><span data-stu-id="4a144-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="4a144-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4a144-115">-CertificateFile</span></span>
<span data-ttu-id="4a144-116">A parancsmag által hozzáadott hitelesítési tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a144-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4a144-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a144-117">-DefaultProfile</span></span>
<span data-ttu-id="4a144-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a144-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a144-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a144-119">-Name</span></span>
<span data-ttu-id="4a144-120">Annak a tanúsítványnak a nevét adja meg, amelyre a parancsmag hozzáadja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="4a144-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="4a144-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a144-121">-Confirm</span></span>
<span data-ttu-id="4a144-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a144-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a144-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a144-123">-WhatIf</span></span>
<span data-ttu-id="4a144-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a144-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a144-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a144-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a144-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a144-126">CommonParameters</span></span>
<span data-ttu-id="4a144-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a144-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a144-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a144-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a144-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a144-129">INPUTS</span></span>

### <span data-ttu-id="4a144-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a144-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a144-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a144-131">OUTPUTS</span></span>

### <span data-ttu-id="4a144-132">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a144-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a144-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a144-133">NOTES</span></span>
* <span data-ttu-id="4a144-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="4a144-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4a144-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a144-135">RELATED LINKS</span></span>

[<span data-ttu-id="4a144-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4a144-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4a144-137">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4a144-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4a144-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4a144-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4a144-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4a144-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


