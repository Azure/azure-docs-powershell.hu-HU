---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147979"
---
# <span data-ttu-id="65565-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="65565-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="65565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65565-102">SYNOPSIS</span></span>
<span data-ttu-id="65565-103">Rekordkészlet törlése.</span><span class="sxs-lookup"><span data-stu-id="65565-103">Deletes a record set.</span></span>

## <span data-ttu-id="65565-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65565-104">SYNTAX</span></span>

### <span data-ttu-id="65565-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="65565-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65565-106">Vegyes</span><span class="sxs-lookup"><span data-stu-id="65565-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65565-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="65565-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65565-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65565-108">DESCRIPTION</span></span>
<span data-ttu-id="65565-109">A **Remove-AzDnsRecordSet** parancsmag törli a megadott rekordkészletet a megadott zónából.</span><span class="sxs-lookup"><span data-stu-id="65565-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="65565-110">A zóna csúcsán automatikusan létrehozott SOA- vagy névkiszolgáló-rekordok nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="65565-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="65565-111">A **RecordSet-objektumot** ehhez a parancsmaghoz a folyamat műveleti jelét használva vagy paraméterként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="65565-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="65565-112">Ha a **RecordSet-objektum** használata nélkül, név szerint és típus szerint meg tud adni egy rekordot, a zónát **DnsZone-objektumként** kell átadnia ennek a parancsmagnak a folyamat műveleti jelének vagy paraméterének használatával, vagy megadhatja a *ZoneName* és *az ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="65565-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="65565-113">A Confirm paraméter és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="65565-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="65565-114">Amikor rekordkészletet ad meg **Egy RecordSet-objektummal,** a rekordkészlet nem törlődik, ha módosult az Azure DNS-ben a helyi **RecordSet objektum lekérése** óta.</span><span class="sxs-lookup"><span data-stu-id="65565-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="65565-115">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="65565-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="65565-116">Ezt letilthatja a  Felülírás paraméter használatával, amely törli a rekordkészletet az egyidejű módosításoktól függetlenül.</span><span class="sxs-lookup"><span data-stu-id="65565-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="65565-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65565-117">EXAMPLES</span></span>

### <span data-ttu-id="65565-118">1. példa: Rekordkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="65565-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="65565-119">Az első parancs megkapja a megadott rekordkészletet, majd a $RecordSet tárolja. A második parancs eltávolítja a rekordkészletet a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="65565-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="65565-120">2. példa: Rekordkészlet eltávolítása és az összes megerősítés mellőzése</span><span class="sxs-lookup"><span data-stu-id="65565-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="65565-121">Az első parancs megkapja a megadott rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="65565-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="65565-122">A második parancs törli a rekordkészletet, még akkor is, ha időközben megváltozott.</span><span class="sxs-lookup"><span data-stu-id="65565-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="65565-123">A megerősítést kérő kérések nincsenek letiltva.</span><span class="sxs-lookup"><span data-stu-id="65565-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="65565-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65565-124">PARAMETERS</span></span>

