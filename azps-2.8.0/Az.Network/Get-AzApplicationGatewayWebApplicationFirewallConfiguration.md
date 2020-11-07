---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: e2f477aa657bc4d21a650edffb7f014ae3c1ba62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837621"
---
# <span data-ttu-id="5ecef-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ecef-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="5ecef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ecef-102">SYNOPSIS</span></span>
<span data-ttu-id="5ecef-103">Az WAF konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="5ecef-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="5ecef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ecef-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ecef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ecef-105">DESCRIPTION</span></span>
<span data-ttu-id="5ecef-106">A **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag az WAF webalkalmazás-tűzfal () konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ecef-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="5ecef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ecef-107">EXAMPLES</span></span>

### <span data-ttu-id="5ecef-108">1. példa: alkalmazás-átjáró webalkalmazás-tűzfal konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5ecef-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="5ecef-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd a $AppGW változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ecef-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="5ecef-110">A második parancs beolvassa az $AppGW alkalmazás-átjáró tűzfal-konfigurációját, majd a $FirewallConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ecef-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="5ecef-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ecef-111">PARAMETERS</span></span>

### <span data-ttu-id="5ecef-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ecef-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ecef-113">Egy Application Gateway-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ecef-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="5ecef-114">Az Get-AzApplicationGateway parancsmag használatával beszerezhet egy Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="5ecef-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="5ecef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ecef-115">-DefaultProfile</span></span>
<span data-ttu-id="5ecef-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ecef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ecef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ecef-117">CommonParameters</span></span>
<span data-ttu-id="5ecef-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ecef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ecef-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ecef-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ecef-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ecef-120">INPUTS</span></span>

### <span data-ttu-id="5ecef-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ecef-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ecef-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ecef-122">OUTPUTS</span></span>

### <span data-ttu-id="5ecef-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ecef-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="5ecef-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ecef-124">NOTES</span></span>

## <span data-ttu-id="5ecef-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ecef-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ecef-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ecef-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="5ecef-127">Új – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ecef-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="5ecef-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ecef-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


