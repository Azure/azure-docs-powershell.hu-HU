---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 8995c91484bba1c11944bf9d2a6e3dbc8ff5738d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504371"
---
# <span data-ttu-id="3972b-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3972b-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="3972b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3972b-102">SYNOPSIS</span></span>
<span data-ttu-id="3972b-103">Az alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3972b-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3972b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3972b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3972b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3972b-105">DESCRIPTION</span></span>
<span data-ttu-id="3972b-106">A **Get-AzureRmApplicationGatewayIPConfiguration** parancsmag az alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3972b-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="3972b-107">Az IP-konfiguráció azt az alhálózatot tartalmazza, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="3972b-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="3972b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3972b-108">EXAMPLES</span></span>

### <span data-ttu-id="3972b-109">1. példa: meghatározott IP-konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="3972b-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="3972b-110">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs beolvassa a GateSubnet01 nevű IP-konfigurációt az $AppGw-ban tárolt átjáróból.</span><span class="sxs-lookup"><span data-stu-id="3972b-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="3972b-111">2. példa: az IP-konfigurációk listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3972b-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="3972b-112">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs a teljes IP-konfigurációk listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="3972b-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="3972b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3972b-113">PARAMETERS</span></span>

### <span data-ttu-id="3972b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3972b-114">-ApplicationGateway</span></span>
<span data-ttu-id="3972b-115">Az IP-konfigurációt tartalmazó Application Gateway-objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="3972b-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="3972b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3972b-116">-DefaultProfile</span></span>
<span data-ttu-id="3972b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3972b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3972b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3972b-118">-Name</span></span>
<span data-ttu-id="3972b-119">Itt adhatja meg annak az IP-konfigurációnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="3972b-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="3972b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3972b-120">CommonParameters</span></span>
<span data-ttu-id="3972b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3972b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3972b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3972b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3972b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3972b-123">INPUTS</span></span>

### <span data-ttu-id="3972b-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3972b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="3972b-125">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3972b-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="3972b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3972b-126">OUTPUTS</span></span>

### <span data-ttu-id="3972b-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3972b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="3972b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3972b-128">NOTES</span></span>

## <span data-ttu-id="3972b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3972b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3972b-130">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3972b-130">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3972b-131">Új – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3972b-131">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3972b-132">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3972b-132">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3972b-133">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3972b-133">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)

