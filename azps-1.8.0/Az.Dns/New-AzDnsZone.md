---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670891"
---
# <span data-ttu-id="8960e-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8960e-101">New-AzDnsZone</span></span>

## <span data-ttu-id="8960e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8960e-102">SYNOPSIS</span></span>
<span data-ttu-id="8960e-103">Új DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="8960e-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="8960e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8960e-104">SYNTAX</span></span>

### <span data-ttu-id="8960e-105">Azonosítók (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8960e-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8960e-106">Objektumok</span><span class="sxs-lookup"><span data-stu-id="8960e-106">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8960e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8960e-107">DESCRIPTION</span></span>
<span data-ttu-id="8960e-108">A **New-AzDnsZone** parancsmag egy új DNS-zónát hoz létre a megadott erőforráscsoport-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="8960e-108">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="8960e-109">Adjon meg egy egyedi DNS-zóna nevét a *Name* paraméterhez, vagy a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8960e-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="8960e-110">A zóna létrehozása után a New-AzDnsRecordSet parancsmagot használva hozhat létre rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="8960e-110">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="8960e-111">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8960e-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8960e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8960e-112">EXAMPLES</span></span>

### <span data-ttu-id="8960e-113">Példa 1: DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="8960e-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8960e-114">Ez a parancs létrehoz egy új DNS-zónát a megadott erőforráscsoport myzone.com, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8960e-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="8960e-115">2. példa: privát DNS-zóna létrehozása virtuális hálózati azonosítók megadásával</span><span class="sxs-lookup"><span data-stu-id="8960e-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="8960e-116">Ez a parancs létrehoz egy új, myprivatezone.com nevű privát DNS-zónát a megadott erőforráscsoporthoz egy kapcsolódó virtuális hálózattal (megadhatja az AZONOSÍTÓját), majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8960e-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="8960e-117">3. példa: privát DNS-zóna létrehozása virtuális hálózati objektumok megadásával</span><span class="sxs-lookup"><span data-stu-id="8960e-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="8960e-118">Ez a parancs létrehoz egy új, myprivatezone.com nevű privát DNS-zónát a megadott erőforráscsoporthoz egy olyan virtuális hálózattal (amelyre $ResVirtualNetwork változó), majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8960e-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="8960e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8960e-119">PARAMETERS</span></span>

### <span data-ttu-id="8960e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8960e-120">-DefaultProfile</span></span>
<span data-ttu-id="8960e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8960e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8960e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8960e-122">-Name</span></span>
<span data-ttu-id="8960e-123">A létrehozandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8960e-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="8960e-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8960e-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="8960e-125">Azoknak a virtuális hálózatoknak a listája, amelyek regisztrálják a Virtual Machine-állomásnevek rekordjait ebben a DNS-zónában, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="8960e-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8960e-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8960e-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="8960e-127">Azoknak a virtuális hálózati azonosítóknak a listája, amelyek a virtuális gép állomásnevek rekordjait a DNS-zónában regisztrálják, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="8960e-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8960e-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8960e-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="8960e-129">A virtuális hálózatok listája, amelyekkel megoldhatja a DNS-zóna rekordjait, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="8960e-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8960e-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8960e-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="8960e-131">Azon virtuális hálózati azonosítók listája, amelyek képesek a DNS-zónában lévő rekordok megoldására, csak a privát zónákhoz.</span><span class="sxs-lookup"><span data-stu-id="8960e-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8960e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8960e-132">-ResourceGroupName</span></span>
<span data-ttu-id="8960e-133">Azt az erőforráscsoportot adja meg, amelybe a zónát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="8960e-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="8960e-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="8960e-134">-Tag</span></span>
<span data-ttu-id="8960e-135">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="8960e-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8960e-136">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="8960e-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8960e-137">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="8960e-137">-ZoneType</span></span>
<span data-ttu-id="8960e-138">A zóna típusa, nyilvános vagy privát.</span><span class="sxs-lookup"><span data-stu-id="8960e-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="8960e-139">A DNS-hierarchiában használható, típus nélküli vagy a nyilvánosságot nem tartalmazó zónák elérhetők a DNS-alapú nyilvános DNS-síkon.</span><span class="sxs-lookup"><span data-stu-id="8960e-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="8960e-140">A magánjellegű típusú zónák csak a kapcsolódó virtuális hálózatok készletével láthatók (ez a funkció előzetes verzió).</span><span class="sxs-lookup"><span data-stu-id="8960e-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="8960e-141">Ezt a tulajdonságot nem lehet zóna esetén módosítani.</span><span class="sxs-lookup"><span data-stu-id="8960e-141">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="8960e-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8960e-142">-Confirm</span></span>
<span data-ttu-id="8960e-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8960e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8960e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8960e-144">-WhatIf</span></span>
<span data-ttu-id="8960e-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8960e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8960e-146">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8960e-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8960e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8960e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8960e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8960e-148">CommonParameters</span></span>
<span data-ttu-id="8960e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8960e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8960e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8960e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8960e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8960e-151">INPUTS</span></span>

### <span data-ttu-id="8960e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8960e-152">System.String</span></span>

### <span data-ttu-id="8960e-153">System. null ' 1 [[Microsoft. Azure. Management. DNS. models. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8960e-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8960e-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8960e-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8960e-155">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8960e-155">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8960e-156">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8960e-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8960e-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8960e-157">OUTPUTS</span></span>

### <span data-ttu-id="8960e-158">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="8960e-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="8960e-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8960e-159">NOTES</span></span>
<span data-ttu-id="8960e-160">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8960e-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8960e-161">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="8960e-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="8960e-162">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8960e-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8960e-163">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8960e-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8960e-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8960e-164">RELATED LINKS</span></span>

[<span data-ttu-id="8960e-165">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8960e-165">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="8960e-166">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8960e-166">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8960e-167">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8960e-167">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
