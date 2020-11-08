---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184110"
---
# <span data-ttu-id="f45b1-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f45b1-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f45b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f45b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f45b1-103">IP-konfiguráció eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="f45b1-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="f45b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f45b1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f45b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f45b1-106">A **Remove-AzApplicationGatewayIPConfiguration** parancsmag az Azure Application Gateway-ből távolítja el az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f45b1-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="f45b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f45b1-107">EXAMPLES</span></span>

### <span data-ttu-id="f45b1-108">Példa 1: IP-konfiguráció eltávolítása Azure Application Gateway-ből</span><span class="sxs-lookup"><span data-stu-id="f45b1-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="f45b1-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f45b1-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f45b1-110">A második parancs eltávolítja a Subnet02 nevű IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="f45b1-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f45b1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f45b1-111">PARAMETERS</span></span>

### <span data-ttu-id="f45b1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f45b1-112">-ApplicationGateway</span></span>
<span data-ttu-id="f45b1-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f45b1-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="f45b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45b1-114">-DefaultProfile</span></span>
<span data-ttu-id="f45b1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f45b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f45b1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f45b1-116">-Name</span></span>
<span data-ttu-id="f45b1-117">Az eltávolítandó IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f45b1-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="f45b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45b1-118">CommonParameters</span></span>
<span data-ttu-id="f45b1-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f45b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45b1-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45b1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45b1-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f45b1-121">INPUTS</span></span>

### <span data-ttu-id="f45b1-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f45b1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f45b1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f45b1-123">OUTPUTS</span></span>

### <span data-ttu-id="f45b1-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f45b1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f45b1-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f45b1-125">NOTES</span></span>

## <span data-ttu-id="f45b1-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f45b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="f45b1-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f45b1-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f45b1-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f45b1-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f45b1-129">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f45b1-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f45b1-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f45b1-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


