---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025163"
---
# <span data-ttu-id="9bb22-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9bb22-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="9bb22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bb22-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb22-103">Eltávolítja az előtér-portot egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="9bb22-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="9bb22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bb22-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bb22-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bb22-105">DESCRIPTION</span></span>
<span data-ttu-id="9bb22-106">A **Remove-AzApplicationGatewayFrontendPort** parancsmag eltávolítja az előtér-portot egy Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="9bb22-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="9bb22-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9bb22-107">EXAMPLES</span></span>

### <span data-ttu-id="9bb22-108">Példa: az előtér-port eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="9bb22-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="9bb22-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és az átjárót az $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9bb22-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="9bb22-110">A második parancs eltávolítja a FrontEndPort02 nevű portot az Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="9bb22-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="9bb22-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bb22-111">PARAMETERS</span></span>

### <span data-ttu-id="9bb22-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bb22-112">-ApplicationGateway</span></span>
<span data-ttu-id="9bb22-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér-portot.</span><span class="sxs-lookup"><span data-stu-id="9bb22-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="9bb22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb22-114">-DefaultProfile</span></span>
<span data-ttu-id="9bb22-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bb22-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bb22-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9bb22-116">-Name</span></span>
<span data-ttu-id="9bb22-117">Az eltávolítandó frontend-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9bb22-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="9bb22-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb22-118">CommonParameters</span></span>
<span data-ttu-id="9bb22-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bb22-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb22-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb22-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb22-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bb22-121">INPUTS</span></span>

### <span data-ttu-id="9bb22-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bb22-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9bb22-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bb22-123">OUTPUTS</span></span>

### <span data-ttu-id="9bb22-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bb22-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9bb22-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bb22-125">NOTES</span></span>

## <span data-ttu-id="9bb22-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bb22-126">RELATED LINKS</span></span>

[<span data-ttu-id="9bb22-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9bb22-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9bb22-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9bb22-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9bb22-129">Új – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9bb22-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9bb22-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9bb22-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


