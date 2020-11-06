---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: e009eea8276bbfe9653c506864604ca955a6367f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493513"
---
# <span data-ttu-id="6ef8b-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ef8b-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="6ef8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ef8b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef8b-103">Rekord törlése</span><span class="sxs-lookup"><span data-stu-id="6ef8b-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ef8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ef8b-104">SYNTAX</span></span>

### <span data-ttu-id="6ef8b-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="6ef8b-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ef8b-106">Vegyes</span><span class="sxs-lookup"><span data-stu-id="6ef8b-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ef8b-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="6ef8b-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ef8b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ef8b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ef8b-109">A **Remove-AzureRmDnsRecordSet** parancsmag törli a megadott rekordot a megadott zónából.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="6ef8b-110">Nem törölhet olyan SOA-vagy névkiszolgálói (NS) rekordokat, amelyek automatikusan létrejönnek a zóna APEX-ben.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="6ef8b-111">A **rekordhalmaz** -objektumot átadhatja erre a parancsmagra a pipeline operátorral vagy paraméterként.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="6ef8b-112">Ha a rekordokat név és típus szerint szeretné megadni a **rekordhalmaz** -objektum használata nélkül, a zónát **dnsZone** objektumként kell átadnia ehhez a parancsmaghoz a pipeline operátorral vagy paraméterként, illetve a *ZoneName* és a *ResourceGroupName* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="6ef8b-113">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="6ef8b-114">Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="6ef8b-115">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="6ef8b-116">Ezt úgy teheti meg, hogy a *felülírási* paramétert használja, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="6ef8b-117">Példák</span><span class="sxs-lookup"><span data-stu-id="6ef8b-117">EXAMPLES</span></span>

### <span data-ttu-id="6ef8b-118">1. példa: a rekordtípus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6ef8b-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="6ef8b-119">Az első parancs a megadott rekordot kapja meg, majd a $RecordSet változóban tárolja. A második parancs eltávolítja a rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="6ef8b-120">2. példa: a rekordtípus eltávolítása és az összes megerősítés letiltása</span><span class="sxs-lookup"><span data-stu-id="6ef8b-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="6ef8b-121">Az első parancs a megadott rekordot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="6ef8b-122">A második parancs törli a rekordot, még akkor is, ha időközben megváltozott.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="6ef8b-123">A megerősítési utasításokat a rendszer letiltja.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="6ef8b-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ef8b-124">PARAMETERS</span></span>

### <span data-ttu-id="6ef8b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6ef8b-125">-Force</span></span>
<span data-ttu-id="6ef8b-126">Ez a paraméter érvénytelenítve van ennél a parancsmagnál.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="6ef8b-127">A program eltávolítja a jövőbeli kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-127">It will be removed in a future release.</span></span>

<span data-ttu-id="6ef8b-128">Ha meg szeretné állapítani, hogy ez a parancsmag kéri-e a megerősítést, használja a *Confirm* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="6ef8b-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ef8b-129">-Name</span></span>
<span data-ttu-id="6ef8b-130">Az eltávolítandó **rekordhalmaz** nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="6ef8b-131">Ha a rekordot név szerint adja meg, a DNS-zónát a *Zone* paraméterrel vagy a *ZoneName* és a *ResourceGroupName* paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="6ef8b-132">Másik lehetőségként a rekordhalmazt egy **Recordset** objektum segítségével is megadhatja, amelyet a *rekordhalmaz* paraméterrel adhat meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="6ef8b-133">-Átír</span><span class="sxs-lookup"><span data-stu-id="6ef8b-133">-Overwrite</span></span>
<span data-ttu-id="6ef8b-134">Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="6ef8b-135">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="6ef8b-136">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6ef8b-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ef8b-137">-PassThru</span></span>
<span data-ttu-id="6ef8b-138">passthru</span><span class="sxs-lookup"><span data-stu-id="6ef8b-138">passthru</span></span>

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

### <span data-ttu-id="6ef8b-139">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="6ef8b-139">-RecordSet</span></span>
<span data-ttu-id="6ef8b-140">Az eltávolítandó **Recordset** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="6ef8b-141">Azt is megteheti, hogy a rekord a *név* és a *zóna* paraméter segítségével, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméter segítségével is megadható.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6ef8b-142">-RecordType</span><span class="sxs-lookup"><span data-stu-id="6ef8b-142">-RecordType</span></span>
<span data-ttu-id="6ef8b-143">A DNS-rekord típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="6ef8b-144">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6ef8b-144">Valid values are:</span></span>

