---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 542056ecfb17254802b8ae06ae3fda8a5995f444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837867"
---
# <span data-ttu-id="7ee73-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7ee73-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="7ee73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ee73-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee73-103">Eltávolít egy ExpressRoute-kapcsolatok közötti kapcsolat-összekapcsolási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7ee73-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="7ee73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ee73-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ee73-105">DESCRIPTION</span></span>
<span data-ttu-id="7ee73-106">A **Remove-AzExpressRouteCrossConnectionPeering** parancsmag eltávolítja a ExpressRoute-kapcsolatok közötti kapcsolati konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7ee73-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="7ee73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ee73-107">EXAMPLES</span></span>

### <span data-ttu-id="7ee73-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="7ee73-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="7ee73-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ee73-109">PARAMETERS</span></span>

### <span data-ttu-id="7ee73-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee73-110">-DefaultProfile</span></span>
<span data-ttu-id="7ee73-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ee73-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ee73-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7ee73-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7ee73-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-kereszt kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="7ee73-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="7ee73-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7ee73-114">-Force</span></span>
<span data-ttu-id="7ee73-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ee73-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7ee73-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ee73-116">-Name</span></span>
<span data-ttu-id="7ee73-117">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7ee73-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="7ee73-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7ee73-118">-PeerAddressType</span></span>
<span data-ttu-id="7ee73-119">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="7ee73-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="7ee73-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ee73-120">-Confirm</span></span>
<span data-ttu-id="7ee73-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ee73-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee73-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee73-122">-WhatIf</span></span>
<span data-ttu-id="7ee73-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ee73-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ee73-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ee73-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee73-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee73-125">CommonParameters</span></span>
<span data-ttu-id="7ee73-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ee73-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee73-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee73-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee73-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ee73-128">INPUTS</span></span>

### <span data-ttu-id="7ee73-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7ee73-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="7ee73-130">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7ee73-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="7ee73-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ee73-131">OUTPUTS</span></span>

### <span data-ttu-id="7ee73-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7ee73-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7ee73-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ee73-133">NOTES</span></span>

## <span data-ttu-id="7ee73-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ee73-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ee73-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7ee73-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7ee73-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7ee73-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7ee73-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7ee73-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="7ee73-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7ee73-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
