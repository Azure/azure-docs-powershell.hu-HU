---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: cab20e2b92343549b5138f14f88505c70624effb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941761"
---
# <span data-ttu-id="41110-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="41110-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="41110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41110-102">SYNOPSIS</span></span>
<span data-ttu-id="41110-103">Egy alkalmazás-átjáró előlapi IP-konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="41110-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="41110-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41110-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41110-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41110-105">DESCRIPTION</span></span>
<span data-ttu-id="41110-106">A **Get-AzApplicationGatewayFrontendIPConfig** parancsmag egy alkalmazás-átjáró előtér-IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41110-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="41110-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41110-107">EXAMPLES</span></span>

### <span data-ttu-id="41110-108">1. példa: Az előlapi IP-címek megadott konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="41110-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="41110-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja. A második parancs a FrontEndIP01 nevű előlapi IP-konfigurációt $AppGw és tárolja a $FrontEndIP változóban.</span><span class="sxs-lookup"><span data-stu-id="41110-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="41110-110">2. példa: Előlapi IP-konfigurációk listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="41110-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="41110-111">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja. A második parancs az előlapi IP-konfigurációk listáját $AppGw a $FrontEndIPs tárolja.</span><span class="sxs-lookup"><span data-stu-id="41110-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="41110-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41110-112">PARAMETERS</span></span>

### <span data-ttu-id="41110-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41110-113">-ApplicationGateway</span></span>
<span data-ttu-id="41110-114">Megadja az előlapi IP-konfigurációt tartalmazó alkalmazás átjáróobjektumát.</span><span class="sxs-lookup"><span data-stu-id="41110-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="41110-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41110-115">-DefaultProfile</span></span>
<span data-ttu-id="41110-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41110-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41110-117">-Name</span><span class="sxs-lookup"><span data-stu-id="41110-117">-Name</span></span>
<span data-ttu-id="41110-118">A parancsmag előlapi IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41110-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41110-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41110-119">CommonParameters</span></span>
<span data-ttu-id="41110-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41110-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41110-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41110-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41110-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41110-122">INPUTS</span></span>

### <span data-ttu-id="41110-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41110-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41110-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41110-124">OUTPUTS</span></span>

### <span data-ttu-id="41110-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="41110-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="41110-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41110-126">NOTES</span></span>

## <span data-ttu-id="41110-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41110-127">RELATED LINKS</span></span>

[<span data-ttu-id="41110-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="41110-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="41110-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="41110-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="41110-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="41110-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="41110-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="41110-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


