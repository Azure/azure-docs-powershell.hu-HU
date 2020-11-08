---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: eb90b668bf0466c44e3fde0ef0a8d6777074fb37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014055"
---
# <span data-ttu-id="3e8fa-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3e8fa-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="3e8fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8fa-103">Eltávolít egy ExpressRoute-kapcsolatok közötti kapcsolat-összekapcsolási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="3e8fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e8fa-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e8fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3e8fa-106">A **Remove-AzExpressRouteCrossConnectionPeering** parancsmag eltávolítja a ExpressRoute-kapcsolatok közötti kapcsolati konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="3e8fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e8fa-107">EXAMPLES</span></span>

### <span data-ttu-id="3e8fa-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="3e8fa-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="3e8fa-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e8fa-109">PARAMETERS</span></span>

### <span data-ttu-id="3e8fa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8fa-110">-DefaultProfile</span></span>
<span data-ttu-id="3e8fa-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e8fa-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e8fa-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="3e8fa-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-kereszt kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8fa-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3e8fa-114">-Force</span></span>
<span data-ttu-id="3e8fa-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8fa-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e8fa-116">-Name</span></span>
<span data-ttu-id="3e8fa-117">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8fa-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3e8fa-118">-PeerAddressType</span></span>
<span data-ttu-id="3e8fa-119">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="3e8fa-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8fa-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e8fa-120">-Confirm</span></span>
<span data-ttu-id="3e8fa-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8fa-122">-WhatIf</span></span>
<span data-ttu-id="3e8fa-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e8fa-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e8fa-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8fa-125">CommonParameters</span></span>
<span data-ttu-id="3e8fa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e8fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8fa-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8fa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e8fa-128">INPUTS</span></span>

### <span data-ttu-id="3e8fa-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e8fa-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="3e8fa-130">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3e8fa-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="3e8fa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e8fa-131">OUTPUTS</span></span>

### <span data-ttu-id="3e8fa-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e8fa-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="3e8fa-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e8fa-133">NOTES</span></span>

## <span data-ttu-id="3e8fa-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e8fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e8fa-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3e8fa-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="3e8fa-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3e8fa-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="3e8fa-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e8fa-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="3e8fa-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e8fa-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
