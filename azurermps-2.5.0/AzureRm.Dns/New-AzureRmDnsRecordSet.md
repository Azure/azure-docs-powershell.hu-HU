---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848853"
---
# <span data-ttu-id="bec5a-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bec5a-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="bec5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bec5a-102">SYNOPSIS</span></span>
<span data-ttu-id="bec5a-103">DNS-rekordot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bec5a-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bec5a-104">SYNTAX</span></span>

### <span data-ttu-id="bec5a-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="bec5a-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec5a-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="bec5a-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bec5a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bec5a-107">DESCRIPTION</span></span>
<span data-ttu-id="bec5a-108">A **New-AzureRmDnsRecordSet** PARANCSMAG új DNS-rekordot hoz létre a megadott névvel és típussal a megadott zónában.</span><span class="sxs-lookup"><span data-stu-id="bec5a-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="bec5a-109">A **rekordhalmaz** -objektum a DNS-rekordok halmaza, azonos névvel és típussal.</span><span class="sxs-lookup"><span data-stu-id="bec5a-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="bec5a-110">Ne feledje, hogy a név a zónához viszonyítva nem a teljesen minősített név.</span><span class="sxs-lookup"><span data-stu-id="bec5a-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="bec5a-111">A *DnsRecords* paraméter a rekordtípus rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="bec5a-112">Ez a paraméter a DNS-rekordok egy sorát veszi igénybe, amelyet a New-AzureRmDnsRecordConfig-ban építettek.</span><span class="sxs-lookup"><span data-stu-id="bec5a-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="bec5a-113">A pipeline operátor segítségével átadhatja a **dnsZone** -objektumot erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, illetve a zóna név szerint is megadható.</span><span class="sxs-lookup"><span data-stu-id="bec5a-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="bec5a-114">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bec5a-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="bec5a-115">Ha egy megfelelő **rekordhalmaz** már létezik (ugyanaz a név és a rekordtípus), meg kell adnia a *felülírási* paramétert, különben a parancsmag nem hoz létre új **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="bec5a-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="bec5a-116">Példák</span><span class="sxs-lookup"><span data-stu-id="bec5a-116">EXAMPLES</span></span>

### <span data-ttu-id="bec5a-117">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-118">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-119">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-120">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="bec5a-121">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-122">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-123">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bec5a-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-124">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-124">It contains a single DNS record.</span></span>

<span data-ttu-id="bec5a-125">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-126">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-127">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-128">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-129">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-129">It contains a single DNS record.</span></span>

<span data-ttu-id="bec5a-130">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-131">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-132">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-133">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-134">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-134">It contains a single DNS record.</span></span>

<span data-ttu-id="bec5a-135">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-136">Példa 5: NS típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-137">A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-138">A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-139">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-139">It contains a single DNS record.</span></span>

<span data-ttu-id="bec5a-140">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-141">6. példa: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="bec5a-142">A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="bec5a-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="bec5a-143">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-144">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-144">It contains a single DNS record.</span></span>

<span data-ttu-id="bec5a-145">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-146">7. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-147">A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-148">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-149">Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="bec5a-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="bec5a-150">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="bec5a-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="bec5a-151">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-152">8. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-153">A parancs létrehozza a myzone.com nevű **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="bec5a-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-154">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-155">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bec5a-155">It contains a single DNS record.</span></span>

<span data-ttu-id="bec5a-156">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-157">9. példa: rekordhalmaz létrehozása a Zone APEX-on</span><span class="sxs-lookup"><span data-stu-id="bec5a-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-158">A parancs létrehoz egy **rekordhalmazt** a zóna myzone.com csúcsán (vagy gyökerénél).</span><span class="sxs-lookup"><span data-stu-id="bec5a-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-159">Ehhez a rekordtípus neve "@" (a dupla idézőjelekkel együtt) van megadva.</span><span class="sxs-lookup"><span data-stu-id="bec5a-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="bec5a-160">Nem hozhatók létre CNAME rekordok a zóna csúcsán.</span><span class="sxs-lookup"><span data-stu-id="bec5a-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="bec5a-161">Ez a DNS-szabványok kényszere; Az Azure DNS-t nem korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="bec5a-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="bec5a-162">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-163">10 példa: helyettesítőkarakter-rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="bec5a-164">A parancs létrehozza a \* nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-165">Ez egy helyettesítőkarakter-rekord.</span><span class="sxs-lookup"><span data-stu-id="bec5a-165">This is a wildcard record set.</span></span>

<span data-ttu-id="bec5a-166">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="bec5a-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bec5a-167">11-es példa: üres rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="bec5a-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="bec5a-168">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bec5a-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="bec5a-169">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="bec5a-170">Ez egy üres rekord, amely helyőrzőként működik, majd később rekordokat adhat hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="bec5a-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="bec5a-171">12-es példa: a rekordtípus létrehozása és az összes megerősítés tiltása</span><span class="sxs-lookup"><span data-stu-id="bec5a-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="bec5a-172">A parancs létrehozza a **rekordhalmazt**.</span><span class="sxs-lookup"><span data-stu-id="bec5a-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="bec5a-173">A *felülírási* paraméter biztosítja, hogy a rekord felülírja a meglévő, azonos nevű és típusú rekordokat (az adott rekordban meglévő rekordok elvesznek).</span><span class="sxs-lookup"><span data-stu-id="bec5a-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="bec5a-174">A *Confirm* paraméter $false értékkel letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="bec5a-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="bec5a-175">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bec5a-175">PARAMETERS</span></span>

