---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b991b26d8d6fc7a7cfd33ab051619b7192ae0aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670175"
---
# <span data-ttu-id="ed802-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed802-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ed802-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed802-102">SYNOPSIS</span></span>
<span data-ttu-id="ed802-103">Eltávolít egy ExpressRoute-kapcsolatok közötti kapcsolat-összekapcsolási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ed802-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ed802-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed802-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed802-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed802-105">DESCRIPTION</span></span>
<span data-ttu-id="ed802-106">A **Remove-AzExpressRouteCrossConnectionPeering** parancsmag eltávolítja a ExpressRoute-kapcsolatok közötti kapcsolati konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ed802-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ed802-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed802-107">EXAMPLES</span></span>

### <span data-ttu-id="ed802-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="ed802-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="ed802-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed802-109">PARAMETERS</span></span>

### <span data-ttu-id="ed802-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed802-110">-DefaultProfile</span></span>
<span data-ttu-id="ed802-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed802-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed802-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed802-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ed802-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-kereszt kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="ed802-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ed802-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ed802-114">-Force</span></span>
<span data-ttu-id="ed802-115">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="ed802-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ed802-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed802-116">-Name</span></span>
<span data-ttu-id="ed802-117">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="ed802-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ed802-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ed802-118">-PeerAddressType</span></span>
<span data-ttu-id="ed802-119">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="ed802-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="ed802-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed802-120">-Confirm</span></span>
<span data-ttu-id="ed802-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed802-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed802-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed802-122">-WhatIf</span></span>
<span data-ttu-id="ed802-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed802-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed802-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed802-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed802-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed802-125">CommonParameters</span></span>
<span data-ttu-id="ed802-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed802-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed802-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed802-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed802-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed802-128">INPUTS</span></span>

### <span data-ttu-id="ed802-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed802-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ed802-130">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ed802-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ed802-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed802-131">OUTPUTS</span></span>

### <span data-ttu-id="ed802-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed802-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ed802-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed802-133">NOTES</span></span>

## <span data-ttu-id="ed802-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed802-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed802-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed802-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ed802-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed802-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ed802-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed802-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ed802-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed802-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
