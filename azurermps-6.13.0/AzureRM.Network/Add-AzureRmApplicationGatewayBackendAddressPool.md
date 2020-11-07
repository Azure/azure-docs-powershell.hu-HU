---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 29e127d974b6c7ef0bdf0272c16c036f69e53428
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679543"
---
# <span data-ttu-id="3abbd-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3abbd-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="3abbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3abbd-102">SYNOPSIS</span></span>
<span data-ttu-id="3abbd-103">Egy végponti címkészletet ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3abbd-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3abbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3abbd-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3abbd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3abbd-105">DESCRIPTION</span></span>
<span data-ttu-id="3abbd-106">A **Add-AzureRmApplicationGatewayBackendAddressPool** parancsmag az alkalmazás-átjáróhoz ad hozzá egy háttér-végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="3abbd-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="3abbd-107">A végpontok címe megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs azonosítók használatával.</span><span class="sxs-lookup"><span data-stu-id="3abbd-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="3abbd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3abbd-108">EXAMPLES</span></span>

### <span data-ttu-id="3abbd-109">1. példa: back-end-Címkészlet hozzáadása a back-end Server FQDN használatával</span><span class="sxs-lookup"><span data-stu-id="3abbd-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="3abbd-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs a teljes tartománynevek segítségével felveszi az $AppGw tárolt, a teljes tartománynevet.</span><span class="sxs-lookup"><span data-stu-id="3abbd-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="3abbd-111">2. példa: back-end-Címkészlet hozzáadása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="3abbd-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="3abbd-112">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs hozzáadja az $AppGwban tárolt, az IP-címekkel ellátott, az alkalmazás átjárójának végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="3abbd-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="3abbd-113">Példa 3: seta back-end Address Pool a backend-kiszolgáló IP-címének azonosítójával</span><span class="sxs-lookup"><span data-stu-id="3abbd-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="3abbd-114">Az első parancs beolvassa a Nic01 nevű hálózati kapcsolat objektumát, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $Nic 01 változóban tárolja. A második parancs beolvassa a Nic02 nevű hálózati kapcsolat objektumát, amely a ResourceGroup02 nevű erőforráscsoport csoportjába tartozik, és a $Nic 02 változóban tárolja. A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevű erőforrás csoportba, és a $AppGw változóban tárolja. A Forth parancs a $Nic 01 és az $Nic 02 végponti IP-konfigurációs azonosítóit használja a $AppGwban tárolt alkalmazás-átjáró végpont-címkészlet hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="3abbd-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3abbd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3abbd-115">PARAMETERS</span></span>

### <span data-ttu-id="3abbd-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3abbd-116">-ApplicationGateway</span></span>
<span data-ttu-id="3abbd-117">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a back-end címkészletet adja.</span><span class="sxs-lookup"><span data-stu-id="3abbd-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="3abbd-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="3abbd-118">-BackendFqdns</span></span>
<span data-ttu-id="3abbd-119">A backend-kiszolgálók készlete, amelyet a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="3abbd-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="3abbd-120">-BackendIPAddresses</span></span>
<span data-ttu-id="3abbd-121">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="3abbd-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3abbd-122">-DefaultProfile</span></span>
<span data-ttu-id="3abbd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3abbd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3abbd-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3abbd-124">-Name</span></span>
<span data-ttu-id="3abbd-125">Annak a végfelhasználói készletnek a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="3abbd-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3abbd-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3abbd-126">-Confirm</span></span>
<span data-ttu-id="3abbd-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3abbd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3abbd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3abbd-128">-WhatIf</span></span>
<span data-ttu-id="3abbd-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3abbd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3abbd-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3abbd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3abbd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3abbd-131">CommonParameters</span></span>
<span data-ttu-id="3abbd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3abbd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3abbd-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3abbd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3abbd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3abbd-134">INPUTS</span></span>

### <span data-ttu-id="3abbd-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3abbd-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="3abbd-136">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3abbd-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="3abbd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3abbd-137">OUTPUTS</span></span>

### <span data-ttu-id="3abbd-138">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3abbd-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3abbd-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3abbd-139">NOTES</span></span>

## <span data-ttu-id="3abbd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3abbd-140">RELATED LINKS</span></span>

[<span data-ttu-id="3abbd-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3abbd-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3abbd-142">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3abbd-142">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3abbd-143">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3abbd-143">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3abbd-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3abbd-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3abbd-145">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3abbd-145">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


