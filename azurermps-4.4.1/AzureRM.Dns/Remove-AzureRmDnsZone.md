---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: a9f277c17d0396127ca1b2678d8c9c77ef3628c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504175"
---
# <span data-ttu-id="5bdde-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bdde-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="5bdde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bdde-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdde-103">Eltávolítja a DNS-zónát egy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5bdde-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bdde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bdde-104">SYNTAX</span></span>

### <span data-ttu-id="5bdde-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="5bdde-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdde-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="5bdde-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdde-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bdde-107">DESCRIPTION</span></span>
<span data-ttu-id="5bdde-108">A **Remove-AzureRmDnsZone** parancsmag véglegesen törli a DNS-zónát egy adott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="5bdde-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="5bdde-109">A zónában található összes rekord is törlődik.</span><span class="sxs-lookup"><span data-stu-id="5bdde-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="5bdde-110">A **dnsZone** -objektumokat átadhatja a *Name* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5bdde-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="5bdde-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bdde-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="5bdde-112">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="5bdde-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5bdde-113">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="5bdde-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5bdde-114">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="5bdde-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5bdde-115">Példák</span><span class="sxs-lookup"><span data-stu-id="5bdde-115">EXAMPLES</span></span>

### <span data-ttu-id="5bdde-116">1. példa: zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5bdde-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5bdde-117">Ez a parancs eltávolítja a myzone.com nevű zónát a MyResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="5bdde-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5bdde-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bdde-118">PARAMETERS</span></span>

### <span data-ttu-id="5bdde-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5bdde-119">-Force</span></span>
<span data-ttu-id="5bdde-120">Ez a paraméter érvénytelenítve van ennél a parancsmagnál.</span><span class="sxs-lookup"><span data-stu-id="5bdde-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="5bdde-121">A program eltávolítja a jövőbeli kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="5bdde-121">It will be removed in a future release.</span></span>

<span data-ttu-id="5bdde-122">Ha meg szeretné állapítani, hogy ez a parancsmag kéri-e a megerősítést, használja a *Confirm* paramétert.</span><span class="sxs-lookup"><span data-stu-id="5bdde-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="5bdde-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bdde-123">-Name</span></span>
<span data-ttu-id="5bdde-124">A parancsmag által eltávolított DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bdde-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="5bdde-125">Meg kell adnia a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5bdde-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="5bdde-126">Azt is megteheti, hogy a *zóna* paraméterrel megadhatja a DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="5bdde-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5bdde-127">-Átír</span><span class="sxs-lookup"><span data-stu-id="5bdde-127">-Overwrite</span></span>
<span data-ttu-id="5bdde-128">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="5bdde-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5bdde-129">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="5bdde-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="5bdde-130">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="5bdde-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5bdde-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bdde-131">-PassThru</span></span>
<span data-ttu-id="5bdde-132">passthru</span><span class="sxs-lookup"><span data-stu-id="5bdde-132">passthru</span></span>

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

### <span data-ttu-id="5bdde-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bdde-133">-ResourceGroupName</span></span>
<span data-ttu-id="5bdde-134">Az eltávolítandó zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bdde-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="5bdde-135">Meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5bdde-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="5bdde-136">Azt is megteheti, hogy megadhatja a DNS-zónát egy **dnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="5bdde-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5bdde-137">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="5bdde-137">-Zone</span></span>
<span data-ttu-id="5bdde-138">A törlendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bdde-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="5bdde-139">Az átadott **dnsZone** objektum a csővezetéken keresztül is áthaladhat.</span><span class="sxs-lookup"><span data-stu-id="5bdde-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="5bdde-140">Azt is megteheti, hogy megadhatja a törölni kívánt DNS-zónát a *ZoneName* és a *ResourceGroupName* paraméter segítségével.</span><span class="sxs-lookup"><span data-stu-id="5bdde-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="5bdde-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bdde-141">-Confirm</span></span>
<span data-ttu-id="5bdde-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bdde-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdde-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdde-143">-WhatIf</span></span>
<span data-ttu-id="5bdde-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bdde-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bdde-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bdde-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdde-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdde-146">-DefaultProfile</span></span>
<span data-ttu-id="5bdde-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bdde-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bdde-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdde-148">CommonParameters</span></span>
<span data-ttu-id="5bdde-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bdde-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdde-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdde-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdde-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bdde-151">INPUTS</span></span>

### <span data-ttu-id="5bdde-152">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="5bdde-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="5bdde-153">Ezt a parancsmagot a **dnsZone** -objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="5bdde-153">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="5bdde-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bdde-154">OUTPUTS</span></span>

### <span data-ttu-id="5bdde-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bdde-155">None</span></span>
<span data-ttu-id="5bdde-156">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5bdde-156">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5bdde-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bdde-157">NOTES</span></span>
<span data-ttu-id="5bdde-158">A DNS-zóna törlésének potenciálisan nagy hatása miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést, ha a $ConfirmPreference Windows PowerShell-változó a nincs értéktől eltérő értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="5bdde-158">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="5bdde-159">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bdde-159">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="5bdde-160">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bdde-160">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="5bdde-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bdde-161">RELATED LINKS</span></span>

[<span data-ttu-id="5bdde-162">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bdde-162">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="5bdde-163">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bdde-163">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="5bdde-164">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5bdde-164">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)