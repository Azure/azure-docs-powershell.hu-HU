---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 67997145a327d7f9e47f4cf346cbfd5e3a6bf0f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672943"
---
# <span data-ttu-id="e5080-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5080-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="e5080-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5080-102">SYNOPSIS</span></span>
<span data-ttu-id="e5080-103">Frissíti egy DNS-zóna tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e5080-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5080-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5080-104">SYNTAX</span></span>

### <span data-ttu-id="e5080-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5080-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5080-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="e5080-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5080-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="e5080-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5080-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5080-108">DESCRIPTION</span></span>
<span data-ttu-id="e5080-109">A **set-AzureRmDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e5080-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="e5080-110">Ez a parancsmag nem frissíti a rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="e5080-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="e5080-111">Átadhatja a **dnsZone** -objektumokat paraméterként vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="e5080-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e5080-112">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5080-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e5080-113">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="e5080-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="e5080-114">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="e5080-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="e5080-115">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="e5080-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="e5080-116">Példák</span><span class="sxs-lookup"><span data-stu-id="e5080-116">EXAMPLES</span></span>

### <span data-ttu-id="e5080-117">Példa 1: DNS-zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="e5080-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="e5080-118">Az első parancs a megadott erőforráscsoporthoz tartozó myzone.com nevű zónát kapja, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5080-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="e5080-119">A második parancs frissíti az $Zone címkéit.</span><span class="sxs-lookup"><span data-stu-id="e5080-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="e5080-120">A végleges parancs véglegesíti a módosítást.</span><span class="sxs-lookup"><span data-stu-id="e5080-120">The final command commits the change.</span></span>

### <span data-ttu-id="e5080-121">2. példa: a zóna címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="e5080-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="e5080-122">Ez a parancs frissíti a myzone.com nevű zóna címkéit anélkül, hogy először explicit módon kapja meg a zónát.</span><span class="sxs-lookup"><span data-stu-id="e5080-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="e5080-123">3. példa: privát zóna társítása virtuális hálózattal az AZONOSÍTÓjának megadásával</span><span class="sxs-lookup"><span data-stu-id="e5080-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="e5080-124">Ez a parancs az AZONOSÍTÓjának megadásával társítja a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet.</span><span class="sxs-lookup"><span data-stu-id="e5080-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="e5080-125">Példa 4: privát zóna virtuális hálózattal való társítása a hálózati objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="e5080-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="e5080-126">Ez a parancs a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet a regisztrációs hálózatként társítja úgy, hogy a Set-AzureRmDnsZone parancsmag által képviselt virtuális hálózati objektumot átadja $vnet változónak.</span><span class="sxs-lookup"><span data-stu-id="e5080-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="e5080-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5080-127">PARAMETERS</span></span>

### <span data-ttu-id="e5080-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5080-128">-DefaultProfile</span></span>
<span data-ttu-id="e5080-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5080-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5080-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5080-130">-Name</span></span>
<span data-ttu-id="e5080-131">A frissítendő DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5080-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="e5080-132">-Átír</span><span class="sxs-lookup"><span data-stu-id="e5080-132">-Overwrite</span></span>
<span data-ttu-id="e5080-133">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="e5080-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="e5080-134">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="e5080-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="e5080-135">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="e5080-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e5080-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e5080-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="e5080-137">Azoknak a virtuális hálózatoknak a listája, amelyek regisztrálják a Virtual Machine-állomásnevek rekordjait ebben a DNS-zónában, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="e5080-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e5080-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e5080-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="e5080-139">Azoknak a virtuális hálózati azonosítóknak a listája, amelyek a virtuális gép állomásnevek rekordjait a DNS-zónában regisztrálják, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="e5080-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e5080-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e5080-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="e5080-141">A virtuális hálózatok listája, amelyekkel megoldhatja a DNS-zóna rekordjait, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="e5080-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e5080-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e5080-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="e5080-143">Azon virtuális hálózati azonosítók listája, amelyek képesek a DNS-zónában lévő rekordok megoldására, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="e5080-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e5080-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5080-144">-ResourceGroupName</span></span>
<span data-ttu-id="e5080-145">A frissítendő zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5080-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="e5080-146">Meg kell adnia a ZoneName paramétert is.</span><span class="sxs-lookup"><span data-stu-id="e5080-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="e5080-147">Azt is megteheti, hogy a zónát egy DnsZone-objektummal, a *Zone* paraméterrel vagy a csővezetékkel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="e5080-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="e5080-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="e5080-148">-Tag</span></span>
<span data-ttu-id="e5080-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e5080-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5080-150">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e5080-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e5080-151">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="e5080-151">-Zone</span></span>
<span data-ttu-id="e5080-152">A frissítendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5080-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="e5080-153">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="e5080-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="e5080-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5080-154">-Confirm</span></span>
<span data-ttu-id="e5080-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5080-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5080-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5080-156">-WhatIf</span></span>
<span data-ttu-id="e5080-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5080-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5080-158">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5080-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5080-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5080-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5080-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5080-160">CommonParameters</span></span>
<span data-ttu-id="e5080-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5080-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5080-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5080-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5080-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5080-163">INPUTS</span></span>

### <span data-ttu-id="e5080-164">System. String</span><span class="sxs-lookup"><span data-stu-id="e5080-164">System.String</span></span>

### <span data-ttu-id="e5080-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5080-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e5080-166">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e5080-166">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e5080-167">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. Common. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e5080-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e5080-168">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e5080-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e5080-169">Paraméterek: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e5080-169">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="e5080-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5080-170">OUTPUTS</span></span>

### <span data-ttu-id="e5080-171">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e5080-171">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="e5080-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5080-172">NOTES</span></span>
<span data-ttu-id="e5080-173">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5080-173">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e5080-174">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="e5080-174">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="e5080-175">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5080-175">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="e5080-176">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5080-176">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e5080-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5080-177">RELATED LINKS</span></span>

[<span data-ttu-id="e5080-178">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5080-178">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="e5080-179">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5080-179">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="e5080-180">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5080-180">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
