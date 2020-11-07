---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844009"
---
# <span data-ttu-id="2414d-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2414d-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="2414d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2414d-102">SYNOPSIS</span></span>
<span data-ttu-id="2414d-103">Eltávolítja a DNS-rekordokat egy helyi rekordtípus-objektumból.</span><span class="sxs-lookup"><span data-stu-id="2414d-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="2414d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2414d-104">SYNTAX</span></span>

### <span data-ttu-id="2414d-105">Egy</span><span class="sxs-lookup"><span data-stu-id="2414d-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="2414d-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="2414d-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="2414d-107">NS</span><span class="sxs-lookup"><span data-stu-id="2414d-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="2414d-108">MX</span><span class="sxs-lookup"><span data-stu-id="2414d-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="2414d-109">PTR</span><span class="sxs-lookup"><span data-stu-id="2414d-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="2414d-110">TXT</span><span class="sxs-lookup"><span data-stu-id="2414d-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="2414d-111">SRV</span><span class="sxs-lookup"><span data-stu-id="2414d-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="2414d-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="2414d-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="2414d-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="2414d-113">DESCRIPTION</span></span>
<span data-ttu-id="2414d-114">A **Remove-AzDnsRecordConfig** parancsmag a Domain Name System (DNS) rekordot egy rekorddal távolítja el.</span><span class="sxs-lookup"><span data-stu-id="2414d-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="2414d-115">A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.</span><span class="sxs-lookup"><span data-stu-id="2414d-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="2414d-116">Ha el szeretne távolítani egy rekordot, a rekordtípus minden mezőjének pontosan egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="2414d-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="2414d-117">A SOA rekordok nem vehetők fel és nem távolíthatók el.</span><span class="sxs-lookup"><span data-stu-id="2414d-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="2414d-118">A rendszer automatikusan létrehozza a SOA-rekordokat, amikor létrejön egy DNS-zóna, és automatikusan törlődik a DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="2414d-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="2414d-119">A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="2414d-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="2414d-120">Példák</span><span class="sxs-lookup"><span data-stu-id="2414d-120">EXAMPLES</span></span>

### <span data-ttu-id="2414d-121">1. példa: rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-122">Ez a példa egy meglévő rekordtípus rekordjainak eltávolítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="2414d-123">Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="2414d-124">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="2414d-125">2. példa: az AAAA rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-126">Ez a példa eltávolítja az AAAA-rekordot egy meglévő rekorddal.</span><span class="sxs-lookup"><span data-stu-id="2414d-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="2414d-127">Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="2414d-128">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="2414d-129">3. példa: CNAME rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-130">Ez a példa eltávolítja a CNAME rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="2414d-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="2414d-131">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="2414d-132">4. példa: MX rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-133">Ebben a példában egy MX rekord törlődik egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="2414d-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="2414d-134">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="2414d-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="2414d-135">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="2414d-136">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="2414d-137">Példa 5: a NÉVKISZOLGÁLÓI rekordok eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-138">Ez a példa eltávolítja a NÉVKISZOLGÁLÓI rekordokat egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="2414d-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="2414d-139">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="2414d-140">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="2414d-141">Példa 6: a PTR rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-142">Ez a példa eltávolítja a PTR rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="2414d-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="2414d-143">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="2414d-144">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="2414d-145">7. példa: SRV rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-146">Ez a példa eltávolítja az SRV rekordot egy meglévő rekorddal.</span><span class="sxs-lookup"><span data-stu-id="2414d-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="2414d-147">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="2414d-148">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="2414d-149">8. példa: TXT rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="2414d-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="2414d-150">Ez a példa eltávolítja a TXT rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="2414d-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="2414d-151">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="2414d-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="2414d-152">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="2414d-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="2414d-153">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2414d-153">PARAMETERS</span></span>

### <span data-ttu-id="2414d-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="2414d-154">-Cname</span></span>
<span data-ttu-id="2414d-155">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="2414d-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="2414d-156">-Exchange</span></span>
<span data-ttu-id="2414d-157">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2414d-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="2414d-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="2414d-158">-Ipv4Address</span></span>
<span data-ttu-id="2414d-159">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="2414d-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="2414d-160">-Ipv6Address</span></span>
<span data-ttu-id="2414d-161">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="2414d-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="2414d-162">-Nsdname</span></span>
<span data-ttu-id="2414d-163">A névkiszolgálói (NS) rekordok névkiszolgálói rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="2414d-164">-Port</span><span class="sxs-lookup"><span data-stu-id="2414d-164">-Port</span></span>
<span data-ttu-id="2414d-165">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="2414d-166">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="2414d-166">-Preference</span></span>
<span data-ttu-id="2414d-167">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="2414d-168">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="2414d-168">-Priority</span></span>
<span data-ttu-id="2414d-169">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="2414d-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="2414d-170">-Ptrdname</span></span>
<span data-ttu-id="2414d-171">A Pointer (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="2414d-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="2414d-172">-RecordSet</span></span>
<span data-ttu-id="2414d-173">Megadja az eltávolítandó rekordot tartalmazó **Recordset** objektumot.</span><span class="sxs-lookup"><span data-stu-id="2414d-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="2414d-174">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="2414d-174">-Target</span></span>
<span data-ttu-id="2414d-175">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="2414d-176">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="2414d-176">-Value</span></span>
<span data-ttu-id="2414d-177">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="2414d-178">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="2414d-178">-Weight</span></span>
<span data-ttu-id="2414d-179">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2414d-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="2414d-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2414d-180">CommonParameters</span></span>
<span data-ttu-id="2414d-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2414d-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2414d-182">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2414d-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2414d-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2414d-183">INPUTS</span></span>

### <span data-ttu-id="2414d-184">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2414d-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="2414d-185">Ezt a parancsmagot a **DnsRecordSet** -objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="2414d-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="2414d-186">Ez a rekord kapcsolat nélküli képviselete, és a frissítés nem módosítja a DNS-válaszokat addig, amíg a set-AzDnsRecordSet nem futtatja.</span><span class="sxs-lookup"><span data-stu-id="2414d-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="2414d-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2414d-187">OUTPUTS</span></span>

### <span data-ttu-id="2414d-188">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2414d-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="2414d-189">Ez a parancsmag a módosított **Recordset** objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2414d-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="2414d-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2414d-190">NOTES</span></span>

## <span data-ttu-id="2414d-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2414d-191">RELATED LINKS</span></span>

[<span data-ttu-id="2414d-192">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2414d-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="2414d-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2414d-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="2414d-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2414d-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
