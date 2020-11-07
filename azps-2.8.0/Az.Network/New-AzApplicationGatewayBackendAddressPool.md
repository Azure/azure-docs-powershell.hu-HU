---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1165d7abccdbf21dc94e4f39b8b2dad953fdba07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837249"
---
# <span data-ttu-id="ea749-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ea749-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ea749-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea749-102">SYNOPSIS</span></span>
<span data-ttu-id="ea749-103">Egy végponti címkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ea749-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="ea749-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea749-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea749-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea749-105">DESCRIPTION</span></span>
<span data-ttu-id="ea749-106">A **New-AzApplicationGatewayBackendAddressPool** parancsmag létrehoz egy végpontos címkészletet az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="ea749-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="ea749-107">A back-end cím megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs AZONOSÍTÓként.</span><span class="sxs-lookup"><span data-stu-id="ea749-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="ea749-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ea749-108">EXAMPLES</span></span>

### <span data-ttu-id="ea749-109">Példa 1: back-end-címkészlet létrehozása a back-end kiszolgáló teljes tartománynevének használatával</span><span class="sxs-lookup"><span data-stu-id="ea749-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="ea749-110">Ez a parancs létrehoz egy Pool01 nevű back-end-címkészletet a back-end-kiszolgálók FQDN-jei segítségével, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ea749-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="ea749-111">2. példa: back-end-címkészlet létrehozása a back-end-kiszolgáló IP-címének használatával</span><span class="sxs-lookup"><span data-stu-id="ea749-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="ea749-112">Ez a parancs létrehoz egy Pool02 nevű back-end-címkészletet a back-end-kiszolgálók IP-címeivel, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ea749-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="ea749-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea749-113">PARAMETERS</span></span>

### <span data-ttu-id="ea749-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="ea749-114">-BackendFqdns</span></span>
<span data-ttu-id="ea749-115">Itt adhatja meg azoknak a back-end FQDN-ket a listáját, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="ea749-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="ea749-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="ea749-116">-BackendIPAddresses</span></span>
<span data-ttu-id="ea749-117">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="ea749-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="ea749-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea749-118">-DefaultProfile</span></span>
<span data-ttu-id="ea749-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea749-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea749-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea749-120">-Name</span></span>
<span data-ttu-id="ea749-121">A parancsmag által létrehozott back-end Server-készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea749-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ea749-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea749-122">-Confirm</span></span>
<span data-ttu-id="ea749-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea749-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea749-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea749-124">-WhatIf</span></span>
<span data-ttu-id="ea749-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea749-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea749-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea749-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea749-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea749-127">CommonParameters</span></span>
<span data-ttu-id="ea749-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea749-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea749-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea749-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea749-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea749-130">INPUTS</span></span>

### <span data-ttu-id="ea749-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea749-131">None</span></span>

## <span data-ttu-id="ea749-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea749-132">OUTPUTS</span></span>

### <span data-ttu-id="ea749-133">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ea749-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ea749-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea749-134">NOTES</span></span>

## <span data-ttu-id="ea749-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea749-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea749-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ea749-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ea749-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ea749-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ea749-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ea749-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ea749-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ea749-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


