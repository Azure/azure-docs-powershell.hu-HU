---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481159"
---
# <span data-ttu-id="79b2c-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2c-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="79b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="79b2c-103">Frissíti egy alkalmazás-átjáró háttércímkészletét.</span><span class="sxs-lookup"><span data-stu-id="79b2c-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="79b2c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79b2c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b2c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="79b2c-106">A **Set-AzApplicationGatewayBackendAddressPool** parancsmag frissíti az Azure-alkalmazásátjárók háttércímkészletét.</span><span class="sxs-lookup"><span data-stu-id="79b2c-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="79b2c-107">A háttércímek IP-címekként, teljes tartománynevekként (FQDN) vagy IP-konfigurációként is megadva.</span><span class="sxs-lookup"><span data-stu-id="79b2c-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="79b2c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79b2c-108">EXAMPLES</span></span>

### <span data-ttu-id="79b2c-109">1. példa: Háttércímkészlet beállítása FQDN-ekkel</span><span class="sxs-lookup"><span data-stu-id="79b2c-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="79b2c-110">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="79b2c-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="79b2c-111">A második parancs frissíti az alkalmazás-átjáró háttércímkészletét $AppGw FQDN-ekkel.</span><span class="sxs-lookup"><span data-stu-id="79b2c-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="79b2c-112">2. példa: Háttércímkészlet beállítása háttérkiszolgálói IP-címek használatával</span><span class="sxs-lookup"><span data-stu-id="79b2c-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="79b2c-113">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="79b2c-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="79b2c-114">A második parancs IP-címekkel frissíti az alkalmazás-átjáró $AppGw címkészletét.</span><span class="sxs-lookup"><span data-stu-id="79b2c-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="79b2c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79b2c-115">PARAMETERS</span></span>

### <span data-ttu-id="79b2c-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79b2c-116">-ApplicationGateway</span></span>
<span data-ttu-id="79b2c-117">Azt az alkalmazás-átjárót adja meg, amellyel ez a parancsmag társítja a háttércímkészletet.</span><span class="sxs-lookup"><span data-stu-id="79b2c-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="79b2c-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="79b2c-118">-BackendFqdns</span></span>
<span data-ttu-id="79b2c-119">A háttérkiszolgáló-készletként használható háttér-IP-címek listája.</span><span class="sxs-lookup"><span data-stu-id="79b2c-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="79b2c-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="79b2c-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="79b2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b2c-121">-DefaultProfile</span></span>
<span data-ttu-id="79b2c-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79b2c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b2c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="79b2c-123">-Name</span></span>
<span data-ttu-id="79b2c-124">A háttércímkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b2c-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="79b2c-125">Ennek a háttércímkészletnek az alkalmazás-átjáróban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="79b2c-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="79b2c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79b2c-126">-Confirm</span></span>
<span data-ttu-id="79b2c-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79b2c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b2c-128">-WhatIf</span></span>
<span data-ttu-id="79b2c-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79b2c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b2c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79b2c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b2c-131">CommonParameters</span></span>
<span data-ttu-id="79b2c-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b2c-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b2c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b2c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79b2c-134">INPUTS</span></span>

### <span data-ttu-id="79b2c-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79b2c-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79b2c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79b2c-136">OUTPUTS</span></span>

### <span data-ttu-id="79b2c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79b2c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79b2c-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79b2c-138">NOTES</span></span>

## <span data-ttu-id="79b2c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79b2c-139">RELATED LINKS</span></span>

[<span data-ttu-id="79b2c-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2c-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79b2c-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2c-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79b2c-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2c-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79b2c-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2c-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


