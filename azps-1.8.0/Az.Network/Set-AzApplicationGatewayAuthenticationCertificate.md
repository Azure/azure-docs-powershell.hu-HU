---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6e0194135b93898ea14998d92f8f23afd612f221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670072"
---
# <span data-ttu-id="84aaa-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="84aaa-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="84aaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="84aaa-103">Az alkalmazás-átjárók hitelesítési tanúsítványának frissítése</span><span class="sxs-lookup"><span data-stu-id="84aaa-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="84aaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84aaa-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84aaa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84aaa-105">DESCRIPTION</span></span>
<span data-ttu-id="84aaa-106">A **set-AzApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="84aaa-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="84aaa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84aaa-107">EXAMPLES</span></span>

### <span data-ttu-id="84aaa-108">Példa 1: hitelesítési tanúsítvány frissítése</span><span class="sxs-lookup"><span data-stu-id="84aaa-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="84aaa-109">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és az eredményt az $appgw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84aaa-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="84aaa-110">A második parancs frissíti az cert01 nevű hitelesítési tanúsítványt az Application gatewayban.</span><span class="sxs-lookup"><span data-stu-id="84aaa-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="84aaa-111">A harmadik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="84aaa-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="84aaa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84aaa-112">PARAMETERS</span></span>

### <span data-ttu-id="84aaa-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84aaa-113">-ApplicationGateway</span></span>
<span data-ttu-id="84aaa-114">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag egy hitelesítési tanúsítványt frissít.</span><span class="sxs-lookup"><span data-stu-id="84aaa-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="84aaa-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="84aaa-115">-CertificateFile</span></span>
<span data-ttu-id="84aaa-116">Annak a hitelesítési tanúsítványnak az elérési útját adja meg, amelyen a parancsmag frissíti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="84aaa-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="84aaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84aaa-117">-DefaultProfile</span></span>
<span data-ttu-id="84aaa-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84aaa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84aaa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84aaa-119">-Name</span></span>
<span data-ttu-id="84aaa-120">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="84aaa-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="84aaa-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84aaa-121">-Confirm</span></span>
<span data-ttu-id="84aaa-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84aaa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84aaa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84aaa-123">-WhatIf</span></span>
<span data-ttu-id="84aaa-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84aaa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84aaa-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84aaa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84aaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84aaa-126">CommonParameters</span></span>
<span data-ttu-id="84aaa-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84aaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84aaa-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84aaa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84aaa-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84aaa-129">INPUTS</span></span>

### <span data-ttu-id="84aaa-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84aaa-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84aaa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84aaa-131">OUTPUTS</span></span>

### <span data-ttu-id="84aaa-132">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84aaa-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84aaa-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84aaa-133">NOTES</span></span>
* <span data-ttu-id="84aaa-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="84aaa-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="84aaa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84aaa-135">RELATED LINKS</span></span>

[<span data-ttu-id="84aaa-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="84aaa-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="84aaa-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="84aaa-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="84aaa-138">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="84aaa-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="84aaa-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="84aaa-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


