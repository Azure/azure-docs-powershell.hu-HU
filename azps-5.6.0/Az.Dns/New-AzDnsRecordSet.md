---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: f1731cb0eceb4474c233db859c3f4edb10461fe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935042"
---
# <span data-ttu-id="b7906-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7906-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="b7906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7906-102">SYNOPSIS</span></span>
<span data-ttu-id="b7906-103">Létrehoz egy DNS-rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="b7906-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="b7906-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7906-104">SYNTAX</span></span>

### <span data-ttu-id="b7906-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7906-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7906-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="b7906-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7906-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="b7906-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7906-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="b7906-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7906-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7906-109">DESCRIPTION</span></span>
<span data-ttu-id="b7906-110">A **New-AzDnsRecordSet** parancsmag létrehoz egy új DNS-rekordkészletet, amely a megadott névvel és a megadott zónába ír be.</span><span class="sxs-lookup"><span data-stu-id="b7906-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="b7906-111">A **RecordSet** objektum azonos nevű és típusú DNS-rekordok készlete.</span><span class="sxs-lookup"><span data-stu-id="b7906-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="b7906-112">Ne feledje, hogy a név a zónához képest van, nem pedig a teljesen minősített név.</span><span class="sxs-lookup"><span data-stu-id="b7906-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="b7906-113">A *DnsRecords* paraméter a rekordkészlet rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7906-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="b7906-114">Ez a paraméter a New-AzDnsRecordConfig használatával felépített DNS-rekordok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b7906-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="b7906-115">A folyamat operátorával **dnsZone-objektumot** is átadhat ennek a parancsmagnak, vagy  átadhatja a **DnsZone-objektumokat** zóna paraméterként, vagy másik lehetőségként név szerint is megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="b7906-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="b7906-116">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="b7906-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b7906-117">Ha már létezik egy megfelelő **RecordSet** (ugyanaz a  név és rekordtípus), meg kell adnia a Felülírás paramétert, ellenkező esetben a parancsmag nem hoz létre új **RecordSetet.**</span><span class="sxs-lookup"><span data-stu-id="b7906-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="b7906-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7906-118">EXAMPLES</span></span>

