---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: fce5cbe993861d2a0d97bffd4bf4c7dbe19cc535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672738"
---
# <span data-ttu-id="8e3dd-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e3dd-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="8e3dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3dd-103">Rekord törlése</span><span class="sxs-lookup"><span data-stu-id="8e3dd-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e3dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e3dd-104">SYNTAX</span></span>

### <span data-ttu-id="8e3dd-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="8e3dd-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e3dd-106">Vegyes</span><span class="sxs-lookup"><span data-stu-id="8e3dd-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e3dd-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="8e3dd-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e3dd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e3dd-108">DESCRIPTION</span></span>
<span data-ttu-id="8e3dd-109">A **Remove-AzureRmDnsRecordSet** parancsmag törli a megadott rekordot a megadott zónából.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="8e3dd-110">Nem törölhet olyan SOA-vagy névkiszolgálói (NS) rekordokat, amelyek automatikusan létrejönnek a zóna APEX-ben.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="8e3dd-111">A **rekordhalmaz** -objektumot átadhatja erre a parancsmagra a pipeline operátorral vagy paraméterként.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="8e3dd-112">Ha a rekordokat név és típus szerint szeretné megadni a **rekordhalmaz** -objektum használata nélkül, a zónát **dnsZone** objektumként kell átadnia ehhez a parancsmaghoz a pipeline operátorral vagy paraméterként, illetve a *ZoneName* és a *ResourceGroupName* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="8e3dd-113">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="8e3dd-114">Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="8e3dd-115">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="8e3dd-116">Ezt úgy teheti meg, hogy a *felülírási* paramétert használja, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="8e3dd-117">Példák</span><span class="sxs-lookup"><span data-stu-id="8e3dd-117">EXAMPLES</span></span>

### <span data-ttu-id="8e3dd-118">1. példa: a rekordtípus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8e3dd-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="8e3dd-119">Az első parancs a megadott rekordot kapja meg, majd a $RecordSet változóban tárolja. A második parancs eltávolítja a rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="8e3dd-120">2. példa: a rekordtípus eltávolítása és az összes megerősítés letiltása</span><span class="sxs-lookup"><span data-stu-id="8e3dd-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="8e3dd-121">Az első parancs a megadott rekordot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="8e3dd-122">A második parancs törli a rekordot, még akkor is, ha időközben megváltozott.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="8e3dd-123">A megerősítési utasításokat a rendszer letiltja.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="8e3dd-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e3dd-124">PARAMETERS</span></span>

### <span data-ttu-id="8e3dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3dd-125">-DefaultProfile</span></span>
<span data-ttu-id="8e3dd-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e3dd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3dd-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8e3dd-127">-Force</span></span>
<span data-ttu-id="8e3dd-128">Ez a paraméter érvénytelenítve van ennél a parancsmagnál.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-128">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="8e3dd-129">A program eltávolítja a jövőbeli kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-129">It will be removed in a future release.</span></span>

<span data-ttu-id="8e3dd-130">Ha meg szeretné állapítani, hogy ez a parancsmag kéri-e a megerősítést, használja a *Confirm* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-130">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e3dd-131">-Name</span></span>
<span data-ttu-id="8e3dd-132">Az eltávolítandó **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-132">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="8e3dd-133">Ha a rekordot név szerint adja meg, a DNS-zónát a *Zone* paraméterrel vagy a *ZoneName* és a *ResourceGroupName* paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-133">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="8e3dd-134">Másik lehetőségként a rekordhalmazt egy **Recordset** objektum segítségével is megadhatja, amelyet a *rekordhalmaz* paraméterrel adhat meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-134">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-135">-Átír</span><span class="sxs-lookup"><span data-stu-id="8e3dd-135">-Overwrite</span></span>
<span data-ttu-id="8e3dd-136">Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-136">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="8e3dd-137">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-137">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="8e3dd-138">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-138">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e3dd-139">-PassThru</span></span>
<span data-ttu-id="8e3dd-140">passthru</span><span class="sxs-lookup"><span data-stu-id="8e3dd-140">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-141">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="8e3dd-141">-RecordSet</span></span>
<span data-ttu-id="8e3dd-142">Az eltávolítandó **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-142">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="8e3dd-143">Azt is megteheti, hogy a rekord a *név* és a *zóna* paraméter segítségével, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméter segítségével is megadható.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-143">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-144">-RecordType</span><span class="sxs-lookup"><span data-stu-id="8e3dd-144">-RecordType</span></span>
<span data-ttu-id="8e3dd-145">A DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-145">Specifies the type of DNS record.</span></span>

