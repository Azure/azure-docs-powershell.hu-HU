---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 6f22c8026d3b72a6c9cd52563252aa3d4bcad039
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849645"
---
# <span data-ttu-id="82be3-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82be3-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="82be3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82be3-102">SYNOPSIS</span></span>
<span data-ttu-id="82be3-103">Egy végponti címkészletet ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="82be3-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82be3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82be3-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82be3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82be3-105">DESCRIPTION</span></span>
<span data-ttu-id="82be3-106">A **Add-AzureRmApplicationGatewayBackendAddressPool** parancsmag az alkalmazás-átjáróhoz ad hozzá egy háttér-végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="82be3-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="82be3-107">A végpontok címe megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs azonosítók használatával.</span><span class="sxs-lookup"><span data-stu-id="82be3-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="82be3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="82be3-108">EXAMPLES</span></span>

### <span data-ttu-id="82be3-109">1. példa: back-end-Címkészlet hozzáadása a back-end Server FQDN használatával</span><span class="sxs-lookup"><span data-stu-id="82be3-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="82be3-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs a teljes tartománynevek segítségével felveszi az $AppGw tárolt, a teljes tartománynevet.</span><span class="sxs-lookup"><span data-stu-id="82be3-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="82be3-111">2. példa: back-end-Címkészlet hozzáadása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="82be3-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="82be3-112">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs hozzáadja az $AppGwban tárolt, az IP-címekkel ellátott, az alkalmazás átjárójának végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="82be3-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="82be3-113">Példa 3: seta back-end Address Pool a backend-kiszolgáló IP-címének azonosítójával</span><span class="sxs-lookup"><span data-stu-id="82be3-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="82be3-114">Az első parancs beolvassa a Nic01 nevű hálózati kapcsolat objektumát, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $Nic 01 változóban tárolja. A második parancs beolvassa a Nic02 nevű hálózati kapcsolat objektumát, amely a ResourceGroup02 nevű erőforráscsoport csoportjába tartozik, és a $Nic 02 változóban tárolja. A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevű erőforrás csoportba, és a $AppGw változóban tárolja. A Forth parancs a $Nic 01 és az $Nic 02 végponti IP-konfigurációs azonosítóit használja a $AppGwban tárolt alkalmazás-átjáró végpont-címkészlet hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="82be3-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="82be3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82be3-115">PARAMETERS</span></span>

### <span data-ttu-id="82be3-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82be3-116">-ApplicationGateway</span></span>
<span data-ttu-id="82be3-117">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a back-end címkészletet adja.</span><span class="sxs-lookup"><span data-stu-id="82be3-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="82be3-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="82be3-118">-BackendFqdns</span></span>
<span data-ttu-id="82be3-119">A backend-kiszolgálók készlete, amelyet a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="82be3-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="82be3-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="82be3-120">-BackendIPAddresses</span></span>
<span data-ttu-id="82be3-121">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="82be3-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="82be3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82be3-122">-DefaultProfile</span></span>
<span data-ttu-id="82be3-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82be3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82be3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82be3-124">-Name</span></span>
<span data-ttu-id="82be3-125">Annak a végfelhasználói készletnek a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="82be3-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="82be3-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82be3-126">-Confirm</span></span>
<span data-ttu-id="82be3-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82be3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82be3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82be3-128">-WhatIf</span></span>
<span data-ttu-id="82be3-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82be3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82be3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82be3-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82be3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82be3-131">CommonParameters</span></span>
<span data-ttu-id="82be3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82be3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82be3-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82be3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82be3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82be3-134">INPUTS</span></span>

###  
<span data-ttu-id="82be3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="82be3-135">System.String</span></span>

## <span data-ttu-id="82be3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82be3-136">OUTPUTS</span></span>

### <span data-ttu-id="82be3-137">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82be3-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82be3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82be3-138">NOTES</span></span>

## <span data-ttu-id="82be3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82be3-139">RELATED LINKS</span></span>

[<span data-ttu-id="82be3-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82be3-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82be3-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82be3-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82be3-142">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82be3-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82be3-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82be3-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82be3-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82be3-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


