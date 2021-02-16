---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: aa67873ba55f815e7fdd8ada4658370c16e65c4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209607"
---
# <span data-ttu-id="53d08-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="53d08-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="53d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53d08-102">SYNOPSIS</span></span>
<span data-ttu-id="53d08-103">Eltávolít egy DNS-rekordot egy helyi rekordkészlet-objektumból.</span><span class="sxs-lookup"><span data-stu-id="53d08-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="53d08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53d08-104">SYNTAX</span></span>

### <span data-ttu-id="53d08-105">A</span><span class="sxs-lookup"><span data-stu-id="53d08-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d08-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="53d08-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d08-107">NS</span><span class="sxs-lookup"><span data-stu-id="53d08-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53d08-108">MX</span><span class="sxs-lookup"><span data-stu-id="53d08-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d08-109">PTR</span><span class="sxs-lookup"><span data-stu-id="53d08-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d08-110">TXT</span><span class="sxs-lookup"><span data-stu-id="53d08-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53d08-111">SRV</span><span class="sxs-lookup"><span data-stu-id="53d08-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d08-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="53d08-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53d08-113">Caa</span><span class="sxs-lookup"><span data-stu-id="53d08-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53d08-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53d08-114">DESCRIPTION</span></span>
<span data-ttu-id="53d08-115">A **Remove-AzDnsRecordConfig** parancsmag eltávolít egy DNS-rekordot egy rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="53d08-116">A **RecordSet** objektum egy offline objektum, és a módosításai nem módosítják a DNS-válaszokat mindaddig, amíg a Set-AzDnsRecordSet-parancsmag futtatásával meg nem őrzi a Microsoft Azure DNS-szolgáltatás módosításait.</span><span class="sxs-lookup"><span data-stu-id="53d08-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="53d08-117">Rekord eltávolításához az adott rekordtípus összes mezőjének pontosan egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="53d08-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="53d08-118">SoA rekordokat nem adhat hozzá és nem távolíthat el.</span><span class="sxs-lookup"><span data-stu-id="53d08-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="53d08-119">A SOA-rekordok automatikusan létrejönnek a DNS-zóna létrehozásakor, és a DNS-zóna törlésekor automatikusan törlődnek.</span><span class="sxs-lookup"><span data-stu-id="53d08-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="53d08-120">A **RecordSet** objektumot paraméterként vagy a folyamat műveleti jelének használatával is át lehet adni ennek a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="53d08-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="53d08-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53d08-121">EXAMPLES</span></span>

### <span data-ttu-id="53d08-122">1. példa: A rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-123">Ez a példa eltávolít egy A rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="53d08-124">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet lesz.</span><span class="sxs-lookup"><span data-stu-id="53d08-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="53d08-125">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="53d08-126">2. példa: AAAA rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-127">Ez a példa eltávolít egy AAAA rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="53d08-128">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet lesz.</span><span class="sxs-lookup"><span data-stu-id="53d08-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="53d08-129">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="53d08-130">3. példa: CNAME rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-131">Ez a példa eltávolít egy CNAME rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="53d08-132">Mivel a CNAME rekordkészletek legfeljebb egy rekordot tartalmazhatnak, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="53d08-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="53d08-133">4. példa: MX rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-134">Ez a példa eltávolít egy MX rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="53d08-135">A "@" rekordnév a zóna csúcsán beállított rekordot jelzi.</span><span class="sxs-lookup"><span data-stu-id="53d08-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="53d08-136">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="53d08-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="53d08-137">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="53d08-138">5. példa: NS rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-139">Ez a példa eltávolít egy NS rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="53d08-140">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="53d08-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="53d08-141">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="53d08-142">6. példa: PTR-rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-143">Ez a példa eltávolít egy PTR rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="53d08-144">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="53d08-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="53d08-145">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="53d08-146">7. példa: SRV rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-147">Ez a példa eltávolít egy SRV rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="53d08-148">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="53d08-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="53d08-149">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="53d08-150">8. példa: TXT rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="53d08-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="53d08-151">Ez a példa eltávolít egy TXT rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="53d08-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="53d08-152">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="53d08-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="53d08-153">Ha teljesen el szeretne távolítani egy rekordkészletet, tekintse át a Remove-AzDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="53d08-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="53d08-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53d08-154">PARAMETERS</span></span>