<span data-ttu-id="8e3dd-146">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8e3dd-146">Valid values are:</span></span>

- <span data-ttu-id="8e3dd-147">Egy</span><span class="sxs-lookup"><span data-stu-id="8e3dd-147">A</span></span>
- <span data-ttu-id="8e3dd-148">AAAA</span><span class="sxs-lookup"><span data-stu-id="8e3dd-148">AAAA</span></span>
- <span data-ttu-id="8e3dd-149">CNAME</span><span class="sxs-lookup"><span data-stu-id="8e3dd-149">CNAME</span></span>
- <span data-ttu-id="8e3dd-150">MX</span><span class="sxs-lookup"><span data-stu-id="8e3dd-150">MX</span></span>
- <span data-ttu-id="8e3dd-151">NS</span><span class="sxs-lookup"><span data-stu-id="8e3dd-151">NS</span></span>
- <span data-ttu-id="8e3dd-152">PTR</span><span class="sxs-lookup"><span data-stu-id="8e3dd-152">PTR</span></span>
- <span data-ttu-id="8e3dd-153">SRV</span><span class="sxs-lookup"><span data-stu-id="8e3dd-153">SRV</span></span>
- <span data-ttu-id="8e3dd-154">TXT</span><span class="sxs-lookup"><span data-stu-id="8e3dd-154">TXT</span></span>

<span data-ttu-id="8e3dd-155">A rendszer automatikusan törli a SOA rekordokat a zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-155">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="8e3dd-156">Nem lehet manuálisan törölni a SOA-rekordokat.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-156">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3dd-157">-ResourceGroupName</span></span>
<span data-ttu-id="8e3dd-158">Azt a erőforráscsoportot adja meg, amely a törölni kívánt **rekordhalmazt** tartalmazó DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-158">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="8e3dd-159">Ez a paraméter csak akkor érvényes, ha a Record set és a DNS Zone argumentumot a *Name* és a *ZoneName* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-159">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="8e3dd-160">Azt is megteheti, hogy a *rekordhalmaz* paraméterrel vagy a *név* és a *zóna* paraméterrel megadhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-160">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-161">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="8e3dd-161">-Zone</span></span>
<span data-ttu-id="8e3dd-162">A törlendő **rekordhalmazt** tartalmazó DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-162">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="8e3dd-163">Ez a paraméter csak akkor érvényes, ha a rekordot a *Name* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-163">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="8e3dd-164">Azt is megteheti, hogy a *rekordhalmaz* paraméterrel, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-164">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-165">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="8e3dd-165">-ZoneName</span></span>
<span data-ttu-id="8e3dd-166">A törlendő **rekordhalmazt** tartalmazó zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-166">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="8e3dd-167">A *név* -és *ResourceGroupName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-167">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="8e3dd-168">Másik lehetőségként a *rekordhalmazt a Recordset* paraméterrel vagy a *név* és a *zóna* paraméterrel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-168">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e3dd-169">-Confirm</span></span>
<span data-ttu-id="8e3dd-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e3dd-171">-WhatIf</span></span>
<span data-ttu-id="8e3dd-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e3dd-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3dd-174">CommonParameters</span></span>
<span data-ttu-id="8e3dd-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e3dd-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3dd-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e3dd-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3dd-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e3dd-177">INPUTS</span></span>

### <span data-ttu-id="8e3dd-178">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e3dd-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="8e3dd-179">Ezt a parancsmagot a **rekordhalmaz** -objektum pipe-ba kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="8e3dd-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e3dd-180">OUTPUTS</span></span>

### <span data-ttu-id="8e3dd-181">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e3dd-181">None</span></span>
<span data-ttu-id="8e3dd-182">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8e3dd-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e3dd-183">NOTES</span></span>
<span data-ttu-id="8e3dd-184">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8e3dd-185">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="8e3dd-186">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8e3dd-187">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8e3dd-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e3dd-188">RELATED LINKS</span></span>

[<span data-ttu-id="8e3dd-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e3dd-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="8e3dd-190">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e3dd-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="8e3dd-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e3dd-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
