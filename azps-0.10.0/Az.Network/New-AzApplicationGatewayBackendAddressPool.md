---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 961580d6354c6916ad811d6f8bccd4119d8b07a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841442"
---
# <span data-ttu-id="72191-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72191-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="72191-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72191-102">SYNOPSIS</span></span>
<span data-ttu-id="72191-103">Egy végponti címkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="72191-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="72191-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72191-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72191-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72191-105">DESCRIPTION</span></span>
<span data-ttu-id="72191-106">A **New-AzApplicationGatewayBackendAddressPool** parancsmag létrehoz egy végpontos címkészletet az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="72191-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="72191-107">A back-end cím megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs AZONOSÍTÓként.</span><span class="sxs-lookup"><span data-stu-id="72191-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="72191-108">Példák</span><span class="sxs-lookup"><span data-stu-id="72191-108">EXAMPLES</span></span>

### <span data-ttu-id="72191-109">Példa 1: back-end-címkészlet létrehozása a back-end kiszolgáló teljes tartománynevének használatával</span><span class="sxs-lookup"><span data-stu-id="72191-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="72191-110">Ez a parancs létrehoz egy Pool01 nevű back-end-címkészletet a back-end-kiszolgálók FQDN-jei segítségével, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72191-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="72191-111">2. példa: back-end-címkészlet létrehozása a back-end-kiszolgáló IP-címének használatával</span><span class="sxs-lookup"><span data-stu-id="72191-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="72191-112">Ez a parancs létrehoz egy Pool02 nevű back-end-címkészletet a back-end-kiszolgálók IP-címeivel, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72191-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="72191-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72191-113">PARAMETERS</span></span>

### <span data-ttu-id="72191-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="72191-114">-BackendFqdns</span></span>
<span data-ttu-id="72191-115">Itt adhatja meg azoknak a back-end FQDN-ket a listáját, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="72191-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="72191-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="72191-116">-BackendIPAddresses</span></span>
<span data-ttu-id="72191-117">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="72191-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="72191-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72191-118">-DefaultProfile</span></span>
<span data-ttu-id="72191-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72191-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72191-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72191-120">-Name</span></span>
<span data-ttu-id="72191-121">A parancsmag által létrehozott back-end Server-készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72191-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="72191-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72191-122">-Confirm</span></span>
<span data-ttu-id="72191-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72191-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72191-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72191-124">-WhatIf</span></span>
<span data-ttu-id="72191-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72191-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72191-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72191-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72191-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72191-127">CommonParameters</span></span>
<span data-ttu-id="72191-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72191-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72191-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72191-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72191-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72191-130">INPUTS</span></span>

### <span data-ttu-id="72191-131">System. String</span><span class="sxs-lookup"><span data-stu-id="72191-131">System.String</span></span>

## <span data-ttu-id="72191-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72191-132">OUTPUTS</span></span>

### <span data-ttu-id="72191-133">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72191-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="72191-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72191-134">NOTES</span></span>

## <span data-ttu-id="72191-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72191-135">RELATED LINKS</span></span>

[<span data-ttu-id="72191-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72191-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="72191-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72191-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="72191-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72191-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="72191-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72191-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


