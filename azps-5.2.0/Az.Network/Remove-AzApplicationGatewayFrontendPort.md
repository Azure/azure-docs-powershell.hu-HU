---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369891"
---
# <span data-ttu-id="72047-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="72047-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="72047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72047-102">SYNOPSIS</span></span>
<span data-ttu-id="72047-103">Eltávolít egy előlapi portot egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="72047-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="72047-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72047-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72047-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72047-105">DESCRIPTION</span></span>
<span data-ttu-id="72047-106">A **Remove-AzApplicationGatewayFrontendPort** parancsmag eltávolítja az előtér-portokat az Azure-alkalmazásátjárókból.</span><span class="sxs-lookup"><span data-stu-id="72047-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="72047-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72047-107">EXAMPLES</span></span>

### <span data-ttu-id="72047-108">Példa: Előlapi port eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="72047-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="72047-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és egy változóban $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="72047-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="72047-110">A második parancs eltávolítja a FrontEndPort02 nevű portot az alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="72047-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="72047-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72047-111">PARAMETERS</span></span>

### <span data-ttu-id="72047-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72047-112">-ApplicationGateway</span></span>
<span data-ttu-id="72047-113">Azt az alkalmazás-átjárót adja meg, amelyből el szeretné távolítani az előlapi portot.</span><span class="sxs-lookup"><span data-stu-id="72047-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="72047-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72047-114">-DefaultProfile</span></span>
<span data-ttu-id="72047-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72047-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72047-116">-Name</span><span class="sxs-lookup"><span data-stu-id="72047-116">-Name</span></span>
<span data-ttu-id="72047-117">Az eltávolítható előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72047-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="72047-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72047-118">CommonParameters</span></span>
<span data-ttu-id="72047-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72047-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72047-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72047-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72047-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72047-121">INPUTS</span></span>

### <span data-ttu-id="72047-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72047-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72047-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72047-123">OUTPUTS</span></span>

### <span data-ttu-id="72047-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72047-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72047-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72047-125">NOTES</span></span>

## <span data-ttu-id="72047-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72047-126">RELATED LINKS</span></span>

[<span data-ttu-id="72047-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="72047-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="72047-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="72047-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="72047-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="72047-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="72047-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="72047-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


