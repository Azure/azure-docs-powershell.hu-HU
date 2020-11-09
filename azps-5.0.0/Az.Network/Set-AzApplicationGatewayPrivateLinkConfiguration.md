---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303120"
---
# <span data-ttu-id="13659-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13659-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="13659-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13659-102">SYNOPSIS</span></span>
<span data-ttu-id="13659-103">Módosítja egy PrivateLink-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="13659-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="13659-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13659-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13659-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13659-105">DESCRIPTION</span></span>
<span data-ttu-id="13659-106">A **set-AzApplicationGatewayPrivateLinkConfiguration** parancsmag az Azure Application Gateway privateLink-konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="13659-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="13659-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13659-107">EXAMPLES</span></span>

### <span data-ttu-id="13659-108">1. példa: PrivateLink-konfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="13659-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="13659-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="13659-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="13659-110">A második parancs a privateLink konfigurációt a name privateLinkConfig01-ra állítja be, hogy az IP-konfigurációt használja az $privateLinkIpConfiguration 01-ben tárolva</span><span class="sxs-lookup"><span data-stu-id="13659-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="13659-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13659-111">PARAMETERS</span></span>

### <span data-ttu-id="13659-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13659-112">-ApplicationGateway</span></span>
<span data-ttu-id="13659-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="13659-113">The applicationGateway</span></span>

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

### <span data-ttu-id="13659-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13659-114">-DefaultProfile</span></span>
<span data-ttu-id="13659-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13659-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13659-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="13659-116">-IpConfiguration</span></span>
<span data-ttu-id="13659-117">A ipConfiguration listája</span><span class="sxs-lookup"><span data-stu-id="13659-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13659-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13659-118">-Name</span></span>
<span data-ttu-id="13659-119">A privateLink konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="13659-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="13659-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13659-120">-Confirm</span></span>
<span data-ttu-id="13659-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13659-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13659-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13659-122">-WhatIf</span></span>
<span data-ttu-id="13659-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13659-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13659-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13659-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13659-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13659-125">CommonParameters</span></span>
<span data-ttu-id="13659-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13659-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13659-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13659-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13659-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13659-128">INPUTS</span></span>

### <span data-ttu-id="13659-129">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13659-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="13659-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="13659-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="13659-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13659-131">OUTPUTS</span></span>

### <span data-ttu-id="13659-132">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13659-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13659-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13659-133">NOTES</span></span>

## <span data-ttu-id="13659-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13659-134">RELATED LINKS</span></span>

[<span data-ttu-id="13659-135">Új – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13659-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="13659-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13659-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="13659-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13659-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="13659-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="13659-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)