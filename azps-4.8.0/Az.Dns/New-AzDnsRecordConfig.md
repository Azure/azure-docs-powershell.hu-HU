---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182790"
---
# <span data-ttu-id="acc74-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="acc74-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="acc74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acc74-102">SYNOPSIS</span></span>
<span data-ttu-id="acc74-103">Új DNS-rekord helyi objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="acc74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acc74-104">SYNTAX</span></span>

### <span data-ttu-id="acc74-105">Egy</span><span class="sxs-lookup"><span data-stu-id="acc74-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="acc74-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-107">NS</span><span class="sxs-lookup"><span data-stu-id="acc74-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-108">MX</span><span class="sxs-lookup"><span data-stu-id="acc74-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acc74-109">PTR</span><span class="sxs-lookup"><span data-stu-id="acc74-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-110">Txt</span><span class="sxs-lookup"><span data-stu-id="acc74-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-111">SRV</span><span class="sxs-lookup"><span data-stu-id="acc74-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-112">CName</span><span class="sxs-lookup"><span data-stu-id="acc74-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc74-113">CAA</span><span class="sxs-lookup"><span data-stu-id="acc74-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc74-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="acc74-114">DESCRIPTION</span></span>
<span data-ttu-id="acc74-115">A **New-AzDnsRecordConfig** parancsmag létrehoz egy helyi **DnsRecord** objektumot.</span><span class="sxs-lookup"><span data-stu-id="acc74-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="acc74-116">A *DnsRecords* paraméterrel megadhatja, hogy milyen rekordok kerüljenek az New-AzDnsRecordSet parancsmagba a rekordban létrehozandó rekordok megadásához.</span><span class="sxs-lookup"><span data-stu-id="acc74-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="acc74-117">Példák</span><span class="sxs-lookup"><span data-stu-id="acc74-117">EXAMPLES</span></span>

### <span data-ttu-id="acc74-118">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="acc74-119">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="acc74-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-120">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-121">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="acc74-122">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="acc74-123">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="acc74-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-124">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="acc74-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-125">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-125">It contains a single DNS record.</span></span>
<span data-ttu-id="acc74-126">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="acc74-127">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="acc74-128">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="acc74-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-129">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-130">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-130">It contains a single DNS record.</span></span>
<span data-ttu-id="acc74-131">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="acc74-132">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="acc74-133">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="acc74-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-134">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-135">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-135">It contains a single DNS record.</span></span>
<span data-ttu-id="acc74-136">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="acc74-137">Példa 5: NS típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="acc74-138">A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="acc74-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-139">A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-140">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-140">It contains a single DNS record.</span></span>
<span data-ttu-id="acc74-141">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="acc74-142">6. példa: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="acc74-143">A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="acc74-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="acc74-144">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-145">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-145">It contains a single DNS record.</span></span>
<span data-ttu-id="acc74-146">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="acc74-147">7. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="acc74-148">A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="acc74-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-149">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-150">Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="acc74-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="acc74-151">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="acc74-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="acc74-152">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="acc74-153">8. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="acc74-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="acc74-154">A parancs létrehozza a myzone.com nevű **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="acc74-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="acc74-155">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="acc74-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="acc74-156">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="acc74-156">It contains a single DNS record.</span></span>
<span data-ttu-id="acc74-157">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="acc74-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="acc74-158">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acc74-158">PARAMETERS</span></span>

### <span data-ttu-id="acc74-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="acc74-159">-CaaFlags</span></span>
<span data-ttu-id="acc74-160">A felvenni kívánt CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="acc74-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="acc74-161">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="acc74-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="acc74-162">-CaaTag</span></span>
<span data-ttu-id="acc74-163">A felvenni kívánt CAA-rekord címke mezője</span><span class="sxs-lookup"><span data-stu-id="acc74-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="acc74-164">-CaaValue</span></span>
<span data-ttu-id="acc74-165">A hozzáadni kívánt CAA rekord érték mezője</span><span class="sxs-lookup"><span data-stu-id="acc74-165">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="acc74-166">-Cname</span></span>
<span data-ttu-id="acc74-167">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc74-168">-DefaultProfile</span></span>
<span data-ttu-id="acc74-169">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="acc74-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acc74-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="acc74-170">-Exchange</span></span>
<span data-ttu-id="acc74-171">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="acc74-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="acc74-172">-Ipv4Address</span></span>
<span data-ttu-id="acc74-173">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-173">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="acc74-174">-Ipv6Address</span></span>
<span data-ttu-id="acc74-175">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="acc74-176">-Nsdname</span></span>
<span data-ttu-id="acc74-177">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="acc74-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-178">-Port</span><span class="sxs-lookup"><span data-stu-id="acc74-178">-Port</span></span>
<span data-ttu-id="acc74-179">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-180">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="acc74-180">-Preference</span></span>
<span data-ttu-id="acc74-181">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-182">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="acc74-182">-Priority</span></span>
<span data-ttu-id="acc74-183">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="acc74-184">-Ptrdname</span></span>
<span data-ttu-id="acc74-185">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-186">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="acc74-186">-Target</span></span>
<span data-ttu-id="acc74-187">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-188">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="acc74-188">-Value</span></span>
<span data-ttu-id="acc74-189">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-190">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="acc74-190">-Weight</span></span>
<span data-ttu-id="acc74-191">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="acc74-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc74-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc74-192">CommonParameters</span></span>
<span data-ttu-id="acc74-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acc74-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc74-194">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc74-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc74-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acc74-195">INPUTS</span></span>

### <span data-ttu-id="acc74-196">System. String</span><span class="sxs-lookup"><span data-stu-id="acc74-196">System.String</span></span>

### <span data-ttu-id="acc74-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="acc74-197">System.UInt16</span></span>

### <span data-ttu-id="acc74-198">System. byte</span><span class="sxs-lookup"><span data-stu-id="acc74-198">System.Byte</span></span>

## <span data-ttu-id="acc74-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acc74-199">OUTPUTS</span></span>

### <span data-ttu-id="acc74-200">Microsoft. Azure. Command. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="acc74-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="acc74-201">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acc74-201">NOTES</span></span>

## <span data-ttu-id="acc74-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acc74-202">RELATED LINKS</span></span>

[<span data-ttu-id="acc74-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="acc74-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="acc74-204">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="acc74-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="acc74-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="acc74-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
