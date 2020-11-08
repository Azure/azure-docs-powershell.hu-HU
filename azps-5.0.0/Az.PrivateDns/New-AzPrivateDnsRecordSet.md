---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194203"
---
# <span data-ttu-id="cddc4-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cddc4-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="cddc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cddc4-102">SYNOPSIS</span></span>
<span data-ttu-id="cddc4-103">Létrehozott egy rekordot egy privát DNS-zónában.</span><span class="sxs-lookup"><span data-stu-id="cddc4-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="cddc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cddc4-104">SYNTAX</span></span>

### <span data-ttu-id="cddc4-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cddc4-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddc4-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="cddc4-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddc4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddc4-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cddc4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cddc4-108">DESCRIPTION</span></span>
<span data-ttu-id="cddc4-109">A New-AzPrivateDnsRecordSet parancsmag létrehoz egy új, privát tartománynévrendszer (DNS) rekordot a megadott névvel, és beírja a megadott privát zónába.</span><span class="sxs-lookup"><span data-stu-id="cddc4-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="cddc4-110">A rekordhalmaz-objektum egy olyan személyes DNS-rekord halmaza, amelynek a neve és típusa megegyezik.</span><span class="sxs-lookup"><span data-stu-id="cddc4-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="cddc4-111">Ne feledje, hogy a név a magánjellegű zónához viszonyítva nem a teljesen minősített név.</span><span class="sxs-lookup"><span data-stu-id="cddc4-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="cddc4-112">A PrivateDnsRecord paraméter a rekordtípus rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="cddc4-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="cddc4-113">Ez a paraméter a privát DNS-rekordok tömbjét jeleníti meg, amelyet a New-AzPrivateDnsRecordConfig-hoz építettek.</span><span class="sxs-lookup"><span data-stu-id="cddc4-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="cddc4-114">A pipeline operátor segítségével átadhatja a PSPrivateDnsZone-objektumokat erre a parancsmagra, vagy átadhatja a PSPrivateDnsZone-objektumot a zóna paraméterként, vagy megadhatja a zónát a ResourceId, vagy másik lehetőségként megadhatja a zónát név szerint.</span><span class="sxs-lookup"><span data-stu-id="cddc4-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="cddc4-115">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cddc4-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="cddc4-116">Ha egy megfelelő rekordhalmaz már létezik (ugyanaz a név és a rekordtípus), meg kell adnia a felülírási paramétert, különben a parancsmag nem hoz létre új rekordhalmazt.</span><span class="sxs-lookup"><span data-stu-id="cddc4-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="cddc4-117">Példák</span><span class="sxs-lookup"><span data-stu-id="cddc4-117">EXAMPLES</span></span>

### <span data-ttu-id="cddc4-118">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-119">Ez a példa létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-120">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-121">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cddc4-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="cddc4-122">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-123">Ez a példa létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-124">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="cddc4-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-125">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cddc4-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="cddc4-126">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-127">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-128">Ez a példa létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-129">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-130">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cddc4-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="cddc4-131">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-132">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-133">A parancs létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-134">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-135">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cddc4-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="cddc4-136">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-137">Példa 5: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-138">A parancs létrehoz egy 4 nevű rekordhalmazt a privát Zone 3.2.1.in-addr. arpa nevű rekordhalmazban.</span><span class="sxs-lookup"><span data-stu-id="cddc4-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="cddc4-139">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-140">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cddc4-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="cddc4-141">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-142">6. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-143">A parancs létrehoz egy _sip. _tcp nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-144">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-145">Egyetlen magánhálózati DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="cddc4-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="cddc4-146">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="cddc4-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="cddc4-147">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-148">7. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-149">A parancs létrehoz egy, a privát zóna myzone.com szöveget tartalmazó RecordSet nevű rekordhalmazt.</span><span class="sxs-lookup"><span data-stu-id="cddc4-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-150">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-151">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cddc4-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="cddc4-152">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-153">8. példa: rekordhalmaz létrehozása a Zone APEX-on</span><span class="sxs-lookup"><span data-stu-id="cddc4-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-154">Ez a parancs létrehoz egy rekordhalmazt a privát zóna myzone.com csúcsán (vagy gyökerénél).</span><span class="sxs-lookup"><span data-stu-id="cddc4-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-155">Ehhez a rekordtípus neve "@" (a dupla idézőjelekkel együtt) van megadva.</span><span class="sxs-lookup"><span data-stu-id="cddc4-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="cddc4-156">Nem hozhatók létre CNAME rekordok a zóna csúcsán.</span><span class="sxs-lookup"><span data-stu-id="cddc4-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="cddc4-157">Ez a DNS-szabványok kényszere; Az Azure Private DNS nem korlátozható.</span><span class="sxs-lookup"><span data-stu-id="cddc4-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="cddc4-158">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-159">9 példa: helyettesítőkarakter-rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-160">A parancs létrehozza a \* nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-161">Ez egy helyettesítőkarakter-rekord.</span><span class="sxs-lookup"><span data-stu-id="cddc4-161">This is a wildcard record set.</span></span> <span data-ttu-id="cddc4-162">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="cddc4-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="cddc4-163">10. példa: üres rekordtípus létrehozása</span><span class="sxs-lookup"><span data-stu-id="cddc4-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cddc4-164">A parancs létrehozza a \* nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="cddc4-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="cddc4-165">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="cddc4-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="cddc4-166">Ez egy üres rekord, amely helyőrzőként működik, majd később rekordokat adhat hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="cddc4-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="cddc4-167">11-es példa: a rekordtípus létrehozása és az összes megerősítés tiltása</span><span class="sxs-lookup"><span data-stu-id="cddc4-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="cddc4-168">A parancs létrehozza a rekordhalmazt.</span><span class="sxs-lookup"><span data-stu-id="cddc4-168">This command creates a RecordSet.</span></span> <span data-ttu-id="cddc4-169">A felülírási paraméter biztosítja, hogy a rekord felülírja a meglévő, azonos nevű és típusú rekordokat (az adott rekordban meglévő rekordok elvesznek).</span><span class="sxs-lookup"><span data-stu-id="cddc4-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="cddc4-170">A Confirm paraméter $False értékkel letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="cddc4-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="cddc4-171">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cddc4-171">PARAMETERS</span></span>

