---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187469"
---
# <span data-ttu-id="62dcb-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62dcb-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="62dcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="62dcb-103">Rekord törlése</span><span class="sxs-lookup"><span data-stu-id="62dcb-103">Deletes a record set.</span></span>

## <span data-ttu-id="62dcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62dcb-104">SYNTAX</span></span>

### <span data-ttu-id="62dcb-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="62dcb-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcb-106">Vegyes</span><span class="sxs-lookup"><span data-stu-id="62dcb-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcb-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="62dcb-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62dcb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="62dcb-108">DESCRIPTION</span></span>
<span data-ttu-id="62dcb-109">A **Remove-AzDnsRecordSet** parancsmag törli a megadott rekordot a megadott zónából.</span><span class="sxs-lookup"><span data-stu-id="62dcb-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="62dcb-110">Nem törölhet olyan SOA-vagy névkiszolgálói (NS) rekordokat, amelyek automatikusan létrejönnek a zóna APEX-ben.</span><span class="sxs-lookup"><span data-stu-id="62dcb-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="62dcb-111">A **rekordhalmaz** -objektumot átadhatja erre a parancsmagra a pipeline operátorral vagy paraméterként.</span><span class="sxs-lookup"><span data-stu-id="62dcb-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="62dcb-112">Ha a rekordokat név és típus szerint szeretné megadni a **rekordhalmaz** -objektum használata nélkül, a zónát **dnsZone** objektumként kell átadnia ehhez a parancsmaghoz a pipeline operátorral vagy paraméterként, illetve a *ZoneName* és a *ResourceGroupName* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="62dcb-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="62dcb-113">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62dcb-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="62dcb-114">Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.</span><span class="sxs-lookup"><span data-stu-id="62dcb-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="62dcb-115">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="62dcb-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="62dcb-116">Ezt úgy teheti meg, hogy a *felülírási* paramétert használja, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="62dcb-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="62dcb-117">Példák</span><span class="sxs-lookup"><span data-stu-id="62dcb-117">EXAMPLES</span></span>

### <span data-ttu-id="62dcb-118">1. példa: a rekordtípus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="62dcb-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="62dcb-119">Az első parancs a megadott rekordot kapja meg, majd a $RecordSet változóban tárolja. A második parancs eltávolítja a rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="62dcb-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="62dcb-120">2. példa: a rekordtípus eltávolítása és az összes megerősítés letiltása</span><span class="sxs-lookup"><span data-stu-id="62dcb-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="62dcb-121">Az első parancs a megadott rekordot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="62dcb-122">A második parancs törli a rekordot, még akkor is, ha időközben megváltozott.</span><span class="sxs-lookup"><span data-stu-id="62dcb-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="62dcb-123">A megerősítési utasításokat a rendszer letiltja.</span><span class="sxs-lookup"><span data-stu-id="62dcb-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="62dcb-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62dcb-124">PARAMETERS</span></span>

### <span data-ttu-id="62dcb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62dcb-125">-DefaultProfile</span></span>
<span data-ttu-id="62dcb-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62dcb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62dcb-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62dcb-127">-Name</span></span>
<span data-ttu-id="62dcb-128">Az eltávolítandó **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="62dcb-129">Ha a rekordot név szerint adja meg, a DNS-zónát a *Zone* paraméterrel vagy a *ZoneName* és a *ResourceGroupName* paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="62dcb-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="62dcb-130">Másik lehetőségként a rekordhalmazt egy **Recordset** objektum segítségével is megadhatja, amelyet a *rekordhalmaz* paraméterrel adhat meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="62dcb-131">-Átír</span><span class="sxs-lookup"><span data-stu-id="62dcb-131">-Overwrite</span></span>
<span data-ttu-id="62dcb-132">Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.</span><span class="sxs-lookup"><span data-stu-id="62dcb-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="62dcb-133">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="62dcb-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="62dcb-134">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="62dcb-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="62dcb-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62dcb-135">-PassThru</span></span>
<span data-ttu-id="62dcb-136">passthru</span><span class="sxs-lookup"><span data-stu-id="62dcb-136">passthru</span></span>

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

