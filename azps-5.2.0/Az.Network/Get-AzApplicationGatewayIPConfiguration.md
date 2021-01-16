---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326266"
---
# <span data-ttu-id="395ec-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="395ec-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="395ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395ec-102">SYNOPSIS</span></span>
<span data-ttu-id="395ec-103">Egy alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="395ec-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="395ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="395ec-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="395ec-105">DESCRIPTION</span></span>
<span data-ttu-id="395ec-106">A **Get-AzApplicationGatewayIPConfiguration** parancsmag egy alkalmazás-átjáró IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="395ec-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="395ec-107">Az IP-konfiguráció tartalmazza azt az alhálózatot, amelyen az alkalmazás-átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="395ec-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="395ec-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="395ec-108">EXAMPLES</span></span>

### <span data-ttu-id="395ec-109">1. példa: Adott IP-konfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="395ec-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="395ec-110">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja. A második parancs egy GateSubnet01 nevű IP-konfigurációt kap a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="395ec-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="395ec-111">2. példa: IP-konfigurációk listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="395ec-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="395ec-112">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja. A második parancs az összes IP-konfiguráció listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="395ec-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="395ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="395ec-113">PARAMETERS</span></span>

### <span data-ttu-id="395ec-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="395ec-114">-ApplicationGateway</span></span>
<span data-ttu-id="395ec-115">Az IP-konfigurációt tartalmazó alkalmazás-átjáróobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="395ec-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="395ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395ec-116">-DefaultProfile</span></span>
<span data-ttu-id="395ec-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="395ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="395ec-118">-Name</span><span class="sxs-lookup"><span data-stu-id="395ec-118">-Name</span></span>
<span data-ttu-id="395ec-119">Annak az IP-konfigurációnak a nevét adja meg, amelyet ez a parancsmag kap.</span><span class="sxs-lookup"><span data-stu-id="395ec-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="395ec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395ec-120">CommonParameters</span></span>
<span data-ttu-id="395ec-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395ec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395ec-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="395ec-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395ec-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="395ec-123">INPUTS</span></span>

### <span data-ttu-id="395ec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="395ec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="395ec-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="395ec-125">OUTPUTS</span></span>

### <span data-ttu-id="395ec-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="395ec-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="395ec-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="395ec-127">NOTES</span></span>

## <span data-ttu-id="395ec-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="395ec-128">RELATED LINKS</span></span>

[<span data-ttu-id="395ec-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="395ec-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="395ec-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="395ec-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="395ec-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="395ec-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="395ec-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="395ec-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