- <span data-ttu-id="6ef8b-145">Egy</span><span class="sxs-lookup"><span data-stu-id="6ef8b-145">A</span></span>
- <span data-ttu-id="6ef8b-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="6ef8b-146">AAAA</span></span>
- <span data-ttu-id="6ef8b-147">CNAME</span><span class="sxs-lookup"><span data-stu-id="6ef8b-147">CNAME</span></span>
- <span data-ttu-id="6ef8b-148">MX</span><span class="sxs-lookup"><span data-stu-id="6ef8b-148">MX</span></span>
- <span data-ttu-id="6ef8b-149">NS</span><span class="sxs-lookup"><span data-stu-id="6ef8b-149">NS</span></span>
- <span data-ttu-id="6ef8b-150">PTR</span><span class="sxs-lookup"><span data-stu-id="6ef8b-150">PTR</span></span>
- <span data-ttu-id="6ef8b-151">SRV</span><span class="sxs-lookup"><span data-stu-id="6ef8b-151">SRV</span></span>
- <span data-ttu-id="6ef8b-152">TXT</span><span class="sxs-lookup"><span data-stu-id="6ef8b-152">TXT</span></span>

<span data-ttu-id="6ef8b-153">A rendszer automatikusan törli a SOA rekordokat a zóna törlésekor.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="6ef8b-154">Nem lehet manuálisan törölni a SOA-rekordokat.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef8b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef8b-155">-ResourceGroupName</span></span>
<span data-ttu-id="6ef8b-156">Azt a erőforráscsoportot adja meg, amely a törölni kívánt **rekordhalmazt** tartalmazó DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="6ef8b-157">Ez a paraméter csak akkor érvényes, ha a Record set és a DNS Zone argumentumot a *Name* és a *ZoneName* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="6ef8b-158">Azt is megteheti, hogy a *rekordhalmaz* paraméterrel vagy a *név* és a *zóna* paraméterrel megadhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="6ef8b-159">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="6ef8b-159">-Zone</span></span>
<span data-ttu-id="6ef8b-160">A törlendő **rekordhalmazt** tartalmazó DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="6ef8b-161">Ez a paraméter csak akkor érvényes, ha a rekordot a *Name* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="6ef8b-162">Azt is megteheti, hogy a *rekordhalmaz* paraméterrel, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a rekordot.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6ef8b-163">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="6ef8b-163">-ZoneName</span></span>
<span data-ttu-id="6ef8b-164">A törlendő **rekordhalmazt** tartalmazó zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="6ef8b-165">A *név* -és *ResourceGroupName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="6ef8b-166">Másik lehetőségként a *rekordhalmazt a Recordset* paraméterrel vagy a *név* és a *zóna* paraméterrel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="6ef8b-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ef8b-167">-Confirm</span></span>
<span data-ttu-id="6ef8b-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef8b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef8b-169">-WhatIf</span></span>
<span data-ttu-id="6ef8b-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ef8b-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef8b-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef8b-172">-DefaultProfile</span></span>
<span data-ttu-id="6ef8b-173">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef8b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef8b-174">CommonParameters</span></span>
<span data-ttu-id="6ef8b-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ef8b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef8b-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef8b-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef8b-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ef8b-177">INPUTS</span></span>

### <span data-ttu-id="6ef8b-178">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ef8b-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6ef8b-179">Ezt a parancsmagot a **rekordhalmaz** -objektum pipe-ba kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="6ef8b-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ef8b-180">OUTPUTS</span></span>

### <span data-ttu-id="6ef8b-181">Nincs</span><span class="sxs-lookup"><span data-stu-id="6ef8b-181">None</span></span>
<span data-ttu-id="6ef8b-182">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6ef8b-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ef8b-183">NOTES</span></span>
<span data-ttu-id="6ef8b-184">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6ef8b-185">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6ef8b-186">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6ef8b-187">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ef8b-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6ef8b-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ef8b-188">RELATED LINKS</span></span>

[<span data-ttu-id="6ef8b-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ef8b-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="6ef8b-190">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ef8b-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="6ef8b-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ef8b-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
