---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: 885c7ad64b207f74fa7953050a6ceba9ecc44f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935090"
---
# <span data-ttu-id="53b64-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="53b64-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="53b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53b64-102">SYNOPSIS</span></span>
<span data-ttu-id="53b64-103">Hozzáad egy DNS-rekordot egy helyi rekordkészlet-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="53b64-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="53b64-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53b64-104">SYNTAX</span></span>

### <span data-ttu-id="53b64-105">A</span><span class="sxs-lookup"><span data-stu-id="53b64-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b64-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="53b64-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b64-107">NS</span><span class="sxs-lookup"><span data-stu-id="53b64-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b64-108">MX</span><span class="sxs-lookup"><span data-stu-id="53b64-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b64-109">PTR</span><span class="sxs-lookup"><span data-stu-id="53b64-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b64-110">TXT</span><span class="sxs-lookup"><span data-stu-id="53b64-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b64-111">SRV</span><span class="sxs-lookup"><span data-stu-id="53b64-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b64-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="53b64-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b64-113">Caa</span><span class="sxs-lookup"><span data-stu-id="53b64-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53b64-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53b64-114">DESCRIPTION</span></span>
<span data-ttu-id="53b64-115">Az **Add-AzDnsRecordConfig** parancsmag hozzáad egy DNS-rekordot egy **RecordSet-objektumhoz.**</span><span class="sxs-lookup"><span data-stu-id="53b64-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="53b64-116">A **RecordSet** objektum egy offline objektum, és a módosításai nem módosítják a DNS-válaszokat mindaddig, amíg a Set-AzDnsRecordSet-parancsmag futtatásával meg nem őrzi a Microsoft Azure DNS-szolgáltatás módosításait.</span><span class="sxs-lookup"><span data-stu-id="53b64-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="53b64-117">A SOA-rekordok a DNS-zóna létrehozásakor jön létre, és a DNS-zóna törlésekor törlődnek.</span><span class="sxs-lookup"><span data-stu-id="53b64-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="53b64-118">SoA rekordokat nem adhat hozzá és nem távolíthat el, de szerkesztheti őket.</span><span class="sxs-lookup"><span data-stu-id="53b64-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="53b64-119">A **RecordSet** objektumot paraméterként vagy a folyamat műveleti jelének használatával is át lehet adni ennek a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="53b64-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="53b64-120">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53b64-120">EXAMPLES</span></span>

### <span data-ttu-id="53b64-121">1. példa: A rekord hozzáadása rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-122">Ebben a példában egy A rekordot ad hozzá egy meglévő rekordkészlethez.</span><span class="sxs-lookup"><span data-stu-id="53b64-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="53b64-123">2. példa: AAAA rekord hozzáadása egy rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-124">Ebben a példában egy AAAA rekordot egy meglévő rekordkészlethez ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="53b64-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="53b64-125">3. példa: CNAME rekord hozzáadása egy rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-126">Ebben a példában egy CNAME rekordot egy meglévő rekordkészlethez ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="53b64-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="53b64-127">Mivel a CNAME rekordkészletek legfeljebb egy rekordot tartalmazhatnak, kezdetben üres rekordkészletnek kell lennie, vagy a meglévő rekordokat el kell távolítani a Remove-AzDnsRecordConfig használatával.</span><span class="sxs-lookup"><span data-stu-id="53b64-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="53b64-128">4. példa: MX rekord hozzáadása rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-129">Ebben a példában egy MX rekordot egy meglévő rekordkészlethez ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="53b64-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="53b64-130">A "@" rekordnév a zóna csúcsán beállított rekordot jelzi.</span><span class="sxs-lookup"><span data-stu-id="53b64-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="53b64-131">5. példa: NS rekord hozzáadása egy rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-132">Ebben a példában egy NS rekordot ad hozzá egy meglévő rekordkészlethez.</span><span class="sxs-lookup"><span data-stu-id="53b64-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="53b64-133">6. példa: PTR-rekord hozzáadása egy rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-134">Ebben a példában egy PTR rekordot ad hozzá egy meglévő rekordkészlethez.</span><span class="sxs-lookup"><span data-stu-id="53b64-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="53b64-135">7. példa: SRV rekord felvétele rekordkészletbe</span><span class="sxs-lookup"><span data-stu-id="53b64-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-136">Ez a példa hozzáad egy SRV rekordot egy meglévő rekordkészlethez.</span><span class="sxs-lookup"><span data-stu-id="53b64-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="53b64-137">8. példa: TXT rekord hozzáadása egy rekordkészlethez</span><span class="sxs-lookup"><span data-stu-id="53b64-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="53b64-138">Ebben a példában egy TXT rekordot egy meglévő rekordkészlethez ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="53b64-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="53b64-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53b64-139">PARAMETERS</span></span>

