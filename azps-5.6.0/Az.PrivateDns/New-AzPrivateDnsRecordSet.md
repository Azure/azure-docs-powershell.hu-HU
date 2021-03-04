---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7779cf8b357bab9480a9b811303bb19f1f0a6799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925410"
---
# <span data-ttu-id="6b3ba-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b3ba-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="6b3ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3ba-103">Létrehoz egy rekordkészletet egy privát DNS-zónában.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="6b3ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b3ba-104">SYNTAX</span></span>

### <span data-ttu-id="6b3ba-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b3ba-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3ba-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="6b3ba-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3ba-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3ba-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3ba-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b3ba-108">DESCRIPTION</span></span>
<span data-ttu-id="6b3ba-109">A New-AzPrivateDnsRecordSet parancsmag létrehoz egy új, a megadott nevű és a megadott privát zónába beírt DNS-rekordot.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="6b3ba-110">A RecordSet objektum a privát DNS-rekordok azonos nevű és típusú halmaza.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="6b3ba-111">Ne feledje, hogy a név a privát zónához képest van, nem pedig a teljesen minősített név.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="6b3ba-112">A PrivateDnsRecord paraméter a rekordkészlet rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="6b3ba-113">Ez a paraméter a New-AzPrivateDnsRecordConfig használatával felépített privát DNS-rekordok tömbjébe kerül.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="6b3ba-114">A folyamat műveleti jelével átadhatja a PSPrivateDnsZone-objektumot ennek a parancsmagnak, vagy átadhatja a PSPrivateDnsZone-objektumot zóna paraméterként, vagy megadhatja a zónát a ResourceId paramétere alapján, vagy másik lehetőségként megadhatja a zónát név szerint.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="6b3ba-115">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="6b3ba-116">Ha már létezik egy megfelelő RecordSet (ugyanaz a név és rekordtípus), meg kell adnia a Felülírás paramétert, ellenkező esetben a parancsmag nem hoz létre új RecordSetet.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="6b3ba-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b3ba-117">EXAMPLES</span></span>

### <span data-ttu-id="6b3ba-118">1. példa: A típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="6b3ba-119">Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-120">A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-121">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="6b3ba-122">2. példa: AAAA típusú rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="6b3ba-123">Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-124">A rekordkészlet AAAA típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-125">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="6b3ba-126">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-127">3. példa: CNAME típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="6b3ba-128">Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-129">A rekordkészlet CNAME típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-130">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="6b3ba-131">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-132">4. példa: MX típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="6b3ba-133">Ez a parancs létrehoz egy www nevű RecordSetet a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-134">A rekordkészlet MX típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-135">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="6b3ba-136">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-137">5. példa: PTR típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="6b3ba-138">Ez a parancs létrehoz egy 4 nevű RecordSetet a 3.2.1.in-addr.arpa privát zónában.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="6b3ba-139">A rekordkészlet PTR típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-140">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="6b3ba-141">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-142">6. példa: SRV típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="6b3ba-143">Ez a parancs létrehoz egy _sip._tcp nevű RecordSetet a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-144">A rekordkészlet típusa SRV, és TTL-1 óra (3600 másodperc) típusú.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-145">Egyetlen privát DNS-rekordot tartalmaz, amely a 2001.2.3.4-es IP-címre mutat.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="6b3ba-146">A szolgáltatás (sip) és a protokoll (tcp) a rekordkészlet nevének részeként van megadva, nem pedig a rekordadatok részeként.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="6b3ba-147">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-148">7. példa: TXT típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="6b3ba-149">Ez a parancs létrehoz egy RecordSet nevű szöveget a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-150">A rekordkészlet a TXT típusú, és TTL értéke 1 óra (3600 másodperc).</span><span class="sxs-lookup"><span data-stu-id="6b3ba-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-151">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="6b3ba-152">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-153">8. példa: RecordSet létrehozása a zóna csúcsán</span><span class="sxs-lookup"><span data-stu-id="6b3ba-153">Example 8:  Create a RecordSet at the zone apex</span></span>
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

<span data-ttu-id="6b3ba-154">Ez a parancs létrehoz egy RecordSetet a privát zónarekord (vagy gyökér) myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-155">Ehhez a rekordkészlet neve "@" (a dupla idézőjelekkel együtt) lesz megadva.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="6b3ba-156">A CNAME rekordok nem hozhatók létre a zóna csúcsán.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="6b3ba-157">Ez a DNS-szabványok kényszere; nem korlátozza az Azure Private DNS-t.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="6b3ba-158">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-159">9. példa: Helyettesítő karakteres rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-159">Example 9:  Create a wildcard Record Set</span></span>

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

