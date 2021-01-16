---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342665"
---
# <span data-ttu-id="50124-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50124-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="50124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50124-102">SYNOPSIS</span></span>
<span data-ttu-id="50124-103">Frissíti egy alkalmazás-átjáró háttércímkészletét.</span><span class="sxs-lookup"><span data-stu-id="50124-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="50124-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50124-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50124-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50124-105">DESCRIPTION</span></span>
<span data-ttu-id="50124-106">A **Set-AzApplicationGatewayBackendAddressPool** parancsmag frissíti az Azure-alkalmazásátjárók háttércímkészletét.</span><span class="sxs-lookup"><span data-stu-id="50124-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="50124-107">A háttércímek IP-címekként, teljes tartománynevekként (FQDN) vagy IP-konfigurációként is megadva.</span><span class="sxs-lookup"><span data-stu-id="50124-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="50124-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50124-108">EXAMPLES</span></span>

### <span data-ttu-id="50124-109">1. példa: Háttércímkészlet beállítása FQDN-ekkel</span><span class="sxs-lookup"><span data-stu-id="50124-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="50124-110">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="50124-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50124-111">A második parancs frissíti az alkalmazás-átjáró háttércímkészletét $AppGw FQDN-ekkel.</span><span class="sxs-lookup"><span data-stu-id="50124-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="50124-112">2. példa: Háttércímkészlet beállítása háttérkiszolgálói IP-címek használatával</span><span class="sxs-lookup"><span data-stu-id="50124-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="50124-113">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="50124-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50124-114">A második parancs IP-címekkel frissíti az alkalmazás-átjáró $AppGw címkészletét.</span><span class="sxs-lookup"><span data-stu-id="50124-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="50124-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50124-115">PARAMETERS</span></span>

### <span data-ttu-id="50124-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50124-116">-ApplicationGateway</span></span>
<span data-ttu-id="50124-117">Azt az alkalmazás-átjárót adja meg, amellyel a parancsmag társítja a háttércímkészletet.</span><span class="sxs-lookup"><span data-stu-id="50124-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="50124-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="50124-118">-BackendFqdns</span></span>
<span data-ttu-id="50124-119">A háttérkiszolgáló-készletként használható háttér-IP-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="50124-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="50124-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="50124-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="50124-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50124-121">-DefaultProfile</span></span>
<span data-ttu-id="50124-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50124-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50124-123">-Name</span><span class="sxs-lookup"><span data-stu-id="50124-123">-Name</span></span>
<span data-ttu-id="50124-124">A háttércímkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50124-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="50124-125">Ennek a háttércímkészletnek az alkalmazás-átjáróban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="50124-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="50124-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50124-126">-Confirm</span></span>
<span data-ttu-id="50124-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50124-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50124-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50124-128">-WhatIf</span></span>
<span data-ttu-id="50124-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50124-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50124-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50124-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50124-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50124-131">CommonParameters</span></span>
<span data-ttu-id="50124-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50124-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50124-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50124-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50124-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50124-134">INPUTS</span></span>

### <span data-ttu-id="50124-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50124-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50124-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50124-136">OUTPUTS</span></span>

### <span data-ttu-id="50124-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50124-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50124-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50124-138">NOTES</span></span>

## <span data-ttu-id="50124-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50124-139">RELATED LINKS</span></span>

[<span data-ttu-id="50124-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50124-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="50124-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50124-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="50124-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50124-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="50124-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50124-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


