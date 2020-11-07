---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5b41cedc02818db6c309e3c11bb1797fb6525d75
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845965"
---
# <span data-ttu-id="b8b0b-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8b0b-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b8b0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b0b-103">Egy végponti címkészletet ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="b8b0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8b0b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b0b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b0b-106">A **Add-AzApplicationGatewayBackendAddressPool** parancsmag az alkalmazás-átjáróhoz ad hozzá egy háttér-végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="b8b0b-107">A végpontok címe megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs azonosítók használatával.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="b8b0b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b8b0b-108">EXAMPLES</span></span>

### <span data-ttu-id="b8b0b-109">1. példa: back-end-Címkészlet hozzáadása a back-end Server FQDN használatával</span><span class="sxs-lookup"><span data-stu-id="b8b0b-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="b8b0b-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs a teljes tartománynevek segítségével felveszi az $AppGw tárolt, a teljes tartománynevet.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="b8b0b-111">2. példa: back-end-Címkészlet hozzáadása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="b8b0b-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="b8b0b-112">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs hozzáadja az $AppGwban tárolt, az IP-címekkel ellátott, az alkalmazás átjárójának végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="b8b0b-113">Példa 3: seta back-end Address Pool a backend-kiszolgáló IP-címének azonosítójával</span><span class="sxs-lookup"><span data-stu-id="b8b0b-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="b8b0b-114">Az első parancs beolvassa a Nic01 nevű hálózati kapcsolat objektumát, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $Nic 01 változóban tárolja. A második parancs beolvassa a Nic02 nevű hálózati kapcsolat objektumát, amely a ResourceGroup02 nevű erőforráscsoport csoportjába tartozik, és a $Nic 02 változóban tárolja. A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevű erőforrás csoportba, és a $AppGw változóban tárolja. A Forth parancs a $Nic 01 és az $Nic 02 végponti IP-konfigurációs azonosítóit használja a $AppGwban tárolt alkalmazás-átjáró végpont-címkészlet hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b8b0b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8b0b-115">PARAMETERS</span></span>

### <span data-ttu-id="b8b0b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8b0b-116">-ApplicationGateway</span></span>
<span data-ttu-id="b8b0b-117">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a back-end címkészletet adja.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="b8b0b-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="b8b0b-118">-BackendFqdns</span></span>
<span data-ttu-id="b8b0b-119">A backend-kiszolgálók készlete, amelyet a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b0b-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="b8b0b-120">-BackendIPAddresses</span></span>
<span data-ttu-id="b8b0b-121">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b0b-122">-DefaultProfile</span></span>
<span data-ttu-id="b8b0b-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8b0b-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8b0b-124">-Name</span></span>
<span data-ttu-id="b8b0b-125">Annak a végfelhasználói készletnek a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b8b0b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8b0b-126">-Confirm</span></span>
<span data-ttu-id="b8b0b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b0b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b0b-128">-WhatIf</span></span>
<span data-ttu-id="b8b0b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b0b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8b0b-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b0b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b0b-131">CommonParameters</span></span>
<span data-ttu-id="b8b0b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8b0b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b0b-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b0b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b0b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8b0b-134">INPUTS</span></span>

### <span data-ttu-id="b8b0b-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8b0b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8b0b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8b0b-136">OUTPUTS</span></span>

### <span data-ttu-id="b8b0b-137">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8b0b-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8b0b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8b0b-138">NOTES</span></span>

## <span data-ttu-id="b8b0b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8b0b-139">RELATED LINKS</span></span>

[<span data-ttu-id="b8b0b-140">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8b0b-140">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b8b0b-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8b0b-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b8b0b-142">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8b0b-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b8b0b-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8b0b-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b8b0b-144">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8b0b-144">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