### <span data-ttu-id="b7906-119">1. példa: A típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="b7906-120">Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-121">A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-122">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="b7906-123">2. példa: AAAA típusú rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-124">Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-125">A rekordkészlet AAAA típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-126">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-126">It contains a single DNS record.</span></span>
<span data-ttu-id="b7906-127">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-128">3. példa: CNAME típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-129">Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-130">A rekordkészlet CNAME típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-131">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-131">It contains a single DNS record.</span></span>
<span data-ttu-id="b7906-132">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-133">4. példa: MX típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-134">Ez a parancs létrehoz egy www **nevű Rekordkészletet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-135">A rekordkészlet MX típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-136">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-136">It contains a single DNS record.</span></span>
<span data-ttu-id="b7906-137">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-138">5. példa: NS típusú rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-139">Ez a parancs létrehoz egy ns1 **nevű Rekordkészletet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-140">A rekordkészlet NS típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-141">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-141">It contains a single DNS record.</span></span>
<span data-ttu-id="b7906-142">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-143">6. példa: PTR típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="b7906-144">Ez a parancs létrehoz egy 4 **nevű RecordSetet** a 3.2.1.in-addr.arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="b7906-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="b7906-145">A rekordkészlet PTR típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-146">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-146">It contains a single DNS record.</span></span>
<span data-ttu-id="b7906-147">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-148">7. példa: SRV típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-149">Ez a parancs létrehoz egy _sip._tcp nevű **RecordSetet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-150">A rekordkészlet típusa SRV, és TTL-1 óra (3600 másodperc) típusú.</span><span class="sxs-lookup"><span data-stu-id="b7906-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-151">Egyetlen DNS-rekordot tartalmaz, amely a 2001.2.3.4-es IP-címre mutat.</span><span class="sxs-lookup"><span data-stu-id="b7906-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="b7906-152">A szolgáltatás (sip) és a protokoll (tcp) a rekordkészlet nevének részeként van megadva, nem pedig a rekordadatok részeként.</span><span class="sxs-lookup"><span data-stu-id="b7906-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="b7906-153">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-154">8. példa: TXT típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-155">Ez a parancs létrehoz egy **RecordSet** nevű szöveget a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-156">A rekordkészlet a TXT típusú, és TTL értéke 1 óra (3600 másodperc).</span><span class="sxs-lookup"><span data-stu-id="b7906-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-157">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b7906-157">It contains a single DNS record.</span></span>
<span data-ttu-id="b7906-158">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-159">9. példa: RecordSet létrehozása a zóna csúcsán</span><span class="sxs-lookup"><span data-stu-id="b7906-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-160">Ezzel a paranccsal **rekordkészletet** hoz létre a zónarekordok myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="b7906-161">Ehhez a rekordkészlet neve "@" (a dupla idézőjelekkel együtt) lesz megadva.</span><span class="sxs-lookup"><span data-stu-id="b7906-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="b7906-162">A CNAME rekordok nem hozhatók létre a zóna csúcsán.</span><span class="sxs-lookup"><span data-stu-id="b7906-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="b7906-163">Ez a DNS-szabványok kényszere; nem korlátozza az Azure DNS-t.</span><span class="sxs-lookup"><span data-stu-id="b7906-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="b7906-164">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-165">10. példa: Helyettesítő karakteres rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="b7906-166">Ez a parancs létrehoz egy \* nevű **Rekordkészletet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-167">Ez egy helyettesítő karakteres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="b7906-167">This is a wildcard record set.</span></span>
<span data-ttu-id="b7906-168">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="b7906-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b7906-169">11. példa: Üres rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7906-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="b7906-170">Ez a parancs létrehoz egy www **nevű Rekordkészletet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b7906-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="b7906-171">A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="b7906-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="b7906-172">Ez egy üres rekordkészlet, amely helyőrzőként működik, amelyhez később rekordokat adhat hozzá.</span><span class="sxs-lookup"><span data-stu-id="b7906-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="b7906-173">12. példa: Rekordkészlet létrehozása és az összes megerősítés mellőzése</span><span class="sxs-lookup"><span data-stu-id="b7906-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="b7906-174">Ezzel a paranccsal **rekordkészletet hoz létre.**</span><span class="sxs-lookup"><span data-stu-id="b7906-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="b7906-175">A *Felülírás* paraméter gondoskodik arról, hogy ez a rekordkészlet felülírja az azonos nevű és típusú meglévő rekordkészleteket (a rekordkészlet meglévő rekordjai elvesznek).</span><span class="sxs-lookup"><span data-stu-id="b7906-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="b7906-176">A *Confirm* paraméter értéke $False a megerősítést kérő üzenet.</span><span class="sxs-lookup"><span data-stu-id="b7906-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="b7906-177">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7906-177">PARAMETERS</span></span>

