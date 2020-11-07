---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: fd9d9c1b7956c16ab981b5426e9453de4d730dd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843706"
---
# <span data-ttu-id="58b43-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b43-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="58b43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58b43-102">SYNOPSIS</span></span>
<span data-ttu-id="58b43-103">Az alkalmazás-átjárók back-end-címkészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="58b43-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="58b43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58b43-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="58b43-105">DESCRIPTION</span></span>
<span data-ttu-id="58b43-106">A **set-AzApplicationGatewayBackendAddressPool** parancsmag a back-end Address poolt frissíti az Azure Application gatewayben.</span><span class="sxs-lookup"><span data-stu-id="58b43-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="58b43-107">A back-end címek IP-címekként, teljesen minősített tartománynevek (FQDN) vagy IP-konfigurációk azonosítóként adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="58b43-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="58b43-108">Példák</span><span class="sxs-lookup"><span data-stu-id="58b43-108">EXAMPLES</span></span>

### <span data-ttu-id="58b43-109">1. példa: a back-end Address Pool beállítása FQDN segítségével</span><span class="sxs-lookup"><span data-stu-id="58b43-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="58b43-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="58b43-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="58b43-111">A második parancs az $AppGw a teljes tartománynevek használatával frissíti az alkalmazás-átjárók back-end Address poolját.</span><span class="sxs-lookup"><span data-stu-id="58b43-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="58b43-112">2. példa: a back-end Address Pool beállítása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="58b43-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="58b43-113">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="58b43-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="58b43-114">A második parancs az IP-címekkel frissíti az alkalmazás-átjáró $AppGwt.</span><span class="sxs-lookup"><span data-stu-id="58b43-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="58b43-115">3. példa: a back-end Address Pool beállítása a backend Server? s IP-cím azonosítójával</span><span class="sxs-lookup"><span data-stu-id="58b43-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="58b43-116">Az első parancs beolvassa a Nic01 nevű hálózati kapcsolat objektumát, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $Nic 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="58b43-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="58b43-117">A második parancs beolvassa a Nic02 nevű hálózati kapcsolat objektumát, amely a ResourceGroup02 nevű erőforráscsoport csoportjába tartozik, és a $Nic 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="58b43-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="58b43-118">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevű erőforrás csoportba, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="58b43-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="58b43-119">A Forth parancs a back-end IP-konfiguráció azonosítóit használja a $Nic 01-ből és az $Nic 02-ből, hogy frissítse a $AppGw alkalmazás átjárójának back-end Address poolját.</span><span class="sxs-lookup"><span data-stu-id="58b43-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="58b43-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58b43-120">PARAMETERS</span></span>

### <span data-ttu-id="58b43-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58b43-121">-ApplicationGateway</span></span>
<span data-ttu-id="58b43-122">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag a back-end címkészletet társítja.</span><span class="sxs-lookup"><span data-stu-id="58b43-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="58b43-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="58b43-123">-BackendFqdns</span></span>
<span data-ttu-id="58b43-124">Itt adhatja meg a back-end kiszolgálói készletként használható back-end IP-címek listáját.</span><span class="sxs-lookup"><span data-stu-id="58b43-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="58b43-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="58b43-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="58b43-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b43-126">-DefaultProfile</span></span>
<span data-ttu-id="58b43-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58b43-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b43-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58b43-128">-Name</span></span>
<span data-ttu-id="58b43-129">A back-end Address Pool nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58b43-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="58b43-130">Ehhez a végpont-címkészlet csak az alkalmazás-átjáróban lehet.</span><span class="sxs-lookup"><span data-stu-id="58b43-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="58b43-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="58b43-131">-Confirm</span></span>
<span data-ttu-id="58b43-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="58b43-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b43-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b43-133">-WhatIf</span></span>
<span data-ttu-id="58b43-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="58b43-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b43-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58b43-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b43-136">CommonParameters</span></span>
<span data-ttu-id="58b43-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58b43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b43-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b43-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b43-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58b43-139">INPUTS</span></span>

### <span data-ttu-id="58b43-140">System. String</span><span class="sxs-lookup"><span data-stu-id="58b43-140">System.String</span></span>

## <span data-ttu-id="58b43-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58b43-141">OUTPUTS</span></span>

### <span data-ttu-id="58b43-142">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58b43-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58b43-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58b43-143">NOTES</span></span>

## <span data-ttu-id="58b43-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58b43-144">RELATED LINKS</span></span>

[<span data-ttu-id="58b43-145">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b43-145">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58b43-146">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b43-146">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58b43-147">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b43-147">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58b43-148">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b43-148">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


