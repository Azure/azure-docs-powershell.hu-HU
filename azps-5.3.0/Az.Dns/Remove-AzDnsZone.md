---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466177"
---
# <span data-ttu-id="7e010-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7e010-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="7e010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e010-102">SYNOPSIS</span></span>
<span data-ttu-id="7e010-103">Eltávolít egy DNS-zónát egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="7e010-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="7e010-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e010-104">SYNTAX</span></span>

### <span data-ttu-id="7e010-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="7e010-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e010-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="7e010-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e010-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e010-107">DESCRIPTION</span></span>
<span data-ttu-id="7e010-108">Az **Remove-AzDnsZone** parancsmag véglegesen töröl egy DNS-zónát egy adott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="7e010-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="7e010-109">A zónában található összes rekordkészlet is törlődik.</span><span class="sxs-lookup"><span data-stu-id="7e010-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="7e010-110">A **DnsZone-objektumokat** átadhatja a Name paraméterrel vagy a folyamat műveleti jelével, vagy másik lehetőségként megadhatja a *ZoneName* és *az ResourceGroupName* paramétert. </span><span class="sxs-lookup"><span data-stu-id="7e010-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7e010-111">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="7e010-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7e010-112">Amikor **dnsZone-objektummal** adja meg a zónát  (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **DnsZone-objektum** beolvasása óta (csak a DNS-zóna erőforrásának módosításain végrehajtott műveletek számítanak változásnak, a zónán belüli rekordkészletek műveletei nem).</span><span class="sxs-lookup"><span data-stu-id="7e010-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7e010-113">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="7e010-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7e010-114">Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="7e010-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="7e010-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e010-115">EXAMPLES</span></span>

### <span data-ttu-id="7e010-116">1. példa: Zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7e010-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7e010-117">Ez a parancs eltávolítja a myzone.com myResourceGroup nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="7e010-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7e010-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e010-118">PARAMETERS</span></span>

### <span data-ttu-id="7e010-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e010-119">-DefaultProfile</span></span>
<span data-ttu-id="7e010-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e010-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e010-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e010-121">-Name</span></span>
<span data-ttu-id="7e010-122">A parancsmag által eltávolított DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="7e010-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="7e010-123">Az *ResourceGroupName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="7e010-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="7e010-124">Másik lehetőségként megadhatja a DNS-zónát a *Zone paraméter* használatával.</span><span class="sxs-lookup"><span data-stu-id="7e010-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7e010-125">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="7e010-125">-Overwrite</span></span>
<span data-ttu-id="7e010-126">Amikor **dnsZone-objektummal** adja meg a zónát  (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **DnsZone-objektum** beolvasása óta (csak a DNS-zóna erőforrásának módosításain végrehajtott műveletek számítanak változásnak, a zónán belüli rekordkészletek műveletei nem).</span><span class="sxs-lookup"><span data-stu-id="7e010-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7e010-127">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="7e010-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7e010-128">Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="7e010-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="7e010-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e010-129">-PassThru</span></span>
<span data-ttu-id="7e010-130">passthru</span><span class="sxs-lookup"><span data-stu-id="7e010-130">passthru</span></span>

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

### <span data-ttu-id="7e010-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e010-131">-ResourceGroupName</span></span>
<span data-ttu-id="7e010-132">Az eltávolítható zónát tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e010-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="7e010-133">A *ZoneName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="7e010-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="7e010-134">Másik lehetőségként megadhatja a DNS-zónát egy **DnsZone-objektum** használatával, amely vagy a folyamaton, vagy a Zone paraméteren *keresztül adható* meg.</span><span class="sxs-lookup"><span data-stu-id="7e010-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7e010-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="7e010-135">-Zone</span></span>
<span data-ttu-id="7e010-136">A törlendni kívánt DNS-zóna.</span><span class="sxs-lookup"><span data-stu-id="7e010-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="7e010-137">A **átadott DnsZone-objektum** a folyamaton keresztül is áthaladhat.</span><span class="sxs-lookup"><span data-stu-id="7e010-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="7e010-138">Másik lehetőségként megadhatja a törölni kívánt DNS-zónát a *ZoneName* és *az ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="7e010-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="7e010-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e010-139">-Confirm</span></span>
<span data-ttu-id="7e010-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e010-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e010-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e010-141">-WhatIf</span></span>
<span data-ttu-id="7e010-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e010-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e010-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e010-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e010-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e010-144">CommonParameters</span></span>
<span data-ttu-id="7e010-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e010-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e010-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e010-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e010-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e010-147">INPUTS</span></span>

### <span data-ttu-id="7e010-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7e010-148">System.String</span></span>

### <span data-ttu-id="7e010-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="7e010-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="7e010-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e010-150">OUTPUTS</span></span>

### <span data-ttu-id="7e010-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7e010-151">System.Boolean</span></span>

## <span data-ttu-id="7e010-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e010-152">NOTES</span></span>
<span data-ttu-id="7e010-153">A DNS-zóna törlésének potenciálisan nagy hatása miatt ez a parancsmag alapértelmezés szerint megerősítést kér, ha a $ConfirmPreference Windows PowerShell-változó értéke a Nincs értéktől különböző.</span><span class="sxs-lookup"><span data-stu-id="7e010-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="7e010-154">Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatás előtt.</span><span class="sxs-lookup"><span data-stu-id="7e010-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="7e010-155">Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e010-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="7e010-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e010-156">RELATED LINKS</span></span>

[<span data-ttu-id="7e010-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7e010-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="7e010-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7e010-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="7e010-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7e010-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
