---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: f5be63987e055a7a7b6053820c22522bae021ad3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499956"
---
# <span data-ttu-id="ff3a7-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff3a7-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ff3a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3a7-103">Egy végponti címkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff3a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff3a7-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff3a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ff3a7-106">A **New-AzureRmApplicationGatewayBackendAddressPool** parancsmag létrehoz egy végpontos címkészletet az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="ff3a7-107">A back-end cím megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs AZONOSÍTÓként.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="ff3a7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ff3a7-108">EXAMPLES</span></span>

### <span data-ttu-id="ff3a7-109">Példa 1: back-end-címkészlet létrehozása a back-end kiszolgáló teljes tartománynevének használatával</span><span class="sxs-lookup"><span data-stu-id="ff3a7-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="ff3a7-110">Ez a parancs létrehoz egy Pool01 nevű back-end-címkészletet a back-end-kiszolgálók FQDN-jei segítségével, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="ff3a7-111">2. példa: back-end-címkészlet létrehozása a back-end-kiszolgáló IP-címének használatával</span><span class="sxs-lookup"><span data-stu-id="ff3a7-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="ff3a7-112">Ez a parancs létrehoz egy Pool02 nevű back-end-címkészletet a back-end-kiszolgálók IP-címeivel, és a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="ff3a7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff3a7-113">PARAMETERS</span></span>

### <span data-ttu-id="ff3a7-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="ff3a7-114">-BackendFqdns</span></span>
<span data-ttu-id="ff3a7-115">Itt adhatja meg azoknak a back-end FQDN-ket a listáját, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="ff3a7-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="ff3a7-116">-BackendIPAddresses</span></span>
<span data-ttu-id="ff3a7-117">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készlettel társít.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="ff3a7-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff3a7-118">-Name</span></span>
<span data-ttu-id="ff3a7-119">A parancsmag által létrehozott back-end Server-készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-119">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ff3a7-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff3a7-120">-Confirm</span></span>
<span data-ttu-id="ff3a7-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3a7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3a7-122">-WhatIf</span></span>
<span data-ttu-id="ff3a7-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3a7-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3a7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3a7-125">-DefaultProfile</span></span>
<span data-ttu-id="ff3a7-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff3a7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff3a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3a7-127">CommonParameters</span></span>
<span data-ttu-id="ff3a7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff3a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3a7-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3a7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3a7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff3a7-130">INPUTS</span></span>

### <span data-ttu-id="ff3a7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ff3a7-131">System.String</span></span>

## <span data-ttu-id="ff3a7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff3a7-132">OUTPUTS</span></span>

### <span data-ttu-id="ff3a7-133">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff3a7-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ff3a7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff3a7-134">NOTES</span></span>

## <span data-ttu-id="ff3a7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff3a7-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff3a7-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff3a7-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ff3a7-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff3a7-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ff3a7-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff3a7-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ff3a7-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff3a7-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


