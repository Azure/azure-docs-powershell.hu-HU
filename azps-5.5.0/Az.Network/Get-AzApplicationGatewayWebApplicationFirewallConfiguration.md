---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203113"
---
# <span data-ttu-id="cebad-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebad-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="cebad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cebad-102">SYNOPSIS</span></span>
<span data-ttu-id="cebad-103">Egy alkalmazás-átjáró waf-konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="cebad-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="cebad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cebad-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cebad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cebad-105">DESCRIPTION</span></span>
<span data-ttu-id="cebad-106">A **Get-AzApplicationGatewayWebApplicationFirewallConfiguration parancsmag** egy alkalmazás-átjáró webalkalmazás tűzfalának (WAF) konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cebad-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="cebad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cebad-107">EXAMPLES</span></span>

### <span data-ttu-id="cebad-108">1. példa: Alkalmazásátjáró webalkalmazás tűzfalának beállítása</span><span class="sxs-lookup"><span data-stu-id="cebad-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="cebad-109">Az első parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, majd tárolja azt a $AppGW változóban.</span><span class="sxs-lookup"><span data-stu-id="cebad-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="cebad-110">A második parancs az alkalmazás átjárójának tűzfalkonfigurációját kapja $AppGW, majd tárolja $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="cebad-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="cebad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cebad-111">PARAMETERS</span></span>

### <span data-ttu-id="cebad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cebad-112">-ApplicationGateway</span></span>
<span data-ttu-id="cebad-113">Egy alkalmazás-átjáróobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cebad-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="cebad-114">A Get-AzApplicationGateway parancsmag használatával lekért egy alkalmazás-átjáróobjektumot.</span><span class="sxs-lookup"><span data-stu-id="cebad-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="cebad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebad-115">-DefaultProfile</span></span>
<span data-ttu-id="cebad-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cebad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cebad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebad-117">CommonParameters</span></span>
<span data-ttu-id="cebad-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebad-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cebad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebad-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cebad-120">INPUTS</span></span>

### <span data-ttu-id="cebad-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cebad-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cebad-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cebad-122">OUTPUTS</span></span>

### <span data-ttu-id="cebad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="cebad-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cebad-124">NOTES</span></span>

## <span data-ttu-id="cebad-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cebad-125">RELATED LINKS</span></span>

[<span data-ttu-id="cebad-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cebad-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="cebad-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebad-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="cebad-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebad-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


