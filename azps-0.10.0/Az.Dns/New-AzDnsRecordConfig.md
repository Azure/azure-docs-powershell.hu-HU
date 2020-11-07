---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: 0bc25aecae445ba18634df578de590f514640c07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844010"
---
# <span data-ttu-id="0e4d3-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0e4d3-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="0e4d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4d3-103">Új DNS-rekord helyi objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="0e4d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e4d3-104">SYNTAX</span></span>

### <span data-ttu-id="0e4d3-105">Egy</span><span class="sxs-lookup"><span data-stu-id="0e4d3-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="0e4d3-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-107">NS</span><span class="sxs-lookup"><span data-stu-id="0e4d3-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-108">MX</span><span class="sxs-lookup"><span data-stu-id="0e4d3-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-109">PTR</span><span class="sxs-lookup"><span data-stu-id="0e4d3-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-110">Txt</span><span class="sxs-lookup"><span data-stu-id="0e4d3-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-111">SRV</span><span class="sxs-lookup"><span data-stu-id="0e4d3-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="0e4d3-112">CName</span><span class="sxs-lookup"><span data-stu-id="0e4d3-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="0e4d3-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e4d3-113">DESCRIPTION</span></span>
<span data-ttu-id="0e4d3-114">A **New-AzDnsRecordConfig** parancsmag létrehoz egy helyi **DnsRecord** objektumot.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-114">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="0e4d3-115">A *DnsRecords* paraméterrel megadhatja, hogy milyen rekordok kerüljenek az New-AzDnsRecordSet parancsmagba a rekordban létrehozandó rekordok megadásához.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-115">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="0e4d3-116">Példák</span><span class="sxs-lookup"><span data-stu-id="0e4d3-116">EXAMPLES</span></span>

### <span data-ttu-id="0e4d3-117">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-118">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-119">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-120">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="0e4d3-121">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-122">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-123">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-124">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-124">It contains a single DNS record.</span></span>

<span data-ttu-id="0e4d3-125">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e4d3-126">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-127">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-128">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-129">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-129">It contains a single DNS record.</span></span>

<span data-ttu-id="0e4d3-130">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e4d3-131">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-132">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-133">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-134">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-134">It contains a single DNS record.</span></span>

<span data-ttu-id="0e4d3-135">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e4d3-136">Példa 5: NS típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-137">A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-138">A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-139">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-139">It contains a single DNS record.</span></span>

<span data-ttu-id="0e4d3-140">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e4d3-141">6. példa: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-142">A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="0e4d3-143">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-144">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-144">It contains a single DNS record.</span></span>

<span data-ttu-id="0e4d3-145">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e4d3-146">7. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-147">A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-148">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-149">Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="0e4d3-150">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="0e4d3-151">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e4d3-152">8. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e4d3-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0e4d3-153">A parancs létrehozza a myzone.com nevű **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="0e4d3-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="0e4d3-154">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0e4d3-155">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-155">It contains a single DNS record.</span></span>

<span data-ttu-id="0e4d3-156">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="0e4d3-157">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e4d3-157">PARAMETERS</span></span>

### <span data-ttu-id="0e4d3-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="0e4d3-158">-Cname</span></span>
<span data-ttu-id="0e4d3-159">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0e4d3-160">-Exchange</span></span>
<span data-ttu-id="0e4d3-161">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="0e4d3-162">-Ipv4Address</span></span>
<span data-ttu-id="0e4d3-163">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="0e4d3-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="0e4d3-164">-Ipv6Address</span></span>
<span data-ttu-id="0e4d3-165">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="0e4d3-166">-Nsdname</span></span>
<span data-ttu-id="0e4d3-167">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-168">-Port</span><span class="sxs-lookup"><span data-stu-id="0e4d3-168">-Port</span></span>
<span data-ttu-id="0e4d3-169">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-170">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="0e4d3-170">-Preference</span></span>
<span data-ttu-id="0e4d3-171">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-172">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="0e4d3-172">-Priority</span></span>
<span data-ttu-id="0e4d3-173">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="0e4d3-174">-Ptrdname</span></span>
<span data-ttu-id="0e4d3-175">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-176">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="0e4d3-176">-Target</span></span>
<span data-ttu-id="0e4d3-177">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-178">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="0e4d3-178">-Value</span></span>
<span data-ttu-id="0e4d3-179">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-180">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="0e4d3-180">-Weight</span></span>
<span data-ttu-id="0e4d3-181">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4d3-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4d3-182">CommonParameters</span></span>
<span data-ttu-id="0e4d3-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e4d3-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4d3-184">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e4d3-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4d3-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e4d3-185">INPUTS</span></span>

### <span data-ttu-id="0e4d3-186">Nincs.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-186">None.</span></span>

## <span data-ttu-id="0e4d3-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e4d3-187">OUTPUTS</span></span>

### <span data-ttu-id="0e4d3-188">Microsoft. Azure. Command. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="0e4d3-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="0e4d3-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e4d3-189">NOTES</span></span>

## <span data-ttu-id="0e4d3-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e4d3-190">RELATED LINKS</span></span>

[<span data-ttu-id="0e4d3-191">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0e4d3-191">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="0e4d3-192">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0e4d3-192">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="0e4d3-193">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0e4d3-193">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
