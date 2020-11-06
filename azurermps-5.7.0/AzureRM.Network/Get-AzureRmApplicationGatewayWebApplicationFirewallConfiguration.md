---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 44411d8f763e217d5513440a90f713c92c6d6398
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499776"
---
# <span data-ttu-id="3a430-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a430-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="3a430-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a430-102">SYNOPSIS</span></span>
<span data-ttu-id="3a430-103">Az WAF konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="3a430-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a430-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a430-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a430-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a430-105">DESCRIPTION</span></span>
<span data-ttu-id="3a430-106">A **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** parancsmag az WAF webalkalmazás-tűzfal () konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a430-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="3a430-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a430-107">EXAMPLES</span></span>

### <span data-ttu-id="3a430-108">1. példa: alkalmazás-átjáró webalkalmazás-tűzfal konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a430-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="3a430-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd a $AppGW változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3a430-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="3a430-110">A második parancs beolvassa az $AppGW alkalmazás-átjáró tűzfal-konfigurációját, majd a $FirewallConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="3a430-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="3a430-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a430-111">PARAMETERS</span></span>

### <span data-ttu-id="3a430-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a430-112">-ApplicationGateway</span></span>
<span data-ttu-id="3a430-113">Egy Application Gateway-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3a430-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="3a430-114">Az Get-AzureRmApplicationGateway parancsmag használatával beszerezhet egy Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="3a430-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="3a430-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a430-115">-DefaultProfile</span></span>
<span data-ttu-id="3a430-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a430-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a430-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a430-117">CommonParameters</span></span>
<span data-ttu-id="3a430-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a430-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a430-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a430-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a430-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a430-120">INPUTS</span></span>

### <span data-ttu-id="3a430-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a430-121">PSApplicationGateway</span></span>
<span data-ttu-id="3a430-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3a430-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="3a430-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a430-123">OUTPUTS</span></span>

### <span data-ttu-id="3a430-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a430-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="3a430-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a430-125">NOTES</span></span>

## <span data-ttu-id="3a430-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a430-126">RELATED LINKS</span></span>

[<span data-ttu-id="3a430-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a430-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="3a430-128">Új – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a430-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="3a430-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a430-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


