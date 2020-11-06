---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f44472ac83c1d92baab5d4c7c3b4c8d325e3dfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500612"
---
# <span data-ttu-id="84ef2-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="84ef2-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="84ef2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="84ef2-103">Új DNS-rekord helyi objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84ef2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84ef2-104">SYNTAX</span></span>

### <span data-ttu-id="84ef2-105">Egy</span><span class="sxs-lookup"><span data-stu-id="84ef2-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84ef2-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="84ef2-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84ef2-107">NS</span><span class="sxs-lookup"><span data-stu-id="84ef2-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84ef2-108">MX</span><span class="sxs-lookup"><span data-stu-id="84ef2-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84ef2-109">PTR</span><span class="sxs-lookup"><span data-stu-id="84ef2-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84ef2-110">Txt</span><span class="sxs-lookup"><span data-stu-id="84ef2-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84ef2-111">SRV</span><span class="sxs-lookup"><span data-stu-id="84ef2-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84ef2-112">CName</span><span class="sxs-lookup"><span data-stu-id="84ef2-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84ef2-113">CAA</span><span class="sxs-lookup"><span data-stu-id="84ef2-113">Caa</span></span>
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84ef2-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="84ef2-114">DESCRIPTION</span></span>
<span data-ttu-id="84ef2-115">A **New-AzureRmDnsRecordConfig** parancsmag létrehoz egy helyi **DnsRecord** objektumot.</span><span class="sxs-lookup"><span data-stu-id="84ef2-115">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="84ef2-116">A *DnsRecords* paraméterrel megadhatja, hogy milyen rekordok kerüljenek az New-AzureRmDnsRecordSet parancsmagba a rekordban létrehozandó rekordok megadásához.</span><span class="sxs-lookup"><span data-stu-id="84ef2-116">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="84ef2-117">Példák</span><span class="sxs-lookup"><span data-stu-id="84ef2-117">EXAMPLES</span></span>

### <span data-ttu-id="84ef2-118">1. példa: az A típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="84ef2-119">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="84ef2-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-120">A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-121">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="84ef2-122">2. példa: AAAA típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="84ef2-123">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="84ef2-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-124">A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="84ef2-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-125">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-125">It contains a single DNS record.</span></span>

<span data-ttu-id="84ef2-126">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="84ef2-127">3. példa: CNAME típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="84ef2-128">Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="84ef2-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-129">A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-130">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-130">It contains a single DNS record.</span></span>

<span data-ttu-id="84ef2-131">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="84ef2-132">4. példa: MX típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="84ef2-133">A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="84ef2-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-134">A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-135">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-135">It contains a single DNS record.</span></span>

<span data-ttu-id="84ef2-136">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="84ef2-137">Példa 5: NS típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="84ef2-138">A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="84ef2-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-139">A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-140">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-140">It contains a single DNS record.</span></span>

<span data-ttu-id="84ef2-141">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="84ef2-142">6. példa: PTR típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="84ef2-143">A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="84ef2-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="84ef2-144">A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-145">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-145">It contains a single DNS record.</span></span>

<span data-ttu-id="84ef2-146">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="84ef2-147">7. példa: SRV típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="84ef2-148">A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="84ef2-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-149">A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-150">Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.</span><span class="sxs-lookup"><span data-stu-id="84ef2-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="84ef2-151">A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.</span><span class="sxs-lookup"><span data-stu-id="84ef2-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="84ef2-152">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="84ef2-153">8. példa: TXT típusú rekordhalmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="84ef2-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="84ef2-154">A parancs létrehozza a myzone.com nevű **rekordhalmazt** .</span><span class="sxs-lookup"><span data-stu-id="84ef2-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="84ef2-155">A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="84ef2-156">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-156">It contains a single DNS record.</span></span>

<span data-ttu-id="84ef2-157">Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="84ef2-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="84ef2-158">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84ef2-158">PARAMETERS</span></span>

### <span data-ttu-id="84ef2-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="84ef2-159">-CaaFlags</span></span>
<span data-ttu-id="84ef2-160">A felvenni kívánt CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="84ef2-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="84ef2-161">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84ef2-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ef2-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="84ef2-162">-CaaTag</span></span>
<span data-ttu-id="84ef2-163">A felvenni kívánt CAA-rekord címke mezője</span><span class="sxs-lookup"><span data-stu-id="84ef2-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ef2-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="84ef2-164">-CaaValue</span></span>
<span data-ttu-id="84ef2-165">A hozzáadni kívánt CAA rekord érték mezője</span><span class="sxs-lookup"><span data-stu-id="84ef2-165">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ef2-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="84ef2-166">-Cname</span></span>
<span data-ttu-id="84ef2-167">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="84ef2-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ef2-168">-DefaultProfile</span></span>
<span data-ttu-id="84ef2-169">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="84ef2-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ef2-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="84ef2-170">-Exchange</span></span>
<span data-ttu-id="84ef2-171">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="84ef2-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="84ef2-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="84ef2-172">-Ipv4Address</span></span>
<span data-ttu-id="84ef2-173">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="84ef2-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="84ef2-174">-Ipv6Address</span></span>
<span data-ttu-id="84ef2-175">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="84ef2-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="84ef2-176">-Nsdname</span></span>
<span data-ttu-id="84ef2-177">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="84ef2-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="84ef2-178">-Port</span><span class="sxs-lookup"><span data-stu-id="84ef2-178">-Port</span></span>
<span data-ttu-id="84ef2-179">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="84ef2-180">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="84ef2-180">-Preference</span></span>
<span data-ttu-id="84ef2-181">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="84ef2-182">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="84ef2-182">-Priority</span></span>
<span data-ttu-id="84ef2-183">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="84ef2-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="84ef2-184">-Ptrdname</span></span>
<span data-ttu-id="84ef2-185">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="84ef2-186">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="84ef2-186">-Target</span></span>
<span data-ttu-id="84ef2-187">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="84ef2-188">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="84ef2-188">-Value</span></span>
<span data-ttu-id="84ef2-189">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="84ef2-190">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="84ef2-190">-Weight</span></span>
<span data-ttu-id="84ef2-191">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ef2-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="84ef2-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ef2-192">CommonParameters</span></span>
<span data-ttu-id="84ef2-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84ef2-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ef2-194">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ef2-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ef2-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84ef2-195">INPUTS</span></span>

### <span data-ttu-id="84ef2-196">Nincs.</span><span class="sxs-lookup"><span data-stu-id="84ef2-196">None.</span></span>

## <span data-ttu-id="84ef2-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84ef2-197">OUTPUTS</span></span>

### <span data-ttu-id="84ef2-198">Microsoft. Azure. Command. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="84ef2-198">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="84ef2-199">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84ef2-199">NOTES</span></span>

## <span data-ttu-id="84ef2-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84ef2-200">RELATED LINKS</span></span>

[<span data-ttu-id="84ef2-201">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="84ef2-201">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="84ef2-202">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="84ef2-202">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="84ef2-203">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="84ef2-203">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