### <span data-ttu-id="53d08-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="53d08-155">-CaaFlags</span></span>
<span data-ttu-id="53d08-156">A hozzáadni megfelelő CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="53d08-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="53d08-157">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="53d08-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="53d08-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="53d08-158">-CaaTag</span></span>
<span data-ttu-id="53d08-159">A hozzáadni megfelelő CAA-rekord címkemezője.</span><span class="sxs-lookup"><span data-stu-id="53d08-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="53d08-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="53d08-160">-CaaValue</span></span>
<span data-ttu-id="53d08-161">Az összeadni megfelelő CAA-rekord értékmezője.</span><span class="sxs-lookup"><span data-stu-id="53d08-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="53d08-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="53d08-162">-Cname</span></span>
<span data-ttu-id="53d08-163">Egy canonical name (CNAME) rekord tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d08-164">-DefaultProfile</span></span>
<span data-ttu-id="53d08-165">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53d08-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53d08-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="53d08-166">-Exchange</span></span>
<span data-ttu-id="53d08-167">Egy MX rekord levelezési kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="53d08-168">-Ipv4Address</span></span>
<span data-ttu-id="53d08-169">Egy A rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="53d08-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="53d08-170">-Ipv6Address</span></span>
<span data-ttu-id="53d08-171">Egy AAAA-rekord IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-171">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="53d08-172">-Nsdname</span></span>
<span data-ttu-id="53d08-173">A névkiszolgálói (NS) rekord névkiszolgálóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-173">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-174">-Port</span><span class="sxs-lookup"><span data-stu-id="53d08-174">-Port</span></span>
<span data-ttu-id="53d08-175">Egy szolgáltatásrekord (SRV) portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-175">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-176">-Preference</span><span class="sxs-lookup"><span data-stu-id="53d08-176">-Preference</span></span>
<span data-ttu-id="53d08-177">Az MX rekord beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-177">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-178">-Priority</span><span class="sxs-lookup"><span data-stu-id="53d08-178">-Priority</span></span>
<span data-ttu-id="53d08-179">Egy SRV rekord prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-179">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="53d08-180">-Ptrdname</span></span>
<span data-ttu-id="53d08-181">Egy mutató (PTR) rekord céltartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="53d08-182">-RecordSet</span></span>
<span data-ttu-id="53d08-183">Az **eltávolítható rekordot tartalmazó RecordSet-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-184">-Target</span><span class="sxs-lookup"><span data-stu-id="53d08-184">-Target</span></span>
<span data-ttu-id="53d08-185">Egy SRV rekord célértékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-185">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-186">-Érték</span><span class="sxs-lookup"><span data-stu-id="53d08-186">-Value</span></span>
<span data-ttu-id="53d08-187">Egy TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-187">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-188">-Weight</span><span class="sxs-lookup"><span data-stu-id="53d08-188">-Weight</span></span>
<span data-ttu-id="53d08-189">Az SRV rekord súlyát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="53d08-189">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53d08-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d08-190">CommonParameters</span></span>
<span data-ttu-id="53d08-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d08-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d08-192">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53d08-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d08-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53d08-193">INPUTS</span></span>

### <span data-ttu-id="53d08-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53d08-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="53d08-195">System.String</span><span class="sxs-lookup"><span data-stu-id="53d08-195">System.String</span></span>

### <span data-ttu-id="53d08-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="53d08-196">System.UInt16</span></span>

### <span data-ttu-id="53d08-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="53d08-197">System.Byte</span></span>

## <span data-ttu-id="53d08-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53d08-198">OUTPUTS</span></span>

### <span data-ttu-id="53d08-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53d08-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="53d08-200">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53d08-200">NOTES</span></span>

## <span data-ttu-id="53d08-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53d08-201">RELATED LINKS</span></span>

[<span data-ttu-id="53d08-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="53d08-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="53d08-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53d08-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="53d08-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53d08-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
