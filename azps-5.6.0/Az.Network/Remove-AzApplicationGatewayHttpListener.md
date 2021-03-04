---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 46cf3a786642262c1f6d0df0e2c1fd770d61ec6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922361"
---
# <span data-ttu-id="366d8-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="366d8-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="366d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="366d8-102">SYNOPSIS</span></span>
<span data-ttu-id="366d8-103">Eltávolít egy HTTP-hallgatót egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="366d8-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="366d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="366d8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="366d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="366d8-105">DESCRIPTION</span></span>
<span data-ttu-id="366d8-106">A **Remove-AzApplicationGatewayHttpListener** parancsmag eltávolítja a HTTP-szolgáltatásokat egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="366d8-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="366d8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="366d8-107">EXAMPLES</span></span>

### <span data-ttu-id="366d8-108">1. példa: Alkalmazás-átjáró HTTP-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="366d8-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="366d8-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="366d8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="366d8-110">A második parancs eltávolítja a "Listener02" NEVŰ HTTP-hallgatót a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="366d8-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="366d8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="366d8-111">PARAMETERS</span></span>

### <span data-ttu-id="366d8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="366d8-112">-ApplicationGateway</span></span>
<span data-ttu-id="366d8-113">Azt az alkalmazás-átjárót adja meg, amelyről el szeretné távolítani a HTTP-et.</span><span class="sxs-lookup"><span data-stu-id="366d8-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="366d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366d8-114">-DefaultProfile</span></span>
<span data-ttu-id="366d8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="366d8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="366d8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="366d8-116">-Name</span></span>
<span data-ttu-id="366d8-117">A parancsmag által eltávolított HTTP-hallgató nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="366d8-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="366d8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366d8-118">CommonParameters</span></span>
<span data-ttu-id="366d8-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366d8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366d8-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="366d8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366d8-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="366d8-121">INPUTS</span></span>

### <span data-ttu-id="366d8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="366d8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="366d8-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="366d8-123">OUTPUTS</span></span>

### <span data-ttu-id="366d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="366d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="366d8-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="366d8-125">NOTES</span></span>

## <span data-ttu-id="366d8-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="366d8-126">RELATED LINKS</span></span>

[<span data-ttu-id="366d8-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="366d8-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="366d8-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="366d8-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="366d8-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="366d8-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="366d8-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="366d8-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


