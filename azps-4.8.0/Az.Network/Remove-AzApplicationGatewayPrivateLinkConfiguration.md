---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025156"
---
# <span data-ttu-id="c7df8-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7df8-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="c7df8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7df8-102">SYNOPSIS</span></span>
<span data-ttu-id="c7df8-103">PrivateLink-konfiguráció eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="c7df8-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="c7df8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7df8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7df8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7df8-105">DESCRIPTION</span></span>
<span data-ttu-id="c7df8-106">A **Remove-AzApplicationGatewayPrivateLinkConfiguration** parancsmag privateLink-konfigurációt távolít el egy Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="c7df8-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="c7df8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7df8-107">EXAMPLES</span></span>

### <span data-ttu-id="c7df8-108">1. példa: az alkalmazás-átjáró PrivateLink-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c7df8-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="c7df8-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c7df8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c7df8-110">A második parancs eltávolítja a privateLinkConfig01 nevű privateLink-konfigurációt a $AppGwban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="c7df8-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c7df8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7df8-111">PARAMETERS</span></span>

### <span data-ttu-id="c7df8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7df8-112">-ApplicationGateway</span></span>
<span data-ttu-id="c7df8-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7df8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c7df8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7df8-114">-DefaultProfile</span></span>
<span data-ttu-id="c7df8-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7df8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7df8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7df8-116">-Name</span></span>
<span data-ttu-id="c7df8-117">Az Application Gateway privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="c7df8-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="c7df8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7df8-118">CommonParameters</span></span>
<span data-ttu-id="c7df8-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7df8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7df8-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c7df8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7df8-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7df8-121">INPUTS</span></span>

### <span data-ttu-id="c7df8-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7df8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7df8-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7df8-123">OUTPUTS</span></span>

### <span data-ttu-id="c7df8-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7df8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7df8-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7df8-125">NOTES</span></span>

## <span data-ttu-id="c7df8-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7df8-126">RELATED LINKS</span></span>

[<span data-ttu-id="c7df8-127">Új – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7df8-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c7df8-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7df8-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c7df8-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7df8-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c7df8-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7df8-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)