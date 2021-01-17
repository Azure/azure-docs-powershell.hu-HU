---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376849"
---
# <span data-ttu-id="6a3e4-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="6a3e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3e4-103">Frissíti egy DNS-zóna tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="6a3e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a3e4-104">SYNTAX</span></span>

### <span data-ttu-id="6a3e4-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a3e4-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3e4-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="6a3e4-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3e4-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="6a3e4-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a3e4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a3e4-108">DESCRIPTION</span></span>
<span data-ttu-id="6a3e4-109">A **Set-AzDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="6a3e4-110">Ez a parancsmag nem frissíti a zónában található rekordkészleteket.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="6a3e4-111">A **DnsZone-objektumokat** paraméterként vagy a folyamat műveleti jelének használatával is átadhatja, vagy megadhatja a *ZoneName* és *az ResourceGroupName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="6a3e4-112">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6a3e4-113">Ha egy DNS-zóna objektumként (a Zone objektum használatával vagy a folyamaton keresztül) halad át, az nem frissül, ha az Azure DNS-ben módosult a helyi DnsZone-objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6a3e4-114">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6a3e4-115">Ezt a viselkedést  letilthatja a Felülírás paraméterrel, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="6a3e4-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a3e4-116">EXAMPLES</span></span>

### <span data-ttu-id="6a3e4-117">1. példa: DNS-zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="6a3e4-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="6a3e4-118">Az első parancs lekérte a myzone.com nevű zónát a megadott erőforráscsoportból, majd a $Zone tárolja.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="6a3e4-119">A második parancs frissíti a $Zone.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="6a3e4-120">Az utolsó parancs véglegesen véglegesi a változtatást.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-120">The final command commits the change.</span></span>

### <span data-ttu-id="6a3e4-121">2. példa: Zóna címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="6a3e4-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="6a3e4-122">Ez a parancs anélkül frissíti az myzone.com zóna címkéit, hogy először explicit módon behozná a zónát.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="6a3e4-123">3. példa: Privát zóna társítása virtuális hálózathoz az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="6a3e4-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="6a3e4-124">Ez a parancs a saját DNS-zóna myprivatezone.com a virtuális hálózat myvnetével regisztrációs hálózatként társítja az azonosító megadásával.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="6a3e4-125">4. példa: Privát zóna társítása virtuális hálózathoz a hálózati objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="6a3e4-126">Ez a parancs regisztrációs hálózatként társítja myprivatezone.com myvnet virtuális hálózattal a privát DNS-zónazónát úgy, hogy egy változó által képviselt virtuális hálózati objektumot továbbítja $vnet Set-AzDnsZone parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="6a3e4-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a3e4-127">PARAMETERS</span></span>

### <span data-ttu-id="6a3e4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3e4-128">-DefaultProfile</span></span>
<span data-ttu-id="6a3e4-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a3e4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a3e4-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6a3e4-130">-Name</span></span>
<span data-ttu-id="6a3e4-131">A frissítenie kell DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="6a3e4-132">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="6a3e4-132">-Overwrite</span></span>
<span data-ttu-id="6a3e4-133">Ha egy DNS-zóna objektumként (a Zone objektum használatával vagy a folyamaton keresztül) halad át, az nem frissül, ha az Azure DNS-ben módosult a helyi DnsZone-objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6a3e4-134">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6a3e4-135">Ezt a viselkedést  letilthatja a Felülírás paraméterrel, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6a3e4-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6a3e4-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="6a3e4-137">Azon virtuális hálózatok listája, amelyek a virtuális gép állomásneveit regisztrálják ebben a DNS-zónában, csak privát zónákhoz érhetők el.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6a3e4-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6a3e4-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="6a3e4-139">A virtuális hálózati adatok azon listája, amelyek a virtuális gép állomásnevének rekordjait regisztrálják ebben a DNS-zónában, csak privát zónákhoz érhetők el.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6a3e4-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6a3e4-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="6a3e4-141">Az ebben a DNS-zónában lévő rekordok feloldására képes virtuális hálózatok listája, amelyek csak privát zónákhoz érhetők el.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6a3e4-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6a3e4-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="6a3e4-143">Az ebben a DNS-zónában lévő rekordok feloldására képes virtuális hálózati adatok listája, amelyek csak privát zónákban érhetők el.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6a3e4-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3e4-144">-ResourceGroupName</span></span>
<span data-ttu-id="6a3e4-145">Annak az erőforráscsoportnak a nevét adja meg, amely a frissíteni kívánt zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="6a3e4-146">A ZoneName paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="6a3e4-147">Másik lehetőségként megadhatja a zónát egy DnsZone-objektummal a *Zone* paraméterrel vagy a folyamattal.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="6a3e4-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a3e4-148">-Tag</span></span>
<span data-ttu-id="6a3e4-149">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a3e4-150">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="6a3e4-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6a3e4-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-151">-Zone</span></span>
<span data-ttu-id="6a3e4-152">Megadja a frissítenie kell a DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="6a3e4-153">Másik lehetőségként a *ZoneName* és az *ResourceGroupName* paramétert használva is megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6a3e4-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a3e4-154">-Confirm</span></span>
<span data-ttu-id="6a3e4-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3e4-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3e4-156">-WhatIf</span></span>
<span data-ttu-id="6a3e4-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a3e4-158">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a3e4-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3e4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3e4-160">CommonParameters</span></span>
<span data-ttu-id="6a3e4-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3e4-162">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3e4-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3e4-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a3e4-163">INPUTS</span></span>

### <span data-ttu-id="6a3e4-164">System.String</span><span class="sxs-lookup"><span data-stu-id="6a3e4-164">System.String</span></span>

### <span data-ttu-id="6a3e4-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a3e4-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6a3e4-166">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a3e4-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a3e4-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6a3e4-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6a3e4-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="6a3e4-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a3e4-169">OUTPUTS</span></span>

### <span data-ttu-id="6a3e4-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="6a3e4-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a3e4-171">NOTES</span></span>
<span data-ttu-id="6a3e4-172">A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6a3e4-173">A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="6a3e4-174">Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6a3e4-175">Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a3e4-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6a3e4-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a3e4-176">RELATED LINKS</span></span>

[<span data-ttu-id="6a3e4-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="6a3e4-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="6a3e4-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a3e4-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
