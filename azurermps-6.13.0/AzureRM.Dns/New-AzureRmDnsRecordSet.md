---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 7f271ee6a946356fe9cbf09379e2e620a240b733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497499"
---
# <span data-ttu-id="a3860-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a3860-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="a3860-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3860-102">SYNOPSIS</span></span>
<span data-ttu-id="a3860-103">DNS-rekordot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a3860-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3860-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3860-104">SYNTAX</span></span>

### <span data-ttu-id="a3860-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3860-105">Fields (Default)</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3860-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="a3860-106">AliasFields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3860-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="a3860-107">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3860-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="a3860-108">AliasObject</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3860-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3860-109">DESCRIPTION</span></span>
<span data-ttu-id="a3860-110">A **New-AzureRmDnsRecordSet** PARANCSMAG új DNS-rekordot hoz létre a megadott névvel és típussal a megadott zónában.</span><span class="sxs-lookup"><span data-stu-id="a3860-110">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="a3860-111">A **rekordhalmaz** -objektum a DNS-rekordok halmaza, azonos névvel és típussal.</span><span class="sxs-lookup"><span data-stu-id="a3860-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="a3860-112">Ne feledje, hogy a név a zónához viszonyítva nem a teljesen minősített név.</span><span class="sxs-lookup"><span data-stu-id="a3860-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="a3860-113">A *DnsRecords* paraméter a rekordtípus rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="a3860-114">Ez a paraméter a DNS-rekordok egy sorát veszi igénybe, amelyet a New-AzureRmDnsRecordConfig-ban építettek.</span><span class="sxs-lookup"><span data-stu-id="a3860-114">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>
<span data-ttu-id="a3860-115">A pipeline operátor segítségével átadhatja a **dnsZone** -objektumot erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, illetve a zóna név szerint is megadható.</span><span class="sxs-lookup"><span data-stu-id="a3860-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="a3860-116">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3860-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a3860-117">Ha egy megfelelő **rekordhalmaz** már létezik (ugyanaz a név és a rekordtípus), meg kell adnia a *felülírási* paramétert, különben a parancsmag nem hoz létre új **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="a3860-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="a3860-118">Példák</span><span class="sxs-lookup"><span data-stu-id="a3860-118">EXAMPLES</span></span>

### <span data-ttu-id="a3860-119">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="a3860-120">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-121">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-122">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="a3860-123">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-124">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-125">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="a3860-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-126">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-126">It contains a single DNS record.</span></span>
<span data-ttu-id="a3860-127">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-128">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-129">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-130">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-131">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-131">It contains a single DNS record.</span></span>
<span data-ttu-id="a3860-132">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-133">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-134">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-135">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-136">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-136">It contains a single DNS record.</span></span>
<span data-ttu-id="a3860-137">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-138">Példa 5: NS típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-139">A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-140">A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-141">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-141">It contains a single DNS record.</span></span>
<span data-ttu-id="a3860-142">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-143">6. példa: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="a3860-144">A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="a3860-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="a3860-145">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-146">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-146">It contains a single DNS record.</span></span>
<span data-ttu-id="a3860-147">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-148">7. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-149">A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-150">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-151">Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="a3860-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="a3860-152">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="a3860-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="a3860-153">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-154">8. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-155">A parancs létrehozza a myzone.com nevű **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="a3860-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-156">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-157">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a3860-157">It contains a single DNS record.</span></span>
<span data-ttu-id="a3860-158">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-159">9. példa: rekordhalmaz létrehozása a Zone APEX-on</span><span class="sxs-lookup"><span data-stu-id="a3860-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-160">A parancs létrehoz egy **rekordhalmazt** a zóna myzone.com csúcsán (vagy gyökerénél).</span><span class="sxs-lookup"><span data-stu-id="a3860-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="a3860-161">Ehhez a rekordtípus neve "@" (a dupla idézőjelekkel együtt) van megadva.</span><span class="sxs-lookup"><span data-stu-id="a3860-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="a3860-162">Nem hozhatók létre CNAME rekordok a zóna csúcsán.</span><span class="sxs-lookup"><span data-stu-id="a3860-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="a3860-163">Ez a DNS-szabványok kényszere; Az Azure DNS-t nem korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="a3860-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="a3860-164">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-165">10 példa: helyettesítőkarakter-rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a3860-166">A parancs létrehozza a \* nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-167">Ez egy helyettesítőkarakter-rekord.</span><span class="sxs-lookup"><span data-stu-id="a3860-167">This is a wildcard record set.</span></span>
<span data-ttu-id="a3860-168">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="a3860-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a3860-169">11-es példa: üres rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3860-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="a3860-170">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a3860-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a3860-171">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="a3860-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a3860-172">Ez egy üres rekord, amely helyőrzőként működik, majd később rekordokat adhat hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="a3860-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="a3860-173">12-es példa: a rekordtípus létrehozása és az összes megerősítés tiltása</span><span class="sxs-lookup"><span data-stu-id="a3860-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="a3860-174">A parancs létrehozza a **rekordhalmazt**.</span><span class="sxs-lookup"><span data-stu-id="a3860-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="a3860-175">A *felülírási* paraméter biztosítja, hogy a rekord felülírja a meglévő, azonos nevű és típusú rekordokat (az adott rekordban meglévő rekordok elvesznek).</span><span class="sxs-lookup"><span data-stu-id="a3860-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="a3860-176">A *Confirm* paraméter $false értékkel letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="a3860-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="a3860-177">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3860-177">PARAMETERS</span></span>

