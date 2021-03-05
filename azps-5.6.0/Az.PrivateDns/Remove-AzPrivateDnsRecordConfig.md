---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: cd0e2f2913a950e677b1f7294076351556b81c80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005862"
---
# <span data-ttu-id="71f0e-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="71f0e-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="71f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="71f0e-103">Eltávolít egy privát DNS-rekordot egy helyi rekordkészlet-objektumból.</span><span class="sxs-lookup"><span data-stu-id="71f0e-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="71f0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71f0e-104">SYNTAX</span></span>

### <span data-ttu-id="71f0e-105">A (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71f0e-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f0e-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="71f0e-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f0e-107">MX</span><span class="sxs-lookup"><span data-stu-id="71f0e-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f0e-108">PTR</span><span class="sxs-lookup"><span data-stu-id="71f0e-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f0e-109">TXT</span><span class="sxs-lookup"><span data-stu-id="71f0e-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f0e-110">SRV</span><span class="sxs-lookup"><span data-stu-id="71f0e-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f0e-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="71f0e-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71f0e-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71f0e-112">DESCRIPTION</span></span>
<span data-ttu-id="71f0e-113">A Remove-AzPrivateDnsRecordConfig parancsmag eltávolít egy DNS-rekordot egy rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="71f0e-114">A RecordSet objektum egy offline objektum, és módosításai nem módosítják a privát DNS-válaszokat mindaddig, amíg a Set-AzPrivateDnsRecordSet-parancsmag futtatásával meg nem őrzi a Módosítást a Microsoft Azure Private DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="71f0e-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="71f0e-115">Rekord eltávolításához az adott rekordtípus összes mezőjének pontosan egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="71f0e-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="71f0e-116">SoA rekordokat nem adhat hozzá és nem távolíthat el.</span><span class="sxs-lookup"><span data-stu-id="71f0e-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="71f0e-117">A SOA-rekordok automatikusan létrejönnek egy privát DNS-zóna létrehozásakor, és a privát DNS-zóna törlésekor automatikusan törlődnek.</span><span class="sxs-lookup"><span data-stu-id="71f0e-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="71f0e-118">A RecordSet objektumot paraméterként vagy a folyamat műveleti jelének használatával is át lehet adni ennek a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="71f0e-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="71f0e-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71f0e-119">EXAMPLES</span></span>

### <span data-ttu-id="71f0e-120">1. példa: A rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-121">Ez a példa eltávolít egy A rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="71f0e-122">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet lesz.</span><span class="sxs-lookup"><span data-stu-id="71f0e-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="71f0e-123">Ha teljes egészében el szeretne távolítani egy rekordkészletet, tekintse meg a Remove-AzPrivateDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="71f0e-124">2. példa: AAAA rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-125">Ez a példa eltávolít egy AAAA rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="71f0e-126">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet lesz.</span><span class="sxs-lookup"><span data-stu-id="71f0e-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="71f0e-127">Ha teljes egészében el szeretne távolítani egy rekordkészletet, tekintse meg a Remove-AzPrivateDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="71f0e-128">3. példa: CNAME rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-129">Ez a példa eltávolít egy CNAME rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="71f0e-130">Mivel a CNAME rekordkészletek legfeljebb egy rekordot tartalmazhatnak, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="71f0e-131">4. példa: MX rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-132">Ez a példa eltávolít egy MX rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="71f0e-133">A "@" rekordnév a zóna csúcsán beállított rekordot jelzi.</span><span class="sxs-lookup"><span data-stu-id="71f0e-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="71f0e-134">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="71f0e-135">Ha teljes egészében el szeretne távolítani egy rekordkészletet, tekintse meg a Remove-AzPrivateDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="71f0e-136">5. példa: PTR-rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-137">Ez a példa eltávolít egy PTR rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="71f0e-138">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="71f0e-139">Ha teljes egészében el szeretne távolítani egy rekordkészletet, tekintse meg a Remove-AzPrivateDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="71f0e-140">6. példa: SRV rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-141">Ez a példa eltávolít egy SRV rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="71f0e-142">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="71f0e-143">Ha teljes egészében el szeretne távolítani egy rekordkészletet, tekintse meg a Remove-AzPrivateDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="71f0e-144">7. példa: TXT rekord eltávolítása egy rekordkészletből</span><span class="sxs-lookup"><span data-stu-id="71f0e-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="71f0e-145">Ez a példa eltávolít egy TXT rekordot egy meglévő rekordkészletből.</span><span class="sxs-lookup"><span data-stu-id="71f0e-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="71f0e-146">Ha ez az egyetlen rekord a rekordkészletben, az eredmény egy üres rekordkészlet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="71f0e-147">Ha teljes egészében el szeretne távolítani egy rekordkészletet, tekintse meg a Remove-AzPrivateDnsRecordSet rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="71f0e-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="71f0e-148">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71f0e-148">PARAMETERS</span></span>

