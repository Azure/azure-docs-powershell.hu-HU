---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301424"
---
# <span data-ttu-id="ed130-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed130-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ed130-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed130-102">SYNOPSIS</span></span>
<span data-ttu-id="ed130-103">Eltávolít egy ExpressRoute-kapcsolatok közötti kapcsolat-összekapcsolási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ed130-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ed130-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed130-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed130-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed130-105">DESCRIPTION</span></span>
<span data-ttu-id="ed130-106">A **Remove-AzExpressRouteCrossConnectionPeering** parancsmag eltávolítja a ExpressRoute-kapcsolatok közötti kapcsolati konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ed130-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ed130-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed130-107">EXAMPLES</span></span>

### <span data-ttu-id="ed130-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="ed130-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="ed130-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed130-109">PARAMETERS</span></span>

### <span data-ttu-id="ed130-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed130-110">-DefaultProfile</span></span>
<span data-ttu-id="ed130-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed130-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed130-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed130-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ed130-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-kereszt kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="ed130-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ed130-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ed130-114">-Force</span></span>
<span data-ttu-id="ed130-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed130-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ed130-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed130-116">-Name</span></span>
<span data-ttu-id="ed130-117">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="ed130-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ed130-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ed130-118">-PeerAddressType</span></span>
<span data-ttu-id="ed130-119">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="ed130-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="ed130-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed130-120">-Confirm</span></span>
<span data-ttu-id="ed130-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed130-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed130-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed130-122">-WhatIf</span></span>
<span data-ttu-id="ed130-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed130-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed130-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed130-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed130-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed130-125">CommonParameters</span></span>
<span data-ttu-id="ed130-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed130-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed130-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed130-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed130-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed130-128">INPUTS</span></span>

### <span data-ttu-id="ed130-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed130-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ed130-130">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ed130-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ed130-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed130-131">OUTPUTS</span></span>

### <span data-ttu-id="ed130-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed130-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ed130-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed130-133">NOTES</span></span>

## <span data-ttu-id="ed130-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed130-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed130-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed130-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ed130-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed130-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ed130-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed130-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ed130-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed130-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
