---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187475"
---
# <span data-ttu-id="b2aa2-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2aa2-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="b2aa2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="b2aa2-103">DNS-rekordot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="b2aa2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2aa2-104">SYNTAX</span></span>

### <span data-ttu-id="b2aa2-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2aa2-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2aa2-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="b2aa2-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2aa2-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="b2aa2-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2aa2-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="b2aa2-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2aa2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2aa2-109">DESCRIPTION</span></span>
<span data-ttu-id="b2aa2-110">A **New-AzDnsRecordSet** PARANCSMAG új DNS-rekordot hoz létre a megadott névvel és típussal a megadott zónában.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="b2aa2-111">A **rekordhalmaz** -objektum a DNS-rekordok halmaza, azonos névvel és típussal.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="b2aa2-112">Ne feledje, hogy a név a zónához viszonyítva nem a teljesen minősített név.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="b2aa2-113">A *DnsRecords* paraméter a rekordtípus rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="b2aa2-114">Ez a paraméter a DNS-rekordok egy sorát veszi igénybe, amelyet a New-AzDnsRecordConfig-ban építettek.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="b2aa2-115">A pipeline operátor segítségével átadhatja a **dnsZone** -objektumot erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, illetve a zóna név szerint is megadható.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="b2aa2-116">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b2aa2-117">Ha egy megfelelő **rekordhalmaz** már létezik (ugyanaz a név és a rekordtípus), meg kell adnia a *felülírási* paramétert, különben a parancsmag nem hoz létre új **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="b2aa2-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="b2aa2-118">Példák</span><span class="sxs-lookup"><span data-stu-id="b2aa2-118">EXAMPLES</span></span>

### <span data-ttu-id="b2aa2-119">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="b2aa2-120">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-121">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-122">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="b2aa2-123">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-124">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-125">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-126">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-126">It contains a single DNS record.</span></span>
<span data-ttu-id="b2aa2-127">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-128">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-129">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-130">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-131">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-131">It contains a single DNS record.</span></span>
<span data-ttu-id="b2aa2-132">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-133">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-134">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-135">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-136">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-136">It contains a single DNS record.</span></span>
<span data-ttu-id="b2aa2-137">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-138">Példa 5: NS típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-139">A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-140">A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-141">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-141">It contains a single DNS record.</span></span>
<span data-ttu-id="b2aa2-142">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-143">6. példa: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-144">A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="b2aa2-145">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-146">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-146">It contains a single DNS record.</span></span>
<span data-ttu-id="b2aa2-147">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-148">7. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-149">A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-150">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-151">Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="b2aa2-152">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="b2aa2-153">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-154">8. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-155">A parancs létrehozza a myzone.com nevű **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="b2aa2-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-156">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-157">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-157">It contains a single DNS record.</span></span>
<span data-ttu-id="b2aa2-158">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-159">9. példa: rekordhalmaz létrehozása a Zone APEX-on</span><span class="sxs-lookup"><span data-stu-id="b2aa2-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-160">A parancs létrehoz egy **rekordhalmazt** a zóna myzone.com csúcsán (vagy gyökerénél).</span><span class="sxs-lookup"><span data-stu-id="b2aa2-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-161">Ehhez a rekordtípus neve "@" (a dupla idézőjelekkel együtt) van megadva.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="b2aa2-162">Nem hozhatók létre CNAME rekordok a zóna csúcsán.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="b2aa2-163">Ez a DNS-szabványok kényszere; Az Azure DNS-t nem korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="b2aa2-164">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-165">10 példa: helyettesítőkarakter-rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b2aa2-166">A parancs létrehozza a \* nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-167">Ez egy helyettesítőkarakter-rekord.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-167">This is a wildcard record set.</span></span>
<span data-ttu-id="b2aa2-168">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b2aa2-169">11-es példa: üres rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="b2aa2-170">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b2aa2-171">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b2aa2-172">Ez egy üres rekord, amely helyőrzőként működik, majd később rekordokat adhat hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="b2aa2-173">12-es példa: a rekordtípus létrehozása és az összes megerősítés tiltása</span><span class="sxs-lookup"><span data-stu-id="b2aa2-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="b2aa2-174">A parancs létrehozza a **rekordhalmazt**.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="b2aa2-175">A *felülírási* paraméter biztosítja, hogy a rekord felülírja a meglévő, azonos nevű és típusú rekordokat (az adott rekordban meglévő rekordok elvesznek).</span><span class="sxs-lookup"><span data-stu-id="b2aa2-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="b2aa2-176">A *Confirm* paraméter $false értékkel letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="b2aa2-177">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2aa2-177">PARAMETERS</span></span>

