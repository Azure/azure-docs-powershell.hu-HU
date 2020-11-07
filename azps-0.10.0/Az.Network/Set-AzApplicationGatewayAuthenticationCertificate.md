---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843721"
---
# <span data-ttu-id="ffb85-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb85-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ffb85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffb85-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb85-103">Az alkalmazás-átjárók hitelesítési tanúsítványának frissítése</span><span class="sxs-lookup"><span data-stu-id="ffb85-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="ffb85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffb85-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffb85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffb85-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb85-106">A **set-AzApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="ffb85-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ffb85-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ffb85-107">EXAMPLES</span></span>

### <span data-ttu-id="ffb85-108">1:</span><span class="sxs-lookup"><span data-stu-id="ffb85-108">1:</span></span>
```

```

## <span data-ttu-id="ffb85-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffb85-109">PARAMETERS</span></span>

### <span data-ttu-id="ffb85-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffb85-110">-ApplicationGateway</span></span>
<span data-ttu-id="ffb85-111">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag egy hitelesítési tanúsítványt frissít.</span><span class="sxs-lookup"><span data-stu-id="ffb85-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="ffb85-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ffb85-112">-CertificateFile</span></span>
<span data-ttu-id="ffb85-113">Annak a hitelesítési tanúsítványnak az elérési útját adja meg, amelyen a parancsmag frissíti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="ffb85-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="ffb85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb85-114">-DefaultProfile</span></span>
<span data-ttu-id="ffb85-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffb85-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffb85-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffb85-116">-Name</span></span>
<span data-ttu-id="ffb85-117">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="ffb85-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="ffb85-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ffb85-118">-Confirm</span></span>
<span data-ttu-id="ffb85-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffb85-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb85-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb85-120">-WhatIf</span></span>
<span data-ttu-id="ffb85-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ffb85-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb85-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffb85-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb85-123">CommonParameters</span></span>
<span data-ttu-id="ffb85-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffb85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb85-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb85-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb85-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffb85-126">INPUTS</span></span>

### <span data-ttu-id="ffb85-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ffb85-127">System.String</span></span>

## <span data-ttu-id="ffb85-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffb85-128">OUTPUTS</span></span>

### <span data-ttu-id="ffb85-129">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffb85-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ffb85-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffb85-130">NOTES</span></span>
* <span data-ttu-id="ffb85-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="ffb85-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ffb85-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffb85-132">RELATED LINKS</span></span>

[<span data-ttu-id="ffb85-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb85-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ffb85-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb85-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ffb85-135">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb85-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ffb85-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffb85-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


