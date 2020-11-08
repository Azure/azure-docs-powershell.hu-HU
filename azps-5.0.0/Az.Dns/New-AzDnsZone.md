---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187473"
---
# <span data-ttu-id="b342c-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b342c-101">New-AzDnsZone</span></span>

## <span data-ttu-id="b342c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b342c-102">SYNOPSIS</span></span>
<span data-ttu-id="b342c-103">Új DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="b342c-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="b342c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b342c-104">SYNTAX</span></span>

### <span data-ttu-id="b342c-105">Azonosítók (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b342c-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b342c-106">Nevek</span><span class="sxs-lookup"><span data-stu-id="b342c-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b342c-107">Objektumok</span><span class="sxs-lookup"><span data-stu-id="b342c-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b342c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b342c-108">DESCRIPTION</span></span>
<span data-ttu-id="b342c-109">A **New-AzDnsZone** parancsmag egy új DNS-zónát hoz létre a megadott erőforráscsoport-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="b342c-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="b342c-110">Adjon meg egy egyedi DNS-zóna nevét a *Name* paraméterhez, vagy a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b342c-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="b342c-111">A zóna létrehozása után a New-AzDnsRecordSet parancsmagot használva hozhat létre rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="b342c-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="b342c-112">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b342c-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b342c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b342c-113">EXAMPLES</span></span>

### <span data-ttu-id="b342c-114">Példa 1: DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="b342c-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b342c-115">Ez a parancs létrehoz egy új DNS-zónát a megadott erőforráscsoport myzone.com, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b342c-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b342c-116">2. példa: privát DNS-zóna létrehozása virtuális hálózati azonosítók megadásával</span><span class="sxs-lookup"><span data-stu-id="b342c-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="b342c-117">Ez a parancs létrehoz egy új, myprivatezone.com nevű privát DNS-zónát a megadott erőforráscsoporthoz egy kapcsolódó virtuális hálózattal (megadhatja az AZONOSÍTÓját), majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b342c-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b342c-118">3. példa: privát DNS-zóna létrehozása virtuális hálózati objektumok megadásával</span><span class="sxs-lookup"><span data-stu-id="b342c-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="b342c-119">Ez a parancs létrehoz egy új, myprivatezone.com nevű privát DNS-zónát a megadott erőforráscsoporthoz egy olyan virtuális hálózattal (amelyre $ResVirtualNetwork változó), majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b342c-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b342c-120">Példa 4: DNS-zóna létrehozása delegálással a szülő zóna nevének megadásával</span><span class="sxs-lookup"><span data-stu-id="b342c-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="b342c-121">A parancs létrehoz egy új, mychild.zone.com nevű alárendelt DNS-zónát a megadott erőforráscsoporthoz, és a $Zone változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="b342c-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="b342c-122">Emellett a zone.com nevű szülő DNS-zónában is felveszi a delegálást, ha az ugyanazon az előfizetésben és az erőforrásban van, mint gyermek zóna.</span><span class="sxs-lookup"><span data-stu-id="b342c-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="b342c-123">Példa 5: DNS-zóna létrehozása delegálással a szülő zóna azonosítójának megadásával</span><span class="sxs-lookup"><span data-stu-id="b342c-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="b342c-124">A parancs létrehoz egy új, mychild.zone.com nevű alárendelt DNS-zónát a megadott erőforráscsoporthoz, és a $Zone változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="b342c-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="b342c-125">Emellett a zone.com nevű szülő DNS-zónában is felveszi a delegálást, ha az előfizetése megegyezik a létrehozott gyermektartomány zónájával.</span><span class="sxs-lookup"><span data-stu-id="b342c-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="b342c-126">6. példa: DNS-zóna létrehozása delegálással a szülő Zone objektum megadásával</span><span class="sxs-lookup"><span data-stu-id="b342c-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="b342c-127">A parancs létrehoz egy új, mychild.zone.com nevű alárendelt DNS-zónát a megadott erőforráscsoporthoz, és a $Zone változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="b342c-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="b342c-128">Emellett a zone.com nevű szülő DNS-zónában delegált delegálást is felveszi az ParentZone objektumba.</span><span class="sxs-lookup"><span data-stu-id="b342c-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="b342c-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b342c-129">PARAMETERS</span></span>