<span data-ttu-id="6b3ba-160">Ez a parancs létrehoz egy \* nevű Rekordkészletet a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-161">Ez egy helyettesítő karakteres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-161">This is a wildcard record set.</span></span> <span data-ttu-id="6b3ba-162">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6b3ba-163">10. példa: Üres rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b3ba-163">Example 10:  Create an empty Record Set</span></span>

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

<span data-ttu-id="6b3ba-164">Ez a parancs létrehoz egy \* nevű Rekordkészletet a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="6b3ba-165">A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="6b3ba-166">Ez egy üres rekordkészlet, amely helyőrzőként működik, amelyhez később rekordokat adhat hozzá.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="6b3ba-167">11. példa: Rekordkészlet létrehozása és az összes megerősítés mellőzése</span><span class="sxs-lookup"><span data-stu-id="6b3ba-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="6b3ba-168">Ezzel a paranccsal rekordkészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-168">This command creates a RecordSet.</span></span> <span data-ttu-id="6b3ba-169">A Felülírás paraméter gondoskodik arról, hogy ez a rekordkészlet felülírja az azonos nevű és típusú meglévő rekordkészleteket (a rekordkészlet meglévő rekordjai elvesznek).</span><span class="sxs-lookup"><span data-stu-id="6b3ba-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="6b3ba-170">A Confirm paraméter értéke $False a megerősítést kérő üzenet.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="6b3ba-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b3ba-171">PARAMETERS</span></span>

### <span data-ttu-id="6b3ba-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3ba-172">-DefaultProfile</span></span>
<span data-ttu-id="6b3ba-173">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b3ba-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6b3ba-174">-Metadata</span></span>
<span data-ttu-id="6b3ba-175">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-175">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6b3ba-176">-Name</span><span class="sxs-lookup"><span data-stu-id="6b3ba-176">-Name</span></span>
<span data-ttu-id="6b3ba-177">A rekordkészlet rekordjainak neve (a zóna nevéhez képest és befejezési pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="6b3ba-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="6b3ba-178">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="6b3ba-178">-Overwrite</span></span>
<span data-ttu-id="6b3ba-179">Ha a rekordkészlet már létezik, akkor nem kell sikertelenül működnie.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="6b3ba-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3ba-180">-ParentResourceId</span></span>
<span data-ttu-id="6b3ba-181">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-181">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="6b3ba-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="6b3ba-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="6b3ba-183">Az ebben a rekordkészletben lévő privát DNS-rekordok.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-183">The private dns records that are part of this record set.</span></span>

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

### <span data-ttu-id="6b3ba-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="6b3ba-184">-RecordType</span></span>
<span data-ttu-id="6b3ba-185">A privát DNS-rekordok típusa ebben a rekordkészletben.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-185">The type of Private DNS records in this record set.</span></span>

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

### <span data-ttu-id="6b3ba-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b3ba-186">-ResourceGroupName</span></span>
<span data-ttu-id="6b3ba-187">Az az erőforráscsoport, amelyhez a zóna tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-187">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="6b3ba-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="6b3ba-188">-Ttl</span></span>
<span data-ttu-id="6b3ba-189">A rekordkészlet összes rekordja TTL-értéke.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-189">The TTL value of all the records in this record set.</span></span>

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

### <span data-ttu-id="6b3ba-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="6b3ba-190">-Zone</span></span>
<span data-ttu-id="6b3ba-191">The PrivateDnsZone object representing the zone in which to create the record set.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="6b3ba-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="6b3ba-192">-ZoneName</span></span>
<span data-ttu-id="6b3ba-193">Az a zóna, amelyben létre kell hoznia a rekordkészletet (befejezési pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="6b3ba-193">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="6b3ba-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b3ba-194">-Confirm</span></span>
<span data-ttu-id="6b3ba-195">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3ba-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3ba-196">-WhatIf</span></span>
<span data-ttu-id="6b3ba-197">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b3ba-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3ba-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3ba-199">CommonParameters</span></span>
<span data-ttu-id="6b3ba-200">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b3ba-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3ba-201">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b3ba-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3ba-202">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b3ba-202">INPUTS</span></span>

### <span data-ttu-id="6b3ba-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="6b3ba-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="6b3ba-204">System.String</span><span class="sxs-lookup"><span data-stu-id="6b3ba-204">System.String</span></span>

## <span data-ttu-id="6b3ba-205">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b3ba-205">OUTPUTS</span></span>

### <span data-ttu-id="6b3ba-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b3ba-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="6b3ba-207">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b3ba-207">NOTES</span></span>

## <span data-ttu-id="6b3ba-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b3ba-208">RELATED LINKS</span></span>