### <span data-ttu-id="b2aa2-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2aa2-178">-DefaultProfile</span></span>
<span data-ttu-id="b2aa2-179">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2aa2-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2aa2-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="b2aa2-180">-DnsRecords</span></span>
<span data-ttu-id="b2aa2-181">A rekordban szerepeltetni kívánt DNS-rekordok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="b2aa2-182">A New-AzDnsRecordConfig parancsmaggal DNS-rekord objektumokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="b2aa2-183">További információért olvassa el a példákat.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b2aa2-184">-Metadata</span></span>
<span data-ttu-id="b2aa2-185">A rekordhalmazhoz társítani kívánt metaadatok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="b2aa2-186">A metaadatok a hash-táblázatként megjelölt név-érték párokkal, például @ {"dept" = "Shopping"; " env "=" termelés}.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-187">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2aa2-187">-Name</span></span>
<span data-ttu-id="b2aa2-188">A létrehozandó **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="b2aa2-189">-Átír</span><span class="sxs-lookup"><span data-stu-id="b2aa2-189">-Overwrite</span></span>
<span data-ttu-id="b2aa2-190">Jelzi, hogy ez a parancsmag felülírja a megadott **rekordhalmazt** , ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b2aa2-191">-RecordType</span></span>
<span data-ttu-id="b2aa2-192">A létrehozandó DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="b2aa2-193">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b2aa2-193">Valid values are:</span></span>
- <span data-ttu-id="b2aa2-194">Egy</span><span class="sxs-lookup"><span data-stu-id="b2aa2-194">A</span></span>
- <span data-ttu-id="b2aa2-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="b2aa2-195">AAAA</span></span>
- <span data-ttu-id="b2aa2-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="b2aa2-196">CNAME</span></span>
- <span data-ttu-id="b2aa2-197">MX</span><span class="sxs-lookup"><span data-stu-id="b2aa2-197">MX</span></span>
- <span data-ttu-id="b2aa2-198">NS</span><span class="sxs-lookup"><span data-stu-id="b2aa2-198">NS</span></span>
- <span data-ttu-id="b2aa2-199">PTR</span><span class="sxs-lookup"><span data-stu-id="b2aa2-199">PTR</span></span>
- <span data-ttu-id="b2aa2-200">SRV</span><span class="sxs-lookup"><span data-stu-id="b2aa2-200">SRV</span></span>
- <span data-ttu-id="b2aa2-201">A TXT SOA rekordok automatikusan létrejönnek a zóna létrehozásakor, és nem hozhatók létre manuálisan.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2aa2-202">-ResourceGroupName</span></span>
<span data-ttu-id="b2aa2-203">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="b2aa2-204">A zóna nevének megadásához meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="b2aa2-205">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b2aa2-206">-TargetResourceId</span></span>
<span data-ttu-id="b2aa2-207">Alias-cél erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-208">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="b2aa2-208">-Ttl</span></span>
<span data-ttu-id="b2aa2-209">A DNS-rekordhalmaz élettartamának (TTL) értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-210">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="b2aa2-210">-Zone</span></span>
<span data-ttu-id="b2aa2-211">Annak a DnsZone a meghatározása, amelyben a **rekordhalmazt** létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="b2aa2-212">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="b2aa2-213">-ZoneName</span></span>
<span data-ttu-id="b2aa2-214">Annak a zónának a nevét adja meg, amelybe a **rekordhalmazt** létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="b2aa2-215">Meg kell adnia a zónát tartalmazó erőforráscsoportot is a *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="b2aa2-216">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2aa2-217">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b2aa2-217">-Confirm</span></span>
<span data-ttu-id="b2aa2-218">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2aa2-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2aa2-219">-WhatIf</span></span>
<span data-ttu-id="b2aa2-220">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2aa2-221">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2aa2-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2aa2-222">CommonParameters</span></span>
<span data-ttu-id="b2aa2-223">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2aa2-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2aa2-224">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2aa2-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2aa2-225">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2aa2-225">INPUTS</span></span>

### <span data-ttu-id="b2aa2-226">System. String</span><span class="sxs-lookup"><span data-stu-id="b2aa2-226">System.String</span></span>

### <span data-ttu-id="b2aa2-227">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b2aa2-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="b2aa2-228">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="b2aa2-228">System.UInt32</span></span>

### <span data-ttu-id="b2aa2-229">Microsoft. Azure. Management. DNS. models. RecordType</span><span class="sxs-lookup"><span data-stu-id="b2aa2-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="b2aa2-230">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2aa2-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b2aa2-231">Microsoft. Azure. Command. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="b2aa2-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="b2aa2-232">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2aa2-232">OUTPUTS</span></span>

### <span data-ttu-id="b2aa2-233">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2aa2-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b2aa2-234">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2aa2-234">NOTES</span></span>
<span data-ttu-id="b2aa2-235">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b2aa2-236">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b2aa2-237">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-237">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b2aa2-238">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-238">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b2aa2-239">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2aa2-239">RELATED LINKS</span></span>

[<span data-ttu-id="b2aa2-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b2aa2-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="b2aa2-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2aa2-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="b2aa2-242">Új – AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b2aa2-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="b2aa2-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2aa2-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="b2aa2-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2aa2-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
