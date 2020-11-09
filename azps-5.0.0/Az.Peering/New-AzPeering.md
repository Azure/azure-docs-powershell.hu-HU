---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300284"
---
# <span data-ttu-id="a47c1-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a47c1-101">New-AzPeering</span></span>

## <span data-ttu-id="a47c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a47c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a47c1-103">Új társközi erőforrás-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="a47c1-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="a47c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a47c1-104">SYNTAX</span></span>

### <span data-ttu-id="a47c1-105">Exchange (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a47c1-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47c1-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="a47c1-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47c1-107">Közvetlen</span><span class="sxs-lookup"><span data-stu-id="a47c1-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a47c1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a47c1-108">DESCRIPTION</span></span>
<span data-ttu-id="a47c1-109">Az előfizetéshez hozzon létre egy ARM-munkatársat.</span><span class="sxs-lookup"><span data-stu-id="a47c1-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="a47c1-110">További információt az [új AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) vagy a [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) című témakörben talál a kapcsolati objektum létrehozásáról.</span><span class="sxs-lookup"><span data-stu-id="a47c1-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="a47c1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a47c1-111">EXAMPLES</span></span>

### <span data-ttu-id="a47c1-112">Új közvetlen társas nézet létrehozása</span><span class="sxs-lookup"><span data-stu-id="a47c1-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="a47c1-113">Új, közvetlen társközi kapcsolat létrehozása a Seattle-i létesítményben a PeerAsn 65000 használatával</span><span class="sxs-lookup"><span data-stu-id="a47c1-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="a47c1-114">Új Exchange-alapú peer létrehozása</span><span class="sxs-lookup"><span data-stu-id="a47c1-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a47c1-115">Új Exchange-alapú peer létrehozása</span><span class="sxs-lookup"><span data-stu-id="a47c1-115">Create a new exchange peering</span></span>

### <span data-ttu-id="a47c1-116">Korábbi társközi nézet konvertálása az ARM-partnerek számára</span><span class="sxs-lookup"><span data-stu-id="a47c1-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="a47c1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a47c1-117">PARAMETERS</span></span>

### <span data-ttu-id="a47c1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a47c1-118">-AsJob</span></span>
<span data-ttu-id="a47c1-119">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a47c1-119">Run in the background.</span></span>

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

### <span data-ttu-id="a47c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47c1-120">-DefaultProfile</span></span>
<span data-ttu-id="a47c1-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a47c1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a47c1-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="a47c1-122">-DirectConnection</span></span>
<span data-ttu-id="a47c1-123">Új közvetlen kapcsolatok létrehozása a New-AzExchangePeeringConnection és a pipe parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="a47c1-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a47c1-124">-ExchangeConnection</span></span>
<span data-ttu-id="a47c1-125">Új Exchange-kapcsolatok létrehozása a New-AzExchangePeeringConnection és a pipe segítségével a parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="a47c1-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a47c1-126">-InputObject</span></span>
<span data-ttu-id="a47c1-127">Az objektum beolvasásához használja a Get-AzLegacyPeering.</span><span class="sxs-lookup"><span data-stu-id="a47c1-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="a47c1-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="a47c1-129">Jelölje ki a használni kívánt Microsoft-hálózatot.</span><span class="sxs-lookup"><span data-stu-id="a47c1-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a47c1-130">-Name</span></span>
<span data-ttu-id="a47c1-131">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="a47c1-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="a47c1-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="a47c1-133">A társközi ASN-erőforrás azonosítója. az azonosító lekéréséhez használja a Get-AzPeerAsn.</span><span class="sxs-lookup"><span data-stu-id="a47c1-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a47c1-134">-PeeringLocation</span></span>
<span data-ttu-id="a47c1-135">Az Azure-területtől eltérő fizikai hely.</span><span class="sxs-lookup"><span data-stu-id="a47c1-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="a47c1-136">Használja a Get-AzPeeringLocation-Kind ( \<kind\> város neve) nevet kulcsként.</span><span class="sxs-lookup"><span data-stu-id="a47c1-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47c1-137">-ResourceGroupName</span></span>
<span data-ttu-id="a47c1-138">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a47c1-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="a47c1-139">-Sku</span></span>
<span data-ttu-id="a47c1-140">Válassza a Basic_Direct_Free vagy a Premium_Direct_Free lehetőséget, ha kifejezetten azt szeretné, hogy válasszon másik lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="a47c1-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="a47c1-141">-Tag</span></span>
<span data-ttu-id="a47c1-142">A Microsoft társközi szolgáltatásához társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="a47c1-142">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c1-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a47c1-143">-Confirm</span></span>
<span data-ttu-id="a47c1-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a47c1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47c1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47c1-145">-WhatIf</span></span>
<span data-ttu-id="a47c1-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a47c1-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a47c1-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a47c1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47c1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47c1-148">CommonParameters</span></span>
<span data-ttu-id="a47c1-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a47c1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47c1-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a47c1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47c1-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a47c1-151">INPUTS</span></span>

### <span data-ttu-id="a47c1-152">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a47c1-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a47c1-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a47c1-153">OUTPUTS</span></span>

### <span data-ttu-id="a47c1-154">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a47c1-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a47c1-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a47c1-155">NOTES</span></span>

## <span data-ttu-id="a47c1-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a47c1-156">RELATED LINKS</span></span>
