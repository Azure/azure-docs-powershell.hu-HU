---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: aa67873ba55f815e7fdd8ada4658370c16e65c4e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183607"
---
# <span data-ttu-id="9f944-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9f944-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="9f944-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f944-102">SYNOPSIS</span></span>
<span data-ttu-id="9f944-103">Eltávolítja a DNS-rekordokat egy helyi rekordtípus-objektumból.</span><span class="sxs-lookup"><span data-stu-id="9f944-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="9f944-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f944-104">SYNTAX</span></span>

### <span data-ttu-id="9f944-105">Egy</span><span class="sxs-lookup"><span data-stu-id="9f944-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f944-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9f944-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f944-107">NS</span><span class="sxs-lookup"><span data-stu-id="9f944-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f944-108">MX</span><span class="sxs-lookup"><span data-stu-id="9f944-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f944-109">PTR</span><span class="sxs-lookup"><span data-stu-id="9f944-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f944-110">TXT</span><span class="sxs-lookup"><span data-stu-id="9f944-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f944-111">SRV</span><span class="sxs-lookup"><span data-stu-id="9f944-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f944-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f944-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f944-113">CAA</span><span class="sxs-lookup"><span data-stu-id="9f944-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f944-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f944-114">DESCRIPTION</span></span>
<span data-ttu-id="9f944-115">A **Remove-AzDnsRecordConfig** parancsmag a Domain Name System (DNS) rekordot egy rekorddal távolítja el.</span><span class="sxs-lookup"><span data-stu-id="9f944-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="9f944-116">A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.</span><span class="sxs-lookup"><span data-stu-id="9f944-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="9f944-117">Ha el szeretne távolítani egy rekordot, a rekordtípus minden mezőjének pontosan egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="9f944-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="9f944-118">A SOA rekordok nem vehetők fel és nem távolíthatók el.</span><span class="sxs-lookup"><span data-stu-id="9f944-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="9f944-119">A rendszer automatikusan létrehozza a SOA-rekordokat, amikor létrejön egy DNS-zóna, és automatikusan törlődik a DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="9f944-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="9f944-120">A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="9f944-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="9f944-121">Példák</span><span class="sxs-lookup"><span data-stu-id="9f944-121">EXAMPLES</span></span>

### <span data-ttu-id="9f944-122">1. példa: rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-123">Ez a példa egy meglévő rekordtípus rekordjainak eltávolítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="9f944-124">Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="9f944-125">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9f944-126">2. példa: az AAAA rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-127">Ez a példa eltávolítja az AAAA-rekordot egy meglévő rekorddal.</span><span class="sxs-lookup"><span data-stu-id="9f944-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="9f944-128">Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="9f944-129">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9f944-130">3. példa: CNAME rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-131">Ez a példa eltávolítja a CNAME rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="9f944-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="9f944-132">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="9f944-133">4. példa: MX rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-134">Ebben a példában egy MX rekord törlődik egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="9f944-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="9f944-135">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="9f944-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="9f944-136">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9f944-137">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9f944-138">Példa 5: a NÉVKISZOLGÁLÓI rekordok eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-139">Ez a példa eltávolítja a NÉVKISZOLGÁLÓI rekordokat egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="9f944-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="9f944-140">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9f944-141">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9f944-142">Példa 6: a PTR rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-143">Ez a példa eltávolítja a PTR rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="9f944-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="9f944-144">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9f944-145">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9f944-146">7. példa: SRV rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-147">Ez a példa eltávolítja az SRV rekordot egy meglévő rekorddal.</span><span class="sxs-lookup"><span data-stu-id="9f944-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="9f944-148">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9f944-149">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9f944-150">8. példa: TXT rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="9f944-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="9f944-151">Ez a példa eltávolítja a TXT rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="9f944-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="9f944-152">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="9f944-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9f944-153">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="9f944-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="9f944-154">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f944-154">PARAMETERS</span></span>

### <span data-ttu-id="9f944-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="9f944-155">-CaaFlags</span></span>
<span data-ttu-id="9f944-156">A felvenni kívánt CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="9f944-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="9f944-157">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="9f944-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="9f944-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="9f944-158">-CaaTag</span></span>
<span data-ttu-id="9f944-159">A felvenni kívánt CAA-rekord címke mezője</span><span class="sxs-lookup"><span data-stu-id="9f944-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="9f944-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="9f944-160">-CaaValue</span></span>
<span data-ttu-id="9f944-161">A hozzáadni kívánt CAA rekord érték mezője</span><span class="sxs-lookup"><span data-stu-id="9f944-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="9f944-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="9f944-162">-Cname</span></span>
<span data-ttu-id="9f944-163">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="9f944-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f944-164">-DefaultProfile</span></span>
<span data-ttu-id="9f944-165">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f944-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f944-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9f944-166">-Exchange</span></span>
<span data-ttu-id="9f944-167">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="9f944-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="9f944-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9f944-168">-Ipv4Address</span></span>
<span data-ttu-id="9f944-169">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="9f944-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="9f944-170">-Ipv6Address</span></span>
<span data-ttu-id="9f944-171">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="9f944-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="9f944-172">-Nsdname</span></span>
<span data-ttu-id="9f944-173">A névkiszolgálói (NS) rekordok névkiszolgálói rekordjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="9f944-174">-Port</span><span class="sxs-lookup"><span data-stu-id="9f944-174">-Port</span></span>
<span data-ttu-id="9f944-175">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="9f944-176">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="9f944-176">-Preference</span></span>
<span data-ttu-id="9f944-177">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="9f944-178">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="9f944-178">-Priority</span></span>
<span data-ttu-id="9f944-179">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="9f944-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9f944-180">-Ptrdname</span></span>
<span data-ttu-id="9f944-181">A Pointer (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="9f944-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="9f944-182">-RecordSet</span></span>
<span data-ttu-id="9f944-183">Megadja az eltávolítandó rekordot tartalmazó **Recordset** objektumot.</span><span class="sxs-lookup"><span data-stu-id="9f944-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="9f944-184">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="9f944-184">-Target</span></span>
<span data-ttu-id="9f944-185">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="9f944-186">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="9f944-186">-Value</span></span>
<span data-ttu-id="9f944-187">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="9f944-188">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="9f944-188">-Weight</span></span>
<span data-ttu-id="9f944-189">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f944-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="9f944-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f944-190">CommonParameters</span></span>
<span data-ttu-id="9f944-191">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f944-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f944-192">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f944-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f944-193">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f944-193">INPUTS</span></span>

### <span data-ttu-id="9f944-194">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9f944-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="9f944-195">System. String</span><span class="sxs-lookup"><span data-stu-id="9f944-195">System.String</span></span>

### <span data-ttu-id="9f944-196">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="9f944-196">System.UInt16</span></span>

### <span data-ttu-id="9f944-197">System. byte</span><span class="sxs-lookup"><span data-stu-id="9f944-197">System.Byte</span></span>

## <span data-ttu-id="9f944-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f944-198">OUTPUTS</span></span>

### <span data-ttu-id="9f944-199">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9f944-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="9f944-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f944-200">NOTES</span></span>

## <span data-ttu-id="9f944-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f944-201">RELATED LINKS</span></span>

[<span data-ttu-id="9f944-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9f944-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="9f944-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9f944-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="9f944-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9f944-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
