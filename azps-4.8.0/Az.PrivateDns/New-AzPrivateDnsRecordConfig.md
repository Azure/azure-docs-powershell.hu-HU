---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 6653491e7ee4a60b6ad9b392895454e5ee6dc3ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182907"
---
# <span data-ttu-id="ac337-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ac337-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="ac337-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac337-102">SYNOPSIS</span></span>
<span data-ttu-id="ac337-103">Új magánhálózati DNS-rekord helyi objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="ac337-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac337-104">SYNTAX</span></span>

### <span data-ttu-id="ac337-105">A (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac337-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac337-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="ac337-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac337-107">MX</span><span class="sxs-lookup"><span data-stu-id="ac337-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac337-108">PTR</span><span class="sxs-lookup"><span data-stu-id="ac337-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac337-109">TXT</span><span class="sxs-lookup"><span data-stu-id="ac337-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac337-110">SRV</span><span class="sxs-lookup"><span data-stu-id="ac337-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac337-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="ac337-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac337-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac337-112">DESCRIPTION</span></span>
<span data-ttu-id="ac337-113">A New-AzPrivateDnsRecordConfig parancsmag helyi PSPrivateDnsRecord objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ac337-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="ac337-114">A PrivateDnsRecord paraméterrel megadhatja, hogy milyen rekordok kerüljenek az New-AzPrivateDnsRecordSet parancsmagba a rekordban létrehozandó rekordok megadásához.</span><span class="sxs-lookup"><span data-stu-id="ac337-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="ac337-115">Példák</span><span class="sxs-lookup"><span data-stu-id="ac337-115">EXAMPLES</span></span>

### <span data-ttu-id="ac337-116">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="ac337-117">Ez a példa létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ac337-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="ac337-118">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ac337-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-119">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ac337-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="ac337-120">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="ac337-121">Ez a példa létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ac337-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="ac337-122">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="ac337-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-123">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ac337-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="ac337-124">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="ac337-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ac337-125">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="ac337-126">Ez a példa létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ac337-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="ac337-127">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ac337-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-128">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ac337-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="ac337-129">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="ac337-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ac337-130">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="ac337-131">A parancs létrehoz egy www nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ac337-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="ac337-132">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ac337-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-133">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ac337-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="ac337-134">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="ac337-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ac337-135">Példa 5: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="ac337-136">A parancs létrehoz egy 4 nevű rekordhalmazt a privát Zone 3.2.1.in-addr. arpa nevű rekordhalmazban.</span><span class="sxs-lookup"><span data-stu-id="ac337-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="ac337-137">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ac337-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-138">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ac337-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="ac337-139">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="ac337-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ac337-140">6. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="ac337-141">A parancs létrehoz egy _sip. _tcp nevű rekordhalmazt a privát zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ac337-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="ac337-142">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ac337-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-143">Egyetlen magánhálózati DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="ac337-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="ac337-144">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="ac337-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="ac337-145">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="ac337-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ac337-146">7. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac337-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="ac337-147">A parancs létrehoz egy, a privát zóna myzone.com szöveget tartalmazó RecordSet nevű rekordhalmazt.</span><span class="sxs-lookup"><span data-stu-id="ac337-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="ac337-148">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ac337-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="ac337-149">Egy privát DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ac337-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="ac337-150">Ha olyan rekordhalmazt szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="ac337-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="ac337-151">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac337-151">PARAMETERS</span></span>

### <span data-ttu-id="ac337-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="ac337-152">-Cname</span></span>
<span data-ttu-id="ac337-153">A hozzáadni kívánt CNAME rekord kanonikus neve.</span><span class="sxs-lookup"><span data-stu-id="ac337-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="ac337-154">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="ac337-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="ac337-155">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="ac337-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="ac337-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac337-156">-DefaultProfile</span></span>
<span data-ttu-id="ac337-157">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac337-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac337-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="ac337-158">-Exchange</span></span>
<span data-ttu-id="ac337-159">A felvenni kívánt MX rekord levelezési Exchange-állomása.</span><span class="sxs-lookup"><span data-stu-id="ac337-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="ac337-160">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="ac337-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="ac337-161">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="ac337-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="ac337-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="ac337-162">-Ipv4Address</span></span>
<span data-ttu-id="ac337-163">A hozzáadni kívánt rekord IPv4-címe.</span><span class="sxs-lookup"><span data-stu-id="ac337-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="ac337-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="ac337-164">-Ipv6Address</span></span>
<span data-ttu-id="ac337-165">A felvenni kívánt AAAA-rekord IPv6-címe.</span><span class="sxs-lookup"><span data-stu-id="ac337-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="ac337-166">-Port</span><span class="sxs-lookup"><span data-stu-id="ac337-166">-Port</span></span>
<span data-ttu-id="ac337-167">A hozzáadni kívánt SRV rekord portszáma.</span><span class="sxs-lookup"><span data-stu-id="ac337-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="ac337-168">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="ac337-168">-Preference</span></span>
<span data-ttu-id="ac337-169">A felvenni kívánt MX rekord preferencia értéke.</span><span class="sxs-lookup"><span data-stu-id="ac337-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="ac337-170">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="ac337-170">-Priority</span></span>
<span data-ttu-id="ac337-171">A hozzáadandó SRV rekord prioritási értéke.</span><span class="sxs-lookup"><span data-stu-id="ac337-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="ac337-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="ac337-172">-Ptrdname</span></span>
<span data-ttu-id="ac337-173">A felvenni kívánt PTR-rekord célállomása.</span><span class="sxs-lookup"><span data-stu-id="ac337-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="ac337-174">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="ac337-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="ac337-175">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="ac337-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="ac337-176">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="ac337-176">-Target</span></span>
<span data-ttu-id="ac337-177">A hozzáadni kívánt SRV rekord célállomása.</span><span class="sxs-lookup"><span data-stu-id="ac337-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="ac337-178">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="ac337-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="ac337-179">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="ac337-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="ac337-180">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="ac337-180">-Value</span></span>
<span data-ttu-id="ac337-181">A hozzáadni kívánt TXT rekord szöveges értéke.</span><span class="sxs-lookup"><span data-stu-id="ac337-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="ac337-182">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="ac337-182">-Weight</span></span>
<span data-ttu-id="ac337-183">A hozzáadandó SRV rekord súlyozó értéke.</span><span class="sxs-lookup"><span data-stu-id="ac337-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="ac337-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac337-184">CommonParameters</span></span>
<span data-ttu-id="ac337-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac337-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac337-186">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac337-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac337-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac337-187">INPUTS</span></span>

### <span data-ttu-id="ac337-188">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac337-188">None</span></span>

## <span data-ttu-id="ac337-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac337-189">OUTPUTS</span></span>

### <span data-ttu-id="ac337-190">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ac337-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ac337-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac337-191">NOTES</span></span>

## <span data-ttu-id="ac337-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac337-192">RELATED LINKS</span></span>
