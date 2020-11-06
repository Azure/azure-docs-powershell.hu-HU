---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 3facee36f6862c02975566dee20d9e7fb8c8824f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493419"
---
# <span data-ttu-id="c1c81-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c81-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c1c81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1c81-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c81-103">Hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="c1c81-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1c81-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c81-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1c81-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c81-106">A **Remove-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway-ből távolítja el a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c1c81-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="c1c81-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c1c81-107">EXAMPLES</span></span>

## <span data-ttu-id="c1c81-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1c81-108">PARAMETERS</span></span>

### <span data-ttu-id="c1c81-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1c81-109">-ApplicationGateway</span></span>
<span data-ttu-id="c1c81-110">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c1c81-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="c1c81-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1c81-111">-Name</span></span>
<span data-ttu-id="c1c81-112">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c1c81-112">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1c81-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1c81-113">-Confirm</span></span>
<span data-ttu-id="c1c81-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1c81-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c81-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c81-115">-WhatIf</span></span>
<span data-ttu-id="c1c81-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1c81-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c81-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1c81-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c81-118">-DefaultProfile</span></span>
<span data-ttu-id="c1c81-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1c81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1c81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c81-120">CommonParameters</span></span>
<span data-ttu-id="c1c81-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1c81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c81-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c81-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c81-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c81-123">INPUTS</span></span>

### <span data-ttu-id="c1c81-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c81-124">System.String</span></span>

## <span data-ttu-id="c1c81-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c81-125">OUTPUTS</span></span>

### <span data-ttu-id="c1c81-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1c81-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1c81-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1c81-127">NOTES</span></span>
* <span data-ttu-id="c1c81-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="c1c81-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c1c81-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1c81-129">RELATED LINKS</span></span>

[<span data-ttu-id="c1c81-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c81-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c1c81-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c81-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c1c81-132">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c81-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c1c81-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c81-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


