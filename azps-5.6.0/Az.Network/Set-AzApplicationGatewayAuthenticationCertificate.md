---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a060ddde57fc3d0cfadde487a147b8743acd5fbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003509"
---
# <span data-ttu-id="1b5c1-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b5c1-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="1b5c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5c1-103">Frissíti egy alkalmazás-átjáró hitelesítési tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="1b5c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b5c1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b5c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="1b5c1-106">A **Set-AzApplicationGatewayAuthenticationCertificate parancsmag** frissíti az Azure-alkalmazásátjárók hitelesítési tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="1b5c1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b5c1-107">EXAMPLES</span></span>

### <span data-ttu-id="1b5c1-108">1. példa: Hitelesítési tanúsítvány frissítése</span><span class="sxs-lookup"><span data-stu-id="1b5c1-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="1b5c1-109">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és az eredményt a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="1b5c1-110">A második parancs frissíti a cert01 nevű hitelesítési tanúsítványt az alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="1b5c1-111">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="1b5c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b5c1-112">PARAMETERS</span></span>

### <span data-ttu-id="1b5c1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b5c1-113">-ApplicationGateway</span></span>
<span data-ttu-id="1b5c1-114">Megadja annak az alkalmazás-átjárónak a nevét, amelynek a parancsmagja frissíti a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="1b5c1-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1b5c1-115">-CertificateFile</span></span>
<span data-ttu-id="1b5c1-116">Annak a hitelesítési tanúsítványfájlnak az elérési útját adja meg, amellyel ez a parancsmag frissíti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="1b5c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5c1-117">-DefaultProfile</span></span>
<span data-ttu-id="1b5c1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b5c1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1b5c1-119">-Name</span></span>
<span data-ttu-id="1b5c1-120">A parancsmag által frissülő hitelesítési tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1b5c1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b5c1-121">-Confirm</span></span>
<span data-ttu-id="1b5c1-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b5c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b5c1-123">-WhatIf</span></span>
<span data-ttu-id="1b5c1-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b5c1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b5c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5c1-126">CommonParameters</span></span>
<span data-ttu-id="1b5c1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b5c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5c1-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b5c1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5c1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b5c1-129">INPUTS</span></span>

### <span data-ttu-id="1b5c1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b5c1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b5c1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b5c1-131">OUTPUTS</span></span>

### <span data-ttu-id="1b5c1-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b5c1-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b5c1-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b5c1-133">NOTES</span></span>
* <span data-ttu-id="1b5c1-134">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="1b5c1-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1b5c1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b5c1-135">RELATED LINKS</span></span>

[<span data-ttu-id="1b5c1-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b5c1-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1b5c1-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b5c1-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1b5c1-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b5c1-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1b5c1-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1b5c1-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


