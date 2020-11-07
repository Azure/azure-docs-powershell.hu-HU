---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 16df8726fc0018bbc89dfbee025223b9e35792c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837630"
---
# <span data-ttu-id="a0ed4-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ed4-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="a0ed4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ed4-103">Az alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="a0ed4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0ed4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0ed4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ed4-106">A **Get-AzApplicationGatewayIPConfiguration** parancsmag az alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="a0ed4-107">Az IP-konfiguráció azt az alhálózatot tartalmazza, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="a0ed4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a0ed4-108">EXAMPLES</span></span>

### <span data-ttu-id="a0ed4-109">1. példa: meghatározott IP-konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0ed4-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a0ed4-110">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs beolvassa a GateSubnet01 nevű IP-konfigurációt az $AppGw-ban tárolt átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="a0ed4-111">2. példa: az IP-konfigurációk listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0ed4-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="a0ed4-112">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs a teljes IP-konfigurációk listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="a0ed4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0ed4-113">PARAMETERS</span></span>

### <span data-ttu-id="a0ed4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0ed4-114">-ApplicationGateway</span></span>
<span data-ttu-id="a0ed4-115">Az IP-konfigurációt tartalmazó Application Gateway-objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="a0ed4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ed4-116">-DefaultProfile</span></span>
<span data-ttu-id="a0ed4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0ed4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0ed4-118">-Name</span></span>
<span data-ttu-id="a0ed4-119">Itt adhatja meg annak az IP-konfigurációnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0ed4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ed4-120">CommonParameters</span></span>
<span data-ttu-id="a0ed4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0ed4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ed4-122">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0ed4-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ed4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0ed4-123">INPUTS</span></span>

### <span data-ttu-id="a0ed4-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0ed4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0ed4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0ed4-125">OUTPUTS</span></span>

### <span data-ttu-id="a0ed4-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ed4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="a0ed4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0ed4-127">NOTES</span></span>

## <span data-ttu-id="a0ed4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0ed4-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0ed4-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ed4-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a0ed4-130">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ed4-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a0ed4-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ed4-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a0ed4-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ed4-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


