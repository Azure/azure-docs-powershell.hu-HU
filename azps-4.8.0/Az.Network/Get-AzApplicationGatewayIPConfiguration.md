---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182510"
---
# <span data-ttu-id="0e783-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e783-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="0e783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e783-102">SYNOPSIS</span></span>
<span data-ttu-id="0e783-103">Az alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e783-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="0e783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e783-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e783-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e783-105">DESCRIPTION</span></span>
<span data-ttu-id="0e783-106">A **Get-AzApplicationGatewayIPConfiguration** parancsmag az alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e783-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="0e783-107">Az IP-konfiguráció azt az alhálózatot tartalmazza, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="0e783-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="0e783-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0e783-108">EXAMPLES</span></span>

### <span data-ttu-id="0e783-109">1. példa: meghatározott IP-konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e783-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="0e783-110">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs beolvassa a GateSubnet01 nevű IP-konfigurációt az $AppGw-ban tárolt átjáróból.</span><span class="sxs-lookup"><span data-stu-id="0e783-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="0e783-111">2. példa: az IP-konfigurációk listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e783-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="0e783-112">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs a teljes IP-konfigurációk listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="0e783-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="0e783-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e783-113">PARAMETERS</span></span>

### <span data-ttu-id="0e783-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e783-114">-ApplicationGateway</span></span>
<span data-ttu-id="0e783-115">Az IP-konfigurációt tartalmazó Application Gateway-objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="0e783-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="0e783-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e783-116">-DefaultProfile</span></span>
<span data-ttu-id="0e783-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e783-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e783-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e783-118">-Name</span></span>
<span data-ttu-id="0e783-119">Itt adhatja meg annak az IP-konfigurációnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="0e783-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e783-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e783-120">CommonParameters</span></span>
<span data-ttu-id="0e783-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e783-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e783-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e783-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e783-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e783-123">INPUTS</span></span>

### <span data-ttu-id="0e783-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e783-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e783-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e783-125">OUTPUTS</span></span>

### <span data-ttu-id="0e783-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e783-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="0e783-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e783-127">NOTES</span></span>

## <span data-ttu-id="0e783-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e783-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e783-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e783-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0e783-130">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e783-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0e783-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e783-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0e783-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e783-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


