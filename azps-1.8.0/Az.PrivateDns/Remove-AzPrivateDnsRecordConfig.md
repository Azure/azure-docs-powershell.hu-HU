---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 9e5daaac0807f84da73d0701c82cf7542b5182fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669780"
---
# <span data-ttu-id="8147f-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8147f-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="8147f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8147f-102">SYNOPSIS</span></span>
<span data-ttu-id="8147f-103">Egy privát DNS-rekord eltávolítása egy helyi rekordazonosító-objektumból.</span><span class="sxs-lookup"><span data-stu-id="8147f-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="8147f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8147f-104">SYNTAX</span></span>

### <span data-ttu-id="8147f-105">A (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8147f-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8147f-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="8147f-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8147f-107">MX</span><span class="sxs-lookup"><span data-stu-id="8147f-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8147f-108">PTR</span><span class="sxs-lookup"><span data-stu-id="8147f-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8147f-109">TXT</span><span class="sxs-lookup"><span data-stu-id="8147f-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8147f-110">SRV</span><span class="sxs-lookup"><span data-stu-id="8147f-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8147f-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="8147f-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8147f-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="8147f-112">DESCRIPTION</span></span>
<span data-ttu-id="8147f-113">A Remove-AzPrivateDnsRecordConfig parancsmag eltávolítja a saját tartománynévrendszer (DNS) rekordját egy rekordból.</span><span class="sxs-lookup"><span data-stu-id="8147f-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="8147f-114">A RecordSet objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a magánjellegű DNS-válaszokat, amíg a Set-AzPrivateDnsRecordSet parancsmagot nem futtatja, hogy továbbra is megmaradjon a módosítás a Microsoft Azure Private DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8147f-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="8147f-115">Ha el szeretne távolítani egy rekordot, a rekordtípus minden mezőjének pontosan egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="8147f-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="8147f-116">A SOA rekordok nem vehetők fel és nem távolíthatók el.</span><span class="sxs-lookup"><span data-stu-id="8147f-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="8147f-117">A rendszer automatikusan létrehozza a SOA-rekordokat, amikor egy privát DNS-zóna jön létre, és a rendszer automatikusan törli a magánjellegű DNS-zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="8147f-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="8147f-118">A rekordhalmaz-objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="8147f-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="8147f-119">Példák</span><span class="sxs-lookup"><span data-stu-id="8147f-119">EXAMPLES</span></span>

### <span data-ttu-id="8147f-120">1. példa: rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-120">Example 1: Remove an A record from a record set</span></span>
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

<span data-ttu-id="8147f-121">Ez a példa egy meglévő rekordtípus rekordjainak eltávolítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8147f-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="8147f-122">Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="8147f-123">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzPrivateDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="8147f-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8147f-124">2. példa: az AAAA rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-124">Example 2: Remove an AAAA record from a record set</span></span>
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

<span data-ttu-id="8147f-125">Ez a példa eltávolítja az AAAA-rekordot egy meglévő rekorddal.</span><span class="sxs-lookup"><span data-stu-id="8147f-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="8147f-126">Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="8147f-127">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzPrivateDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="8147f-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8147f-128">3. példa: CNAME rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-128">Example 3: Remove a CNAME record from a record set</span></span>
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

<span data-ttu-id="8147f-129">Ez a példa eltávolítja a CNAME rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="8147f-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="8147f-130">Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="8147f-131">4. példa: MX rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-131">Example 4: Remove a MX record from a record set</span></span>
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

<span data-ttu-id="8147f-132">Ebben a példában egy MX rekord törlődik egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="8147f-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="8147f-133">A "@" rekord a zóna APEX nevű rekordjait jelzi.</span><span class="sxs-lookup"><span data-stu-id="8147f-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="8147f-134">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8147f-135">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzPrivateDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="8147f-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8147f-136">Példa 5: a PTR rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-136">Example 5: Remove a PTR record from a record set</span></span>
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

<span data-ttu-id="8147f-137">Ez a példa eltávolítja a PTR rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="8147f-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="8147f-138">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8147f-139">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzPrivateDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="8147f-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8147f-140">Példa 6: SRV rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-140">Example 6: Remove a SRV record from a record set</span></span>
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

<span data-ttu-id="8147f-141">Ez a példa eltávolítja az SRV rekordot egy meglévő rekorddal.</span><span class="sxs-lookup"><span data-stu-id="8147f-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="8147f-142">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8147f-143">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzPrivateDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="8147f-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8147f-144">7. példa: TXT rekord eltávolítása a rekordból</span><span class="sxs-lookup"><span data-stu-id="8147f-144">Example 7: Remove a TXT record from a record set</span></span>
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

