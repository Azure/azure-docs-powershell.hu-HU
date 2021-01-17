---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466184"
---
# <span data-ttu-id="8c3ed-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8c3ed-101">New-AzDnsZone</span></span>

## <span data-ttu-id="8c3ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3ed-103">Létrehoz egy új DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="8c3ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c3ed-104">SYNTAX</span></span>

### <span data-ttu-id="8c3ed-105">Azonosítók (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c3ed-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3ed-106">Nevek</span><span class="sxs-lookup"><span data-stu-id="8c3ed-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3ed-107">Objektumok</span><span class="sxs-lookup"><span data-stu-id="8c3ed-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c3ed-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c3ed-108">DESCRIPTION</span></span>
<span data-ttu-id="8c3ed-109">A **New-AzDnsZone** parancsmag létrehoz egy új DNS-zónát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="8c3ed-110">A Name paraméterhez egyedi DNS-zónanevet kell megadnia, különben a parancsmag hibát ad vissza. </span><span class="sxs-lookup"><span data-stu-id="8c3ed-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="8c3ed-111">A zóna létrehozása után a New-AzDnsRecordSet parancsmag használatával hozzon létre rekordkészleteket a zónában.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="8c3ed-112">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8c3ed-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c3ed-113">EXAMPLES</span></span>

### <span data-ttu-id="8c3ed-114">1. példa: DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c3ed-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8c3ed-115">Ez a parancs létrehoz egy új DNS-myzone.com nevű dns-zónát a megadott erőforráscsoportban, majd a $Zone tárolja.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="8c3ed-116">2. példa: Privát DNS-zóna létrehozása virtuális hálózati adatok megadásával</span><span class="sxs-lookup"><span data-stu-id="8c3ed-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="8c3ed-117">Ez a parancs létrehoz egy új, myprivatezone.com nevű privát DNS-zónát a megadott erőforráscsoportban egy társított megoldási virtuális hálózattal (megadva az azonosítóját), majd a $Zone tárolja.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="8c3ed-118">3. példa: Privát DNS-zóna létrehozása virtuális hálózati objektumok megadásával</span><span class="sxs-lookup"><span data-stu-id="8c3ed-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="8c3ed-119">Ez $ResVirtualNetwork parancs létrehoz egy új, myprivatezone.com nevű privát DNS-zónát a megadott erőforráscsoportban egy társított megoldási virtuális hálózattal (ezt $ResVirtualNetwork változó nevezi el), majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="8c3ed-120">4. példa: Dns-zóna létrehozása delegálással a szülőzóna nevének megadásával</span><span class="sxs-lookup"><span data-stu-id="8c3ed-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="8c3ed-121">Ez a parancs létrehoz egy új, az mychild.zone.com nevű gyermek DNS-zónát a megadott erőforráscsoportban, és tárolja a $Zone változóban.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="8c3ed-122">Delegálást is hozzáad a szülő DNS-zónához, zone.com gyermekzónában ugyanabban az előfizetésben és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="8c3ed-123">5. példa: Dns-zóna létrehozása delegálással szülőzóna-azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="8c3ed-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="8c3ed-124">Ez a parancs létrehoz egy új, az mychild.zone.com nevű gyermek DNS-zónát a megadott erőforráscsoportban, és tárolja a $Zone változóban.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="8c3ed-125">Delegálást is hozzáad a szülő DNS zone.com nevű szülő DNS-zónához az erőforráscsoport más-rg megadott előfizetésében, megegyezik a létrehozott gyermekzónához.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="8c3ed-126">6. példa: Dns-zóna létrehozása meghatalmazással szülőzóna-objektum megadásával</span><span class="sxs-lookup"><span data-stu-id="8c3ed-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="8c3ed-127">Ez a parancs létrehoz egy új, az mychild.zone.com nevű gyermek DNS-zónát a megadott erőforráscsoportban, és tárolja a $Zone változóban.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="8c3ed-128">Delegálást is hozzáad a SzülőZóna objektumban átadott zone.com DNS-zóna szülő DNS-zónájában.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="8c3ed-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c3ed-129">PARAMETERS</span></span>

