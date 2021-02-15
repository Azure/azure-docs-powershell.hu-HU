---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151562"
---
# <span data-ttu-id="2695f-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="2695f-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="2695f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2695f-102">SYNOPSIS</span></span>
<span data-ttu-id="2695f-103">Eltávolít egy identitást egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="2695f-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="2695f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2695f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2695f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2695f-105">DESCRIPTION</span></span>
<span data-ttu-id="2695f-106">**A Remove-AzApplicationGatewayIdentity** parancsmag eltávolítja az identitást egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="2695f-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="2695f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2695f-107">EXAMPLES</span></span>

### <span data-ttu-id="2695f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2695f-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2695f-109">Ebben a példában eltávolítjuk az identitást egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="2695f-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="2695f-110">Megjegyzés: Ha az átjáró keyvault-kulcsra hivatkozik, akkor a művelet során el kell távolítania ezeket az ssl-tanúsítványhivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="2695f-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="2695f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2695f-111">PARAMETERS</span></span>

### <span data-ttu-id="2695f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2695f-112">-ApplicationGateway</span></span>
<span data-ttu-id="2695f-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2695f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2695f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2695f-114">-DefaultProfile</span></span>
<span data-ttu-id="2695f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2695f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2695f-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2695f-116">-Confirm</span></span>
<span data-ttu-id="2695f-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2695f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2695f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2695f-118">-WhatIf</span></span>
<span data-ttu-id="2695f-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2695f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2695f-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2695f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2695f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2695f-121">CommonParameters</span></span>
<span data-ttu-id="2695f-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2695f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2695f-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2695f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2695f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2695f-124">INPUTS</span></span>

### <span data-ttu-id="2695f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2695f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2695f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2695f-126">OUTPUTS</span></span>

### <span data-ttu-id="2695f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2695f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2695f-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2695f-128">NOTES</span></span>

## <span data-ttu-id="2695f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2695f-129">RELATED LINKS</span></span>
