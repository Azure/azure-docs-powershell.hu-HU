---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: de99be99c7b393af6cbbcac8ad9d293c93f4d5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493636"
---
# <span data-ttu-id="13ec9-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="13ec9-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="13ec9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="13ec9-103">Eltávolítja az előtér-portot egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="13ec9-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ec9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13ec9-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ec9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="13ec9-106">A **Remove-AzureRmApplicationGatewayFrontendPort** parancsmag eltávolítja az előtér-portot egy Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="13ec9-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="13ec9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="13ec9-108">Példa: az előtér-port eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="13ec9-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="13ec9-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és az átjárót az $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="13ec9-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="13ec9-110">A második parancs eltávolítja a FrontEndPort02 nevű portot az Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="13ec9-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="13ec9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13ec9-111">PARAMETERS</span></span>

### <span data-ttu-id="13ec9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ec9-112">-ApplicationGateway</span></span>
<span data-ttu-id="13ec9-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér-portot.</span><span class="sxs-lookup"><span data-stu-id="13ec9-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="13ec9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ec9-114">-DefaultProfile</span></span>
<span data-ttu-id="13ec9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13ec9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13ec9-116">-Name</span></span>
<span data-ttu-id="13ec9-117">Az eltávolítandó frontend-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec9-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="13ec9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ec9-118">CommonParameters</span></span>
<span data-ttu-id="13ec9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13ec9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ec9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ec9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ec9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ec9-121">INPUTS</span></span>

### <span data-ttu-id="13ec9-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ec9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="13ec9-123">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13ec9-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="13ec9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ec9-124">OUTPUTS</span></span>

### <span data-ttu-id="13ec9-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ec9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13ec9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13ec9-126">NOTES</span></span>

## <span data-ttu-id="13ec9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13ec9-127">RELATED LINKS</span></span>

[<span data-ttu-id="13ec9-128">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="13ec9-128">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="13ec9-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="13ec9-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="13ec9-130">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="13ec9-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="13ec9-131">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="13ec9-131">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