### <span data-ttu-id="8c3ed-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3ed-130">-DefaultProfile</span></span>
<span data-ttu-id="8c3ed-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c3ed-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c3ed-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8c3ed-132">-Name</span></span>
<span data-ttu-id="8c3ed-133">A létrehozni szükséges DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="8c3ed-134">-ParentZone</span></span>
<span data-ttu-id="8c3ed-135">A delegáláshoz hozzáadni tervezett szülőzóna teljes neve (záró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="8c3ed-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="8c3ed-136">-ParentZoneId</span></span>
<span data-ttu-id="8c3ed-137">A delegálás hozzáadásához szükséges szülőzóna erőforrás-azonosítója (záró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="8c3ed-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="8c3ed-138">-ParentZoneName</span></span>
<span data-ttu-id="8c3ed-139">A delegáláshoz hozzáadni tervezett szülőzóna teljes neve (záró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="8c3ed-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8c3ed-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="8c3ed-141">Azon virtuális hálózatok listája, amelyek a virtuális gép állomásneveit regisztrálják ebben a DNS-zónában, csak privát zónákhoz érhetők el.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8c3ed-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="8c3ed-143">A virtuális hálózati adatok azon listája, amelyek a virtuális gép állomásnevének rekordjait regisztrálják ebben a DNS-zónában, csak privát zónákhoz érhetők el.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8c3ed-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="8c3ed-145">Az ebben a DNS-zónában lévő rekordok feloldására képes virtuális hálózatok listája, amelyek csak privát zónákhoz érhetők el.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8c3ed-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="8c3ed-147">Az ebben a DNS-zónában lévő rekordok feloldására képes virtuális hálózati adatok listája, amelyek csak privát zónákban érhetők el.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3ed-148">-ResourceGroupName</span></span>
<span data-ttu-id="8c3ed-149">Megadja azt az erőforráscsoportot, amelyben létre kell hoznia a zónát.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c3ed-150">-Tag</span></span>
<span data-ttu-id="8c3ed-151">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c3ed-152">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="8c3ed-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="8c3ed-153">-ZoneType</span></span>
<span data-ttu-id="8c3ed-154">A nyilvános vagy a privát zóna típusa.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="8c3ed-155">A típus nélküli vagy a nyilvános típusú zónák a nyilvános DNS-kiszolgáló repülőgépen érhetők el a DNS-hierarchiában való használatra.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="8c3ed-156">A privát típusú zónák csak a társított virtuális hálózatok készletében láthatók (ez a funkció előzetes verzióban érhető el).</span><span class="sxs-lookup"><span data-stu-id="8c3ed-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="8c3ed-157">Ez a tulajdonság nem módosítható a zónában.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ed-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c3ed-158">-Confirm</span></span>
<span data-ttu-id="8c3ed-159">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3ed-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3ed-160">-WhatIf</span></span>
<span data-ttu-id="8c3ed-161">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c3ed-162">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c3ed-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3ed-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3ed-164">CommonParameters</span></span>
<span data-ttu-id="8c3ed-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3ed-166">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3ed-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3ed-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c3ed-167">INPUTS</span></span>

### <span data-ttu-id="8c3ed-168">System.String</span><span class="sxs-lookup"><span data-stu-id="8c3ed-168">System.String</span></span>

### <span data-ttu-id="8c3ed-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8c3ed-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8c3ed-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8c3ed-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8c3ed-171">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8c3ed-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8c3ed-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8c3ed-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8c3ed-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c3ed-173">OUTPUTS</span></span>

### <span data-ttu-id="8c3ed-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="8c3ed-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="8c3ed-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c3ed-175">NOTES</span></span>
<span data-ttu-id="8c3ed-176">A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8c3ed-177">A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="8c3ed-178">Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatás előtt.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8c3ed-179">Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c3ed-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8c3ed-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c3ed-180">RELATED LINKS</span></span>

[<span data-ttu-id="8c3ed-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8c3ed-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="8c3ed-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8c3ed-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8c3ed-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8c3ed-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
