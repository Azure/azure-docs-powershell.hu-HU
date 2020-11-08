---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186093"
---
# <span data-ttu-id="a3618-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3618-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="a3618-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3618-102">SYNOPSIS</span></span>
<span data-ttu-id="a3618-103">Az előtér IP-konfigurációjának eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="a3618-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="a3618-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3618-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3618-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3618-105">DESCRIPTION</span></span>
<span data-ttu-id="a3618-106">A **Remove-AzApplicationGatewayFrontendIPConfig** parancsmag az Azure Application Gateway-ből eltávolítja az IP-felületet.</span><span class="sxs-lookup"><span data-stu-id="a3618-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="a3618-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a3618-107">EXAMPLES</span></span>

### <span data-ttu-id="a3618-108">Példa 1: előtér IP-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3618-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="a3618-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a3618-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3618-110">A második parancs eltávolítja a FrontEndIP02 nevű előtér-IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="a3618-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a3618-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3618-111">PARAMETERS</span></span>

### <span data-ttu-id="a3618-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3618-112">-ApplicationGateway</span></span>
<span data-ttu-id="a3618-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a3618-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3618-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3618-114">-DefaultProfile</span></span>
<span data-ttu-id="a3618-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3618-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3618-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3618-116">-Name</span></span>
<span data-ttu-id="a3618-117">Az eltávolítandó előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3618-117">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3618-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3618-118">CommonParameters</span></span>
<span data-ttu-id="a3618-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3618-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3618-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3618-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3618-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3618-121">INPUTS</span></span>

### <span data-ttu-id="a3618-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3618-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3618-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3618-123">OUTPUTS</span></span>

### <span data-ttu-id="a3618-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3618-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3618-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3618-125">NOTES</span></span>

## <span data-ttu-id="a3618-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3618-126">RELATED LINKS</span></span>

[<span data-ttu-id="a3618-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3618-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3618-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3618-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3618-129">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3618-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a3618-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a3618-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


