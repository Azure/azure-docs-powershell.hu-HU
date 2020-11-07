---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841233"
---
# <span data-ttu-id="38c67-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="38c67-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="38c67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38c67-102">SYNOPSIS</span></span>
<span data-ttu-id="38c67-103">Hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="38c67-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="38c67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38c67-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38c67-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38c67-105">DESCRIPTION</span></span>
<span data-ttu-id="38c67-106">A **Remove-AzApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway-ből távolítja el a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="38c67-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="38c67-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38c67-107">EXAMPLES</span></span>

### <span data-ttu-id="38c67-108">1:</span><span class="sxs-lookup"><span data-stu-id="38c67-108">1:</span></span>
```

```

## <span data-ttu-id="38c67-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38c67-109">PARAMETERS</span></span>

### <span data-ttu-id="38c67-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38c67-110">-ApplicationGateway</span></span>
<span data-ttu-id="38c67-111">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="38c67-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="38c67-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c67-112">-DefaultProfile</span></span>
<span data-ttu-id="38c67-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38c67-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38c67-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38c67-114">-Name</span></span>
<span data-ttu-id="38c67-115">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="38c67-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38c67-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38c67-116">-Confirm</span></span>
<span data-ttu-id="38c67-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38c67-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c67-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c67-118">-WhatIf</span></span>
<span data-ttu-id="38c67-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38c67-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c67-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38c67-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c67-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c67-121">CommonParameters</span></span>
<span data-ttu-id="38c67-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38c67-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c67-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c67-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c67-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38c67-124">INPUTS</span></span>

### <span data-ttu-id="38c67-125">System. String</span><span class="sxs-lookup"><span data-stu-id="38c67-125">System.String</span></span>

## <span data-ttu-id="38c67-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38c67-126">OUTPUTS</span></span>

### <span data-ttu-id="38c67-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38c67-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38c67-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38c67-128">NOTES</span></span>
* <span data-ttu-id="38c67-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="38c67-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="38c67-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38c67-130">RELATED LINKS</span></span>

[<span data-ttu-id="38c67-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="38c67-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="38c67-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="38c67-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="38c67-133">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="38c67-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="38c67-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="38c67-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


