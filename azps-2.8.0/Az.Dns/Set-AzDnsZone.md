---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 42454d41281746e4b95399e74aa4cb7a9c3c7a77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666544"
---
# <span data-ttu-id="5bb51-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bb51-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="5bb51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bb51-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb51-103">Frissíti egy DNS-zóna tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5bb51-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="5bb51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bb51-104">SYNTAX</span></span>

### <span data-ttu-id="5bb51-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bb51-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bb51-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="5bb51-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bb51-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="5bb51-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bb51-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bb51-108">DESCRIPTION</span></span>
<span data-ttu-id="5bb51-109">A **set-AzDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="5bb51-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="5bb51-110">Ez a parancsmag nem frissíti a rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="5bb51-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="5bb51-111">Átadhatja a **dnsZone** -objektumokat paraméterként vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5bb51-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5bb51-112">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bb51-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5bb51-113">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="5bb51-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="5bb51-114">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="5bb51-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="5bb51-115">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="5bb51-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5bb51-116">Példák</span><span class="sxs-lookup"><span data-stu-id="5bb51-116">EXAMPLES</span></span>

### <span data-ttu-id="5bb51-117">Példa 1: DNS-zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="5bb51-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="5bb51-118">Az első parancs a megadott erőforráscsoporthoz tartozó myzone.com nevű zónát kapja, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5bb51-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="5bb51-119">A második parancs frissíti az $Zone címkéit.</span><span class="sxs-lookup"><span data-stu-id="5bb51-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="5bb51-120">A végleges parancs véglegesíti a módosítást.</span><span class="sxs-lookup"><span data-stu-id="5bb51-120">The final command commits the change.</span></span>

### <span data-ttu-id="5bb51-121">2. példa: a zóna címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="5bb51-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="5bb51-122">Ez a parancs frissíti a myzone.com nevű zóna címkéit anélkül, hogy először explicit módon kapja meg a zónát.</span><span class="sxs-lookup"><span data-stu-id="5bb51-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="5bb51-123">3. példa: privát zóna társítása virtuális hálózattal az AZONOSÍTÓjának megadásával</span><span class="sxs-lookup"><span data-stu-id="5bb51-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="5bb51-124">Ez a parancs az AZONOSÍTÓjának megadásával társítja a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet.</span><span class="sxs-lookup"><span data-stu-id="5bb51-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="5bb51-125">Példa 4: privát zóna virtuális hálózattal való társítása a hálózati objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="5bb51-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="5bb51-126">Ez a parancs a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet a regisztrációs hálózatként társítja úgy, hogy a Set-AzDnsZone parancsmag által képviselt virtuális hálózati objektumot átadja $vnet változónak.</span><span class="sxs-lookup"><span data-stu-id="5bb51-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="5bb51-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bb51-127">PARAMETERS</span></span>

### <span data-ttu-id="5bb51-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb51-128">-DefaultProfile</span></span>
<span data-ttu-id="5bb51-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5bb51-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bb51-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bb51-130">-Name</span></span>
<span data-ttu-id="5bb51-131">A frissítendő DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bb51-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-132">-Átír</span><span class="sxs-lookup"><span data-stu-id="5bb51-132">-Overwrite</span></span>
<span data-ttu-id="5bb51-133">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="5bb51-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="5bb51-134">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="5bb51-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="5bb51-135">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="5bb51-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bb51-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="5bb51-137">Azoknak a virtuális hálózatoknak a listája, amelyek regisztrálják a Virtual Machine-állomásnevek rekordjait ebben a DNS-zónában, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="5bb51-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5bb51-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="5bb51-139">Azoknak a virtuális hálózati azonosítóknak a listája, amelyek a virtuális gép állomásnevek rekordjait a DNS-zónában regisztrálják, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="5bb51-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bb51-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="5bb51-141">A virtuális hálózatok listája, amelyekkel megoldhatja a DNS-zóna rekordjait, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="5bb51-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5bb51-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="5bb51-143">Azon virtuális hálózati azonosítók listája, amelyek képesek a DNS-zónában lévő rekordok megoldására, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="5bb51-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb51-144">-ResourceGroupName</span></span>
<span data-ttu-id="5bb51-145">A frissítendő zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bb51-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="5bb51-146">Meg kell adnia a ZoneName paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5bb51-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="5bb51-147">Azt is megteheti, hogy a zónát egy DnsZone-objektummal, a *Zone* paraméterrel vagy a csővezetékkel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="5bb51-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="5bb51-148">-Tag</span></span>
<span data-ttu-id="5bb51-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="5bb51-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5bb51-150">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5bb51-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-151">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="5bb51-151">-Zone</span></span>
<span data-ttu-id="5bb51-152">A frissítendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bb51-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="5bb51-153">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="5bb51-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb51-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bb51-154">-Confirm</span></span>
<span data-ttu-id="5bb51-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bb51-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bb51-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb51-156">-WhatIf</span></span>
<span data-ttu-id="5bb51-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bb51-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bb51-158">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bb51-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bb51-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bb51-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bb51-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb51-160">CommonParameters</span></span>
<span data-ttu-id="5bb51-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bb51-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb51-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bb51-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb51-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bb51-163">INPUTS</span></span>

### <span data-ttu-id="5bb51-164">System. String</span><span class="sxs-lookup"><span data-stu-id="5bb51-164">System.String</span></span>

### <span data-ttu-id="5bb51-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bb51-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5bb51-166">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5bb51-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5bb51-167">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5bb51-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5bb51-168">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="5bb51-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="5bb51-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bb51-169">OUTPUTS</span></span>

### <span data-ttu-id="5bb51-170">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="5bb51-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="5bb51-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bb51-171">NOTES</span></span>
<span data-ttu-id="5bb51-172">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bb51-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5bb51-173">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="5bb51-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="5bb51-174">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bb51-174">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="5bb51-175">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bb51-175">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5bb51-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bb51-176">RELATED LINKS</span></span>

[<span data-ttu-id="5bb51-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bb51-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="5bb51-178">Új – AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bb51-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="5bb51-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bb51-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