### <span data-ttu-id="62dcb-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="62dcb-137">-RecordSet</span></span>
<span data-ttu-id="62dcb-138">Az eltávolítandó **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="62dcb-139">Azt is megteheti, hogy a rekord a *név* és a *zóna* paraméter segítségével, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméter segítségével is megadható.</span><span class="sxs-lookup"><span data-stu-id="62dcb-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="62dcb-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="62dcb-140">-RecordType</span></span>
<span data-ttu-id="62dcb-141">A DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="62dcb-142">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="62dcb-142">Valid values are:</span></span>
- <span data-ttu-id="62dcb-143">Egy</span><span class="sxs-lookup"><span data-stu-id="62dcb-143">A</span></span>
- <span data-ttu-id="62dcb-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="62dcb-144">AAAA</span></span>
- <span data-ttu-id="62dcb-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="62dcb-145">CNAME</span></span>
- <span data-ttu-id="62dcb-146">MX</span><span class="sxs-lookup"><span data-stu-id="62dcb-146">MX</span></span>
- <span data-ttu-id="62dcb-147">NS</span><span class="sxs-lookup"><span data-stu-id="62dcb-147">NS</span></span>
- <span data-ttu-id="62dcb-148">PTR</span><span class="sxs-lookup"><span data-stu-id="62dcb-148">PTR</span></span>
- <span data-ttu-id="62dcb-149">SRV</span><span class="sxs-lookup"><span data-stu-id="62dcb-149">SRV</span></span>
- <span data-ttu-id="62dcb-150">A TXT SOA rekordokat a rendszer automatikusan törli a zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="62dcb-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="62dcb-151">Nem lehet manuálisan törölni a SOA-rekordokat.</span><span class="sxs-lookup"><span data-stu-id="62dcb-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="62dcb-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62dcb-152">-ResourceGroupName</span></span>
<span data-ttu-id="62dcb-153">Azt a erőforráscsoportot adja meg, amely a törölni kívánt **rekordhalmazt** tartalmazó DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="62dcb-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="62dcb-154">Ez a paraméter csak akkor érvényes, ha a Record set és a DNS Zone argumentumot a *Name* és a *ZoneName* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="62dcb-155">Azt is megteheti, hogy a *rekordhalmaz* paraméterrel vagy a *név* és a *zóna* paraméterrel megadhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="62dcb-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="62dcb-156">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="62dcb-156">-Zone</span></span>
<span data-ttu-id="62dcb-157">A törlendő **rekordhalmazt** tartalmazó DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="62dcb-158">Ez a paraméter csak akkor érvényes, ha a rekordot a *Name* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="62dcb-159">Azt is megteheti, hogy a *rekordhalmaz* paraméterrel, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="62dcb-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="62dcb-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="62dcb-160">-ZoneName</span></span>
<span data-ttu-id="62dcb-161">A törlendő **rekordhalmazt** tartalmazó zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62dcb-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="62dcb-162">A *név* -és *ResourceGroupName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="62dcb-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="62dcb-163">Másik lehetőségként a *rekordhalmazt a Recordset* paraméterrel vagy a *név* és a *zóna* paraméterrel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="62dcb-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="62dcb-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62dcb-164">-Confirm</span></span>
<span data-ttu-id="62dcb-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62dcb-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62dcb-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62dcb-166">-WhatIf</span></span>
<span data-ttu-id="62dcb-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62dcb-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62dcb-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62dcb-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62dcb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62dcb-169">CommonParameters</span></span>
<span data-ttu-id="62dcb-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62dcb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62dcb-171">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62dcb-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62dcb-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62dcb-172">INPUTS</span></span>

### <span data-ttu-id="62dcb-173">Microsoft. Azure. Management. DNS. models. RecordType</span><span class="sxs-lookup"><span data-stu-id="62dcb-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="62dcb-174">System. String</span><span class="sxs-lookup"><span data-stu-id="62dcb-174">System.String</span></span>

### <span data-ttu-id="62dcb-175">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="62dcb-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="62dcb-176">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62dcb-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="62dcb-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62dcb-177">OUTPUTS</span></span>

### <span data-ttu-id="62dcb-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62dcb-178">System.Boolean</span></span>

## <span data-ttu-id="62dcb-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62dcb-179">NOTES</span></span>
<span data-ttu-id="62dcb-180">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62dcb-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="62dcb-181">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="62dcb-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="62dcb-182">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62dcb-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="62dcb-183">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62dcb-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="62dcb-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62dcb-184">RELATED LINKS</span></span>

[<span data-ttu-id="62dcb-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62dcb-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="62dcb-186">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62dcb-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="62dcb-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62dcb-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
