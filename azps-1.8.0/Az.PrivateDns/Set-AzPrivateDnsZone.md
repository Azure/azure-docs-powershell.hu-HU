---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: a5c4ae9492d64bc8c84439f747031d6facd88673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669765"
---
# <span data-ttu-id="e5591-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5591-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="e5591-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5591-102">SYNOPSIS</span></span>
<span data-ttu-id="e5591-103">Egy privát DNS-zónát frissít egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="e5591-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="e5591-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5591-104">SYNTAX</span></span>

### <span data-ttu-id="e5591-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5591-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5591-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5591-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5591-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="e5591-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5591-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5591-108">DESCRIPTION</span></span>
<span data-ttu-id="e5591-109">A **set-AzPrivateDnsZone** parancsmag véglegesen frissíti a privát tartománynévrendszer (DNS) zónát egy adott erőforráscsoport alapján.</span><span class="sxs-lookup"><span data-stu-id="e5591-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="e5591-110">A **PrivateDnsZone** -objektumokat a *PrivateZone* paraméterrel vagy a csővezeték-kezelő használatával is átadhatja, vagy megadhatja a *nevet* és a *ResourceGroupName* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="e5591-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e5591-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5591-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e5591-112">Ha a zónát egy **PrivateDnsZone** -objektummal adja meg (a csővezetéken vagy a *Zone* paraméteren keresztül továbbítja), a zóna nem frissül, ha az Azure DNS-ben módosította a helyi **PrivateDnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="e5591-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="e5591-113">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="e5591-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="e5591-114">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="e5591-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="e5591-115">Példák</span><span class="sxs-lookup"><span data-stu-id="e5591-115">EXAMPLES</span></span>

### <span data-ttu-id="e5591-116">Példa 1: privát zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="e5591-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="e5591-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5591-117">PARAMETERS</span></span>

### <span data-ttu-id="e5591-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5591-118">-DefaultProfile</span></span>
<span data-ttu-id="e5591-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5591-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5591-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5591-120">-Name</span></span>
<span data-ttu-id="e5591-121">Annak a magánhálózati DNS-zónának a neve, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="e5591-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="e5591-122">Meg kell adnia a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="e5591-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="e5591-123">Azt is megteheti, hogy a privát DNS-zónát a *Zone* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5591-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5591-124">-Átír</span><span class="sxs-lookup"><span data-stu-id="e5591-124">-Overwrite</span></span>
<span data-ttu-id="e5591-125">Ha a zónát egy **PrivateDnsZone** -objektummal adja meg (a csővezetéken vagy a *Zone* paraméteren keresztül továbbítja), a zóna nem frissül, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="e5591-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="e5591-126">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="e5591-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="e5591-127">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="e5591-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e5591-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="e5591-128">-PrivateZone</span></span>
<span data-ttu-id="e5591-129">A beállítani kívánt zóna-objektum.</span><span class="sxs-lookup"><span data-stu-id="e5591-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5591-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5591-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5591-131">Annak a csoportnak a neve, amely a frissítendő zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e5591-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="e5591-132">Meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="e5591-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="e5591-133">Azt is megteheti, hogy megadhatja a magánjellegű DNS-zónát egy **dnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="e5591-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5591-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5591-134">-ResourceId</span></span>
<span data-ttu-id="e5591-135">Privát DNS-zóna ResourceID.</span><span class="sxs-lookup"><span data-stu-id="e5591-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5591-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="e5591-136">-Tag</span></span>
<span data-ttu-id="e5591-137">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="e5591-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5591-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5591-138">-Confirm</span></span>
<span data-ttu-id="e5591-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5591-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5591-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5591-140">-WhatIf</span></span>
<span data-ttu-id="e5591-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5591-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5591-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5591-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5591-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5591-143">CommonParameters</span></span>
<span data-ttu-id="e5591-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5591-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5591-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5591-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5591-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5591-146">INPUTS</span></span>

### <span data-ttu-id="e5591-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e5591-147">System.String</span></span>

### <span data-ttu-id="e5591-148">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5591-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="e5591-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5591-149">OUTPUTS</span></span>

### <span data-ttu-id="e5591-150">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5591-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="e5591-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5591-151">NOTES</span></span>

## <span data-ttu-id="e5591-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5591-152">RELATED LINKS</span></span>

[<span data-ttu-id="e5591-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5591-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="e5591-154">Új – AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5591-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="e5591-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5591-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