### <span data-ttu-id="b342c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b342c-130">-DefaultProfile</span></span>
<span data-ttu-id="b342c-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b342c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b342c-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b342c-132">-Name</span></span>
<span data-ttu-id="b342c-133">A létrehozandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b342c-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="b342c-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="b342c-134">-ParentZone</span></span>
<span data-ttu-id="b342c-135">A fölérendelt zóna teljes neve a delegálás hozzáadásához (lezáró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="b342c-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="b342c-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="b342c-136">-ParentZoneId</span></span>
<span data-ttu-id="b342c-137">A fölérendelt zóna erőforrás-azonosítója a delegálás hozzáadásához (végpont nélkül).</span><span class="sxs-lookup"><span data-stu-id="b342c-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="b342c-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="b342c-138">-ParentZoneName</span></span>
<span data-ttu-id="b342c-139">A fölérendelt zóna teljes neve a delegálás hozzáadásához (lezáró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="b342c-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="b342c-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b342c-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="b342c-141">Azoknak a virtuális hálózatoknak a listája, amelyek regisztrálják a Virtual Machine-állomásnevek rekordjait ebben a DNS-zónában, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="b342c-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b342c-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b342c-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="b342c-143">Azoknak a virtuális hálózati azonosítóknak a listája, amelyek a virtuális gép állomásnevek rekordjait a DNS-zónában regisztrálják, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="b342c-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b342c-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b342c-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="b342c-145">A virtuális hálózatok listája, amelyekkel megoldhatja a DNS-zóna rekordjait, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="b342c-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b342c-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b342c-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="b342c-147">Azon virtuális hálózati azonosítók listája, amelyek képesek a DNS-zónában lévő rekordok megoldására, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="b342c-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b342c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b342c-148">-ResourceGroupName</span></span>
<span data-ttu-id="b342c-149">Azt az erőforráscsoportot adja meg, amelybe a zónát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="b342c-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="b342c-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="b342c-150">-Tag</span></span>
<span data-ttu-id="b342c-151">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b342c-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b342c-152">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b342c-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b342c-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="b342c-153">-ZoneType</span></span>
<span data-ttu-id="b342c-154">A zóna típusa, nyilvános vagy privát.</span><span class="sxs-lookup"><span data-stu-id="b342c-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="b342c-155">A DNS-hierarchiában használható, típus nélküli vagy a nyilvánosságot nem tartalmazó zónák elérhetők a DNS-alapú nyilvános DNS-síkon.</span><span class="sxs-lookup"><span data-stu-id="b342c-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="b342c-156">A magánjellegű típusú zónák csak a kapcsolódó virtuális hálózatok készletével láthatók (ez a funkció előzetes verzió).</span><span class="sxs-lookup"><span data-stu-id="b342c-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="b342c-157">Ezt a tulajdonságot nem lehet zóna esetén módosítani.</span><span class="sxs-lookup"><span data-stu-id="b342c-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="b342c-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b342c-158">-Confirm</span></span>
<span data-ttu-id="b342c-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b342c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b342c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b342c-160">-WhatIf</span></span>
<span data-ttu-id="b342c-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b342c-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b342c-162">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b342c-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b342c-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b342c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b342c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b342c-164">CommonParameters</span></span>
<span data-ttu-id="b342c-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b342c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b342c-166">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b342c-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b342c-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b342c-167">INPUTS</span></span>

### <span data-ttu-id="b342c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="b342c-168">System.String</span></span>

### <span data-ttu-id="b342c-169">System. null ' 1 [[Microsoft. Azure. Management. DNS. models. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b342c-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b342c-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b342c-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b342c-171">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b342c-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b342c-172">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b342c-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b342c-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b342c-173">OUTPUTS</span></span>

### <span data-ttu-id="b342c-174">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b342c-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b342c-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b342c-175">NOTES</span></span>
<span data-ttu-id="b342c-176">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b342c-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b342c-177">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="b342c-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b342c-178">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b342c-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b342c-179">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b342c-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b342c-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b342c-180">RELATED LINKS</span></span>

[<span data-ttu-id="b342c-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b342c-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="b342c-182">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b342c-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="b342c-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b342c-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
