---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167603"
---
# <span data-ttu-id="2fc3a-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2fc3a-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="2fc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc3a-103">Létrehoz egy új DNS-rekord helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="2fc3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2fc3a-104">SYNTAX</span></span>

### <span data-ttu-id="2fc3a-105">A</span><span class="sxs-lookup"><span data-stu-id="2fc3a-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="2fc3a-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-107">Ns</span><span class="sxs-lookup"><span data-stu-id="2fc3a-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-108">Mx</span><span class="sxs-lookup"><span data-stu-id="2fc3a-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="2fc3a-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-110">Txt</span><span class="sxs-lookup"><span data-stu-id="2fc3a-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-111">Srv</span><span class="sxs-lookup"><span data-stu-id="2fc3a-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-112">CName</span><span class="sxs-lookup"><span data-stu-id="2fc3a-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc3a-113">Caa</span><span class="sxs-lookup"><span data-stu-id="2fc3a-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fc3a-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2fc3a-114">DESCRIPTION</span></span>
<span data-ttu-id="2fc3a-115">A **New-AzDnsRecordConfig** parancsmag helyi **DnsRecord objektumot** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="2fc3a-116">Ezeknek az objektumoknak egy tömbje a New-AzDnsRecordSet *DnsRecords* paramétert használva adható meg a rekordkészletben létrehozandó rekordoknak.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="2fc3a-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2fc3a-117">EXAMPLES</span></span>

### <span data-ttu-id="2fc3a-118">1. példa: A típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="2fc3a-119">Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-120">A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-121">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="2fc3a-122">2. példa: AAAA típusú rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-123">Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-124">A rekordkészlet AAAA típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-125">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-125">It contains a single DNS record.</span></span>
<span data-ttu-id="2fc3a-126">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2fc3a-127">3. példa: CNAME típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-128">Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-129">A rekordkészlet CNAME típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-130">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-130">It contains a single DNS record.</span></span>
<span data-ttu-id="2fc3a-131">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2fc3a-132">4. példa: MX típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-133">Ez a parancs létrehoz egy www **nevű Rekordkészletet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-134">A rekordkészlet MX típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-135">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-135">It contains a single DNS record.</span></span>
<span data-ttu-id="2fc3a-136">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2fc3a-137">5. példa: NS típusú rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-138">Ez a parancs létrehoz egy ns1 **nevű Rekordkészletet** a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-139">A rekordkészlet NS típusú, és 1 órás TTL-t (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-140">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-140">It contains a single DNS record.</span></span>
<span data-ttu-id="2fc3a-141">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2fc3a-142">6. példa: PTR típusú Rekordkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-143">Ez a parancs létrehoz egy 4 **nevű RecordSetet** a 3.2.1.in-addr.arpa zónában.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="2fc3a-144">A rekordkészlet PTR típusú, és TTL-t (1 óra) (3600 másodperc) tart.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-145">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-145">It contains a single DNS record.</span></span>
<span data-ttu-id="2fc3a-146">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2fc3a-147">7. példa: SRV típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-148">Ez a parancs létrehoz egy _sip._tcp nevű **RecordSetet** a myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-149">A rekordkészlet típusa SRV, és TTL 1 óra (3600 másodperc) típusú.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-150">Egyetlen DNS-rekordot tartalmaz, amely a 2001.2.3.4-es IP-címre mutat.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="2fc3a-151">A szolgáltatás (sip) és a protokoll (tcp) a rekordkészlet nevének részeként van megadva, nem pedig a rekordadatok részeként.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="2fc3a-152">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2fc3a-153">8. példa: TXT típusú RecordSet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc3a-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2fc3a-154">Ez a parancs létrehoz egy **RecordSet** nevű szöveget a zóna myzone.com.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="2fc3a-155">A rekordkészlet a TXT típusú, és TTL értéke 1 óra (3600 másodperc).</span><span class="sxs-lookup"><span data-stu-id="2fc3a-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2fc3a-156">Egyetlen DNS-rekordot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-156">It contains a single DNS record.</span></span>
<span data-ttu-id="2fc3a-157">Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="2fc3a-158">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fc3a-158">PARAMETERS</span></span>

