---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188057"
---
# <span data-ttu-id="77c1f-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77c1f-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="77c1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="77c1f-103">A rekordot egy privát DNS-zónából kapja meg.</span><span class="sxs-lookup"><span data-stu-id="77c1f-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="77c1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77c1f-104">SYNTAX</span></span>

### <span data-ttu-id="77c1f-105">FieldsWithNoName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77c1f-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c1f-106">Mezők</span><span class="sxs-lookup"><span data-stu-id="77c1f-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c1f-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="77c1f-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c1f-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="77c1f-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c1f-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77c1f-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c1f-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="77c1f-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77c1f-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="77c1f-111">DESCRIPTION</span></span>
<span data-ttu-id="77c1f-112">A Get-AzPrivateDnsRecordSet parancsmag a saját tartománynévrendszer (DNS) rekordot kapja meg a megadott névvel és típussal, a megadott privát zónában.</span><span class="sxs-lookup"><span data-stu-id="77c1f-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="77c1f-113">Ha nem adja meg a név-vagy RecordType paramétereket, ez a parancsmag a megadott típusú összes rekordot visszaadja a magánjellegű zónában.</span><span class="sxs-lookup"><span data-stu-id="77c1f-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="77c1f-114">Ha a RecordType paramétert adja meg, a name paramétert azonban nem, ez a parancsmag a megadott rekordtípus összes rekordját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="77c1f-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="77c1f-115">A pipeline operátor segítségével átadhatja a PSPrivateDnsZone-objektumokat erre a parancsmagra, vagy átadhatja a PSPrivateDnsZone-objektumot a zóna paraméterének, vagy másik lehetőségként a zóna és az erőforráscsoport név szerint is megadható.</span><span class="sxs-lookup"><span data-stu-id="77c1f-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="77c1f-116">A magánjellegű zónát a magánjellegű zóna erőforrás-azonosítójának használatával is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="77c1f-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="77c1f-117">Példák</span><span class="sxs-lookup"><span data-stu-id="77c1f-117">EXAMPLES</span></span>

### <span data-ttu-id="77c1f-118">1. példa: a bejegyzéstípusok beolvasása megadott névvel és típussal</span><span class="sxs-lookup"><span data-stu-id="77c1f-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="77c1f-119">Ez a parancs a Record Type (rekord) típusú rekordot kapja meg a megadott erőforráscsoport és privát zóna nevű weblapon, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77c1f-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="77c1f-120">Mivel a név-és RecordType paraméterek meg vannak adva, csak egy rekordhalmaz-objektum van visszaadva.</span><span class="sxs-lookup"><span data-stu-id="77c1f-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="77c1f-121">2. példa: megadott típusú bejegyzéstípusok beszerzése</span><span class="sxs-lookup"><span data-stu-id="77c1f-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="77c1f-122">Ez a parancs a MyResourceGroup nevű myzone.com nevű privát zónában az A rekordtípus összes rekord halmazának tömbjét kapja, majd a $RecordSets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="77c1f-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="77c1f-123">3. példa: egy privát zóna minden rekordjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="77c1f-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="77c1f-124">Ez a parancs a MyResourceGroup nevű erőforráscsoport myzone.com nevű privát zónájában minden rekord halmazát beolvassa, majd a $RecordSets változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77c1f-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="77c1f-125">Példa 4: az összes rekord készletének beolvasása egy privát zónában PSPrivateDnsZone objektum használatával</span><span class="sxs-lookup"><span data-stu-id="77c1f-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="77c1f-126">Ez a példa a fenti 3 példával egyenértékű.</span><span class="sxs-lookup"><span data-stu-id="77c1f-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="77c1f-127">Ezúttal a privát zóna egy privát zóna objektummal van megadva.</span><span class="sxs-lookup"><span data-stu-id="77c1f-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="77c1f-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77c1f-128">PARAMETERS</span></span>

### <span data-ttu-id="77c1f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c1f-129">-DefaultProfile</span></span>
<span data-ttu-id="77c1f-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77c1f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77c1f-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77c1f-131">-Name</span></span>
<span data-ttu-id="77c1f-132">Az ebben a rekordban szereplő rekordok neve (a zóna nevéhez és a végpontok nélküli ponthoz viszonyítva).</span><span class="sxs-lookup"><span data-stu-id="77c1f-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c1f-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="77c1f-133">-ParentResourceId</span></span>
<span data-ttu-id="77c1f-134">Privát DNS-zóna ResourceID.</span><span class="sxs-lookup"><span data-stu-id="77c1f-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77c1f-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="77c1f-135">-RecordType</span></span>
<span data-ttu-id="77c1f-136">A rekordhoz tartozó DNS-rekordok típusa.</span><span class="sxs-lookup"><span data-stu-id="77c1f-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c1f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c1f-137">-ResourceGroupName</span></span>
<span data-ttu-id="77c1f-138">Az az erőforráscsoport, amelyhez a zóna tartozik.</span><span class="sxs-lookup"><span data-stu-id="77c1f-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c1f-139">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="77c1f-139">-Zone</span></span>
<span data-ttu-id="77c1f-140">Az a DnsZone objektum, amely a rekord létrehozásához használt zónát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="77c1f-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77c1f-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="77c1f-141">-ZoneName</span></span>
<span data-ttu-id="77c1f-142">Az a zóna, amelyben létre szeretné hozni a rekordot (lezáró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="77c1f-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c1f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c1f-143">CommonParameters</span></span>
<span data-ttu-id="77c1f-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77c1f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c1f-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c1f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c1f-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77c1f-146">INPUTS</span></span>

### <span data-ttu-id="77c1f-147">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="77c1f-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="77c1f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="77c1f-148">System.String</span></span>

## <span data-ttu-id="77c1f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77c1f-149">OUTPUTS</span></span>

### <span data-ttu-id="77c1f-150">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77c1f-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="77c1f-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77c1f-151">NOTES</span></span>

## <span data-ttu-id="77c1f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77c1f-152">RELATED LINKS</span></span>
