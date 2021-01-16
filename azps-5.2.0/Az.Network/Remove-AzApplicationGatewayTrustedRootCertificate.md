---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327525"
---
# <span data-ttu-id="f58b0-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b0-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f58b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f58b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f58b0-103">Eltávolít egy megbízható gyökértanúsítványt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="f58b0-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="f58b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f58b0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f58b0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f58b0-105">DESCRIPTION</span></span>
<span data-ttu-id="f58b0-106">A **Remove-AzApplicationGatewayTrustedRootCertificate** parancsmag eltávolít egy megbízható gyökértanúsítványt egy meglévő alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="f58b0-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="f58b0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f58b0-107">EXAMPLES</span></span>

### <span data-ttu-id="f58b0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f58b0-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f58b0-109">Az első parancs egy alkalmazás-átjárót kap, és a $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="f58b0-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="f58b0-110">A második parancs eltávolítja a myRootCA nevű megbízható gyökértanúsítványt a $gw.</span><span class="sxs-lookup"><span data-stu-id="f58b0-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="f58b0-111">A harmadik parancs frissíti az alkalmazás-átjárót az Azure-on.</span><span class="sxs-lookup"><span data-stu-id="f58b0-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f58b0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f58b0-112">PARAMETERS</span></span>

### <span data-ttu-id="f58b0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f58b0-113">-ApplicationGateway</span></span>
<span data-ttu-id="f58b0-114">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f58b0-114">The applicationGateway</span></span>

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

### <span data-ttu-id="f58b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58b0-115">-DefaultProfile</span></span>
<span data-ttu-id="f58b0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f58b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f58b0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f58b0-117">-Name</span></span>
<span data-ttu-id="f58b0-118">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="f58b0-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f58b0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f58b0-119">-Confirm</span></span>
<span data-ttu-id="f58b0-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f58b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f58b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f58b0-121">-WhatIf</span></span>
<span data-ttu-id="f58b0-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f58b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f58b0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f58b0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f58b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58b0-124">CommonParameters</span></span>
<span data-ttu-id="f58b0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58b0-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58b0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58b0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f58b0-127">INPUTS</span></span>

### <span data-ttu-id="f58b0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f58b0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f58b0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f58b0-129">OUTPUTS</span></span>

### <span data-ttu-id="f58b0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f58b0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f58b0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f58b0-131">NOTES</span></span>

## <span data-ttu-id="f58b0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f58b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="f58b0-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b0-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f58b0-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b0-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f58b0-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b0-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f58b0-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b0-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
