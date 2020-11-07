---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: dcce5b85fc9d3e8046ecc90330da5f3d40b88e33
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849162"
---
# <span data-ttu-id="0d7a3-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7a3-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0d7a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7a3-103">Egy végponti címkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d7a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d7a3-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d7a3-105">DESCRIPTION</span></span>
<span data-ttu-id="0d7a3-106">A **New-AzureRmApplicationGatewayBackendAddressPool** parancsmag létrehoz egy végpontos címkészletet az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="0d7a3-107">A back-end cím megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs AZONOSÍTÓként.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="0d7a3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0d7a3-108">EXAMPLES</span></span>

### <span data-ttu-id="0d7a3-109">Példa 1: back-end-címkészlet létrehozása a back-end kiszolgáló teljes tartománynevének használatával</span><span class="sxs-lookup"><span data-stu-id="0d7a3-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="0d7a3-110">Ez a parancs létrehoz egy Pool01 nevű back-end-címkészletet a back-end-kiszolgálók FQDN-jei segítségével, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="0d7a3-111">2. példa: back-end-címkészlet létrehozása a back-end-kiszolgáló IP-címének használatával</span><span class="sxs-lookup"><span data-stu-id="0d7a3-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="0d7a3-112">Ez a parancs létrehoz egy Pool02 nevű back-end-címkészletet a back-end-kiszolgálók IP-címeivel, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="0d7a3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d7a3-113">PARAMETERS</span></span>

### <span data-ttu-id="0d7a3-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="0d7a3-114">-BackendFqdns</span></span>
<span data-ttu-id="0d7a3-115">Itt adhatja meg azoknak a back-end FQDN-ket a listáját, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="0d7a3-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="0d7a3-116">-BackendIPAddresses</span></span>
<span data-ttu-id="0d7a3-117">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="0d7a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7a3-118">-DefaultProfile</span></span>
<span data-ttu-id="0d7a3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d7a3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d7a3-120">-Name</span></span>
<span data-ttu-id="0d7a3-121">A parancsmag által létrehozott back-end Server-készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0d7a3-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d7a3-122">-Confirm</span></span>
<span data-ttu-id="0d7a3-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7a3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7a3-124">-WhatIf</span></span>
<span data-ttu-id="0d7a3-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7a3-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7a3-127">CommonParameters</span></span>
<span data-ttu-id="0d7a3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d7a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7a3-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d7a3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7a3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d7a3-130">INPUTS</span></span>

### <span data-ttu-id="0d7a3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0d7a3-131">System.String</span></span>

## <span data-ttu-id="0d7a3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d7a3-132">OUTPUTS</span></span>

### <span data-ttu-id="0d7a3-133">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7a3-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0d7a3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d7a3-134">NOTES</span></span>

## <span data-ttu-id="0d7a3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d7a3-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d7a3-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7a3-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0d7a3-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7a3-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0d7a3-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7a3-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0d7a3-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7a3-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


