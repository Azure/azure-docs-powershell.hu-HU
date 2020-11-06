---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500616"
---
# <span data-ttu-id="d2315-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2315-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="d2315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2315-102">SYNOPSIS</span></span>
<span data-ttu-id="d2315-103">Megkapja a DNS-rekord halmazát.</span><span class="sxs-lookup"><span data-stu-id="d2315-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2315-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2315-104">SYNTAX</span></span>

### <span data-ttu-id="d2315-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="d2315-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2315-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="d2315-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2315-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2315-107">DESCRIPTION</span></span>
<span data-ttu-id="d2315-108">A **Get-AzureRmDnsRecordSet** parancsmag a megadott névvel és típussal kapja meg a DNS-rekordot a megadott zónában.</span><span class="sxs-lookup"><span data-stu-id="d2315-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="d2315-109">Ha nem adja meg a *név* -vagy *RecordType* paramétert, ez a parancsmag a megadott típusú rekord összes rekordját visszaadja a zónában.</span><span class="sxs-lookup"><span data-stu-id="d2315-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="d2315-110">Ha a *RecordType* paramétert adja meg, a *Name* paramétert azonban nem, ez a parancsmag a megadott rekordtípus összes rekordját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d2315-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="d2315-111">A pipeline operátor segítségével átadhatja a **dnsZone** -objektumokat erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, vagy másik lehetőségként a zóna és az erőforráscsoport név szerint is megadható.</span><span class="sxs-lookup"><span data-stu-id="d2315-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="d2315-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d2315-112">EXAMPLES</span></span>

### <span data-ttu-id="d2315-113">1. példa: a bejegyzéstípusok beolvasása megadott névvel és típussal</span><span class="sxs-lookup"><span data-stu-id="d2315-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="d2315-114">Ez a parancs a Record Type (rekord) típusú rekordot kapja meg a megadott erőforráscsoport és zóna mezőben, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d2315-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="d2315-115">Mivel a *név* -és *RecordType* paraméterek meg vannak adva, csak egy **rekordhalmaz** -objektum van visszaadva.</span><span class="sxs-lookup"><span data-stu-id="d2315-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="d2315-116">2. példa: megadott típusú bejegyzéstípusok beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2315-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="d2315-117">Ez a parancs a Record Type (A-es) myzone.com egy sorát kapja meg a MyResourceGroup nevű erőforráscsoport nevű zónában, majd a $RecordSets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d2315-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="d2315-118">3. példa: a zóna minden rekordjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="d2315-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="d2315-119">Ez a parancs a MyResourceGroup nevű myzone.com nevű zónában minden rekord halmazát beolvassa, majd a $RecordSets változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d2315-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="d2315-120">Példa 4: egy zóna összes rekordjának beolvasása DnsZone objektum használatával</span><span class="sxs-lookup"><span data-stu-id="d2315-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="d2315-121">Ez a példa a fenti 3 példával egyenértékű.</span><span class="sxs-lookup"><span data-stu-id="d2315-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="d2315-122">Ebben az esetben a zóna zóna objektummal van megadva.</span><span class="sxs-lookup"><span data-stu-id="d2315-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="d2315-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2315-123">PARAMETERS</span></span>

### <span data-ttu-id="d2315-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2315-124">-DefaultProfile</span></span>
<span data-ttu-id="d2315-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d2315-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2315-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2315-126">-Name</span></span>
<span data-ttu-id="d2315-127">A beolvasott **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2315-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="d2315-128">Ha nem adja meg a *Name* paramétert, a függvény a megadott típusú összes rekordot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d2315-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="d2315-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="d2315-129">-RecordType</span></span>
<span data-ttu-id="d2315-130">A parancsmag által kapott DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2315-130">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="d2315-131">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d2315-131">Valid values are:</span></span> 

- <span data-ttu-id="d2315-132">Egy</span><span class="sxs-lookup"><span data-stu-id="d2315-132">A</span></span>
- <span data-ttu-id="d2315-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="d2315-133">AAAA</span></span>
- <span data-ttu-id="d2315-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="d2315-134">CNAME</span></span>
- <span data-ttu-id="d2315-135">MX</span><span class="sxs-lookup"><span data-stu-id="d2315-135">MX</span></span>
- <span data-ttu-id="d2315-136">NS</span><span class="sxs-lookup"><span data-stu-id="d2315-136">NS</span></span>
- <span data-ttu-id="d2315-137">PTR</span><span class="sxs-lookup"><span data-stu-id="d2315-137">PTR</span></span>
- <span data-ttu-id="d2315-138">SOA</span><span class="sxs-lookup"><span data-stu-id="d2315-138">SOA</span></span>
- <span data-ttu-id="d2315-139">SRV</span><span class="sxs-lookup"><span data-stu-id="d2315-139">SRV</span></span>
- <span data-ttu-id="d2315-140">TXT</span><span class="sxs-lookup"><span data-stu-id="d2315-140">TXT</span></span>

<span data-ttu-id="d2315-141">Ha nem adja meg a *RecordType* paramétert, akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="d2315-141">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="d2315-142">Ezzel a parancsmaggal a zóna minden rekordját visszaadja (minden név és típus).</span><span class="sxs-lookup"><span data-stu-id="d2315-142">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="d2315-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2315-143">-ResourceGroupName</span></span>
<span data-ttu-id="d2315-144">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2315-144">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="d2315-145">A zóna nevét a *ZoneName* paraméter használatával is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="d2315-145">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="d2315-146">Másik lehetőségként megadhatja a zóna és az erőforráscsoport értékét egy **dnsZone** -objektum átadásával a *Zone* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="d2315-146">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d2315-147">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="d2315-147">-Zone</span></span>
<span data-ttu-id="d2315-148">Azt a DNS-zónát adja meg, amely a parancsmag által beolvasott rekordot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d2315-148">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="d2315-149">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="d2315-149">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="d2315-150">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="d2315-150">-ZoneName</span></span>
<span data-ttu-id="d2315-151">A beolvasott rekordot tartalmazó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2315-151">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="d2315-152">A zónát tartalmazó erőforráscsoportot is meg kell adni a *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="d2315-152">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="d2315-153">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="d2315-153">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d2315-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2315-154">CommonParameters</span></span>
<span data-ttu-id="d2315-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2315-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2315-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2315-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2315-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2315-157">INPUTS</span></span>

### <span data-ttu-id="d2315-158">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="d2315-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d2315-159">Ezt a parancsmagot a **dnsZone** -objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="d2315-159">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="d2315-160">A **dnsZone** objektum azt a zónát képviseli, amelyben a **Recordset** objektum keresve van.</span><span class="sxs-lookup"><span data-stu-id="d2315-160">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="d2315-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2315-161">OUTPUTS</span></span>

### <span data-ttu-id="d2315-162">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2315-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d2315-163">Ez a parancsmag egy vagy több olyan objektumot ad eredményül, amely a talált rekordok halmazát képviseli.</span><span class="sxs-lookup"><span data-stu-id="d2315-163">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="d2315-164">A *név* és a *RecordType* paraméter megadása esetén a program legfeljebb egy **rekordhalmazt** ad vissza, máskülönben több **rekordhalmazt** ad vissza tömbként.</span><span class="sxs-lookup"><span data-stu-id="d2315-164">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="d2315-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2315-165">NOTES</span></span>

## <span data-ttu-id="d2315-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2315-166">RELATED LINKS</span></span>

[<span data-ttu-id="d2315-167">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2315-167">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d2315-168">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2315-168">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d2315-169">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2315-169">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


