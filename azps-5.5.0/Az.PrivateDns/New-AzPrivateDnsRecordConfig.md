---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: f828c422447768ff59aea413eeca036a60877b09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169354"
---
# <span data-ttu-id="2bef7-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2bef7-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="2bef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bef7-102">SYNOPSIS</span></span>
<span data-ttu-id="2bef7-103">Létrehoz egy új privát DNS-rekord helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="2bef7-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="2bef7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2bef7-104">SYNTAX</span></span>

### <span data-ttu-id="2bef7-105">A (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2bef7-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bef7-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="2bef7-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bef7-107">MX</span><span class="sxs-lookup"><span data-stu-id="2bef7-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bef7-108">PTR</span><span class="sxs-lookup"><span data-stu-id="2bef7-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bef7-109">TXT</span><span class="sxs-lookup"><span data-stu-id="2bef7-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bef7-110">SRV</span><span class="sxs-lookup"><span data-stu-id="2bef7-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bef7-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="2bef7-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bef7-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2bef7-112">DESCRIPTION</span></span>
<span data-ttu-id="2bef7-113">A New-AzPrivateDnsRecordConfig helyi PSPrivateDnsRecord objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bef7-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="2bef7-114">Az objektumok tömbje a New-AzPrivateDnsRecordSet PrivateDnsRecord paraméterrel adható meg a rekordkészletben létrehozandó rekordok megadásához.</span><span class="sxs-lookup"><span data-stu-id="2bef7-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="2bef7-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2bef7-115">EXAMPLES</span></span>

### <span data-ttu-id="2bef7-116">1. példa: A típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="2bef7-117">Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2bef7-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="2bef7-118">A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2bef7-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-119">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="2bef7-120">2. példa: AAAA típusú rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="2bef7-121">Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2bef7-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="2bef7-122">A rekordkészlet AAAA típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2bef7-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-123">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="2bef7-124">Ha egy rekordhalmazt csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2bef7-125">3. példa: CNAME típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-125">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="2bef7-126">Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2bef7-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="2bef7-127">A rekordkészlet CNAME típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2bef7-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-128">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="2bef7-129">Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2bef7-130">4. példa: MX típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-130">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="2bef7-131">Ez a parancs létrehoz egy www nevű RecordSetet a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2bef7-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="2bef7-132">A rekordkészlet MX típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2bef7-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-133">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="2bef7-134">Ha egy rekordhalmazt csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2bef7-135">5. példa: PTR típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="2bef7-136">Ez a parancs létrehoz egy 4 nevű RecordSetet a 3.2.1.in-addr.arpa privát zónában.</span><span class="sxs-lookup"><span data-stu-id="2bef7-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="2bef7-137">A rekordkészlet PTR típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2bef7-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-138">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="2bef7-139">Ha egy rekordhalmazt csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2bef7-140">6. példa: SRV típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="2bef7-141">Ez a parancs létrehoz egy _sip._tcp nevű RecordSetet a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2bef7-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="2bef7-142">A rekordkészlet típusa SRV, és TTL 1 óra (3600 másodperc) típusú.</span><span class="sxs-lookup"><span data-stu-id="2bef7-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-143">Egyetlen privát DNS-rekordot tartalmaz, amely a 2001.2.3.4-es IP-címre mutat.</span><span class="sxs-lookup"><span data-stu-id="2bef7-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="2bef7-144">A szolgáltatás (sip) és a protokoll (tcp) a rekordkészlet nevének részeként van megadva, nem pedig a rekordadatok részeként.</span><span class="sxs-lookup"><span data-stu-id="2bef7-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="2bef7-145">Ha egy rekordhalmazt csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2bef7-146">7. példa: TXT típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bef7-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="2bef7-147">Ez a parancs létrehoz egy RecordSet nevű szöveget a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2bef7-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="2bef7-148">A rekordkészlet a TXT típusú, és TTL értéke 1 óra (3600 másodperc).</span><span class="sxs-lookup"><span data-stu-id="2bef7-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="2bef7-149">Egyetlen privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="2bef7-150">Ha egy rekordhalmazt csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="2bef7-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bef7-151">PARAMETERS</span></span>

