---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194007"
---
# <span data-ttu-id="e7f7b-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7f7b-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e7f7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f7b-103">Az alkalmazás-átjárók back-end-címkészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="e7f7b-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="e7f7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7f7b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f7b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f7b-106">A **set-AzApplicationGatewayBackendAddressPool** parancsmag a back-end Address poolt frissíti az Azure Application gatewayben.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="e7f7b-107">A back-end címek IP-címekként, teljesen minősített tartománynevek (FQDN) vagy IP-konfigurációk azonosítóként adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="e7f7b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e7f7b-108">EXAMPLES</span></span>

### <span data-ttu-id="e7f7b-109">1. példa: a back-end Address Pool beállítása FQDN segítségével</span><span class="sxs-lookup"><span data-stu-id="e7f7b-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="e7f7b-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e7f7b-111">A második parancs az $AppGw a teljes tartománynevek használatával frissíti az alkalmazás-átjárók back-end Address poolját.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="e7f7b-112">2. példa: a back-end Address Pool beállítása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="e7f7b-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="e7f7b-113">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e7f7b-114">A második parancs az IP-címekkel frissíti az alkalmazás-átjáró $AppGwt.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="e7f7b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7f7b-115">PARAMETERS</span></span>

### <span data-ttu-id="e7f7b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7f7b-116">-ApplicationGateway</span></span>
<span data-ttu-id="e7f7b-117">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag a back-end címkészletet társítja.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="e7f7b-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="e7f7b-118">-BackendFqdns</span></span>
<span data-ttu-id="e7f7b-119">Itt adhatja meg a back-end kiszolgálói készletként használható back-end IP-címek listáját.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="e7f7b-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="e7f7b-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="e7f7b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f7b-121">-DefaultProfile</span></span>
<span data-ttu-id="e7f7b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f7b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7f7b-123">-Name</span></span>
<span data-ttu-id="e7f7b-124">A back-end Address Pool nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="e7f7b-125">Ehhez a végpont-címkészlet csak az alkalmazás-átjáróban lehet.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="e7f7b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7f7b-126">-Confirm</span></span>
<span data-ttu-id="e7f7b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f7b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f7b-128">-WhatIf</span></span>
<span data-ttu-id="e7f7b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f7b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7f7b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f7b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f7b-131">CommonParameters</span></span>
<span data-ttu-id="e7f7b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7f7b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f7b-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f7b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f7b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f7b-134">INPUTS</span></span>

### <span data-ttu-id="e7f7b-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7f7b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7f7b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f7b-136">OUTPUTS</span></span>

### <span data-ttu-id="e7f7b-137">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7f7b-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7f7b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7f7b-138">NOTES</span></span>

## <span data-ttu-id="e7f7b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7f7b-139">RELATED LINKS</span></span>

[<span data-ttu-id="e7f7b-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7f7b-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7f7b-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7f7b-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7f7b-142">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7f7b-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7f7b-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7f7b-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

