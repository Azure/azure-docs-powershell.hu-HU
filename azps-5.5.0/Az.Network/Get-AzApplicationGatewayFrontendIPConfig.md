---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203164"
---
# <span data-ttu-id="2eca0-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2eca0-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="2eca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eca0-102">SYNOPSIS</span></span>
<span data-ttu-id="2eca0-103">Egy alkalmazás átjárójának előlapi IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2eca0-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="2eca0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2eca0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eca0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2eca0-105">DESCRIPTION</span></span>
<span data-ttu-id="2eca0-106">A **Get-AzApplicationGatewayFrontendIPConfig** parancsmag egy alkalmazás-átjáró előtér-IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2eca0-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="2eca0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2eca0-107">EXAMPLES</span></span>

### <span data-ttu-id="2eca0-108">1. példa: A megadott előlapi IP-konfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="2eca0-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="2eca0-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja. A második parancs a FrontEndIP01 nevű előlapi IP-konfigurációt kapja $AppGw és tárolja a $FrontEndIP változóban.</span><span class="sxs-lookup"><span data-stu-id="2eca0-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="2eca0-110">2. példa: Előlapi IP-konfigurációk listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="2eca0-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="2eca0-111">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja. A második parancs az előlapi IP-konfigurációk listáját $AppGw a $FrontEndIPs tárolja.</span><span class="sxs-lookup"><span data-stu-id="2eca0-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="2eca0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eca0-112">PARAMETERS</span></span>

### <span data-ttu-id="2eca0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2eca0-113">-ApplicationGateway</span></span>
<span data-ttu-id="2eca0-114">Az előlapi IP-konfigurációt tartalmazó alkalmazás átjáróobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2eca0-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="2eca0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eca0-115">-DefaultProfile</span></span>
<span data-ttu-id="2eca0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eca0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eca0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2eca0-117">-Name</span></span>
<span data-ttu-id="2eca0-118">A parancsmag előlapi IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2eca0-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2eca0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eca0-119">CommonParameters</span></span>
<span data-ttu-id="2eca0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eca0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eca0-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eca0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eca0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eca0-122">INPUTS</span></span>

### <span data-ttu-id="2eca0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2eca0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2eca0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eca0-124">OUTPUTS</span></span>

### <span data-ttu-id="2eca0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2eca0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="2eca0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2eca0-126">NOTES</span></span>

## <span data-ttu-id="2eca0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eca0-127">RELATED LINKS</span></span>

[<span data-ttu-id="2eca0-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2eca0-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2eca0-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2eca0-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2eca0-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2eca0-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2eca0-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2eca0-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


