---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850862"
---
# <span data-ttu-id="2d3b7-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3b7-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="2d3b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3b7-103">Eltávolítja a DNS-zónát egy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d3b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d3b7-104">SYNTAX</span></span>

### <span data-ttu-id="2d3b7-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="2d3b7-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d3b7-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="2d3b7-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d3b7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d3b7-107">DESCRIPTION</span></span>
<span data-ttu-id="2d3b7-108">A **Remove-AzureRmDnsZone** parancsmag véglegesen törli a DNS-zónát egy adott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="2d3b7-109">A zónában található összes rekord is törlődik.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="2d3b7-110">A **dnsZone** -objektumokat átadhatja a *Name* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="2d3b7-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="2d3b7-112">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="2d3b7-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="2d3b7-113">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="2d3b7-114">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2d3b7-115">Példák</span><span class="sxs-lookup"><span data-stu-id="2d3b7-115">EXAMPLES</span></span>

### <span data-ttu-id="2d3b7-116">1. példa: zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2d3b7-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2d3b7-117">Ez a parancs eltávolítja a myzone.com nevű zónát a MyResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2d3b7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d3b7-118">PARAMETERS</span></span>

### <span data-ttu-id="2d3b7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2d3b7-119">-Force</span></span>
<span data-ttu-id="2d3b7-120">Ez a paraméter érvénytelenítve van ennél a parancsmagnál.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="2d3b7-121">A program eltávolítja a jövőbeli kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-121">It will be removed in a future release.</span></span>

<span data-ttu-id="2d3b7-122">Ha meg szeretné állapítani, hogy ez a parancsmag kéri-e a megerősítést, használja a *Confirm* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="2d3b7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d3b7-123">-Name</span></span>
<span data-ttu-id="2d3b7-124">A parancsmag által eltávolított DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="2d3b7-125">Meg kell adnia a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="2d3b7-126">Azt is megteheti, hogy a *zóna* paraméterrel megadhatja a DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2d3b7-127">-Átír</span><span class="sxs-lookup"><span data-stu-id="2d3b7-127">-Overwrite</span></span>
<span data-ttu-id="2d3b7-128">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="2d3b7-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="2d3b7-129">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="2d3b7-130">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="2d3b7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d3b7-131">-PassThru</span></span>
<span data-ttu-id="2d3b7-132">passthru</span><span class="sxs-lookup"><span data-stu-id="2d3b7-132">passthru</span></span>

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

### <span data-ttu-id="2d3b7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3b7-133">-ResourceGroupName</span></span>
<span data-ttu-id="2d3b7-134">Az eltávolítandó zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="2d3b7-135">Meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="2d3b7-136">Azt is megteheti, hogy megadhatja a DNS-zónát egy **dnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2d3b7-137">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="2d3b7-137">-Zone</span></span>
<span data-ttu-id="2d3b7-138">A törlendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="2d3b7-139">Az átadott **dnsZone** objektum a csővezetéken keresztül is áthaladhat.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="2d3b7-140">Azt is megteheti, hogy megadhatja a törölni kívánt DNS-zónát a *ZoneName* és a *ResourceGroupName* paraméter segítségével.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3b7-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d3b7-141">-Confirm</span></span>
<span data-ttu-id="2d3b7-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3b7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d3b7-143">-WhatIf</span></span>
<span data-ttu-id="2d3b7-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d3b7-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d3b7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3b7-146">CommonParameters</span></span>
<span data-ttu-id="2d3b7-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d3b7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3b7-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3b7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3b7-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d3b7-149">INPUTS</span></span>

### <span data-ttu-id="2d3b7-150">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3b7-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2d3b7-151">Ezt a parancsmagot a **dnsZone** -objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="2d3b7-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d3b7-152">OUTPUTS</span></span>

### <span data-ttu-id="2d3b7-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d3b7-153">None</span></span>
<span data-ttu-id="2d3b7-154">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="2d3b7-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d3b7-155">NOTES</span></span>
<span data-ttu-id="2d3b7-156">A DNS-zóna törlésének potenciálisan nagy hatása miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést, ha a $ConfirmPreference Windows PowerShell-változó a nincs értéktől eltérő értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="2d3b7-157">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2d3b7-158">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d3b7-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="2d3b7-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d3b7-159">RELATED LINKS</span></span>

[<span data-ttu-id="2d3b7-160">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3b7-160">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="2d3b7-161">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3b7-161">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="2d3b7-162">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3b7-162">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
