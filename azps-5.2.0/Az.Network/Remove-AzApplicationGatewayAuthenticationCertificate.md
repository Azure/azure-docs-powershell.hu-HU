---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329730"
---
# <span data-ttu-id="5c4bc-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c4bc-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5c4bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4bc-103">Eltávolít egy hitelesítési tanúsítványt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="5c4bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c4bc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="5c4bc-106">A **Remove-AzApplicationGatewayAuthenticationCertificate parancsmag** eltávolít egy hitelesítési tanúsítványt egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="5c4bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c4bc-107">EXAMPLES</span></span>

### <span data-ttu-id="5c4bc-108">1. példa: Hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="5c4bc-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5c4bc-109">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és az eredményt a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="5c4bc-110">A második parancs eltávolítja a cert01 nevű hitelesítési tanúsítványt az alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="5c4bc-111">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="5c4bc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c4bc-112">PARAMETERS</span></span>

### <span data-ttu-id="5c4bc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c4bc-113">-ApplicationGateway</span></span>
<span data-ttu-id="5c4bc-114">Megadja annak az alkalmazás-átjárónak a nevét, amelyből a parancsmag eltávolít egy hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="5c4bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4bc-115">-DefaultProfile</span></span>
<span data-ttu-id="5c4bc-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c4bc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5c4bc-117">-Name</span></span>
<span data-ttu-id="5c4bc-118">A parancsmag által eltávolított hitelesítési tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5c4bc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c4bc-119">-Confirm</span></span>
<span data-ttu-id="5c4bc-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4bc-121">-WhatIf</span></span>
<span data-ttu-id="5c4bc-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4bc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4bc-124">CommonParameters</span></span>
<span data-ttu-id="5c4bc-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4bc-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c4bc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4bc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c4bc-127">INPUTS</span></span>

### <span data-ttu-id="5c4bc-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c4bc-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c4bc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c4bc-129">OUTPUTS</span></span>

### <span data-ttu-id="5c4bc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c4bc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c4bc-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c4bc-131">NOTES</span></span>
* <span data-ttu-id="5c4bc-132">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="5c4bc-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5c4bc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c4bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="5c4bc-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c4bc-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5c4bc-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c4bc-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5c4bc-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c4bc-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5c4bc-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c4bc-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


