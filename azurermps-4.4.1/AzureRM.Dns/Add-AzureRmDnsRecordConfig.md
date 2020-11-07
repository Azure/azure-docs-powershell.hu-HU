---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 65ab77c7ad94224e3ab2c72072834c43ef1434a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679778"
---
# <span data-ttu-id="b2005-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b2005-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="b2005-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2005-102">SYNOPSIS</span></span>
<span data-ttu-id="b2005-103">DNS-rekordot ad hozzá egy helyi rekordtípus-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2005-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2005-104">SYNTAX</span></span>

### <span data-ttu-id="b2005-105">Egy</span><span class="sxs-lookup"><span data-stu-id="b2005-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2005-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="b2005-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2005-107">NS</span><span class="sxs-lookup"><span data-stu-id="b2005-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2005-108">MX</span><span class="sxs-lookup"><span data-stu-id="b2005-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2005-109">PTR</span><span class="sxs-lookup"><span data-stu-id="b2005-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2005-110">TXT</span><span class="sxs-lookup"><span data-stu-id="b2005-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2005-111">SRV</span><span class="sxs-lookup"><span data-stu-id="b2005-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2005-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="b2005-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2005-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2005-113">DESCRIPTION</span></span>
<span data-ttu-id="b2005-114">A **Add-AzureRmDnsRecordConfig** PARANCSMAG egy DNS-rekordot ad hozzá egy **Recordset** objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="b2005-115">A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzureRmDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.</span><span class="sxs-lookup"><span data-stu-id="b2005-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="b2005-116">A SOA rekordok akkor jönnek létre, amikor létrejön egy DNS-zóna, és törlődik a DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="b2005-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="b2005-117">Nem adhat hozzá vagy távolíthat el SOA rekordokat, de szerkesztheti őket.</span><span class="sxs-lookup"><span data-stu-id="b2005-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="b2005-118">A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="b2005-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="b2005-119">Példák</span><span class="sxs-lookup"><span data-stu-id="b2005-119">EXAMPLES</span></span>

### <span data-ttu-id="b2005-120">1. példa: rekord felvétele a rekordba</span><span class="sxs-lookup"><span data-stu-id="b2005-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-121">Ez a példa egy rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="b2005-122">2. példa: AAAA rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="b2005-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-123">Ebben a példában az AAAA-rekordot egy meglévő rekorddal egészíti ki.</span><span class="sxs-lookup"><span data-stu-id="b2005-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="b2005-124">3. példa: CNAME rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="b2005-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-125">Ez a példa CNAME rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="b2005-126">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, kezdetben üres rekordnak kell lennie, vagy a meglévő rekordokat el kell távolítani a Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="b2005-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="b2005-127">4. példa: MX rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="b2005-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-128">Ez a példa MX rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="b2005-129">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="b2005-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="b2005-130">Példa 5: NS rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="b2005-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-131">Ebben a példában egy NS rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="b2005-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="b2005-132">Példa 6: PTR rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="b2005-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-133">Ebben a példában egy PTR rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="b2005-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="b2005-134">7. példa: SRV rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="b2005-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-135">Ebben a példában egy SRV rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="b2005-136">8. példa: TXT rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="b2005-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b2005-137">Ez a példa egy TXT rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="b2005-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="b2005-138">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2005-138">PARAMETERS</span></span>

### <span data-ttu-id="b2005-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="b2005-139">-Cname</span></span>
<span data-ttu-id="b2005-140">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="b2005-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="b2005-141">-Exchange</span></span>
<span data-ttu-id="b2005-142">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="b2005-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="b2005-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="b2005-143">-Ipv4Address</span></span>
<span data-ttu-id="b2005-144">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="b2005-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="b2005-145">-Ipv6Address</span></span>
<span data-ttu-id="b2005-146">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-146">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="b2005-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="b2005-147">-Nsdname</span></span>
<span data-ttu-id="b2005-148">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="b2005-148">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="b2005-149">-Port</span><span class="sxs-lookup"><span data-stu-id="b2005-149">-Port</span></span>
<span data-ttu-id="b2005-150">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-150">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="b2005-151">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="b2005-151">-Preference</span></span>
<span data-ttu-id="b2005-152">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-152">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="b2005-153">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="b2005-153">-Priority</span></span>
<span data-ttu-id="b2005-154">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-154">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="b2005-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="b2005-155">-Ptrdname</span></span>
<span data-ttu-id="b2005-156">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="b2005-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="b2005-157">-RecordSet</span></span>
<span data-ttu-id="b2005-158">A szerkesztendő **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="b2005-159">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="b2005-159">-Target</span></span>
<span data-ttu-id="b2005-160">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-160">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="b2005-161">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="b2005-161">-Value</span></span>
<span data-ttu-id="b2005-162">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-162">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="b2005-163">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="b2005-163">-Weight</span></span>
<span data-ttu-id="b2005-164">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2005-164">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="b2005-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2005-165">-DefaultProfile</span></span>
<span data-ttu-id="b2005-166">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2005-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2005-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2005-167">CommonParameters</span></span>
<span data-ttu-id="b2005-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2005-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2005-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2005-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2005-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2005-170">INPUTS</span></span>

### <span data-ttu-id="b2005-171">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2005-171">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="b2005-172">Ezt a parancsmagot a **rekordhalmaz** -objektum pipe-ba kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="b2005-172">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="b2005-173">Ez a **rekordhalmaz** kapcsolat nélküli megjelenítése, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg az Set-AzureRmDnsRecordSet parancsmagot nem futtatja.</span><span class="sxs-lookup"><span data-stu-id="b2005-173">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="b2005-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2005-174">OUTPUTS</span></span>

### <span data-ttu-id="b2005-175">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2005-175">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="b2005-176">Ez a parancsmag a módosított **Recordset** objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b2005-176">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="b2005-177">Az átadott objektumot a program közvetlenül módosítja.</span><span class="sxs-lookup"><span data-stu-id="b2005-177">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="b2005-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2005-178">NOTES</span></span>

## <span data-ttu-id="b2005-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2005-179">RELATED LINKS</span></span>

[<span data-ttu-id="b2005-180">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2005-180">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="b2005-181">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b2005-181">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="b2005-182">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2005-182">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
