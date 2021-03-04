---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: e01404958156967c6881655ab42eb965152ebaaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919489"
---
# <span data-ttu-id="5352e-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5352e-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="5352e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5352e-102">SYNOPSIS</span></span>
<span data-ttu-id="5352e-103">Módosít egy PrivateLink-konfigurációt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5352e-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="5352e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5352e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5352e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5352e-105">DESCRIPTION</span></span>
<span data-ttu-id="5352e-106">A **Set-AzApplicationGatewayPrivateLinkConfiguration** parancsmag módosítja egy Azure-alkalmazás átjáró privátLink-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5352e-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="5352e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5352e-107">EXAMPLES</span></span>

### <span data-ttu-id="5352e-108">1. példa: PrivateLink-konfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="5352e-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="5352e-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5352e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5352e-110">A második parancs a privateLinkConfig01 nevű privateLinkConfig01 konfigurációt a $privateLinkIpConfiguration 01 ip-konfigurációjának használatára állítja be</span><span class="sxs-lookup"><span data-stu-id="5352e-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="5352e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5352e-111">PARAMETERS</span></span>

### <span data-ttu-id="5352e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5352e-112">-ApplicationGateway</span></span>
<span data-ttu-id="5352e-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5352e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5352e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5352e-114">-DefaultProfile</span></span>
<span data-ttu-id="5352e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5352e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352e-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5352e-116">-IpConfiguration</span></span>
<span data-ttu-id="5352e-117">Az ipConfiguration listája</span><span class="sxs-lookup"><span data-stu-id="5352e-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5352e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5352e-118">-Name</span></span>
<span data-ttu-id="5352e-119">A privateLink-konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="5352e-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="5352e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5352e-120">-Confirm</span></span>
<span data-ttu-id="5352e-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5352e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5352e-122">-WhatIf</span></span>
<span data-ttu-id="5352e-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5352e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5352e-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5352e-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5352e-125">CommonParameters</span></span>
<span data-ttu-id="5352e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5352e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5352e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5352e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5352e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5352e-128">INPUTS</span></span>

### <span data-ttu-id="5352e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5352e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="5352e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="5352e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="5352e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5352e-131">OUTPUTS</span></span>

### <span data-ttu-id="5352e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5352e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5352e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5352e-133">NOTES</span></span>

## <span data-ttu-id="5352e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5352e-134">RELATED LINKS</span></span>

[<span data-ttu-id="5352e-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5352e-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5352e-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5352e-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5352e-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5352e-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5352e-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5352e-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)