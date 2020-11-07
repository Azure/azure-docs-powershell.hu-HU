---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 80248749772bdcfc26bbbc633bbb4919531462be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837131"
---
# <span data-ttu-id="14f78-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14f78-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="14f78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14f78-102">SYNOPSIS</span></span>
<span data-ttu-id="14f78-103">IP-konfiguráció eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="14f78-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="14f78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14f78-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14f78-105">DESCRIPTION</span></span>
<span data-ttu-id="14f78-106">A **Remove-AzApplicationGatewayIPConfiguration** parancsmag az Azure Application Gateway-ből távolítja el az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="14f78-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="14f78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14f78-107">EXAMPLES</span></span>

### <span data-ttu-id="14f78-108">Példa 1: IP-konfiguráció eltávolítása Azure Application Gateway-ből</span><span class="sxs-lookup"><span data-stu-id="14f78-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="14f78-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="14f78-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="14f78-110">A második parancs eltávolítja a Subnet02 nevű IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="14f78-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="14f78-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14f78-111">PARAMETERS</span></span>

### <span data-ttu-id="14f78-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14f78-112">-ApplicationGateway</span></span>
<span data-ttu-id="14f78-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="14f78-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="14f78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f78-114">-DefaultProfile</span></span>
<span data-ttu-id="14f78-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14f78-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f78-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14f78-116">-Name</span></span>
<span data-ttu-id="14f78-117">Az eltávolítandó IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14f78-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="14f78-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f78-118">CommonParameters</span></span>
<span data-ttu-id="14f78-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14f78-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f78-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f78-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f78-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14f78-121">INPUTS</span></span>

### <span data-ttu-id="14f78-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14f78-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14f78-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14f78-123">OUTPUTS</span></span>

### <span data-ttu-id="14f78-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14f78-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14f78-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14f78-125">NOTES</span></span>

## <span data-ttu-id="14f78-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14f78-126">RELATED LINKS</span></span>

[<span data-ttu-id="14f78-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14f78-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="14f78-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14f78-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="14f78-129">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14f78-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="14f78-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14f78-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