### <span data-ttu-id="65565-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65565-125">-DefaultProfile</span></span>
<span data-ttu-id="65565-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65565-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65565-127">-Name</span><span class="sxs-lookup"><span data-stu-id="65565-127">-Name</span></span>
<span data-ttu-id="65565-128">Az eltávolítható **RecordSet neve.**</span><span class="sxs-lookup"><span data-stu-id="65565-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="65565-129">A név szerint beállított rekord megadásakor a DNS-zónát vagy a Zone *paraméter,* illetve *a ZoneName* és *az ResourceGroupName* paraméter használatával kell megadni.</span><span class="sxs-lookup"><span data-stu-id="65565-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="65565-130">Másik lehetőségként a rekordkészletet a **RecordSet** objektummal is meg lehet adni, és *a RecordSet paraméterrel kell* átadottnak lennie.</span><span class="sxs-lookup"><span data-stu-id="65565-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65565-131">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="65565-131">-Overwrite</span></span>
<span data-ttu-id="65565-132">Amikor rekordkészletet ad meg **Egy RecordSet-objektummal,** a rekordkészlet nem törlődik, ha módosult az Azure DNS-ben a helyi **RecordSet objektum lekérése** óta.</span><span class="sxs-lookup"><span data-stu-id="65565-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="65565-133">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="65565-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="65565-134">Ez elrejthető a  Felülírás paraméter használatával, amely törli a rekordkészletet, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="65565-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65565-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65565-135">-PassThru</span></span>
<span data-ttu-id="65565-136">passthru</span><span class="sxs-lookup"><span data-stu-id="65565-136">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65565-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="65565-137">-RecordSet</span></span>
<span data-ttu-id="65565-138">Az **eltávolítható RecordSet-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="65565-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="65565-139">Másik lehetőségként a rekordkészletet  meg lehet adni a Name és *a Zone* paraméter, illetve a *Name,* *a ZoneName* és az *ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="65565-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65565-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="65565-140">-RecordType</span></span>
<span data-ttu-id="65565-141">A DNS-rekord típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="65565-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="65565-142">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="65565-142">Valid values are:</span></span>
- <span data-ttu-id="65565-143">A</span><span class="sxs-lookup"><span data-stu-id="65565-143">A</span></span>
- <span data-ttu-id="65565-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="65565-144">AAAA</span></span>
- <span data-ttu-id="65565-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="65565-145">CNAME</span></span>
- <span data-ttu-id="65565-146">MX</span><span class="sxs-lookup"><span data-stu-id="65565-146">MX</span></span>
- <span data-ttu-id="65565-147">NS</span><span class="sxs-lookup"><span data-stu-id="65565-147">NS</span></span>
- <span data-ttu-id="65565-148">PTR</span><span class="sxs-lookup"><span data-stu-id="65565-148">PTR</span></span>
- <span data-ttu-id="65565-149">SRV</span><span class="sxs-lookup"><span data-stu-id="65565-149">SRV</span></span>
- <span data-ttu-id="65565-150">A TXT SOA rekordok a zóna törlésekor automatikusan törlődnek.</span><span class="sxs-lookup"><span data-stu-id="65565-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="65565-151">A SOA rekordok manuálisan nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="65565-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65565-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65565-152">-ResourceGroupName</span></span>
<span data-ttu-id="65565-153">Azt az erőforráscsoportot adja meg, amely a törlendni **kívánt RecordSet rekordkészletet** tartalmazó DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="65565-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="65565-154">Ez a paraméter csak akkor érvényes, ha a rekordkészlet és a DNS-zóna a *Name* and *ZoneName* paraméterrel van megadva.</span><span class="sxs-lookup"><span data-stu-id="65565-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="65565-155">Másik lehetőségként megadhatja a rekordkészletet a *RecordSet* vagy a *Name* and *Zone paraméterrel.*</span><span class="sxs-lookup"><span data-stu-id="65565-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="65565-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="65565-156">-Zone</span></span>
<span data-ttu-id="65565-157">Azt a DNS-zónát adja meg, amely a **törlendni kívánt RecordSet** rekordkészletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="65565-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="65565-158">Ez a paraméter csak akkor alkalmazható, ha a Rekordkészletet a *Name paraméterrel adja* meg.</span><span class="sxs-lookup"><span data-stu-id="65565-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="65565-159">Másik lehetőségként megadhatja a rekordkészletet a *RecordSet* vagy a *Name,* *ZoneName* és *ResourceGroupName* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="65565-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65565-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="65565-160">-ZoneName</span></span>
<span data-ttu-id="65565-161">Annak a zónának a nevét adja meg, amely a **törlendni kívánt Rekordkészletet** tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="65565-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="65565-162">A Name és  *az ResourceGroupName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="65565-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="65565-163">Másik lehetőségként a rekordkészletet a *RecordSet* paraméterrel, illetve a *Name* and *Zone paraméterrel is meg lehet* adni.</span><span class="sxs-lookup"><span data-stu-id="65565-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="65565-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65565-164">-Confirm</span></span>
<span data-ttu-id="65565-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65565-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65565-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65565-166">-WhatIf</span></span>
<span data-ttu-id="65565-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65565-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65565-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65565-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65565-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65565-169">CommonParameters</span></span>
<span data-ttu-id="65565-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65565-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65565-171">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65565-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65565-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65565-172">INPUTS</span></span>

### <span data-ttu-id="65565-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="65565-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="65565-174">System.String</span><span class="sxs-lookup"><span data-stu-id="65565-174">System.String</span></span>

### <span data-ttu-id="65565-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="65565-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="65565-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="65565-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="65565-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65565-177">OUTPUTS</span></span>

### <span data-ttu-id="65565-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65565-178">System.Boolean</span></span>

## <span data-ttu-id="65565-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65565-179">NOTES</span></span>
<span data-ttu-id="65565-180">A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="65565-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="65565-181">A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.</span><span class="sxs-lookup"><span data-stu-id="65565-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="65565-182">Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="65565-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="65565-183">Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65565-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="65565-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65565-184">RELATED LINKS</span></span>

[<span data-ttu-id="65565-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="65565-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="65565-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="65565-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="65565-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="65565-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
