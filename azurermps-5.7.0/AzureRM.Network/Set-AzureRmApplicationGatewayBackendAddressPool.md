---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: bafc55d3e630b936d2d30efa168f60919cc6c69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680813"
---
# <span data-ttu-id="a7f86-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7f86-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a7f86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7f86-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f86-103">Az alkalmazás-átjárók back-end-címkészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="a7f86-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7f86-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f86-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7f86-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f86-106">A **set-AzureRmApplicationGatewayBackendAddressPool** parancsmag a back-end Address poolt frissíti az Azure Application gatewayben.</span><span class="sxs-lookup"><span data-stu-id="a7f86-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="a7f86-107">A back-end címek IP-címekként, teljesen minősített tartománynevek (FQDN) vagy IP-konfigurációk azonosítóként adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="a7f86-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="a7f86-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a7f86-108">EXAMPLES</span></span>

### <span data-ttu-id="a7f86-109">1. példa: a back-end Address Pool beállítása FQDN segítségével</span><span class="sxs-lookup"><span data-stu-id="a7f86-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="a7f86-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a7f86-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a7f86-111">A második parancs az $AppGw a teljes tartománynevek használatával frissíti az alkalmazás-átjárók back-end Address poolját.</span><span class="sxs-lookup"><span data-stu-id="a7f86-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="a7f86-112">2. példa: a back-end Address Pool beállítása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="a7f86-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="a7f86-113">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a7f86-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a7f86-114">A második parancs az IP-címekkel frissíti az alkalmazás-átjáró $AppGwt.</span><span class="sxs-lookup"><span data-stu-id="a7f86-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="a7f86-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7f86-115">PARAMETERS</span></span>

### <span data-ttu-id="a7f86-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7f86-116">-ApplicationGateway</span></span>
<span data-ttu-id="a7f86-117">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag a back-end címkészletet társítja.</span><span class="sxs-lookup"><span data-stu-id="a7f86-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="a7f86-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="a7f86-118">-BackendFqdns</span></span>
<span data-ttu-id="a7f86-119">Itt adhatja meg a back-end kiszolgálói készletként használható back-end IP-címek listáját.</span><span class="sxs-lookup"><span data-stu-id="a7f86-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="a7f86-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="a7f86-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="a7f86-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f86-121">-DefaultProfile</span></span>
<span data-ttu-id="a7f86-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7f86-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f86-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7f86-123">-Name</span></span>
<span data-ttu-id="a7f86-124">A back-end Address Pool nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7f86-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="a7f86-125">Ehhez a végpont-címkészlet csak az alkalmazás-átjáróban lehet.</span><span class="sxs-lookup"><span data-stu-id="a7f86-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="a7f86-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7f86-126">-Confirm</span></span>
<span data-ttu-id="a7f86-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7f86-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f86-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f86-128">-WhatIf</span></span>
<span data-ttu-id="a7f86-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7f86-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f86-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7f86-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f86-131">CommonParameters</span></span>
<span data-ttu-id="a7f86-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7f86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f86-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f86-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f86-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7f86-134">INPUTS</span></span>

### <span data-ttu-id="a7f86-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f86-135">System.String</span></span>

## <span data-ttu-id="a7f86-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7f86-136">OUTPUTS</span></span>

### <span data-ttu-id="a7f86-137">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7f86-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7f86-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7f86-138">NOTES</span></span>

## <span data-ttu-id="a7f86-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7f86-139">RELATED LINKS</span></span>

[<span data-ttu-id="a7f86-140">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7f86-140">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a7f86-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7f86-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a7f86-142">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7f86-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a7f86-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7f86-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