### <span data-ttu-id="cddc4-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddc4-172">-DefaultProfile</span></span>
<span data-ttu-id="cddc4-173">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cddc4-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cddc4-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cddc4-174">-Metadata</span></span>
<span data-ttu-id="cddc4-175">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="cddc4-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-176">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cddc4-176">-Name</span></span>
<span data-ttu-id="cddc4-177">Az ebben a rekordban szereplő rekordok neve (a zóna nevéhez és a végpontok nélküli ponthoz viszonyítva).</span><span class="sxs-lookup"><span data-stu-id="cddc4-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-178">-Átír</span><span class="sxs-lookup"><span data-stu-id="cddc4-178">-Overwrite</span></span>
<span data-ttu-id="cddc4-179">Ha a rekordtípus már létezik, ne legyen sikertelen.</span><span class="sxs-lookup"><span data-stu-id="cddc4-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="cddc4-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cddc4-180">-ParentResourceId</span></span>
<span data-ttu-id="cddc4-181">Privát DNS-zóna ResourceID.</span><span class="sxs-lookup"><span data-stu-id="cddc4-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="cddc4-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="cddc4-183">A rekord részét képező magánhálózati DNS-rekordok.</span><span class="sxs-lookup"><span data-stu-id="cddc4-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="cddc4-184">-RecordType</span></span>
<span data-ttu-id="cddc4-185">A saját DNS-rekordok típusa ebben a rekordban.</span><span class="sxs-lookup"><span data-stu-id="cddc4-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddc4-186">-ResourceGroupName</span></span>
<span data-ttu-id="cddc4-187">Az az erőforráscsoport, amelyhez a zóna tartozik.</span><span class="sxs-lookup"><span data-stu-id="cddc4-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-188">-TTL (TTL)</span><span class="sxs-lookup"><span data-stu-id="cddc4-188">-Ttl</span></span>
<span data-ttu-id="cddc4-189">A rekord összes rekordjának TTL-értéke.</span><span class="sxs-lookup"><span data-stu-id="cddc4-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-190">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="cddc4-190">-Zone</span></span>
<span data-ttu-id="cddc4-191">Az a PrivateDnsZone objektum, amely a rekord létrehozásához használt zónát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cddc4-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="cddc4-192">-ZoneName</span></span>
<span data-ttu-id="cddc4-193">Az a zóna, amelyben létre szeretné hozni a rekordot (lezáró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="cddc4-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-194">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cddc4-194">-Confirm</span></span>
<span data-ttu-id="cddc4-195">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cddc4-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddc4-196">-WhatIf</span></span>
<span data-ttu-id="cddc4-197">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cddc4-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cddc4-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cddc4-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddc4-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddc4-199">CommonParameters</span></span>
<span data-ttu-id="cddc4-200">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cddc4-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddc4-201">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cddc4-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddc4-202">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cddc4-202">INPUTS</span></span>

### <span data-ttu-id="cddc4-203">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cddc4-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="cddc4-204">System. String</span><span class="sxs-lookup"><span data-stu-id="cddc4-204">System.String</span></span>

## <span data-ttu-id="cddc4-205">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cddc4-205">OUTPUTS</span></span>

### <span data-ttu-id="cddc4-206">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cddc4-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="cddc4-207">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cddc4-207">NOTES</span></span>

## <span data-ttu-id="cddc4-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cddc4-208">RELATED LINKS</span></span>