### <span data-ttu-id="bec5a-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="bec5a-176">-DnsRecords</span></span>
<span data-ttu-id="bec5a-177">A rekordban szerepeltetni kívánt DNS-rekordok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="bec5a-178">A New-AzureRmDnsRecordConfig parancsmaggal DNS-rekord objektumokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="bec5a-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="bec5a-179">További információért olvassa el a példákat.</span><span class="sxs-lookup"><span data-stu-id="bec5a-179">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-180">-Force</span><span class="sxs-lookup"><span data-stu-id="bec5a-180">-Force</span></span>
<span data-ttu-id="bec5a-181">Ez a paraméter érvénytelenítve van ennél a parancsmagnál.</span><span class="sxs-lookup"><span data-stu-id="bec5a-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="bec5a-182">A program eltávolítja a jövőbeli kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="bec5a-182">It will be removed in a future release.</span></span>

<span data-ttu-id="bec5a-183">Ha meg szeretné állapítani, hogy a parancsmag kéri-e a comfirmation, használja a *Confirm* paramétert.</span><span class="sxs-lookup"><span data-stu-id="bec5a-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="bec5a-184">-Metadata</span></span>
<span data-ttu-id="bec5a-185">A rekordhalmazhoz társítani kívánt metaadatok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="bec5a-186">A metaadatok a hash-táblázatként megjelölt név-érték párokkal, például @ (@ {"név" = "dept"; "Érték" = "Shopping"}, @ {"név" = "env"; "Value" = "termelés"})</span><span class="sxs-lookup"><span data-stu-id="bec5a-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-187">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bec5a-187">-Name</span></span>
<span data-ttu-id="bec5a-188">A létrehozandó **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-189">-Átír</span><span class="sxs-lookup"><span data-stu-id="bec5a-189">-Overwrite</span></span>
<span data-ttu-id="bec5a-190">Jelzi, hogy ez a parancsmag felülírja a megadott **rekordhalmazt** , ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="bec5a-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="bec5a-191">-RecordType</span></span>
<span data-ttu-id="bec5a-192">A létrehozandó DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="bec5a-193">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bec5a-193">Valid values are:</span></span>

- <span data-ttu-id="bec5a-194">Egy</span><span class="sxs-lookup"><span data-stu-id="bec5a-194">A</span></span>
- <span data-ttu-id="bec5a-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="bec5a-195">AAAA</span></span>
- <span data-ttu-id="bec5a-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="bec5a-196">CNAME</span></span>
- <span data-ttu-id="bec5a-197">MX</span><span class="sxs-lookup"><span data-stu-id="bec5a-197">MX</span></span>
- <span data-ttu-id="bec5a-198">NS</span><span class="sxs-lookup"><span data-stu-id="bec5a-198">NS</span></span>
- <span data-ttu-id="bec5a-199">PTR</span><span class="sxs-lookup"><span data-stu-id="bec5a-199">PTR</span></span>
- <span data-ttu-id="bec5a-200">SRV</span><span class="sxs-lookup"><span data-stu-id="bec5a-200">SRV</span></span>
- <span data-ttu-id="bec5a-201">TXT</span><span class="sxs-lookup"><span data-stu-id="bec5a-201">TXT</span></span>

<span data-ttu-id="bec5a-202">A SOA rekordok automatikusan létrejönnek a zóna létrehozásakor, és nem hozhatók létre manuálisan.</span><span class="sxs-lookup"><span data-stu-id="bec5a-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec5a-203">-ResourceGroupName</span></span>
<span data-ttu-id="bec5a-204">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="bec5a-205">A zóna nevének megadásához meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="bec5a-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="bec5a-206">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="bec5a-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="bec5a-207">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="bec5a-207">-Ttl</span></span>
<span data-ttu-id="bec5a-208">A DNS-rekordhalmaz élettartamának (TTL) értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec5a-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec5a-209">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="bec5a-209">-Zone</span></span>
<span data-ttu-id="bec5a-210">Annak a DnsZone a meghatározása, amelyben a **rekordhalmazt** létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="bec5a-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="bec5a-211">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="bec5a-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="bec5a-212">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="bec5a-212">-ZoneName</span></span>
<span data-ttu-id="bec5a-213">Annak a zónának a nevét adja meg, amelybe a **rekordhalmazt** létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="bec5a-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="bec5a-214">Meg kell adnia a zónát tartalmazó erőforráscsoportot is a *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="bec5a-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="bec5a-215">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="bec5a-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="bec5a-216">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bec5a-216">-Confirm</span></span>
<span data-ttu-id="bec5a-217">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bec5a-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec5a-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec5a-218">-WhatIf</span></span>
<span data-ttu-id="bec5a-219">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bec5a-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec5a-220">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bec5a-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec5a-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec5a-221">CommonParameters</span></span>
<span data-ttu-id="bec5a-222">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bec5a-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec5a-223">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec5a-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec5a-224">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bec5a-224">INPUTS</span></span>

### <span data-ttu-id="bec5a-225">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="bec5a-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="bec5a-226">Ezt a parancsmagot a DnsZone-objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="bec5a-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="bec5a-227">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bec5a-227">OUTPUTS</span></span>

### <span data-ttu-id="bec5a-228">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bec5a-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="bec5a-229">Ez a parancsmag egy **Recordset** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="bec5a-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="bec5a-230">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bec5a-230">NOTES</span></span>
<span data-ttu-id="bec5a-231">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bec5a-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="bec5a-232">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="bec5a-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="bec5a-233">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bec5a-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="bec5a-234">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bec5a-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bec5a-235">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bec5a-235">RELATED LINKS</span></span>

[<span data-ttu-id="bec5a-236">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bec5a-236">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="bec5a-237">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bec5a-237">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="bec5a-238">Új – AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bec5a-238">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="bec5a-239">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bec5a-239">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="bec5a-240">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bec5a-240">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
