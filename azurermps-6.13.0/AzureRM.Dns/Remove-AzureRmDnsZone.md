---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: f5dd34c15745707df8bb0b91f7a4716e5c0bba6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499523"
---
# <span data-ttu-id="c225a-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c225a-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="c225a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c225a-102">SYNOPSIS</span></span>
<span data-ttu-id="c225a-103">Eltávolítja a DNS-zónát egy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c225a-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c225a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c225a-104">SYNTAX</span></span>

### <span data-ttu-id="c225a-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="c225a-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c225a-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="c225a-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c225a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c225a-107">DESCRIPTION</span></span>
<span data-ttu-id="c225a-108">A **Remove-AzureRmDnsZone** parancsmag véglegesen törli a DNS-zónát egy adott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="c225a-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="c225a-109">A zónában található összes rekord is törlődik.</span><span class="sxs-lookup"><span data-stu-id="c225a-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="c225a-110">A **dnsZone** -objektumokat átadhatja a *Name* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="c225a-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="c225a-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c225a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c225a-112">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="c225a-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="c225a-113">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="c225a-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="c225a-114">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="c225a-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="c225a-115">Példák</span><span class="sxs-lookup"><span data-stu-id="c225a-115">EXAMPLES</span></span>

### <span data-ttu-id="c225a-116">1. példa: zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c225a-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c225a-117">Ez a parancs eltávolítja a myzone.com nevű zónát a MyResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="c225a-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="c225a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c225a-118">PARAMETERS</span></span>

### <span data-ttu-id="c225a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c225a-119">-DefaultProfile</span></span>
<span data-ttu-id="c225a-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c225a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c225a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c225a-121">-Name</span></span>
<span data-ttu-id="c225a-122">A parancsmag által eltávolított DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c225a-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="c225a-123">Meg kell adnia a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="c225a-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="c225a-124">Azt is megteheti, hogy a *zóna* paraméterrel megadhatja a DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="c225a-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="c225a-125">-Átír</span><span class="sxs-lookup"><span data-stu-id="c225a-125">-Overwrite</span></span>
<span data-ttu-id="c225a-126">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="c225a-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="c225a-127">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="c225a-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="c225a-128">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="c225a-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="c225a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c225a-129">-PassThru</span></span>
<span data-ttu-id="c225a-130">passthru</span><span class="sxs-lookup"><span data-stu-id="c225a-130">passthru</span></span>

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

### <span data-ttu-id="c225a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c225a-131">-ResourceGroupName</span></span>
<span data-ttu-id="c225a-132">Az eltávolítandó zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c225a-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="c225a-133">Meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="c225a-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="c225a-134">Azt is megteheti, hogy megadhatja a DNS-zónát egy **dnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="c225a-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="c225a-135">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="c225a-135">-Zone</span></span>
<span data-ttu-id="c225a-136">A törlendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c225a-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="c225a-137">Az átadott **dnsZone** objektum a csővezetéken keresztül is áthaladhat.</span><span class="sxs-lookup"><span data-stu-id="c225a-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="c225a-138">Azt is megteheti, hogy megadhatja a törölni kívánt DNS-zónát a *ZoneName* és a *ResourceGroupName* paraméter segítségével.</span><span class="sxs-lookup"><span data-stu-id="c225a-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="c225a-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c225a-139">-Confirm</span></span>
<span data-ttu-id="c225a-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c225a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c225a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c225a-141">-WhatIf</span></span>
<span data-ttu-id="c225a-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c225a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c225a-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c225a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c225a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c225a-144">CommonParameters</span></span>
<span data-ttu-id="c225a-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c225a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c225a-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c225a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c225a-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c225a-147">INPUTS</span></span>

### <span data-ttu-id="c225a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c225a-148">System.String</span></span>

### <span data-ttu-id="c225a-149">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="c225a-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="c225a-150">Paraméterek: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c225a-150">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="c225a-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c225a-151">OUTPUTS</span></span>

### <span data-ttu-id="c225a-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c225a-152">System.Boolean</span></span>

## <span data-ttu-id="c225a-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c225a-153">NOTES</span></span>
<span data-ttu-id="c225a-154">A DNS-zóna törlésének potenciálisan nagy hatása miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést, ha a $ConfirmPreference Windows PowerShell-változó a nincs értéktől eltérő értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c225a-154">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="c225a-155">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c225a-155">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c225a-156">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c225a-156">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="c225a-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c225a-157">RELATED LINKS</span></span>

[<span data-ttu-id="c225a-158">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c225a-158">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="c225a-159">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c225a-159">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="c225a-160">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c225a-160">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
