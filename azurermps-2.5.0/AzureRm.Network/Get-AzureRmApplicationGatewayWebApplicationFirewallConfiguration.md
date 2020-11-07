---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848462"
---
# <span data-ttu-id="f4cdb-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4cdb-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f4cdb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cdb-103">Az WAF konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4cdb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4cdb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4cdb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4cdb-105">DESCRIPTION</span></span>
<span data-ttu-id="f4cdb-106">A **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** parancsmag az WAF webalkalmazás-tűzfal () konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="f4cdb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4cdb-107">EXAMPLES</span></span>

### <span data-ttu-id="f4cdb-108">1. példa: alkalmazás-átjáró webalkalmazás-tűzfal konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f4cdb-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="f4cdb-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd a $AppGW változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="f4cdb-110">A második parancs beolvassa az $AppGW alkalmazás-átjáró tűzfal-konfigurációját, majd a $FirewallConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="f4cdb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4cdb-111">PARAMETERS</span></span>

### <span data-ttu-id="f4cdb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4cdb-112">-ApplicationGateway</span></span>
<span data-ttu-id="f4cdb-113">Egy Application Gateway-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="f4cdb-114">Az Get-AzureRmApplicationGateway parancsmag használatával beszerezhet egy Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="f4cdb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cdb-115">-DefaultProfile</span></span>
<span data-ttu-id="f4cdb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cdb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cdb-117">CommonParameters</span></span>
<span data-ttu-id="f4cdb-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4cdb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cdb-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4cdb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cdb-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4cdb-120">INPUTS</span></span>

### <span data-ttu-id="f4cdb-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4cdb-121">PSApplicationGateway</span></span>
<span data-ttu-id="f4cdb-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f4cdb-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f4cdb-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4cdb-123">OUTPUTS</span></span>

### <span data-ttu-id="f4cdb-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4cdb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f4cdb-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4cdb-125">NOTES</span></span>

## <span data-ttu-id="f4cdb-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4cdb-126">RELATED LINKS</span></span>

[<span data-ttu-id="f4cdb-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4cdb-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f4cdb-128">Új – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4cdb-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f4cdb-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4cdb-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


