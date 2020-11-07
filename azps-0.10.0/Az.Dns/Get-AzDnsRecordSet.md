---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844033"
---
# <span data-ttu-id="bcda8-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bcda8-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="bcda8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcda8-102">SYNOPSIS</span></span>
<span data-ttu-id="bcda8-103">Megkapja a DNS-rekord halmazát.</span><span class="sxs-lookup"><span data-stu-id="bcda8-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="bcda8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcda8-104">SYNTAX</span></span>

### <span data-ttu-id="bcda8-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="bcda8-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="bcda8-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="bcda8-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="bcda8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcda8-107">DESCRIPTION</span></span>
<span data-ttu-id="bcda8-108">A **Get-AzDnsRecordSet** parancsmag a megadott névvel és típussal kapja meg a DNS-rekordot a megadott zónában.</span><span class="sxs-lookup"><span data-stu-id="bcda8-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="bcda8-109">Ha nem adja meg a *név* -vagy *RecordType* paramétert, ez a parancsmag a megadott típusú rekord összes rekordját visszaadja a zónában.</span><span class="sxs-lookup"><span data-stu-id="bcda8-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="bcda8-110">Ha a *RecordType* paramétert adja meg, a *Name* paramétert azonban nem, ez a parancsmag a megadott rekordtípus összes rekordját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bcda8-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="bcda8-111">A pipeline operátor segítségével átadhatja a **dnsZone** -objektumokat erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, vagy másik lehetőségként a zóna és az erőforráscsoport név szerint is megadható.</span><span class="sxs-lookup"><span data-stu-id="bcda8-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="bcda8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bcda8-112">EXAMPLES</span></span>

### <span data-ttu-id="bcda8-113">1. példa: a bejegyzéstípusok beolvasása megadott névvel és típussal</span><span class="sxs-lookup"><span data-stu-id="bcda8-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="bcda8-114">Ez a parancs a Record Type (rekord) típusú rekordot kapja meg a megadott erőforráscsoport és zóna mezőben, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bcda8-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="bcda8-115">Mivel a *név* -és *RecordType* paraméterek meg vannak adva, csak egy **rekordhalmaz** -objektum van visszaadva.</span><span class="sxs-lookup"><span data-stu-id="bcda8-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="bcda8-116">2. példa: megadott típusú bejegyzéstípusok beszerzése</span><span class="sxs-lookup"><span data-stu-id="bcda8-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="bcda8-117">Ez a parancs a Record Type (A-es) myzone.com egy sorát kapja meg a MyResourceGroup nevű erőforráscsoport nevű zónában, majd a $RecordSets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="bcda8-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="bcda8-118">3. példa: a zóna minden rekordjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="bcda8-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="bcda8-119">Ez a parancs a MyResourceGroup nevű myzone.com nevű zónában minden rekord halmazát beolvassa, majd a $RecordSets változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bcda8-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="bcda8-120">Példa 4: egy zóna összes rekordjának beolvasása DnsZone objektum használatával</span><span class="sxs-lookup"><span data-stu-id="bcda8-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="bcda8-121">Ez a példa a fenti 3 példával egyenértékű.</span><span class="sxs-lookup"><span data-stu-id="bcda8-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="bcda8-122">Ebben az esetben a zóna zóna objektummal van megadva.</span><span class="sxs-lookup"><span data-stu-id="bcda8-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="bcda8-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcda8-123">PARAMETERS</span></span>

### <span data-ttu-id="bcda8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bcda8-124">-Name</span></span>
<span data-ttu-id="bcda8-125">A beolvasott **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcda8-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="bcda8-126">Ha nem adja meg a *Name* paramétert, a függvény a megadott típusú összes rekordot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="bcda8-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcda8-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="bcda8-127">-RecordType</span></span>
<span data-ttu-id="bcda8-128">A parancsmag által kapott DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcda8-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="bcda8-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bcda8-129">Valid values are:</span></span> 

