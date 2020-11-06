---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: c9e824160b04b183414c6b99fce4b09b6d70766a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493791"
---
# <span data-ttu-id="6b1ab-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6b1ab-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="6b1ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1ab-103">DNS-rekordot ad hozzá egy helyi rekordtípus-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b1ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b1ab-104">SYNTAX</span></span>

### <span data-ttu-id="6b1ab-105">Egy</span><span class="sxs-lookup"><span data-stu-id="6b1ab-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="6b1ab-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-107">NS</span><span class="sxs-lookup"><span data-stu-id="6b1ab-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-108">MX</span><span class="sxs-lookup"><span data-stu-id="6b1ab-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-109">PTR</span><span class="sxs-lookup"><span data-stu-id="6b1ab-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-110">TXT</span><span class="sxs-lookup"><span data-stu-id="6b1ab-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-111">SRV</span><span class="sxs-lookup"><span data-stu-id="6b1ab-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="6b1ab-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b1ab-113">CAA</span><span class="sxs-lookup"><span data-stu-id="6b1ab-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b1ab-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b1ab-114">DESCRIPTION</span></span>
<span data-ttu-id="6b1ab-115">A **Add-AzureRmDnsRecordConfig** PARANCSMAG egy DNS-rekordot ad hozzá egy **Recordset** objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="6b1ab-116">A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzureRmDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="6b1ab-117">A SOA rekordok akkor jönnek létre, amikor létrejön egy DNS-zóna, és törlődik a DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="6b1ab-118">Nem adhat hozzá vagy távolíthat el SOA rekordokat, de szerkesztheti őket.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-118">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="6b1ab-119">A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="6b1ab-120">Példák</span><span class="sxs-lookup"><span data-stu-id="6b1ab-120">EXAMPLES</span></span>

### <span data-ttu-id="6b1ab-121">1. példa: rekord felvétele a rekordba</span><span class="sxs-lookup"><span data-stu-id="6b1ab-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-122">Ez a példa egy rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="6b1ab-123">2. példa: AAAA rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="6b1ab-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-124">Ebben a példában az AAAA-rekordot egy meglévő rekorddal egészíti ki.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="6b1ab-125">3. példa: CNAME rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="6b1ab-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-126">Ez a példa CNAME rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="6b1ab-127">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, kezdetben üres rekordnak kell lennie, vagy a meglévő rekordokat el kell távolítani a Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="6b1ab-128">4. példa: MX rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="6b1ab-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-129">Ez a példa MX rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="6b1ab-130">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="6b1ab-131">Példa 5: NS rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="6b1ab-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-132">Ebben a példában egy NS rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="6b1ab-133">Példa 6: PTR rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="6b1ab-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-134">Ebben a példában egy PTR rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="6b1ab-135">7. példa: SRV rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="6b1ab-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-136">Ebben a példában egy SRV rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="6b1ab-137">8. példa: TXT rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="6b1ab-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6b1ab-138">Ez a példa egy TXT rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="6b1ab-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b1ab-139">PARAMETERS</span></span>

### <span data-ttu-id="6b1ab-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="6b1ab-140">-CaaFlags</span></span>
<span data-ttu-id="6b1ab-141">A felvenni kívánt CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="6b1ab-142">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="6b1ab-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="6b1ab-143">-CaaTag</span></span>
<span data-ttu-id="6b1ab-144">A felvenni kívánt CAA-rekord címke mezője</span><span class="sxs-lookup"><span data-stu-id="6b1ab-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="6b1ab-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="6b1ab-145">-CaaValue</span></span>
<span data-ttu-id="6b1ab-146">A hozzáadni kívánt CAA rekord érték mezője</span><span class="sxs-lookup"><span data-stu-id="6b1ab-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="6b1ab-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="6b1ab-147">-Cname</span></span>
<span data-ttu-id="6b1ab-148">Egy kanonikus név (CNAME rekord) tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1ab-149">-DefaultProfile</span></span>
<span data-ttu-id="6b1ab-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6b1ab-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b1ab-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6b1ab-151">-Exchange</span></span>
<span data-ttu-id="6b1ab-152">A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="6b1ab-153">-Ipv4Address</span></span>
<span data-ttu-id="6b1ab-154">Egy rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="6b1ab-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="6b1ab-155">-Ipv6Address</span></span>
<span data-ttu-id="6b1ab-156">Az AAAA rekordok IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-156">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="6b1ab-157">-Nsdname</span></span>
<span data-ttu-id="6b1ab-158">A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-158">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-159">-Port</span><span class="sxs-lookup"><span data-stu-id="6b1ab-159">-Port</span></span>
<span data-ttu-id="6b1ab-160">A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-160">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-161">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="6b1ab-161">-Preference</span></span>
<span data-ttu-id="6b1ab-162">Az MX rekordok beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-162">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-163">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="6b1ab-163">-Priority</span></span>
<span data-ttu-id="6b1ab-164">Az SRV rekordok prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-164">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6b1ab-165">-Ptrdname</span></span>
<span data-ttu-id="6b1ab-166">A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="6b1ab-167">-RecordSet</span></span>
<span data-ttu-id="6b1ab-168">A szerkesztendő **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-168">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-169">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="6b1ab-169">-Target</span></span>
<span data-ttu-id="6b1ab-170">Az SRV rekordok célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-170">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-171">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="6b1ab-171">-Value</span></span>
<span data-ttu-id="6b1ab-172">A TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-172">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-173">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="6b1ab-173">-Weight</span></span>
<span data-ttu-id="6b1ab-174">Az SRV rekordok vastagságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-174">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1ab-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1ab-175">CommonParameters</span></span>
<span data-ttu-id="6b1ab-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b1ab-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1ab-177">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b1ab-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1ab-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b1ab-178">INPUTS</span></span>

### <span data-ttu-id="6b1ab-179">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b1ab-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6b1ab-180">Ezt a parancsmagot a **rekordhalmaz** -objektum pipe-ba kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-180">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="6b1ab-181">Ez a **rekordhalmaz** kapcsolat nélküli megjelenítése, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg az Set-AzureRmDnsRecordSet parancsmagot nem futtatja.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-181">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="6b1ab-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b1ab-182">OUTPUTS</span></span>

### <span data-ttu-id="6b1ab-183">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b1ab-183">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6b1ab-184">Ez a parancsmag a módosított **Recordset** objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-184">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="6b1ab-185">Az átadott objektumot a program közvetlenül módosítja.</span><span class="sxs-lookup"><span data-stu-id="6b1ab-185">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="6b1ab-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b1ab-186">NOTES</span></span>

## <span data-ttu-id="6b1ab-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b1ab-187">RELATED LINKS</span></span>

[<span data-ttu-id="6b1ab-188">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b1ab-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="6b1ab-189">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6b1ab-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="6b1ab-190">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b1ab-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