### <span data-ttu-id="71f0e-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="71f0e-149">-Cname</span></span>
<span data-ttu-id="71f0e-150">Az eltávolítható CNAME rekord canonical neve.</span><span class="sxs-lookup"><span data-stu-id="71f0e-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="71f0e-151">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="71f0e-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="71f0e-152">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="71f0e-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="71f0e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f0e-153">-DefaultProfile</span></span>
<span data-ttu-id="71f0e-154">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71f0e-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71f0e-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="71f0e-155">-Exchange</span></span>
<span data-ttu-id="71f0e-156">Az eltávolítható MX rekord levelezési szolgáltatója.</span><span class="sxs-lookup"><span data-stu-id="71f0e-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="71f0e-157">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="71f0e-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="71f0e-158">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="71f0e-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="71f0e-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="71f0e-159">-Ipv4Address</span></span>
<span data-ttu-id="71f0e-160">Az eltávolítható A rekord IPv4-címe.</span><span class="sxs-lookup"><span data-stu-id="71f0e-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="71f0e-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="71f0e-161">-Ipv6Address</span></span>
<span data-ttu-id="71f0e-162">Az eltávolítható AAAA rekord IPv6-címe.</span><span class="sxs-lookup"><span data-stu-id="71f0e-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="71f0e-163">-Port</span><span class="sxs-lookup"><span data-stu-id="71f0e-163">-Port</span></span>
<span data-ttu-id="71f0e-164">Az eltávolítható SRV rekord portszáma.</span><span class="sxs-lookup"><span data-stu-id="71f0e-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="71f0e-165">-Preference</span><span class="sxs-lookup"><span data-stu-id="71f0e-165">-Preference</span></span>
<span data-ttu-id="71f0e-166">Az eltávolítható MX rekord beállításértéke.</span><span class="sxs-lookup"><span data-stu-id="71f0e-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="71f0e-167">-Priority</span><span class="sxs-lookup"><span data-stu-id="71f0e-167">-Priority</span></span>
<span data-ttu-id="71f0e-168">Az eltávolítható SRV rekord prioritásértéke.</span><span class="sxs-lookup"><span data-stu-id="71f0e-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="71f0e-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="71f0e-169">-Ptrdname</span></span>
<span data-ttu-id="71f0e-170">Az eltávolítható PTR-rekord cél állomása.</span><span class="sxs-lookup"><span data-stu-id="71f0e-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="71f0e-171">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="71f0e-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="71f0e-172">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="71f0e-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="71f0e-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="71f0e-173">-RecordSet</span></span>
<span data-ttu-id="71f0e-174">Az a rekordkészlet, amelyből el szeretné távolítani a rekordot.</span><span class="sxs-lookup"><span data-stu-id="71f0e-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="71f0e-175">-Target</span><span class="sxs-lookup"><span data-stu-id="71f0e-175">-Target</span></span>
<span data-ttu-id="71f0e-176">Az eltávolítható SRV rekord cél állomása.</span><span class="sxs-lookup"><span data-stu-id="71f0e-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="71f0e-177">Nem lehet a zóna nevéhez képest.</span><span class="sxs-lookup"><span data-stu-id="71f0e-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="71f0e-178">Nem lehet befejezési pont</span><span class="sxs-lookup"><span data-stu-id="71f0e-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="71f0e-179">-Érték</span><span class="sxs-lookup"><span data-stu-id="71f0e-179">-Value</span></span>
<span data-ttu-id="71f0e-180">Az eltávolítható TXT rekord szöveges értéke.</span><span class="sxs-lookup"><span data-stu-id="71f0e-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="71f0e-181">-Weight</span><span class="sxs-lookup"><span data-stu-id="71f0e-181">-Weight</span></span>
<span data-ttu-id="71f0e-182">Az eltávolítható SRV rekord súlyértéke.</span><span class="sxs-lookup"><span data-stu-id="71f0e-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="71f0e-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f0e-183">CommonParameters</span></span>
<span data-ttu-id="71f0e-184">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f0e-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f0e-185">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f0e-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f0e-186">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71f0e-186">INPUTS</span></span>

### <span data-ttu-id="71f0e-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="71f0e-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="71f0e-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71f0e-188">OUTPUTS</span></span>

### <span data-ttu-id="71f0e-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="71f0e-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="71f0e-190">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71f0e-190">NOTES</span></span>

## <span data-ttu-id="71f0e-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71f0e-191">RELATED LINKS</span></span>
