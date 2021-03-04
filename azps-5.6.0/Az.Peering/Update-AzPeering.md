---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0824693c2d9f849b80f36065814f8dc57209a2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937553"
---
# <span data-ttu-id="e7254-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e7254-101">Update-AzPeering</span></span>

## <span data-ttu-id="e7254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7254-102">SYNOPSIS</span></span>
<span data-ttu-id="e7254-103">Beállítja a társviszonyt.</span><span class="sxs-lookup"><span data-stu-id="e7254-103">Sets the Peering.</span></span> <span data-ttu-id="e7254-104">Használja ezt a parancsot a vagy a `Set-AzDirectPeeringConnectionObject` `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="e7254-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="e7254-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7254-105">SYNTAX</span></span>

### <span data-ttu-id="e7254-106">DefaultExchange (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7254-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7254-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="e7254-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7254-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="e7254-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7254-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="e7254-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7254-110">Közvetlen</span><span class="sxs-lookup"><span data-stu-id="e7254-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7254-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="e7254-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7254-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7254-112">DESCRIPTION</span></span>
<span data-ttu-id="e7254-113">A PSPeering objektum beállítja</span><span class="sxs-lookup"><span data-stu-id="e7254-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="e7254-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7254-114">EXAMPLES</span></span>

### <span data-ttu-id="e7254-115">Az Md5 hitelesítési kulcs frissítése</span><span class="sxs-lookup"><span data-stu-id="e7254-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="e7254-116">Az Md5 hitelesítési kulcs beállítja</span><span class="sxs-lookup"><span data-stu-id="e7254-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="e7254-117">UseForPeeringService frissítése</span><span class="sxs-lookup"><span data-stu-id="e7254-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="e7254-118">A társviszony-létesítő szolgáltatás jelzőinek beállítja a használatát</span><span class="sxs-lookup"><span data-stu-id="e7254-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="e7254-119">Az IPv4-cím frissítése exchange-társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="e7254-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="e7254-120">Az Exchange-társviszony Ipv4-címének beállítja az ResourceId használatával</span><span class="sxs-lookup"><span data-stu-id="e7254-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="e7254-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7254-121">PARAMETERS</span></span>

### <span data-ttu-id="e7254-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7254-122">-DefaultProfile</span></span>
<span data-ttu-id="e7254-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7254-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7254-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="e7254-124">-DirectConnection</span></span>
<span data-ttu-id="e7254-125">Hozzon létre egy új közvetlen kapcsolatot a parancs New-AzDirectPeeringConnectionObject és egy pipával.</span><span class="sxs-lookup"><span data-stu-id="e7254-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e7254-126">-ExchangeConnection</span></span>
<span data-ttu-id="e7254-127">Hozzon létre egy új Exchange-kapcsolatot a parancs New-AzExchangePeeringConnectionObject és egy pipával.</span><span class="sxs-lookup"><span data-stu-id="e7254-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7254-128">-InputObject</span></span>
<span data-ttu-id="e7254-129">A Társviszony-objektum</span><span class="sxs-lookup"><span data-stu-id="e7254-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e7254-130">-Name</span></span>
<span data-ttu-id="e7254-131">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="e7254-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7254-132">-ResourceGroupName</span></span>
<span data-ttu-id="e7254-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7254-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7254-134">-ResourceId</span></span>
<span data-ttu-id="e7254-135">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="e7254-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7254-136">-Confirm</span></span>
<span data-ttu-id="e7254-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7254-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7254-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7254-138">-WhatIf</span></span>
<span data-ttu-id="e7254-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7254-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7254-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7254-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7254-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7254-141">CommonParameters</span></span>
<span data-ttu-id="e7254-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7254-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7254-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7254-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7254-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7254-144">INPUTS</span></span>

### <span data-ttu-id="e7254-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e7254-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e7254-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e7254-146">System.String</span></span>

## <span data-ttu-id="e7254-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7254-147">OUTPUTS</span></span>

### <span data-ttu-id="e7254-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e7254-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e7254-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7254-149">NOTES</span></span>

## <span data-ttu-id="e7254-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7254-150">RELATED LINKS</span></span>