### <span data-ttu-id="2fc3a-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="2fc3a-159">-CaaFlags</span></span>
<span data-ttu-id="2fc3a-160">A hozzáadni megfelelő CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="2fc3a-161">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="2fc3a-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="2fc3a-162">-CaaTag</span></span>
<span data-ttu-id="2fc3a-163">A hozzáadni megfelelő CAA-rekord címkemezője.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="2fc3a-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="2fc3a-164">-CaaValue</span></span>
<span data-ttu-id="2fc3a-165">Az összeadni megfelelő CAA-rekord értékmezője.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="2fc3a-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="2fc3a-166">-Cname</span></span>
<span data-ttu-id="2fc3a-167">Egy canonical name (CNAME) rekord tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="2fc3a-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc3a-168">-DefaultProfile</span></span>
<span data-ttu-id="2fc3a-169">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2fc3a-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fc3a-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="2fc3a-170">-Exchange</span></span>
<span data-ttu-id="2fc3a-171">Egy MX rekord levelezési kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="2fc3a-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="2fc3a-172">-Ipv4Address</span></span>
<span data-ttu-id="2fc3a-173">Egy A rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="2fc3a-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="2fc3a-174">-Ipv6Address</span></span>
<span data-ttu-id="2fc3a-175">Egy AAAA-rekord IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="2fc3a-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="2fc3a-176">-Nsdname</span></span>
<span data-ttu-id="2fc3a-177">A névkiszolgálói (NS) rekord névkiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="2fc3a-178">-Port</span><span class="sxs-lookup"><span data-stu-id="2fc3a-178">-Port</span></span>
<span data-ttu-id="2fc3a-179">Egy szolgáltatásrekord portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="2fc3a-180">-Preference</span><span class="sxs-lookup"><span data-stu-id="2fc3a-180">-Preference</span></span>
<span data-ttu-id="2fc3a-181">Az MX rekord beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="2fc3a-182">-Priority</span><span class="sxs-lookup"><span data-stu-id="2fc3a-182">-Priority</span></span>
<span data-ttu-id="2fc3a-183">Egy SRV rekord prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="2fc3a-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="2fc3a-184">-Ptrdname</span></span>
<span data-ttu-id="2fc3a-185">Egy mutatóerőforrás (PTR) rekord céltartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="2fc3a-186">-Target</span><span class="sxs-lookup"><span data-stu-id="2fc3a-186">-Target</span></span>
<span data-ttu-id="2fc3a-187">Egy SRV rekord célértékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="2fc3a-188">-Érték</span><span class="sxs-lookup"><span data-stu-id="2fc3a-188">-Value</span></span>
<span data-ttu-id="2fc3a-189">Egy TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="2fc3a-190">-Weight</span><span class="sxs-lookup"><span data-stu-id="2fc3a-190">-Weight</span></span>
<span data-ttu-id="2fc3a-191">Az SRV rekord súlyát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="2fc3a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc3a-192">CommonParameters</span></span>
<span data-ttu-id="2fc3a-193">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc3a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc3a-194">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc3a-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc3a-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fc3a-195">INPUTS</span></span>

### <span data-ttu-id="2fc3a-196">System.String</span><span class="sxs-lookup"><span data-stu-id="2fc3a-196">System.String</span></span>

### <span data-ttu-id="2fc3a-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="2fc3a-197">System.UInt16</span></span>

### <span data-ttu-id="2fc3a-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="2fc3a-198">System.Byte</span></span>

## <span data-ttu-id="2fc3a-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fc3a-199">OUTPUTS</span></span>

### <span data-ttu-id="2fc3a-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="2fc3a-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="2fc3a-201">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2fc3a-201">NOTES</span></span>

## <span data-ttu-id="2fc3a-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fc3a-202">RELATED LINKS</span></span>

[<span data-ttu-id="2fc3a-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2fc3a-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="2fc3a-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2fc3a-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="2fc3a-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2fc3a-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
