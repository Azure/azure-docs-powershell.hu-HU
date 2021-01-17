---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468689"
---
# <span data-ttu-id="815f1-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="815f1-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="815f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="815f1-102">SYNOPSIS</span></span>
<span data-ttu-id="815f1-103">Egy privát DNS-zónából kap egy rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="815f1-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="815f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="815f1-104">SYNTAX</span></span>

### <span data-ttu-id="815f1-105">FieldsWithNoName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="815f1-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815f1-106">Mezők</span><span class="sxs-lookup"><span data-stu-id="815f1-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815f1-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="815f1-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815f1-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="815f1-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815f1-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="815f1-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815f1-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="815f1-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="815f1-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="815f1-111">DESCRIPTION</span></span>
<span data-ttu-id="815f1-112">A Get-AzPrivateDnsRecordSet parancsmag a megadott névvel és típussal megadott DNS-rekordot kapja meg a megadott privát zónában.</span><span class="sxs-lookup"><span data-stu-id="815f1-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="815f1-113">Ha nem adja meg a Name vagy a RecordType paramétert, ez a parancsmag a megadott típusú összes rekordkészletet visszaadja a privát zónában.</span><span class="sxs-lookup"><span data-stu-id="815f1-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="815f1-114">Ha a RecordType paramétert adja meg, de a Name paramétert nem, ez a parancsmag a megadott rekordtípus összes rekordkészletét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="815f1-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="815f1-115">A folyamat műveleti jelét használva átadhatja a PSPrivateDnsZone-objektumot ennek a parancsmagnak, vagy átadhatja a PSPrivateDnsZone objektumot zóna paraméterként, vagy másik lehetőségként név szerint is megadhatja a zónát és az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="815f1-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="815f1-116">A privát zónát a privát zóna erőforrás-azonosítójával is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="815f1-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="815f1-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="815f1-117">EXAMPLES</span></span>

### <span data-ttu-id="815f1-118">1. példa: Meghatározott nevű és típusú rekordkészletek lekérte</span><span class="sxs-lookup"><span data-stu-id="815f1-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="815f1-119">Ez a parancs a megadott erőforráscsoportban és privát zónában beveszi az A rekordtípus (A) nevű rekordkészletet, majd azt a $RecordSet tárolja.</span><span class="sxs-lookup"><span data-stu-id="815f1-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="815f1-120">Mivel a Name és a RecordType paraméter meg van adva, csak egy RecordSet-objektumot ad vissza a visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="815f1-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="815f1-121">2. példa: Adott típusú rekordkészletek lekérte</span><span class="sxs-lookup"><span data-stu-id="815f1-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="815f1-122">Ez a parancs a MyResourceGroup nevű erőforráscsoport myzone.com nevű privát zónában beállítja az A rekordtípusú rekordkészletek tömbét, majd a $RecordSets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="815f1-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="815f1-123">3. példa: Az összes rekordkészlet behozása egy privát zónába</span><span class="sxs-lookup"><span data-stu-id="815f1-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="815f1-124">Ez a parancs a MyResourceGroup nevű erőforráscsoport myzone.com nevű privát zóna összes rekordkészletét beállítja, majd a $RecordSets tárolja.</span><span class="sxs-lookup"><span data-stu-id="815f1-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="815f1-125">4. példa: Az összes rekordkészlet beása egy privát zónába PSPrivateDnsZone-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="815f1-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="815f1-126">Ez a példa egyenértékű a fenti 3. példával.</span><span class="sxs-lookup"><span data-stu-id="815f1-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="815f1-127">A privát zóna ezúttal egy privát zónaobjektum használatával van megadva.</span><span class="sxs-lookup"><span data-stu-id="815f1-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="815f1-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="815f1-128">PARAMETERS</span></span>

### <span data-ttu-id="815f1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815f1-129">-DefaultProfile</span></span>
<span data-ttu-id="815f1-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="815f1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="815f1-131">-Name</span><span class="sxs-lookup"><span data-stu-id="815f1-131">-Name</span></span>
<span data-ttu-id="815f1-132">A rekordkészlet rekordjainak neve (a zóna nevéhez képest és befejezési pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="815f1-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="815f1-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="815f1-133">-ParentResourceId</span></span>
<span data-ttu-id="815f1-134">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="815f1-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="815f1-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="815f1-135">-RecordType</span></span>
<span data-ttu-id="815f1-136">A DNS-rekordok típusa ebben a rekordkészletben.</span><span class="sxs-lookup"><span data-stu-id="815f1-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="815f1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815f1-137">-ResourceGroupName</span></span>
<span data-ttu-id="815f1-138">Az az erőforráscsoport, amelyhez a zóna tartozik.</span><span class="sxs-lookup"><span data-stu-id="815f1-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="815f1-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="815f1-139">-Zone</span></span>
<span data-ttu-id="815f1-140">A rekordkészlet létrehozásához használt zóna DNSZone-objektuma.</span><span class="sxs-lookup"><span data-stu-id="815f1-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="815f1-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="815f1-141">-ZoneName</span></span>
<span data-ttu-id="815f1-142">Az a zóna, amelyben létre kell hoznia a rekordkészletet (befejezési pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="815f1-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="815f1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815f1-143">CommonParameters</span></span>
<span data-ttu-id="815f1-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815f1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815f1-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815f1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815f1-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="815f1-146">INPUTS</span></span>

### <span data-ttu-id="815f1-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="815f1-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="815f1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="815f1-148">System.String</span></span>

## <span data-ttu-id="815f1-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="815f1-149">OUTPUTS</span></span>

### <span data-ttu-id="815f1-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="815f1-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="815f1-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="815f1-151">NOTES</span></span>

## <span data-ttu-id="815f1-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="815f1-152">RELATED LINKS</span></span>
