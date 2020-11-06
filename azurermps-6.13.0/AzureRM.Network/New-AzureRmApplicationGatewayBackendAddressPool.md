---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1d6c207fe009133db03136ca09840fb0a8646750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498327"
---
# <span data-ttu-id="bbd2c-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd2c-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bbd2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd2c-103">Egy végponti címkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbd2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbd2c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd2c-106">A **New-AzureRmApplicationGatewayBackendAddressPool** parancsmag létrehoz egy végpontos címkészletet az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="bbd2c-107">A back-end cím megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs AZONOSÍTÓként.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="bbd2c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bbd2c-108">EXAMPLES</span></span>

### <span data-ttu-id="bbd2c-109">Példa 1: back-end-címkészlet létrehozása a back-end kiszolgáló teljes tartománynevének használatával</span><span class="sxs-lookup"><span data-stu-id="bbd2c-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="bbd2c-110">Ez a parancs létrehoz egy Pool01 nevű back-end-címkészletet a back-end-kiszolgálók FQDN-jei segítségével, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="bbd2c-111">2. példa: back-end-címkészlet létrehozása a back-end-kiszolgáló IP-címének használatával</span><span class="sxs-lookup"><span data-stu-id="bbd2c-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="bbd2c-112">Ez a parancs létrehoz egy Pool02 nevű back-end-címkészletet a back-end-kiszolgálók IP-címeivel, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="bbd2c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbd2c-113">PARAMETERS</span></span>

### <span data-ttu-id="bbd2c-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="bbd2c-114">-BackendFqdns</span></span>
<span data-ttu-id="bbd2c-115">Itt adhatja meg azoknak a back-end FQDN-ket a listáját, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="bbd2c-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="bbd2c-116">-BackendIPAddresses</span></span>
<span data-ttu-id="bbd2c-117">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="bbd2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd2c-118">-DefaultProfile</span></span>
<span data-ttu-id="bbd2c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd2c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bbd2c-120">-Name</span></span>
<span data-ttu-id="bbd2c-121">A parancsmag által létrehozott back-end Server-készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bbd2c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbd2c-122">-Confirm</span></span>
<span data-ttu-id="bbd2c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd2c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd2c-124">-WhatIf</span></span>
<span data-ttu-id="bbd2c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd2c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbd2c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd2c-127">CommonParameters</span></span>
<span data-ttu-id="bbd2c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbd2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd2c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd2c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd2c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd2c-130">INPUTS</span></span>

### <span data-ttu-id="bbd2c-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="bbd2c-131">None</span></span>

## <span data-ttu-id="bbd2c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd2c-132">OUTPUTS</span></span>

### <span data-ttu-id="bbd2c-133">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd2c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bbd2c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbd2c-134">NOTES</span></span>

## <span data-ttu-id="bbd2c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbd2c-135">RELATED LINKS</span></span>

[<span data-ttu-id="bbd2c-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd2c-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bbd2c-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd2c-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bbd2c-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd2c-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bbd2c-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd2c-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


