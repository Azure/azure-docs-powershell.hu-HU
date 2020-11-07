---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842377"
---
# <span data-ttu-id="13cc0-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13cc0-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="13cc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="13cc0-103">Frissíti egy DNS-zóna tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="13cc0-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="13cc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13cc0-104">SYNTAX</span></span>

### <span data-ttu-id="13cc0-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="13cc0-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13cc0-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="13cc0-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13cc0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="13cc0-107">DESCRIPTION</span></span>
<span data-ttu-id="13cc0-108">A **set-AzDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="13cc0-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="13cc0-109">Ez a parancsmag nem frissíti a rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="13cc0-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="13cc0-110">Átadhatja a **dnsZone** -objektumokat paraméterként vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="13cc0-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="13cc0-111">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13cc0-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="13cc0-112">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="13cc0-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="13cc0-113">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="13cc0-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="13cc0-114">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="13cc0-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="13cc0-115">Példák</span><span class="sxs-lookup"><span data-stu-id="13cc0-115">EXAMPLES</span></span>

### <span data-ttu-id="13cc0-116">Példa 1: DNS-zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="13cc0-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="13cc0-117">Az első parancs a megadott erőforráscsoporthoz tartozó myzone.com nevű zónát kapja, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="13cc0-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="13cc0-118">A második parancs frissíti az $Zone címkéit.</span><span class="sxs-lookup"><span data-stu-id="13cc0-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="13cc0-119">A végleges parancs véglegesíti a módosítást.</span><span class="sxs-lookup"><span data-stu-id="13cc0-119">The final command commits the change.</span></span>

### <span data-ttu-id="13cc0-120">2. példa: a zóna címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="13cc0-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="13cc0-121">Ez a parancs frissíti a myzone.com nevű zóna címkéit anélkül, hogy először explicit módon kapja meg a zónát.</span><span class="sxs-lookup"><span data-stu-id="13cc0-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="13cc0-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13cc0-122">PARAMETERS</span></span>

### <span data-ttu-id="13cc0-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13cc0-123">-Name</span></span>
<span data-ttu-id="13cc0-124">A frissítendő DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13cc0-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13cc0-125">-Átír</span><span class="sxs-lookup"><span data-stu-id="13cc0-125">-Overwrite</span></span>
<span data-ttu-id="13cc0-126">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="13cc0-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="13cc0-127">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="13cc0-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="13cc0-128">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="13cc0-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="13cc0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13cc0-129">-ResourceGroupName</span></span>
<span data-ttu-id="13cc0-130">A frissítendő zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13cc0-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="13cc0-131">Meg kell adnia a ZoneName paramétert is.</span><span class="sxs-lookup"><span data-stu-id="13cc0-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="13cc0-132">Azt is megteheti, hogy a zónát egy DnsZone-objektummal, a *Zone* paraméterrel vagy a csővezetékkel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="13cc0-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13cc0-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="13cc0-133">-Tag</span></span>
<span data-ttu-id="13cc0-134">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="13cc0-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="13cc0-135">Példa:</span><span class="sxs-lookup"><span data-stu-id="13cc0-135">For example:</span></span>

<span data-ttu-id="13cc0-136">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="13cc0-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13cc0-137">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="13cc0-137">-Zone</span></span>
<span data-ttu-id="13cc0-138">A frissítendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="13cc0-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="13cc0-139">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="13cc0-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="13cc0-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13cc0-140">-Confirm</span></span>
<span data-ttu-id="13cc0-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13cc0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13cc0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13cc0-142">-WhatIf</span></span>
<span data-ttu-id="13cc0-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13cc0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13cc0-144">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13cc0-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13cc0-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13cc0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13cc0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13cc0-146">CommonParameters</span></span>
<span data-ttu-id="13cc0-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13cc0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13cc0-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13cc0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13cc0-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13cc0-149">INPUTS</span></span>

### <span data-ttu-id="13cc0-150">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="13cc0-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="13cc0-151">Ezt a parancsmagot a DnsZone-objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="13cc0-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="13cc0-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13cc0-152">OUTPUTS</span></span>

### <span data-ttu-id="13cc0-153">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="13cc0-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="13cc0-154">Ez a parancsmag egy DnsZone-objektumot ad eredményül, amely a frissített DNS-zónát egy új ETAG jelképezi.</span><span class="sxs-lookup"><span data-stu-id="13cc0-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="13cc0-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13cc0-155">NOTES</span></span>
<span data-ttu-id="13cc0-156">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13cc0-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="13cc0-157">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="13cc0-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="13cc0-158">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13cc0-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="13cc0-159">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13cc0-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="13cc0-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13cc0-160">RELATED LINKS</span></span>

[<span data-ttu-id="13cc0-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13cc0-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="13cc0-162">Új – AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13cc0-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="13cc0-163">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13cc0-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)