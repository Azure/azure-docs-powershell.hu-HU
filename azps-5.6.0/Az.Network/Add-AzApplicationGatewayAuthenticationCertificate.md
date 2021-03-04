---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ba0d82ab04f8e0c990c7bbf15facb3ee725f7609
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926642"
---
# <span data-ttu-id="787eb-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="787eb-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="787eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="787eb-102">SYNOPSIS</span></span>
<span data-ttu-id="787eb-103">Hozzáad egy hitelesítési tanúsítványt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="787eb-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="787eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="787eb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="787eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="787eb-105">DESCRIPTION</span></span>
<span data-ttu-id="787eb-106">Az **Add-AzApplicationGatewayAuthenticationCertificate parancsmag** hozzáad egy hitelesítési tanúsítványt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="787eb-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="787eb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="787eb-107">EXAMPLES</span></span>

### <span data-ttu-id="787eb-108">1. példa: Hitelesítési tanúsítvány hozzáadása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="787eb-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="787eb-109">Az első parancs egy appGwName nevű alkalmazás-átjárót kap, és egy $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="787eb-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="787eb-110">A második parancs hozzáadja a cert01 nevű hitelesítési tanúsítványt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="787eb-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="787eb-111">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="787eb-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="787eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="787eb-112">PARAMETERS</span></span>

### <span data-ttu-id="787eb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="787eb-113">-ApplicationGateway</span></span>
<span data-ttu-id="787eb-114">Megadja annak az alkalmazás-átjárónak a nevét, amelyhez ez a parancsmag hozzáad egy hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="787eb-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="787eb-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="787eb-115">-CertificateFile</span></span>
<span data-ttu-id="787eb-116">A parancsmag által megadott hitelesítési tanúsítvány elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="787eb-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="787eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787eb-117">-DefaultProfile</span></span>
<span data-ttu-id="787eb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="787eb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="787eb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="787eb-119">-Name</span></span>
<span data-ttu-id="787eb-120">Annak a tanúsítványnak a nevét adja meg, amely az alkalmazás-átjáróhoz hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="787eb-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="787eb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="787eb-121">-Confirm</span></span>
<span data-ttu-id="787eb-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="787eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787eb-123">-WhatIf</span></span>
<span data-ttu-id="787eb-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="787eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="787eb-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="787eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787eb-126">CommonParameters</span></span>
<span data-ttu-id="787eb-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787eb-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787eb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787eb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="787eb-129">INPUTS</span></span>

### <span data-ttu-id="787eb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="787eb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="787eb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="787eb-131">OUTPUTS</span></span>

### <span data-ttu-id="787eb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="787eb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="787eb-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="787eb-133">NOTES</span></span>
* <span data-ttu-id="787eb-134">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="787eb-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="787eb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="787eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="787eb-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="787eb-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="787eb-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="787eb-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="787eb-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="787eb-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="787eb-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="787eb-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


