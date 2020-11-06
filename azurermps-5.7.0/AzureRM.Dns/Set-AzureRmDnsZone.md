---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493132"
---
# <span data-ttu-id="70dd0-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="70dd0-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="70dd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="70dd0-103">Frissíti egy DNS-zóna tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="70dd0-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70dd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70dd0-104">SYNTAX</span></span>

### <span data-ttu-id="70dd0-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70dd0-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70dd0-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="70dd0-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70dd0-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="70dd0-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70dd0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="70dd0-108">DESCRIPTION</span></span>
<span data-ttu-id="70dd0-109">A **set-AzureRmDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="70dd0-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="70dd0-110">Ez a parancsmag nem frissíti a rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="70dd0-110">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="70dd0-111">Átadhatja a **dnsZone** -objektumokat paraméterként vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="70dd0-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="70dd0-112">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70dd0-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="70dd0-113">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="70dd0-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="70dd0-114">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="70dd0-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="70dd0-115">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="70dd0-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="70dd0-116">Példák</span><span class="sxs-lookup"><span data-stu-id="70dd0-116">EXAMPLES</span></span>

### <span data-ttu-id="70dd0-117">Példa 1: DNS-zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="70dd0-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="70dd0-118">Az első parancs a megadott erőforráscsoporthoz tartozó myzone.com nevű zónát kapja, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="70dd0-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="70dd0-119">A második parancs frissíti az $Zone címkéit.</span><span class="sxs-lookup"><span data-stu-id="70dd0-119">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="70dd0-120">A végleges parancs véglegesíti a módosítást.</span><span class="sxs-lookup"><span data-stu-id="70dd0-120">The final command commits the change.</span></span>

### <span data-ttu-id="70dd0-121">2. példa: a zóna címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="70dd0-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="70dd0-122">Ez a parancs frissíti a myzone.com nevű zóna címkéit anélkül, hogy először explicit módon kapja meg a zónát.</span><span class="sxs-lookup"><span data-stu-id="70dd0-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="70dd0-123">3. példa: privát zóna társítása virtuális hálózattal az AZONOSÍTÓjának megadásával</span><span class="sxs-lookup"><span data-stu-id="70dd0-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="70dd0-124">Ez a parancs az AZONOSÍTÓjának megadásával társítja a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet.</span><span class="sxs-lookup"><span data-stu-id="70dd0-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="70dd0-125">Példa 4: privát zóna virtuális hálózattal való társítása a hálózati objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="70dd0-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="70dd0-126">Ez a parancs a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet a regisztrációs hálózatként társítja úgy, hogy a Set-AzureRmDnsZone parancsmag által képviselt virtuális hálózati objektumot átadja $vnet változónak.</span><span class="sxs-lookup"><span data-stu-id="70dd0-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="70dd0-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70dd0-127">PARAMETERS</span></span>

### <span data-ttu-id="70dd0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70dd0-128">-DefaultProfile</span></span>
<span data-ttu-id="70dd0-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="70dd0-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70dd0-130">-Name</span></span>
<span data-ttu-id="70dd0-131">A frissítendő DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70dd0-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-132">-Átír</span><span class="sxs-lookup"><span data-stu-id="70dd0-132">-Overwrite</span></span>
<span data-ttu-id="70dd0-133">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="70dd0-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="70dd0-134">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="70dd0-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="70dd0-135">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="70dd0-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70dd0-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="70dd0-137">Azoknak a virtuális hálózatoknak a listája, amelyek regisztrálják a Virtual Machine-állomásnevek rekordjait ebben a DNS-zónában, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="70dd0-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="70dd0-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="70dd0-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="70dd0-139">Azoknak a virtuális hálózati azonosítóknak a listája, amelyek a virtuális gép állomásnevek rekordjait a DNS-zónában regisztrálják, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="70dd0-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="70dd0-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70dd0-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="70dd0-141">A virtuális hálózatok listája, amelyekkel megoldhatja a DNS-zóna rekordjait, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="70dd0-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="70dd0-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="70dd0-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="70dd0-143">Azon virtuális hálózati azonosítók listája, amelyek képesek a DNS-zónában lévő rekordok megoldására, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="70dd0-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="70dd0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70dd0-144">-ResourceGroupName</span></span>
<span data-ttu-id="70dd0-145">A frissítendő zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70dd0-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="70dd0-146">Meg kell adnia a ZoneName paramétert is.</span><span class="sxs-lookup"><span data-stu-id="70dd0-146">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="70dd0-147">Azt is megteheti, hogy a zónát egy DnsZone-objektummal, a *Zone* paraméterrel vagy a csővezetékkel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="70dd0-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="70dd0-148">-Tag</span></span>
<span data-ttu-id="70dd0-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="70dd0-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="70dd0-150">Példa:</span><span class="sxs-lookup"><span data-stu-id="70dd0-150">For example:</span></span>

<span data-ttu-id="70dd0-151">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="70dd0-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-152">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="70dd0-152">-Zone</span></span>
<span data-ttu-id="70dd0-153">A frissítendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70dd0-153">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="70dd0-154">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="70dd0-154">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70dd0-155">-Confirm</span></span>
<span data-ttu-id="70dd0-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70dd0-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70dd0-157">-WhatIf</span></span>
<span data-ttu-id="70dd0-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70dd0-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70dd0-159">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70dd0-159">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70dd0-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70dd0-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dd0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70dd0-161">CommonParameters</span></span>
<span data-ttu-id="70dd0-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70dd0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70dd0-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70dd0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70dd0-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70dd0-164">INPUTS</span></span>

### <span data-ttu-id="70dd0-165">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="70dd0-165">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="70dd0-166">Ezt a parancsmagot a DnsZone-objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="70dd0-166">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="70dd0-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70dd0-167">OUTPUTS</span></span>

### <span data-ttu-id="70dd0-168">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="70dd0-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="70dd0-169">Ez a parancsmag egy DnsZone-objektumot ad eredményül, amely a frissített DNS-zónát egy új ETAG jelképezi.</span><span class="sxs-lookup"><span data-stu-id="70dd0-169">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="70dd0-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70dd0-170">NOTES</span></span>
<span data-ttu-id="70dd0-171">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70dd0-171">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="70dd0-172">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="70dd0-172">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="70dd0-173">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70dd0-173">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="70dd0-174">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70dd0-174">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="70dd0-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70dd0-175">RELATED LINKS</span></span>

[<span data-ttu-id="70dd0-176">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="70dd0-176">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="70dd0-177">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="70dd0-177">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="70dd0-178">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="70dd0-178">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
