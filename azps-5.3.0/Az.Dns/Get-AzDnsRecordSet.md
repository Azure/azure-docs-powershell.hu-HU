---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467745"
---
# <span data-ttu-id="e533f-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e533f-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="e533f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e533f-102">SYNOPSIS</span></span>
<span data-ttu-id="e533f-103">DNS-rekordkészletet kap.</span><span class="sxs-lookup"><span data-stu-id="e533f-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="e533f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e533f-104">SYNTAX</span></span>

### <span data-ttu-id="e533f-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="e533f-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e533f-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="e533f-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e533f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e533f-107">DESCRIPTION</span></span>
<span data-ttu-id="e533f-108">A **Get-AzDnsRecordSet** parancsmag a megadott névvel és típussal megadott DNS-rekordot kapja a megadott zónában.</span><span class="sxs-lookup"><span data-stu-id="e533f-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="e533f-109">Ha nem adja meg a *Name* vagy *a RecordType* paramétert, ez a parancsmag a zónában megadott típusú összes rekordkészletet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="e533f-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="e533f-110">Ha a *RecordType* paramétert adja meg, de a *Name* paramétert nem, ez a parancsmag a megadott rekordtípus összes rekordkészletét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="e533f-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="e533f-111">A folyamat operátorával **dnsZone-objektumot** is átadhat ennek a parancsmagnak, vagy  átadhatja a **DnsZone-objektumokat** zóna paraméterként, vagy másik lehetőségként név szerint is megadhatja a zónát és az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="e533f-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="e533f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e533f-112">EXAMPLES</span></span>

### <span data-ttu-id="e533f-113">1. példa: Rekordkészletek lekérte a megadott nevet és típust</span><span class="sxs-lookup"><span data-stu-id="e533f-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="e533f-114">Ez a parancs a megadott erőforráscsoportban és zónában a www nevű A rekordkészletet kapja meg, majd a rekordot a $RecordSet tárolja.</span><span class="sxs-lookup"><span data-stu-id="e533f-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="e533f-115">Mivel a *Name és* *a RecordType* paraméter meg van adva, csak egy **RecordSet-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="e533f-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="e533f-116">2. példa: Adott típusú rekordkészletek lekérte</span><span class="sxs-lookup"><span data-stu-id="e533f-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="e533f-117">Ez a parancs a MyResourceGroup nevű erőforráscsoport myzone.com nevű zónában az A rekordkészletek összes rekordkészletét beállítja, majd az $RecordSets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="e533f-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="e533f-118">3. példa: Az összes rekordkészlet lekérte egy zónába</span><span class="sxs-lookup"><span data-stu-id="e533f-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="e533f-119">Ez a parancs a MyResourceGroup nevű erőforráscsoport zónájában található myzone.com tömböt, majd a $RecordSets tárolja.</span><span class="sxs-lookup"><span data-stu-id="e533f-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="e533f-120">4. példa: Az összes rekordkészlet begyűjtése egy zónába DnsZone-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="e533f-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="e533f-121">Ez a példa egyenértékű a fenti 3. példával.</span><span class="sxs-lookup"><span data-stu-id="e533f-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="e533f-122">A zóna ezúttal zónaobjektum használatával van megadva.</span><span class="sxs-lookup"><span data-stu-id="e533f-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="e533f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e533f-123">PARAMETERS</span></span>

### <span data-ttu-id="e533f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e533f-124">-DefaultProfile</span></span>
<span data-ttu-id="e533f-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e533f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e533f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e533f-126">-Name</span></span>
<span data-ttu-id="e533f-127">A lekért **Rekordkészlet** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e533f-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="e533f-128">Ha nem adja meg a *Name* paramétert, a visszaadott érték a megadott típusú összes rekordkészletet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="e533f-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e533f-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="e533f-129">-RecordType</span></span>
<span data-ttu-id="e533f-130">A parancsmag által lekért DNS-rekord típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e533f-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="e533f-131">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="e533f-131">Valid values are:</span></span> 
- <span data-ttu-id="e533f-132">A</span><span class="sxs-lookup"><span data-stu-id="e533f-132">A</span></span>
- <span data-ttu-id="e533f-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="e533f-133">AAAA</span></span>
- <span data-ttu-id="e533f-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="e533f-134">CNAME</span></span>
- <span data-ttu-id="e533f-135">MX</span><span class="sxs-lookup"><span data-stu-id="e533f-135">MX</span></span>
- <span data-ttu-id="e533f-136">NS</span><span class="sxs-lookup"><span data-stu-id="e533f-136">NS</span></span>
- <span data-ttu-id="e533f-137">PTR</span><span class="sxs-lookup"><span data-stu-id="e533f-137">PTR</span></span>
- <span data-ttu-id="e533f-138">SOA</span><span class="sxs-lookup"><span data-stu-id="e533f-138">SOA</span></span>
- <span data-ttu-id="e533f-139">SRV</span><span class="sxs-lookup"><span data-stu-id="e533f-139">SRV</span></span>
- <span data-ttu-id="e533f-140">TXT Ha nem adja meg a *RecordType* paramétert, a Name paramétert is ki kell *mellőznie.*</span><span class="sxs-lookup"><span data-stu-id="e533f-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="e533f-141">Ez a parancsmag a zóna összes rekordkészletét visszaadja (az összes névből és típusból).</span><span class="sxs-lookup"><span data-stu-id="e533f-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e533f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e533f-142">-ResourceGroupName</span></span>
<span data-ttu-id="e533f-143">A DNS-zónát tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e533f-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="e533f-144">A zónanevet a *ZoneName* paraméter használatával is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="e533f-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="e533f-145">Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy **DnsZone-objektumot** *ad* át.</span><span class="sxs-lookup"><span data-stu-id="e533f-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e533f-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="e533f-146">-Zone</span></span>
<span data-ttu-id="e533f-147">Azt a DNS-zónát adja meg, amely a parancsmag által behozott rekordkészletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e533f-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="e533f-148">Másik lehetőségként a *ZoneName* és az *ResourceGroupName* paramétert használva is megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="e533f-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e533f-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="e533f-149">-ZoneName</span></span>
<span data-ttu-id="e533f-150">Annak a DNS-zónának a neve, amely a behozni kívánt rekordot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e533f-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="e533f-151">A zónát tartalmazó erőforráscsoportot is meg kell adni az *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="e533f-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="e533f-152">Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy DNS Zone-objektumot *ad* át.</span><span class="sxs-lookup"><span data-stu-id="e533f-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e533f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e533f-153">CommonParameters</span></span>
<span data-ttu-id="e533f-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e533f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e533f-155">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e533f-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e533f-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e533f-156">INPUTS</span></span>

### <span data-ttu-id="e533f-157">System.String</span><span class="sxs-lookup"><span data-stu-id="e533f-157">System.String</span></span>

### <span data-ttu-id="e533f-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="e533f-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="e533f-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e533f-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e533f-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e533f-160">OUTPUTS</span></span>

### <span data-ttu-id="e533f-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e533f-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="e533f-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e533f-162">NOTES</span></span>

## <span data-ttu-id="e533f-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e533f-163">RELATED LINKS</span></span>

[<span data-ttu-id="e533f-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e533f-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="e533f-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e533f-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="e533f-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e533f-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


