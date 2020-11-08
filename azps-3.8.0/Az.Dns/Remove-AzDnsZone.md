---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010949"
---
# <span data-ttu-id="a0c85-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a0c85-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="a0c85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0c85-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c85-103">Eltávolítja a DNS-zónát egy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a0c85-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="a0c85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0c85-104">SYNTAX</span></span>

### <span data-ttu-id="a0c85-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="a0c85-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0c85-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="a0c85-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0c85-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0c85-107">DESCRIPTION</span></span>
<span data-ttu-id="a0c85-108">A **Remove-AzDnsZone** parancsmag véglegesen törli a DNS-zónát egy adott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="a0c85-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="a0c85-109">A zónában található összes rekord is törlődik.</span><span class="sxs-lookup"><span data-stu-id="a0c85-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="a0c85-110">A **dnsZone** -objektumokat átadhatja a *Name* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="a0c85-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="a0c85-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0c85-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a0c85-112">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="a0c85-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="a0c85-113">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="a0c85-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="a0c85-114">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="a0c85-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="a0c85-115">Példák</span><span class="sxs-lookup"><span data-stu-id="a0c85-115">EXAMPLES</span></span>

### <span data-ttu-id="a0c85-116">1. példa: zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a0c85-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a0c85-117">Ez a parancs eltávolítja a myzone.com nevű zónát a MyResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="a0c85-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a0c85-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0c85-118">PARAMETERS</span></span>

### <span data-ttu-id="a0c85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c85-119">-DefaultProfile</span></span>
<span data-ttu-id="a0c85-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0c85-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0c85-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0c85-121">-Name</span></span>
<span data-ttu-id="a0c85-122">A parancsmag által eltávolított DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0c85-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="a0c85-123">Meg kell adnia a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="a0c85-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a0c85-124">Azt is megteheti, hogy a *zóna* paraméterrel megadhatja a DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="a0c85-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a0c85-125">-Átír</span><span class="sxs-lookup"><span data-stu-id="a0c85-125">-Overwrite</span></span>
<span data-ttu-id="a0c85-126">Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="a0c85-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="a0c85-127">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="a0c85-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="a0c85-128">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="a0c85-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="a0c85-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0c85-129">-PassThru</span></span>
<span data-ttu-id="a0c85-130">passthru</span><span class="sxs-lookup"><span data-stu-id="a0c85-130">passthru</span></span>

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

### <span data-ttu-id="a0c85-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c85-131">-ResourceGroupName</span></span>
<span data-ttu-id="a0c85-132">Az eltávolítandó zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0c85-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="a0c85-133">Meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="a0c85-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="a0c85-134">Azt is megteheti, hogy megadhatja a DNS-zónát egy **dnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="a0c85-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a0c85-135">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="a0c85-135">-Zone</span></span>
<span data-ttu-id="a0c85-136">A törlendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0c85-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="a0c85-137">Az átadott **dnsZone** objektum a csővezetéken keresztül is áthaladhat.</span><span class="sxs-lookup"><span data-stu-id="a0c85-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="a0c85-138">Azt is megteheti, hogy megadhatja a törölni kívánt DNS-zónát a *ZoneName* és a *ResourceGroupName* paraméter segítségével.</span><span class="sxs-lookup"><span data-stu-id="a0c85-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="a0c85-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0c85-139">-Confirm</span></span>
<span data-ttu-id="a0c85-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0c85-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0c85-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c85-141">-WhatIf</span></span>
<span data-ttu-id="a0c85-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0c85-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0c85-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0c85-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0c85-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c85-144">CommonParameters</span></span>
<span data-ttu-id="a0c85-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0c85-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c85-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c85-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c85-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0c85-147">INPUTS</span></span>

### <span data-ttu-id="a0c85-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a0c85-148">System.String</span></span>

### <span data-ttu-id="a0c85-149">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a0c85-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="a0c85-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0c85-150">OUTPUTS</span></span>

### <span data-ttu-id="a0c85-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0c85-151">System.Boolean</span></span>

## <span data-ttu-id="a0c85-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0c85-152">NOTES</span></span>
<span data-ttu-id="a0c85-153">A DNS-zóna törlésének potenciálisan nagy hatása miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést, ha a $ConfirmPreference Windows PowerShell-változó a nincs értéktől eltérő értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="a0c85-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="a0c85-154">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0c85-154">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a0c85-155">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0c85-155">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="a0c85-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0c85-156">RELATED LINKS</span></span>

[<span data-ttu-id="a0c85-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a0c85-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="a0c85-158">Új – AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a0c85-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="a0c85-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a0c85-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