- <span data-ttu-id="bcda8-130">Egy</span><span class="sxs-lookup"><span data-stu-id="bcda8-130">A</span></span>
- <span data-ttu-id="bcda8-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="bcda8-131">AAAA</span></span>
- <span data-ttu-id="bcda8-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="bcda8-132">CNAME</span></span>
- <span data-ttu-id="bcda8-133">MX</span><span class="sxs-lookup"><span data-stu-id="bcda8-133">MX</span></span>
- <span data-ttu-id="bcda8-134">NS</span><span class="sxs-lookup"><span data-stu-id="bcda8-134">NS</span></span>
- <span data-ttu-id="bcda8-135">PTR</span><span class="sxs-lookup"><span data-stu-id="bcda8-135">PTR</span></span>
- <span data-ttu-id="bcda8-136">SOA</span><span class="sxs-lookup"><span data-stu-id="bcda8-136">SOA</span></span>
- <span data-ttu-id="bcda8-137">SRV</span><span class="sxs-lookup"><span data-stu-id="bcda8-137">SRV</span></span>
- <span data-ttu-id="bcda8-138">TXT</span><span class="sxs-lookup"><span data-stu-id="bcda8-138">TXT</span></span>

<span data-ttu-id="bcda8-139">Ha nem adja meg a *RecordType* paramétert, akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="bcda8-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="bcda8-140">Ezzel a parancsmaggal a zóna minden rekordját visszaadja (minden név és típus).</span><span class="sxs-lookup"><span data-stu-id="bcda8-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcda8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcda8-141">-ResourceGroupName</span></span>
<span data-ttu-id="bcda8-142">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcda8-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="bcda8-143">A zóna nevét a *ZoneName* paraméter használatával is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="bcda8-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="bcda8-144">Másik lehetőségként megadhatja a zóna és az erőforráscsoport értékét egy **dnsZone** -objektum átadásával a *Zone* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="bcda8-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="bcda8-145">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="bcda8-145">-Zone</span></span>
<span data-ttu-id="bcda8-146">Azt a DNS-zónát adja meg, amely a parancsmag által beolvasott rekordot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bcda8-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="bcda8-147">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="bcda8-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="bcda8-148">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="bcda8-148">-ZoneName</span></span>
<span data-ttu-id="bcda8-149">A beolvasott rekordot tartalmazó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcda8-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="bcda8-150">A zónát tartalmazó erőforráscsoportot is meg kell adni a *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="bcda8-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="bcda8-151">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="bcda8-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="bcda8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcda8-152">CommonParameters</span></span>
<span data-ttu-id="bcda8-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcda8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcda8-154">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcda8-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcda8-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcda8-155">INPUTS</span></span>

### <span data-ttu-id="bcda8-156">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="bcda8-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="bcda8-157">Ezt a parancsmagot a **dnsZone** -objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="bcda8-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="bcda8-158">A **dnsZone** objektum azt a zónát képviseli, amelyben a **Recordset** objektum keresve van.</span><span class="sxs-lookup"><span data-stu-id="bcda8-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="bcda8-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcda8-159">OUTPUTS</span></span>

### <span data-ttu-id="bcda8-160">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bcda8-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="bcda8-161">Ez a parancsmag egy vagy több olyan objektumot ad eredményül, amely a talált rekordok halmazát képviseli.</span><span class="sxs-lookup"><span data-stu-id="bcda8-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="bcda8-162">A *név* és a *RecordType* paraméter megadása esetén a program legfeljebb egy **rekordhalmazt** ad vissza, máskülönben több **rekordhalmazt** ad vissza tömbként.</span><span class="sxs-lookup"><span data-stu-id="bcda8-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="bcda8-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcda8-163">NOTES</span></span>

## <span data-ttu-id="bcda8-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcda8-164">RELATED LINKS</span></span>

[<span data-ttu-id="bcda8-165">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bcda8-165">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="bcda8-166">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bcda8-166">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="bcda8-167">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bcda8-167">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