### <span data-ttu-id="53b64-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="53b64-140">-CaaFlags</span></span>
<span data-ttu-id="53b64-141">A hozzáadni megfelelő CAA-rekord jelzői.</span><span class="sxs-lookup"><span data-stu-id="53b64-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="53b64-142">0 és 255 közötti számnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="53b64-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="53b64-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="53b64-143">-CaaTag</span></span>
<span data-ttu-id="53b64-144">A hozzáadni megfelelő CAA-rekord címkemezője.</span><span class="sxs-lookup"><span data-stu-id="53b64-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="53b64-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="53b64-145">-CaaValue</span></span>
<span data-ttu-id="53b64-146">Az összeadni megfelelő CAA-rekord értékmezője.</span><span class="sxs-lookup"><span data-stu-id="53b64-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="53b64-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="53b64-147">-Cname</span></span>
<span data-ttu-id="53b64-148">Egy canonical name (CNAME) rekord tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="53b64-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b64-149">-DefaultProfile</span></span>
<span data-ttu-id="53b64-150">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53b64-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53b64-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="53b64-151">-Exchange</span></span>
<span data-ttu-id="53b64-152">Egy MX rekord levelezési kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="53b64-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="53b64-153">-Ipv4Address</span></span>
<span data-ttu-id="53b64-154">Egy A rekord IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="53b64-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="53b64-155">-Ipv6Address</span></span>
<span data-ttu-id="53b64-156">Egy AAAA-rekord IPv6-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="53b64-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="53b64-157">-Nsdname</span></span>
<span data-ttu-id="53b64-158">A névkiszolgálói (NS) rekord névkiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="53b64-159">-Port</span><span class="sxs-lookup"><span data-stu-id="53b64-159">-Port</span></span>
<span data-ttu-id="53b64-160">Egy szolgáltatásrekord portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="53b64-161">-Preference</span><span class="sxs-lookup"><span data-stu-id="53b64-161">-Preference</span></span>
<span data-ttu-id="53b64-162">Az MX rekord beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="53b64-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="53b64-163">-Priority</span></span>
<span data-ttu-id="53b64-164">Egy SRV rekord prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="53b64-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="53b64-165">-Ptrdname</span></span>
<span data-ttu-id="53b64-166">Egy mutatóerőforrás (PTR) céltartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="53b64-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="53b64-167">-RecordSet</span></span>
<span data-ttu-id="53b64-168">A **szerkesztenie kell a RecordSet** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="53b64-169">-Target</span><span class="sxs-lookup"><span data-stu-id="53b64-169">-Target</span></span>
<span data-ttu-id="53b64-170">Egy SRV rekord célértékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="53b64-171">-Érték</span><span class="sxs-lookup"><span data-stu-id="53b64-171">-Value</span></span>
<span data-ttu-id="53b64-172">Egy TXT rekord értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="53b64-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="53b64-173">-Weight</span></span>
<span data-ttu-id="53b64-174">Az SRV rekord súlyát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="53b64-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="53b64-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b64-175">CommonParameters</span></span>
<span data-ttu-id="53b64-176">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b64-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b64-177">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b64-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b64-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53b64-178">INPUTS</span></span>

### <span data-ttu-id="53b64-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53b64-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="53b64-180">System.String</span><span class="sxs-lookup"><span data-stu-id="53b64-180">System.String</span></span>

### <span data-ttu-id="53b64-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="53b64-181">System.UInt16</span></span>

### <span data-ttu-id="53b64-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="53b64-182">System.Byte</span></span>

## <span data-ttu-id="53b64-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53b64-183">OUTPUTS</span></span>

### <span data-ttu-id="53b64-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53b64-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="53b64-185">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53b64-185">NOTES</span></span>

## <span data-ttu-id="53b64-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53b64-186">RELATED LINKS</span></span>

[<span data-ttu-id="53b64-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53b64-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="53b64-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="53b64-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="53b64-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="53b64-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
