---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 4bed76f6fa80e5f901d5deeba45940d16332fa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670232"
---
# <span data-ttu-id="17194-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="17194-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="17194-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17194-102">SYNOPSIS</span></span>
<span data-ttu-id="17194-103">Hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="17194-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="17194-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17194-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17194-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17194-105">DESCRIPTION</span></span>
<span data-ttu-id="17194-106">A **Remove-AzApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway-ből távolítja el a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="17194-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="17194-107">Példák</span><span class="sxs-lookup"><span data-stu-id="17194-107">EXAMPLES</span></span>

### <span data-ttu-id="17194-108">1. példa: hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="17194-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="17194-109">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és az eredményt az $appgw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="17194-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="17194-110">A második parancs eltávolítja a cert01 nevű hitelesítési tanúsítványt az Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="17194-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="17194-111">A harmadik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="17194-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="17194-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17194-112">PARAMETERS</span></span>

### <span data-ttu-id="17194-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17194-113">-ApplicationGateway</span></span>
<span data-ttu-id="17194-114">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="17194-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="17194-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17194-115">-DefaultProfile</span></span>
<span data-ttu-id="17194-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17194-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17194-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17194-117">-Name</span></span>
<span data-ttu-id="17194-118">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="17194-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="17194-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17194-119">-Confirm</span></span>
<span data-ttu-id="17194-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17194-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17194-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17194-121">-WhatIf</span></span>
<span data-ttu-id="17194-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17194-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17194-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17194-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17194-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17194-124">CommonParameters</span></span>
<span data-ttu-id="17194-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17194-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17194-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17194-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17194-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17194-127">INPUTS</span></span>

### <span data-ttu-id="17194-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17194-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="17194-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17194-129">OUTPUTS</span></span>

### <span data-ttu-id="17194-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17194-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="17194-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17194-131">NOTES</span></span>
* <span data-ttu-id="17194-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="17194-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="17194-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17194-133">RELATED LINKS</span></span>

[<span data-ttu-id="17194-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="17194-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="17194-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="17194-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="17194-136">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="17194-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="17194-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="17194-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


