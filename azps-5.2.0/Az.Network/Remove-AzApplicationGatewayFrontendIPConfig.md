---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340698"
---
# <span data-ttu-id="d072c-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d072c-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="d072c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d072c-102">SYNOPSIS</span></span>
<span data-ttu-id="d072c-103">Eltávolítja az előlapi IP-konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="d072c-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="d072c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d072c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d072c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d072c-105">DESCRIPTION</span></span>
<span data-ttu-id="d072c-106">A **Remove-AzApplicationGatewayFrontendIPConfig** parancsmag eltávolítja a frontend IP-címet egy Azure-alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="d072c-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="d072c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d072c-107">EXAMPLES</span></span>

### <span data-ttu-id="d072c-108">1. példa: Előlapi IP-konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d072c-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="d072c-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, és azt a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="d072c-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d072c-110">A második parancs eltávolítja a FrontEndIP02 nevű előlapi IP-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d072c-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d072c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d072c-111">PARAMETERS</span></span>

### <span data-ttu-id="d072c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d072c-112">-ApplicationGateway</span></span>
<span data-ttu-id="d072c-113">Egy olyan alkalmazás átjárót ad meg, amelyből el szeretné távolítani az előlapi IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="d072c-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d072c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d072c-114">-DefaultProfile</span></span>
<span data-ttu-id="d072c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d072c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d072c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d072c-116">-Name</span></span>
<span data-ttu-id="d072c-117">Az eltávolítható előlapi IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d072c-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="d072c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d072c-118">CommonParameters</span></span>
<span data-ttu-id="d072c-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d072c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d072c-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d072c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d072c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d072c-121">INPUTS</span></span>

### <span data-ttu-id="d072c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d072c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d072c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d072c-123">OUTPUTS</span></span>

### <span data-ttu-id="d072c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d072c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d072c-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d072c-125">NOTES</span></span>

## <span data-ttu-id="d072c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d072c-126">RELATED LINKS</span></span>

[<span data-ttu-id="d072c-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d072c-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d072c-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d072c-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d072c-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d072c-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="d072c-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d072c-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