### <span data-ttu-id="b7906-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7906-178">-DefaultProfile</span></span>
<span data-ttu-id="b7906-179">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7906-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7906-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="b7906-180">-DnsRecords</span></span>
<span data-ttu-id="b7906-181">A rekordkészletbe foglalandó DNS-rekordok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b7906-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="b7906-182">A dns-rekordobjektumok létrehozásához New-AzDnsRecordConfig a New-AzDnsRecordConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b7906-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="b7906-183">További információt a példákban talál.</span><span class="sxs-lookup"><span data-stu-id="b7906-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="b7906-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b7906-184">-Metadata</span></span>
<span data-ttu-id="b7906-185">A RecordSethez társítandó metaadatok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b7906-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="b7906-186">A metaadatok olyan névérték-párok használatával vannak megadva, amelyek kivonattáblákként vannak megadva, például @{"dept"="vásárlás";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="b7906-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="b7906-187">-Name</span><span class="sxs-lookup"><span data-stu-id="b7906-187">-Name</span></span>
<span data-ttu-id="b7906-188">A létrehozni szükséges **RecordSet** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7906-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="b7906-189">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="b7906-189">-Overwrite</span></span>
<span data-ttu-id="b7906-190">Azt jelzi, hogy ez a parancsmag felülírja a megadott **RecordSetet,** ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="b7906-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="b7906-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b7906-191">-RecordType</span></span>
<span data-ttu-id="b7906-192">A létrehozni szükséges DNS-rekord típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b7906-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="b7906-193">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="b7906-193">Valid values are:</span></span>
- <span data-ttu-id="b7906-194">A</span><span class="sxs-lookup"><span data-stu-id="b7906-194">A</span></span>
- <span data-ttu-id="b7906-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="b7906-195">AAAA</span></span>
- <span data-ttu-id="b7906-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="b7906-196">CNAME</span></span>
- <span data-ttu-id="b7906-197">MX</span><span class="sxs-lookup"><span data-stu-id="b7906-197">MX</span></span>
- <span data-ttu-id="b7906-198">NS</span><span class="sxs-lookup"><span data-stu-id="b7906-198">NS</span></span>
- <span data-ttu-id="b7906-199">PTR</span><span class="sxs-lookup"><span data-stu-id="b7906-199">PTR</span></span>
- <span data-ttu-id="b7906-200">SRV</span><span class="sxs-lookup"><span data-stu-id="b7906-200">SRV</span></span>
- <span data-ttu-id="b7906-201">A TXT SOA rekordok a zóna létrehozásakor automatikusan létrejönnek, és nem állíthatók be manuálisan.</span><span class="sxs-lookup"><span data-stu-id="b7906-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="b7906-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7906-202">-ResourceGroupName</span></span>
<span data-ttu-id="b7906-203">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7906-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="b7906-204">A zónanév megadásához *a ZoneName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="b7906-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="b7906-205">Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy DNS Zone-objektumot *ad* át.</span><span class="sxs-lookup"><span data-stu-id="b7906-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b7906-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b7906-206">-TargetResourceId</span></span>
<span data-ttu-id="b7906-207">Alias Target Resource Id.</span><span class="sxs-lookup"><span data-stu-id="b7906-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="b7906-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="b7906-208">-Ttl</span></span>
<span data-ttu-id="b7906-209">A DNS RecordSet időkorrekta (TTL) megadása.</span><span class="sxs-lookup"><span data-stu-id="b7906-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="b7906-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="b7906-210">-Zone</span></span>
<span data-ttu-id="b7906-211">Azt a DnsZone-t adja meg, amelyben létre kell hoznia a **RecordSet rekordkészletet.**</span><span class="sxs-lookup"><span data-stu-id="b7906-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="b7906-212">Másik lehetőségként a *ZoneName* és az *ResourceGroupName* paramétert használva is megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="b7906-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="b7906-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="b7906-213">-ZoneName</span></span>
<span data-ttu-id="b7906-214">Annak a zónának a nevét adja meg, amelyben létre kell hoznia a **RecordSet rekordkészletet.**</span><span class="sxs-lookup"><span data-stu-id="b7906-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="b7906-215">A zónát tartalmazó erőforráscsoportot is meg kell adnia az *ResourceGroupName* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="b7906-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="b7906-216">Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy DNS Zone-objektumot *ad* át.</span><span class="sxs-lookup"><span data-stu-id="b7906-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b7906-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7906-217">-Confirm</span></span>
<span data-ttu-id="b7906-218">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7906-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7906-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7906-219">-WhatIf</span></span>
<span data-ttu-id="b7906-220">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7906-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7906-221">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7906-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7906-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7906-222">CommonParameters</span></span>
<span data-ttu-id="b7906-223">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7906-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7906-224">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7906-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7906-225">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7906-225">INPUTS</span></span>

### <span data-ttu-id="b7906-226">System.String</span><span class="sxs-lookup"><span data-stu-id="b7906-226">System.String</span></span>

### <span data-ttu-id="b7906-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="b7906-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="b7906-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="b7906-228">System.UInt32</span></span>

### <span data-ttu-id="b7906-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="b7906-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="b7906-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7906-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b7906-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="b7906-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="b7906-232">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7906-232">OUTPUTS</span></span>

### <span data-ttu-id="b7906-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7906-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b7906-234">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7906-234">NOTES</span></span>
<span data-ttu-id="b7906-235">A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="b7906-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b7906-236">A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.</span><span class="sxs-lookup"><span data-stu-id="b7906-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b7906-237">Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatás előtt.</span><span class="sxs-lookup"><span data-stu-id="b7906-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b7906-238">Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7906-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b7906-239">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7906-239">RELATED LINKS</span></span>

[<span data-ttu-id="b7906-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b7906-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="b7906-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7906-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="b7906-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b7906-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="b7906-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7906-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="b7906-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7906-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
