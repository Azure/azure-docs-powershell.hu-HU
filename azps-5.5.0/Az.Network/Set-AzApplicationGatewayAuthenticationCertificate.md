---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160651"
---
# <span data-ttu-id="11a36-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="11a36-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="11a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11a36-102">SYNOPSIS</span></span>
<span data-ttu-id="11a36-103">Frissíti egy alkalmazás-átjáró hitelesítési tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="11a36-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="11a36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11a36-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11a36-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11a36-105">DESCRIPTION</span></span>
<span data-ttu-id="11a36-106">A **Set-AzApplicationGatewayAuthenticationCertificate parancsmag** frissíti az Azure-alkalmazásátjárók hitelesítési tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="11a36-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="11a36-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11a36-107">EXAMPLES</span></span>

### <span data-ttu-id="11a36-108">1. példa: Hitelesítési tanúsítvány frissítése</span><span class="sxs-lookup"><span data-stu-id="11a36-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="11a36-109">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és az eredményt a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="11a36-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="11a36-110">A második parancs frissíti a cert01 nevű hitelesítési tanúsítványt az alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="11a36-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="11a36-111">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="11a36-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="11a36-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11a36-112">PARAMETERS</span></span>

### <span data-ttu-id="11a36-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11a36-113">-ApplicationGateway</span></span>
<span data-ttu-id="11a36-114">Megadja annak az alkalmazás-átjárónak a nevét, amelynek a parancsmagja frissíti a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="11a36-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="11a36-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="11a36-115">-CertificateFile</span></span>
<span data-ttu-id="11a36-116">Annak a hitelesítési tanúsítványfájlnak az elérési útját adja meg, amellyel ez a parancsmag frissíti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="11a36-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="11a36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a36-117">-DefaultProfile</span></span>
<span data-ttu-id="11a36-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11a36-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a36-119">-Name</span><span class="sxs-lookup"><span data-stu-id="11a36-119">-Name</span></span>
<span data-ttu-id="11a36-120">A parancsmag által frissülő hitelesítési tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="11a36-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="11a36-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11a36-121">-Confirm</span></span>
<span data-ttu-id="11a36-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11a36-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11a36-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11a36-123">-WhatIf</span></span>
<span data-ttu-id="11a36-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11a36-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11a36-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11a36-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11a36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a36-126">CommonParameters</span></span>
<span data-ttu-id="11a36-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a36-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a36-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a36-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11a36-129">INPUTS</span></span>

### <span data-ttu-id="11a36-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11a36-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11a36-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11a36-131">OUTPUTS</span></span>

### <span data-ttu-id="11a36-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11a36-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11a36-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11a36-133">NOTES</span></span>
* <span data-ttu-id="11a36-134">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="11a36-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="11a36-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11a36-135">RELATED LINKS</span></span>

[<span data-ttu-id="11a36-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="11a36-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="11a36-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="11a36-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="11a36-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="11a36-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="11a36-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="11a36-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