<span data-ttu-id="8147f-145">Ez a példa eltávolítja a TXT rekordot egy meglévő rekordból.</span><span class="sxs-lookup"><span data-stu-id="8147f-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="8147f-146">Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.</span><span class="sxs-lookup"><span data-stu-id="8147f-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8147f-147">Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzPrivateDnsRecordSet című témakört.</span><span class="sxs-lookup"><span data-stu-id="8147f-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="8147f-148">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8147f-148">PARAMETERS</span></span>

### <span data-ttu-id="8147f-149">-CNAME</span><span class="sxs-lookup"><span data-stu-id="8147f-149">-Cname</span></span>
<span data-ttu-id="8147f-150">Az eltávolítandó CNAME rekord kanonikus neve.</span><span class="sxs-lookup"><span data-stu-id="8147f-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="8147f-151">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="8147f-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8147f-152">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="8147f-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8147f-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8147f-153">-DefaultProfile</span></span>
<span data-ttu-id="8147f-154">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8147f-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8147f-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8147f-155">-Exchange</span></span>
<span data-ttu-id="8147f-156">Az eltávolítandó MX rekord levelezési Exchange-állomása.</span><span class="sxs-lookup"><span data-stu-id="8147f-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="8147f-157">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="8147f-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8147f-158">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="8147f-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8147f-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="8147f-159">-Ipv4Address</span></span>
<span data-ttu-id="8147f-160">Az eltávolítandó rekord IPv4-címe.</span><span class="sxs-lookup"><span data-stu-id="8147f-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="8147f-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="8147f-161">-Ipv6Address</span></span>
<span data-ttu-id="8147f-162">Az eltávolítandó AAAA rekord IPv6-címe.</span><span class="sxs-lookup"><span data-stu-id="8147f-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="8147f-163">-Port</span><span class="sxs-lookup"><span data-stu-id="8147f-163">-Port</span></span>
<span data-ttu-id="8147f-164">Az eltávolítandó SRV rekord portszáma.</span><span class="sxs-lookup"><span data-stu-id="8147f-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="8147f-165">-Preferencia</span><span class="sxs-lookup"><span data-stu-id="8147f-165">-Preference</span></span>
<span data-ttu-id="8147f-166">Az eltávolítandó MX rekord preferencia értéke.</span><span class="sxs-lookup"><span data-stu-id="8147f-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="8147f-167">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="8147f-167">-Priority</span></span>
<span data-ttu-id="8147f-168">Az eltávolítandó SRV rekord prioritási értéke.</span><span class="sxs-lookup"><span data-stu-id="8147f-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="8147f-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="8147f-169">-Ptrdname</span></span>
<span data-ttu-id="8147f-170">Az eltávolítandó PTR-rekord célállomása.</span><span class="sxs-lookup"><span data-stu-id="8147f-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="8147f-171">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="8147f-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8147f-172">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="8147f-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8147f-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="8147f-173">-RecordSet</span></span>
<span data-ttu-id="8147f-174">Annak a rekordnak a készlete, amelyből el szeretné távolítani a rekordot.</span><span class="sxs-lookup"><span data-stu-id="8147f-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="8147f-175">-Target (cél)</span><span class="sxs-lookup"><span data-stu-id="8147f-175">-Target</span></span>
<span data-ttu-id="8147f-176">Az eltávolítandó SRV rekord célállomása.</span><span class="sxs-lookup"><span data-stu-id="8147f-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="8147f-177">Nem lehet a zóna nevéhez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="8147f-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8147f-178">Nem rendelkezhet lezáró ponttal</span><span class="sxs-lookup"><span data-stu-id="8147f-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8147f-179">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="8147f-179">-Value</span></span>
<span data-ttu-id="8147f-180">Az eltávolítandó TXT rekord szöveges értéke.</span><span class="sxs-lookup"><span data-stu-id="8147f-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="8147f-181">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="8147f-181">-Weight</span></span>
<span data-ttu-id="8147f-182">Az eltávolítandó SRV rekord súlya.</span><span class="sxs-lookup"><span data-stu-id="8147f-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="8147f-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8147f-183">CommonParameters</span></span>
<span data-ttu-id="8147f-184">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8147f-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8147f-185">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8147f-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8147f-186">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8147f-186">INPUTS</span></span>

### <span data-ttu-id="8147f-187">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8147f-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8147f-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8147f-188">OUTPUTS</span></span>

### <span data-ttu-id="8147f-189">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8147f-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8147f-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8147f-190">NOTES</span></span>

## <span data-ttu-id="8147f-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8147f-191">RELATED LINKS</span></span>
