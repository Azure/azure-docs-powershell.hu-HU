---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 9ec4522da3c5a75a1c9e5bad977f294e0987f4fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494039"
---
# <span data-ttu-id="985a3-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="985a3-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="985a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="985a3-102">SYNOPSIS</span></span>
<span data-ttu-id="985a3-103">Hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="985a3-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="985a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="985a3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="985a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="985a3-105">DESCRIPTION</span></span>
<span data-ttu-id="985a3-106">A **Remove-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway-ből távolítja el a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="985a3-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="985a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="985a3-107">EXAMPLES</span></span>

## <span data-ttu-id="985a3-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="985a3-108">PARAMETERS</span></span>

### <span data-ttu-id="985a3-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="985a3-109">-ApplicationGateway</span></span>
<span data-ttu-id="985a3-110">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="985a3-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="985a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985a3-111">-DefaultProfile</span></span>
<span data-ttu-id="985a3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="985a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="985a3-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="985a3-113">-Name</span></span>
<span data-ttu-id="985a3-114">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="985a3-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="985a3-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="985a3-115">-Confirm</span></span>
<span data-ttu-id="985a3-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="985a3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="985a3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="985a3-117">-WhatIf</span></span>
<span data-ttu-id="985a3-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="985a3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="985a3-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="985a3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="985a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985a3-120">CommonParameters</span></span>
<span data-ttu-id="985a3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="985a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985a3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="985a3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985a3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="985a3-123">INPUTS</span></span>

### <span data-ttu-id="985a3-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="985a3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="985a3-125">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="985a3-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="985a3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="985a3-126">OUTPUTS</span></span>

### <span data-ttu-id="985a3-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="985a3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="985a3-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="985a3-128">NOTES</span></span>
* <span data-ttu-id="985a3-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="985a3-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="985a3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="985a3-130">RELATED LINKS</span></span>

[<span data-ttu-id="985a3-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="985a3-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="985a3-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="985a3-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="985a3-133">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="985a3-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="985a3-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="985a3-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