### <span data-ttu-id="a3860-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3860-178">-DefaultProfile</span></span>
<span data-ttu-id="a3860-179">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3860-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3860-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="a3860-180">-DnsRecords</span></span>
<span data-ttu-id="a3860-181">A rekordban szerepeltetni kívánt DNS-rekordok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="a3860-182">A New-AzureRmDnsRecordConfig parancsmaggal DNS-rekord objektumokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="a3860-182">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="a3860-183">További információért olvassa el a példákat.</span><span class="sxs-lookup"><span data-stu-id="a3860-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="a3860-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a3860-184">-Metadata</span></span>
<span data-ttu-id="a3860-185">A rekordhalmazhoz társítani kívánt metaadatok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="a3860-186">A metaadatok a hash-táblázatként megjelölt név-érték párokkal, például @ (@ {"név" = "dept"; "Érték" = "Shopping"}, @ {"név" = "env"; "Value" = "termelés"})</span><span class="sxs-lookup"><span data-stu-id="a3860-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="a3860-187">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3860-187">-Name</span></span>
<span data-ttu-id="a3860-188">A létrehozandó **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="a3860-189">-Átír</span><span class="sxs-lookup"><span data-stu-id="a3860-189">-Overwrite</span></span>
<span data-ttu-id="a3860-190">Jelzi, hogy ez a parancsmag felülírja a megadott **rekordhalmazt** , ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="a3860-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="a3860-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a3860-191">-RecordType</span></span>
<span data-ttu-id="a3860-192">A létrehozandó DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="a3860-193">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a3860-193">Valid values are:</span></span>
- <span data-ttu-id="a3860-194">Egy</span><span class="sxs-lookup"><span data-stu-id="a3860-194">A</span></span>
- <span data-ttu-id="a3860-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="a3860-195">AAAA</span></span>
- <span data-ttu-id="a3860-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="a3860-196">CNAME</span></span>
- <span data-ttu-id="a3860-197">MX</span><span class="sxs-lookup"><span data-stu-id="a3860-197">MX</span></span>
- <span data-ttu-id="a3860-198">NS</span><span class="sxs-lookup"><span data-stu-id="a3860-198">NS</span></span>
- <span data-ttu-id="a3860-199">PTR</span><span class="sxs-lookup"><span data-stu-id="a3860-199">PTR</span></span>
- <span data-ttu-id="a3860-200">SRV</span><span class="sxs-lookup"><span data-stu-id="a3860-200">SRV</span></span>
- <span data-ttu-id="a3860-201">A TXT SOA rekordok automatikusan létrejönnek a zóna létrehozásakor, és nem hozhatók létre manuálisan.</span><span class="sxs-lookup"><span data-stu-id="a3860-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="a3860-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3860-202">-ResourceGroupName</span></span>
<span data-ttu-id="a3860-203">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="a3860-204">A zóna nevének megadásához meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="a3860-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="a3860-205">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="a3860-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a3860-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a3860-206">-TargetResourceId</span></span>
<span data-ttu-id="a3860-207">Alias-cél erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3860-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="a3860-208">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="a3860-208">-Ttl</span></span>
<span data-ttu-id="a3860-209">A DNS-rekordhalmaz élettartamának (TTL) értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3860-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="a3860-210">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="a3860-210">-Zone</span></span>
<span data-ttu-id="a3860-211">Annak a DnsZone a meghatározása, amelyben a **rekordhalmazt** létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="a3860-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="a3860-212">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="a3860-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="a3860-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="a3860-213">-ZoneName</span></span>
<span data-ttu-id="a3860-214">Annak a zónának a nevét adja meg, amelybe a **rekordhalmazt** létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="a3860-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="a3860-215">Meg kell adnia a zónát tartalmazó erőforráscsoportot is a *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="a3860-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a3860-216">Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="a3860-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a3860-217">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3860-217">-Confirm</span></span>
<span data-ttu-id="a3860-218">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3860-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3860-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3860-219">-WhatIf</span></span>
<span data-ttu-id="a3860-220">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3860-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3860-221">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3860-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3860-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3860-222">CommonParameters</span></span>
<span data-ttu-id="a3860-223">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3860-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3860-224">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3860-224">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3860-225">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3860-225">INPUTS</span></span>

### <span data-ttu-id="a3860-226">System. String</span><span class="sxs-lookup"><span data-stu-id="a3860-226">System.String</span></span>

### <span data-ttu-id="a3860-227">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a3860-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a3860-228">Paraméterek: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3860-228">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="a3860-229">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="a3860-229">System.UInt32</span></span>

### <span data-ttu-id="a3860-230">Microsoft. Azure. Management. DNS. models. RecordType</span><span class="sxs-lookup"><span data-stu-id="a3860-230">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="a3860-231">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3860-231">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a3860-232">Microsoft. Azure. Command. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="a3860-232">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>
<span data-ttu-id="a3860-233">Paraméterek: DnsRecords (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3860-233">Parameters: DnsRecords (ByValue)</span></span>

## <span data-ttu-id="a3860-234">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3860-234">OUTPUTS</span></span>

### <span data-ttu-id="a3860-235">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a3860-235">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="a3860-236">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3860-236">NOTES</span></span>
<span data-ttu-id="a3860-237">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3860-237">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a3860-238">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="a3860-238">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="a3860-239">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3860-239">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a3860-240">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3860-240">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a3860-241">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3860-241">RELATED LINKS</span></span>

[<span data-ttu-id="a3860-242">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a3860-242">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="a3860-243">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a3860-243">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="a3860-244">Új – AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a3860-244">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="a3860-245">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a3860-245">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="a3860-246">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a3860-246">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