### <span data-ttu-id="2bef7-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="2bef7-152">-Cname</span></span>
<span data-ttu-id="2bef7-153">Az összeadni képes CNAME rekord canonical neve.</span><span class="sxs-lookup"><span data-stu-id="2bef7-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="2bef7-154">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="2bef7-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="2bef7-155">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="2bef7-155">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bef7-156">-DefaultProfile</span></span>
<span data-ttu-id="2bef7-157">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2bef7-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bef7-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="2bef7-158">-Exchange</span></span>
<span data-ttu-id="2bef7-159">A hozzáadni megfelelő MX rekord levelezési szolgáltatója.</span><span class="sxs-lookup"><span data-stu-id="2bef7-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="2bef7-160">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="2bef7-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="2bef7-161">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="2bef7-161">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="2bef7-162">-Ipv4Address</span></span>
<span data-ttu-id="2bef7-163">Az A rekord IPv4-címe.</span><span class="sxs-lookup"><span data-stu-id="2bef7-163">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="2bef7-164">-Ipv6Address</span></span>
<span data-ttu-id="2bef7-165">A hozzáadni használt AAAA rekord IPv6-címe.</span><span class="sxs-lookup"><span data-stu-id="2bef7-165">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-166">-Port</span><span class="sxs-lookup"><span data-stu-id="2bef7-166">-Port</span></span>
<span data-ttu-id="2bef7-167">Az hozzáadni fog egy SRV rekord portszámát.</span><span class="sxs-lookup"><span data-stu-id="2bef7-167">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-168">-Preference</span><span class="sxs-lookup"><span data-stu-id="2bef7-168">-Preference</span></span>
<span data-ttu-id="2bef7-169">A hozzáadni kiválasztott MX rekord beállításértéke.</span><span class="sxs-lookup"><span data-stu-id="2bef7-169">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-170">-Priority</span><span class="sxs-lookup"><span data-stu-id="2bef7-170">-Priority</span></span>
<span data-ttu-id="2bef7-171">A hozzáadni célként megadott SRV rekord.</span><span class="sxs-lookup"><span data-stu-id="2bef7-171">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="2bef7-172">-Ptrdname</span></span>
<span data-ttu-id="2bef7-173">A hozzáadni megfelelő PTR-rekord cél állomása.</span><span class="sxs-lookup"><span data-stu-id="2bef7-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="2bef7-174">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="2bef7-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="2bef7-175">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="2bef7-175">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-176">-Target</span><span class="sxs-lookup"><span data-stu-id="2bef7-176">-Target</span></span>
<span data-ttu-id="2bef7-177">Az hozzáadni cél állomása az SRV rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2bef7-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="2bef7-178">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="2bef7-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="2bef7-179">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="2bef7-179">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-180">-Érték</span><span class="sxs-lookup"><span data-stu-id="2bef7-180">-Value</span></span>
<span data-ttu-id="2bef7-181">Az összeadni megfelelő TXT rekord szöveges értéke.</span><span class="sxs-lookup"><span data-stu-id="2bef7-181">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-182">-Weight</span><span class="sxs-lookup"><span data-stu-id="2bef7-182">-Weight</span></span>
<span data-ttu-id="2bef7-183">Az összeadni megfelelő SRV rekord súlyértéke.</span><span class="sxs-lookup"><span data-stu-id="2bef7-183">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef7-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bef7-184">CommonParameters</span></span>
<span data-ttu-id="2bef7-185">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bef7-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bef7-186">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bef7-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bef7-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bef7-187">INPUTS</span></span>

### <span data-ttu-id="2bef7-188">Nincs</span><span class="sxs-lookup"><span data-stu-id="2bef7-188">None</span></span>

## <span data-ttu-id="2bef7-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bef7-189">OUTPUTS</span></span>

### <span data-ttu-id="2bef7-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2bef7-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="2bef7-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2bef7-191">NOTES</span></span>

## <span data-ttu-id="2bef7-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bef7-192">RELATED LINKS</span></span>
