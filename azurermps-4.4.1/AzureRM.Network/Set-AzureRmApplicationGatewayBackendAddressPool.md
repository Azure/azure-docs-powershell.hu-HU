---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: dd5a0a14a0c2146ce6187a3ae08fda1bc3e60702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680855"
---
# <span data-ttu-id="9ceca-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9ceca-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9ceca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ceca-102">SYNOPSIS</span></span>
<span data-ttu-id="9ceca-103">Az alkalmazás-átjárók back-end-címkészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="9ceca-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ceca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ceca-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ceca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ceca-105">DESCRIPTION</span></span>
<span data-ttu-id="9ceca-106">A **set-AzureRmApplicationGatewayBackendAddressPool** parancsmag a back-end Address poolt frissíti az Azure Application gatewayben.</span><span class="sxs-lookup"><span data-stu-id="9ceca-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="9ceca-107">A back-end címek IP-címekként, teljesen minősített tartománynevek (FQDN) vagy IP-konfigurációk azonosítóként adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="9ceca-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="9ceca-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9ceca-108">EXAMPLES</span></span>

### <span data-ttu-id="9ceca-109">1. példa: a back-end Address Pool beállítása FQDN segítségével</span><span class="sxs-lookup"><span data-stu-id="9ceca-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="9ceca-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ceca-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9ceca-111">A második parancs az $AppGw a teljes tartománynevek használatával frissíti az alkalmazás-átjárók back-end Address poolját.</span><span class="sxs-lookup"><span data-stu-id="9ceca-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="9ceca-112">2. példa: a back-end Address Pool beállítása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="9ceca-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="9ceca-113">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ceca-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9ceca-114">A második parancs az IP-címekkel frissíti az alkalmazás-átjáró $AppGwt.</span><span class="sxs-lookup"><span data-stu-id="9ceca-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="9ceca-115">3. példa: a back-end Address Pool beállítása a backend Server? s IP-cím azonosítójával</span><span class="sxs-lookup"><span data-stu-id="9ceca-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="9ceca-116">Az első parancs beolvassa a Nic01 nevű hálózati kapcsolat objektumát, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $Nic 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ceca-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="9ceca-117">A második parancs beolvassa a Nic02 nevű hálózati kapcsolat objektumát, amely a ResourceGroup02 nevű erőforráscsoport csoportjába tartozik, és a $Nic 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ceca-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="9ceca-118">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevű erőforrás csoportba, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ceca-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9ceca-119">A Forth parancs a back-end IP-konfiguráció azonosítóit használja a $Nic 01-ből és az $Nic 02-ből, hogy frissítse a $AppGw alkalmazás átjárójának back-end Address poolját.</span><span class="sxs-lookup"><span data-stu-id="9ceca-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="9ceca-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ceca-120">PARAMETERS</span></span>

### <span data-ttu-id="9ceca-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ceca-121">-ApplicationGateway</span></span>
<span data-ttu-id="9ceca-122">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag a back-end címkészletet társítja.</span><span class="sxs-lookup"><span data-stu-id="9ceca-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="9ceca-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="9ceca-123">-BackendFqdns</span></span>
<span data-ttu-id="9ceca-124">Itt adhatja meg a back-end kiszolgálói készletként használható back-end IP-címek listáját.</span><span class="sxs-lookup"><span data-stu-id="9ceca-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="9ceca-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="9ceca-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="9ceca-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ceca-126">-Name</span></span>
<span data-ttu-id="9ceca-127">A back-end Address Pool nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ceca-127">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="9ceca-128">Ehhez a végpont-címkészlet csak az alkalmazás-átjáróban lehet.</span><span class="sxs-lookup"><span data-stu-id="9ceca-128">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="9ceca-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ceca-129">-Confirm</span></span>
<span data-ttu-id="9ceca-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ceca-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ceca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ceca-131">-WhatIf</span></span>
<span data-ttu-id="9ceca-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ceca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ceca-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ceca-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ceca-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ceca-134">-DefaultProfile</span></span>
<span data-ttu-id="9ceca-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ceca-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ceca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ceca-136">CommonParameters</span></span>
<span data-ttu-id="9ceca-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ceca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ceca-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ceca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ceca-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ceca-139">INPUTS</span></span>

### <span data-ttu-id="9ceca-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9ceca-140">System.String</span></span>

## <span data-ttu-id="9ceca-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ceca-141">OUTPUTS</span></span>

### <span data-ttu-id="9ceca-142">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ceca-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ceca-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ceca-143">NOTES</span></span>

## <span data-ttu-id="9ceca-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ceca-144">RELATED LINKS</span></span>

[<span data-ttu-id="9ceca-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9ceca-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9ceca-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9ceca-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9ceca-147">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9ceca-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9ceca-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9ceca-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


