---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842390"
---
# <span data-ttu-id="72038-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="72038-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="72038-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72038-102">SYNOPSIS</span></span>
<span data-ttu-id="72038-103">DNS-rekordot ad hozzá egy helyi rekordtípus-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="72038-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72038-104">SYNTAX</span></span>

### <span data-ttu-id="72038-105">Egy</span><span class="sxs-lookup"><span data-stu-id="72038-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="72038-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="72038-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="72038-107">NS</span><span class="sxs-lookup"><span data-stu-id="72038-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="72038-108">MX</span><span class="sxs-lookup"><span data-stu-id="72038-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="72038-109">PTR</span><span class="sxs-lookup"><span data-stu-id="72038-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="72038-110">TXT</span><span class="sxs-lookup"><span data-stu-id="72038-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="72038-111">SRV</span><span class="sxs-lookup"><span data-stu-id="72038-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="72038-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="72038-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="72038-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="72038-113">DESCRIPTION</span></span>
<span data-ttu-id="72038-114">A **Add-AzDnsRecordConfig** PARANCSMAG egy DNS-rekordot ad hozzá egy **Recordset** objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="72038-115">A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.</span><span class="sxs-lookup"><span data-stu-id="72038-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="72038-116">A SOA rekordok akkor jönnek létre, amikor létrejön egy DNS-zóna, és törlődik a DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="72038-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="72038-117">Nem adhat hozzá vagy távolíthat el SOA rekordokat, de szerkesztheti őket.</span><span class="sxs-lookup"><span data-stu-id="72038-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="72038-118">A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="72038-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="72038-119">Példák</span><span class="sxs-lookup"><span data-stu-id="72038-119">EXAMPLES</span></span>

### <span data-ttu-id="72038-120">1. példa: rekord felvétele a rekordba</span><span class="sxs-lookup"><span data-stu-id="72038-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-121">Ez a példa egy rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="72038-122">2. példa: AAAA rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="72038-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-123">Ebben a példában az AAAA-rekordot egy meglévő rekorddal egészíti ki.</span><span class="sxs-lookup"><span data-stu-id="72038-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="72038-124">3. példa: CNAME rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="72038-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-125">Ez a példa CNAME rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="72038-126">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, kezdetben üres rekordnak kell lennie, vagy a meglévő rekordokat el kell távolítani a Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="72038-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="72038-127">4. példa: MX rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="72038-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-128">Ez a példa MX rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="72038-129">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="72038-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="72038-130">Példa 5: NS rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="72038-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-131">Ebben a példában egy NS rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="72038-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="72038-132">Példa 6: PTR rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="72038-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-133">Ebben a példában egy PTR rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="72038-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="72038-134">7. példa: SRV rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="72038-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-135">Ebben a példában egy SRV rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="72038-136">8. példa: TXT rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="72038-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="72038-137">Ez a példa egy TXT rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="72038-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="72038-138">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72038-138">PARAMETERS</span></span>

### <span data-ttu-id="72038-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="72038-139">-Cname</span></span>
<span data-ttu-id="72038-140">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="72038-141">-Exchange</span></span>
<span data-ttu-id="72038-142">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="72038-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="72038-143">-Ipv4Address</span></span>
<span data-ttu-id="72038-144">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-144">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="72038-145">-Ipv6Address</span></span>
<span data-ttu-id="72038-146">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="72038-147">-Nsdname</span></span>
<span data-ttu-id="72038-148">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="72038-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-149">-Port</span><span class="sxs-lookup"><span data-stu-id="72038-149">-Port</span></span>
<span data-ttu-id="72038-150">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-151">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="72038-151">-Preference</span></span>
<span data-ttu-id="72038-152">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-153">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="72038-153">-Priority</span></span>
<span data-ttu-id="72038-154">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="72038-155">-Ptrdname</span></span>
<span data-ttu-id="72038-156">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="72038-157">-RecordSet</span></span>
<span data-ttu-id="72038-158">A szerkesztendő **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-159">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="72038-159">-Target</span></span>
<span data-ttu-id="72038-160">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-161">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="72038-161">-Value</span></span>
<span data-ttu-id="72038-162">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-163">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="72038-163">-Weight</span></span>
<span data-ttu-id="72038-164">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="72038-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72038-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72038-165">CommonParameters</span></span>
<span data-ttu-id="72038-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72038-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72038-167">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72038-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72038-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72038-168">INPUTS</span></span>

### <span data-ttu-id="72038-169">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72038-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="72038-170">Ezt a parancsmagot a **rekordhalmaz** -objektum pipe-ba kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="72038-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="72038-171">Ez a **rekordhalmaz** kapcsolat nélküli megjelenítése, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg az Set-AzDnsRecordSet parancsmagot nem futtatja.</span><span class="sxs-lookup"><span data-stu-id="72038-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="72038-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72038-172">OUTPUTS</span></span>

### <span data-ttu-id="72038-173">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72038-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="72038-174">Ez a parancsmag a módosított **Recordset** objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="72038-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="72038-175">Az átadott objektumot a program közvetlenül módosítja.</span><span class="sxs-lookup"><span data-stu-id="72038-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="72038-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72038-176">NOTES</span></span>

## <span data-ttu-id="72038-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72038-177">RELATED LINKS</span></span>

[<span data-ttu-id="72038-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72038-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="72038-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="72038-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="72038-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72038-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
