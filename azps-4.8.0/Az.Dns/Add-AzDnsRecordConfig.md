---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025363"
---
# <span data-ttu-id="2688b-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2688b-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="2688b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2688b-102">SYNOPSIS</span></span>
<span data-ttu-id="2688b-103">DNS-rekordot ad hozzá egy helyi rekordtípus-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="2688b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2688b-104">SYNTAX</span></span>

### <span data-ttu-id="2688b-105">Egy</span><span class="sxs-lookup"><span data-stu-id="2688b-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2688b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="2688b-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2688b-107">NS</span><span class="sxs-lookup"><span data-stu-id="2688b-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2688b-108">MX</span><span class="sxs-lookup"><span data-stu-id="2688b-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2688b-109">PTR</span><span class="sxs-lookup"><span data-stu-id="2688b-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2688b-110">TXT</span><span class="sxs-lookup"><span data-stu-id="2688b-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2688b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="2688b-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2688b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="2688b-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2688b-113">CAA</span><span class="sxs-lookup"><span data-stu-id="2688b-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2688b-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="2688b-114">DESCRIPTION</span></span>
<span data-ttu-id="2688b-115">A **Add-AzDnsRecordConfig** PARANCSMAG egy DNS-rekordot ad hozzá egy **Recordset** objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="2688b-116">A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.</span><span class="sxs-lookup"><span data-stu-id="2688b-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="2688b-117">A SOA rekordok akkor jönnek létre, amikor létrejön egy DNS-zóna, és törlődik a DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="2688b-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="2688b-118">Nem adhat hozzá vagy távolíthat el SOA rekordokat, de szerkesztheti őket.</span><span class="sxs-lookup"><span data-stu-id="2688b-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="2688b-119">A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="2688b-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="2688b-120">Példák</span><span class="sxs-lookup"><span data-stu-id="2688b-120">EXAMPLES</span></span>

### <span data-ttu-id="2688b-121">1. példa: rekord felvétele a rekordba</span><span class="sxs-lookup"><span data-stu-id="2688b-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-122">Ez a példa egy rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="2688b-123">2. példa: AAAA rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="2688b-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-124">Ebben a példában az AAAA-rekordot egy meglévő rekorddal egészíti ki.</span><span class="sxs-lookup"><span data-stu-id="2688b-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="2688b-125">3. példa: CNAME rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="2688b-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-126">Ez a példa CNAME rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="2688b-127">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, kezdetben üres rekordnak kell lennie, vagy a meglévő rekordokat el kell távolítani a Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="2688b-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="2688b-128">4. példa: MX rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="2688b-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-129">Ez a példa MX rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="2688b-130">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="2688b-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="2688b-131">Példa 5: NS rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="2688b-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-132">Ebben a példában egy NS rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="2688b-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="2688b-133">Példa 6: PTR rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="2688b-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-134">Ebben a példában egy PTR rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="2688b-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="2688b-135">7. példa: SRV rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="2688b-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-136">Ebben a példában egy SRV rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="2688b-137">8. példa: TXT rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="2688b-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="2688b-138">Ez a példa egy TXT rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="2688b-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="2688b-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2688b-139">PARAMETERS</span></span>

### <span data-ttu-id="2688b-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="2688b-140">-CaaFlags</span></span>
<span data-ttu-id="2688b-141">A felvenni kívánt CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="2688b-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="2688b-142">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2688b-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="2688b-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="2688b-143">-CaaTag</span></span>
<span data-ttu-id="2688b-144">A felvenni kívánt CAA-rekord címke mezője</span><span class="sxs-lookup"><span data-stu-id="2688b-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="2688b-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="2688b-145">-CaaValue</span></span>
<span data-ttu-id="2688b-146">A hozzáadni kívánt CAA rekord érték mezője</span><span class="sxs-lookup"><span data-stu-id="2688b-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="2688b-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="2688b-147">-Cname</span></span>
<span data-ttu-id="2688b-148">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="2688b-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2688b-149">-DefaultProfile</span></span>
<span data-ttu-id="2688b-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2688b-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2688b-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="2688b-151">-Exchange</span></span>
<span data-ttu-id="2688b-152">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="2688b-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="2688b-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="2688b-153">-Ipv4Address</span></span>
<span data-ttu-id="2688b-154">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="2688b-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="2688b-155">-Ipv6Address</span></span>
<span data-ttu-id="2688b-156">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="2688b-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="2688b-157">-Nsdname</span></span>
<span data-ttu-id="2688b-158">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="2688b-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="2688b-159">-Port</span><span class="sxs-lookup"><span data-stu-id="2688b-159">-Port</span></span>
<span data-ttu-id="2688b-160">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="2688b-161">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="2688b-161">-Preference</span></span>
<span data-ttu-id="2688b-162">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="2688b-163">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="2688b-163">-Priority</span></span>
<span data-ttu-id="2688b-164">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="2688b-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="2688b-165">-Ptrdname</span></span>
<span data-ttu-id="2688b-166">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="2688b-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="2688b-167">-RecordSet</span></span>
<span data-ttu-id="2688b-168">A szerkesztendő **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="2688b-169">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="2688b-169">-Target</span></span>
<span data-ttu-id="2688b-170">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="2688b-171">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="2688b-171">-Value</span></span>
<span data-ttu-id="2688b-172">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="2688b-173">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="2688b-173">-Weight</span></span>
<span data-ttu-id="2688b-174">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2688b-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="2688b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2688b-175">CommonParameters</span></span>
<span data-ttu-id="2688b-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2688b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2688b-177">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2688b-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2688b-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2688b-178">INPUTS</span></span>

### <span data-ttu-id="2688b-179">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2688b-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="2688b-180">System. String</span><span class="sxs-lookup"><span data-stu-id="2688b-180">System.String</span></span>

### <span data-ttu-id="2688b-181">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="2688b-181">System.UInt16</span></span>

### <span data-ttu-id="2688b-182">System. byte</span><span class="sxs-lookup"><span data-stu-id="2688b-182">System.Byte</span></span>

## <span data-ttu-id="2688b-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2688b-183">OUTPUTS</span></span>

### <span data-ttu-id="2688b-184">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2688b-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="2688b-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2688b-185">NOTES</span></span>

## <span data-ttu-id="2688b-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2688b-186">RELATED LINKS</span></span>

[<span data-ttu-id="2688b-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2688b-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="2688b-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2688b-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="2688b-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2688b-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
