---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384788"
---
# <span data-ttu-id="f6f45-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f6f45-101">New-AzPeering</span></span>

## <span data-ttu-id="f6f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f45-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f45-103">Létrehoz egy új társviszony-ARM erőforrást</span><span class="sxs-lookup"><span data-stu-id="f6f45-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="f6f45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6f45-104">SYNTAX</span></span>

### <span data-ttu-id="f6f45-105">Exchange (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6f45-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6f45-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="f6f45-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6f45-107">Közvetlen</span><span class="sxs-lookup"><span data-stu-id="f6f45-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f45-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6f45-108">DESCRIPTION</span></span>
<span data-ttu-id="f6f45-109">Létrehoz egy ARM társviszony-létesítésről az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="f6f45-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="f6f45-110">A csatlakozási objektumok létrehozásáról további információt a [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) vagy [a New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) oldalon talál.</span><span class="sxs-lookup"><span data-stu-id="f6f45-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="f6f45-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6f45-111">EXAMPLES</span></span>

### <span data-ttu-id="f6f45-112">Új közvetlen társviszony létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6f45-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="f6f45-113">Új közvetlen társviszony létrehozása egyetlen kapcsolattal a Seattle-i raktárban a PeerAsn 65000 segítségével</span><span class="sxs-lookup"><span data-stu-id="f6f45-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="f6f45-114">Új Exchange-társviszony létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6f45-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="f6f45-115">Új társviszony-létesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6f45-115">Create a new exchange peering</span></span>

### <span data-ttu-id="f6f45-116">Régi társviszony átalakítása ARM társviszony-létesítéské</span><span class="sxs-lookup"><span data-stu-id="f6f45-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="f6f45-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6f45-117">PARAMETERS</span></span>

### <span data-ttu-id="f6f45-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6f45-118">-AsJob</span></span>
<span data-ttu-id="f6f45-119">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="f6f45-119">Run in the background.</span></span>

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

### <span data-ttu-id="f6f45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f45-120">-DefaultProfile</span></span>
<span data-ttu-id="f6f45-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6f45-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f45-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="f6f45-122">-DirectConnection</span></span>
<span data-ttu-id="f6f45-123">Hozzon létre egy új közvetlen kapcsolatot a parancs New-AzExchangePeeringConnection és egy pipával.</span><span class="sxs-lookup"><span data-stu-id="f6f45-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="f6f45-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="f6f45-124">-ExchangeConnection</span></span>
<span data-ttu-id="f6f45-125">Hozzon létre új Exchange-kapcsolatokat a parancs New-AzExchangePeeringConnection és bevezető vezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="f6f45-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="f6f45-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6f45-126">-InputObject</span></span>
<span data-ttu-id="f6f45-127">Használja Get-AzLegacyPeering objektum beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="f6f45-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="f6f45-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="f6f45-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="f6f45-129">Jelölje ki azt a Microsoft-hálózatot, amelybe társközi partnert szeretne társként társként társként.</span><span class="sxs-lookup"><span data-stu-id="f6f45-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="f6f45-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f6f45-130">-Name</span></span>
<span data-ttu-id="f6f45-131">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="f6f45-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f6f45-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="f6f45-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="f6f45-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span><span class="sxs-lookup"><span data-stu-id="f6f45-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="f6f45-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="f6f45-134">-PeeringLocation</span></span>
<span data-ttu-id="f6f45-135">Az Azure Régiótól eltérő fizikai hely.</span><span class="sxs-lookup"><span data-stu-id="f6f45-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="f6f45-136">A Get-AzPeeringLocation -Kind \<kind\> kulcsként a Város nevet használja.</span><span class="sxs-lookup"><span data-stu-id="f6f45-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="f6f45-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f45-137">-ResourceGroupName</span></span>
<span data-ttu-id="f6f45-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6f45-138">The resource group name.</span></span>

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

### <span data-ttu-id="f6f45-139">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="f6f45-139">-Sku</span></span>
<span data-ttu-id="f6f45-140">Jelölje Basic_Direct_Free vagy Premium_Direct_Free, kivéve, ha kifejezetten másik lehetőséget kell választania.</span><span class="sxs-lookup"><span data-stu-id="f6f45-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="f6f45-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6f45-141">-Tag</span></span>
<span data-ttu-id="f6f45-142">A Microsoft társviszony-létesítő szolgáltatásával társítania kell a címkéket.</span><span class="sxs-lookup"><span data-stu-id="f6f45-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="f6f45-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6f45-143">-Confirm</span></span>
<span data-ttu-id="f6f45-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f6f45-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f45-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f45-145">-WhatIf</span></span>
<span data-ttu-id="f6f45-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f6f45-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6f45-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6f45-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f45-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f45-148">CommonParameters</span></span>
<span data-ttu-id="f6f45-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f45-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f45-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6f45-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f45-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6f45-151">INPUTS</span></span>

### <span data-ttu-id="f6f45-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="f6f45-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f6f45-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f45-153">OUTPUTS</span></span>

### <span data-ttu-id="f6f45-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="f6f45-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f6f45-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6f45-155">NOTES</span></span>

## <span data-ttu-id="f6f45-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6f45-156">RELATED LINKS</span></span>
