---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: fe7c4550e3f54268e600414f8516095132b72115
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402286"
---
# <span data-ttu-id="03807-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="03807-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="03807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03807-102">SYNOPSIS</span></span>
<span data-ttu-id="03807-103">Eltávolít egy ExpressRoute-kapcsolatközi társviszony-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="03807-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="03807-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03807-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03807-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03807-105">DESCRIPTION</span></span>
<span data-ttu-id="03807-106">A **Remove-AzExpressRouteCrossConnectionPeering** parancsmag eltávolítja az ExpressRoute-kapcsolatközi társviszony-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="03807-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="03807-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03807-107">EXAMPLES</span></span>

### <span data-ttu-id="03807-108">1. példa: Társviszony-konfiguráció eltávolítása ExpressRoute-keresztkapcsolatból</span><span class="sxs-lookup"><span data-stu-id="03807-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="03807-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03807-109">PARAMETERS</span></span>

### <span data-ttu-id="03807-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03807-110">-DefaultProfile</span></span>
<span data-ttu-id="03807-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03807-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03807-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="03807-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="03807-113">Az eltávolítható társviszony-konfigurációt tartalmazó ExpressRoute-keresztkapcsolat.</span><span class="sxs-lookup"><span data-stu-id="03807-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="03807-114">-Force</span><span class="sxs-lookup"><span data-stu-id="03807-114">-Force</span></span>
<span data-ttu-id="03807-115">Ne kérjen megerősítést, ha szeretné felülírni az erőforrást</span><span class="sxs-lookup"><span data-stu-id="03807-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="03807-116">-Name</span><span class="sxs-lookup"><span data-stu-id="03807-116">-Name</span></span>
<span data-ttu-id="03807-117">Az eltávolítható társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="03807-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="03807-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="03807-118">-PeerAddressType</span></span>
<span data-ttu-id="03807-119">A társviszony címjegyzéke</span><span class="sxs-lookup"><span data-stu-id="03807-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="03807-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03807-120">-Confirm</span></span>
<span data-ttu-id="03807-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03807-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03807-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03807-122">-WhatIf</span></span>
<span data-ttu-id="03807-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03807-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03807-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03807-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03807-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03807-125">CommonParameters</span></span>
<span data-ttu-id="03807-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03807-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03807-127">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03807-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03807-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03807-128">INPUTS</span></span>

### <span data-ttu-id="03807-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="03807-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="03807-130">Az "ExpressRouteCrossConnection" paraméter a "PSExpressRouteCrossConnection" típusú értéket fogadja el a folyamatból.</span><span class="sxs-lookup"><span data-stu-id="03807-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="03807-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03807-131">OUTPUTS</span></span>

### <span data-ttu-id="03807-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="03807-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="03807-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03807-133">NOTES</span></span>

## <span data-ttu-id="03807-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03807-134">RELATED LINKS</span></span>

[<span data-ttu-id="03807-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="03807-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)



[<span data-ttu-id="03807-136">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="03807-136">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="03807-137">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="03807-137">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
