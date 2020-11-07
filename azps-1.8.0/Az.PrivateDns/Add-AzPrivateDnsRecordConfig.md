---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: af3e2e3494aa7f7f98856db3709d4716f5b04e44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669790"
---
# <span data-ttu-id="85c8a-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="85c8a-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="85c8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="85c8a-103">Privát DNS-rekordot ad hozzá egy helyi rekordtípus-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85c8a-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="85c8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85c8a-104">SYNTAX</span></span>

### <span data-ttu-id="85c8a-105">A (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85c8a-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c8a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="85c8a-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c8a-107">MX</span><span class="sxs-lookup"><span data-stu-id="85c8a-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c8a-108">PTR</span><span class="sxs-lookup"><span data-stu-id="85c8a-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c8a-109">TXT</span><span class="sxs-lookup"><span data-stu-id="85c8a-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c8a-110">SRV</span><span class="sxs-lookup"><span data-stu-id="85c8a-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c8a-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="85c8a-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c8a-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="85c8a-112">DESCRIPTION</span></span>
<span data-ttu-id="85c8a-113">A Add-AzPrivateDnsRecordConfig parancsmag egy privát tartománynévrendszer (DNS) rekordot ad hozzá egy RecordSet objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85c8a-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="85c8a-114">A RecordSet objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a magánjellegű DNS-válaszokat, amíg a Set-AzPrivateDnsRecordSet parancsmagot nem futtatja, hogy továbbra is megmaradjon a módosítás a Microsoft Azure Private DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="85c8a-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="85c8a-115">A SOA rekordok akkor jönnek létre, ha egy privát DNS-zóna jön létre, és törlődik a magánhálózati DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="85c8a-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="85c8a-116">Nem adhat hozzá vagy távolíthat el SOA rekordokat, de szerkesztheti őket.</span><span class="sxs-lookup"><span data-stu-id="85c8a-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="85c8a-117">A rekordhalmaz-objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="85c8a-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="85c8a-118">Példák</span><span class="sxs-lookup"><span data-stu-id="85c8a-118">EXAMPLES</span></span>

### <span data-ttu-id="85c8a-119">1. példa: rekord felvétele a rekordba</span><span class="sxs-lookup"><span data-stu-id="85c8a-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="85c8a-120">Ez a példa egy rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="85c8a-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="85c8a-121">2. példa: AAAA rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="85c8a-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="85c8a-122">Ebben a példában egy AAAAA-rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="85c8a-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="85c8a-123">3. példa: CNAME rekord felvétele a Record set-ba</span><span class="sxs-lookup"><span data-stu-id="85c8a-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="85c8a-124">Ez a példa CNAME rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="85c8a-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="85c8a-125">4. példa: MX rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="85c8a-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="85c8a-126">Ez a példa MX rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="85c8a-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="85c8a-127">Példa 5: PTR rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="85c8a-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="85c8a-128">Ebben a példában egy PTR rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="85c8a-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="85c8a-129">Példa 6: SRV rekord hozzáadása a rekordhoz</span><span class="sxs-lookup"><span data-stu-id="85c8a-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="85c8a-130">Ez a példa egy SRV rekordot ad hozzá egy meglévő rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="85c8a-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="85c8a-131">7. példa: TXT rekord hozzáadása a Record set-hoz</span><span class="sxs-lookup"><span data-stu-id="85c8a-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="85c8a-132">Ez a példa egy TXT rekordot szúr be egy meglévő rekordba.</span><span class="sxs-lookup"><span data-stu-id="85c8a-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="85c8a-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85c8a-133">PARAMETERS</span></span>

### <span data-ttu-id="85c8a-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="85c8a-134">-Cname</span></span>
<span data-ttu-id="85c8a-135">A hozzáadni kívánt CNAME rekord kanonikus neve.</span><span class="sxs-lookup"><span data-stu-id="85c8a-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="85c8a-136">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="85c8a-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="85c8a-137">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="85c8a-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="85c8a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c8a-138">-DefaultProfile</span></span>
<span data-ttu-id="85c8a-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85c8a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c8a-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="85c8a-140">-Exchange</span></span>
<span data-ttu-id="85c8a-141">A felvenni kívánt MX rekord levelezési Exchange-állomása.</span><span class="sxs-lookup"><span data-stu-id="85c8a-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="85c8a-142">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="85c8a-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="85c8a-143">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="85c8a-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="85c8a-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="85c8a-144">-Ipv4Address</span></span>
<span data-ttu-id="85c8a-145">A hozzáadni kívánt rekord IPv4-címe.</span><span class="sxs-lookup"><span data-stu-id="85c8a-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="85c8a-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="85c8a-146">-Ipv6Address</span></span>
<span data-ttu-id="85c8a-147">A felvenni kívánt AAAA-rekord IPv6-címe.</span><span class="sxs-lookup"><span data-stu-id="85c8a-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="85c8a-148">-Port</span><span class="sxs-lookup"><span data-stu-id="85c8a-148">-Port</span></span>
<span data-ttu-id="85c8a-149">A hozzáadni kívánt SRV rekord portszáma.</span><span class="sxs-lookup"><span data-stu-id="85c8a-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="85c8a-150">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="85c8a-150">-Preference</span></span>
<span data-ttu-id="85c8a-151">A felvenni kívánt MX rekord preferencia értéke.</span><span class="sxs-lookup"><span data-stu-id="85c8a-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="85c8a-152">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="85c8a-152">-Priority</span></span>
<span data-ttu-id="85c8a-153">A hozzáadandó SRV rekord prioritási értéke.</span><span class="sxs-lookup"><span data-stu-id="85c8a-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="85c8a-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="85c8a-154">-Ptrdname</span></span>
<span data-ttu-id="85c8a-155">A felvenni kívánt PTR-rekord célállomása.</span><span class="sxs-lookup"><span data-stu-id="85c8a-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="85c8a-156">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="85c8a-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="85c8a-157">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="85c8a-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="85c8a-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="85c8a-158">-RecordSet</span></span>
<span data-ttu-id="85c8a-159">Az a rekord, amelybe be szeretné szúrni a rekordot.</span><span class="sxs-lookup"><span data-stu-id="85c8a-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85c8a-160">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="85c8a-160">-Target</span></span>
<span data-ttu-id="85c8a-161">A hozzáadni kívánt SRV rekord célállomása.</span><span class="sxs-lookup"><span data-stu-id="85c8a-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="85c8a-162">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="85c8a-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="85c8a-163">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="85c8a-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="85c8a-164">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="85c8a-164">-Value</span></span>
<span data-ttu-id="85c8a-165">A hozzáadni kívánt TXT rekord szöveges értéke.</span><span class="sxs-lookup"><span data-stu-id="85c8a-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="85c8a-166">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="85c8a-166">-Weight</span></span>
<span data-ttu-id="85c8a-167">A hozzáadandó SRV rekord súlyozó értéke.</span><span class="sxs-lookup"><span data-stu-id="85c8a-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="85c8a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c8a-168">CommonParameters</span></span>
<span data-ttu-id="85c8a-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85c8a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c8a-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c8a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c8a-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85c8a-171">INPUTS</span></span>

### <span data-ttu-id="85c8a-172">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="85c8a-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="85c8a-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85c8a-173">OUTPUTS</span></span>

### <span data-ttu-id="85c8a-174">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="85c8a-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="85c8a-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85c8a-175">NOTES</span></span>

## <span data-ttu-id="85c8a-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85c8a-176">RELATED LINKS</span></span>
