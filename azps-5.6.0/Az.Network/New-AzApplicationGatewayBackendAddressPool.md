---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 3ce9cb761bb945c777a39e728ac8ebea2c40b885
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010357"
---
# <span data-ttu-id="ae4de-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae4de-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ae4de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4de-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4de-103">Létrehoz egy háttércímkészletet egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ae4de-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="ae4de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae4de-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae4de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae4de-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4de-106">A **New-AzApplicationGatewayBackendAddressPool** parancsmag létrehoz egy háttércímkészletet egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ae4de-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="ae4de-107">A háttércímek IP-címként, teljes tartománynévként vagy IP-konfigurációs azonosítóként is megadva.</span><span class="sxs-lookup"><span data-stu-id="ae4de-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="ae4de-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae4de-108">EXAMPLES</span></span>

### <span data-ttu-id="ae4de-109">1. példa: Háttércímkészlet létrehozása a háttérkiszolgáló teljes tartományának használatával</span><span class="sxs-lookup"><span data-stu-id="ae4de-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="ae4de-110">Ez a parancs létrehoz egy Pool01 nevű háttércímkészletet a háttérkiszolgálók teljes tartománynevének használatával, és azt egy másik $Pool tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae4de-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="ae4de-111">2. példa: Háttércímkészlet létrehozása a háttérkiszolgáló IP-címével</span><span class="sxs-lookup"><span data-stu-id="ae4de-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="ae4de-112">Ez a parancs létrehoz egy Pool02 nevű háttércímkészletet a háttérkiszolgálók IP-címeinek használatával, és tárolja azt a $Pool változóban.</span><span class="sxs-lookup"><span data-stu-id="ae4de-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="ae4de-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4de-113">PARAMETERS</span></span>

### <span data-ttu-id="ae4de-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="ae4de-114">-BackendFqdns</span></span>
<span data-ttu-id="ae4de-115">Megadja azokat a háttér-FQDN-eket, amelyekhez a parancsmag társítja a háttérkiszolgáló-készletet.</span><span class="sxs-lookup"><span data-stu-id="ae4de-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="ae4de-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="ae4de-116">-BackendIPAddresses</span></span>
<span data-ttu-id="ae4de-117">A parancsmag által a háttérkiszolgáló-készlethez társítható háttér-IP-címek listája.</span><span class="sxs-lookup"><span data-stu-id="ae4de-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="ae4de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4de-118">-DefaultProfile</span></span>
<span data-ttu-id="ae4de-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae4de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae4de-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ae4de-120">-Name</span></span>
<span data-ttu-id="ae4de-121">A parancsmag által létrehozott háttérkiszolgáló-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="ae4de-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ae4de-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae4de-122">-Confirm</span></span>
<span data-ttu-id="ae4de-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ae4de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4de-124">-WhatIf</span></span>
<span data-ttu-id="ae4de-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ae4de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4de-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae4de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4de-127">CommonParameters</span></span>
<span data-ttu-id="ae4de-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4de-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4de-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4de-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae4de-130">INPUTS</span></span>

### <span data-ttu-id="ae4de-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="ae4de-131">None</span></span>

## <span data-ttu-id="ae4de-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae4de-132">OUTPUTS</span></span>

### <span data-ttu-id="ae4de-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae4de-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ae4de-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae4de-134">NOTES</span></span>

## <span data-ttu-id="ae4de-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae4de-135">RELATED LINKS</span></span>

[<span data-ttu-id="ae4de-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae4de-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ae4de-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae4de-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ae4de-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae4de-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ae4de-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae4de-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


