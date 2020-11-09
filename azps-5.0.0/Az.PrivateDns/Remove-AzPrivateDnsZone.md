---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303407"
---
# <span data-ttu-id="067eb-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="067eb-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="067eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="067eb-102">SYNOPSIS</span></span>
<span data-ttu-id="067eb-103">Eltávolít egy privát DNS-zónát egy erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="067eb-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="067eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="067eb-104">SYNTAX</span></span>

### <span data-ttu-id="067eb-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="067eb-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="067eb-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="067eb-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="067eb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="067eb-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="067eb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="067eb-108">DESCRIPTION</span></span>
<span data-ttu-id="067eb-109">A **Remove-AzPrivateDnsZone** parancsmag véglegesen törli a privát tartománynévrendszer (DNS) zónát egy adott erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="067eb-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="067eb-110">A zónában található összes rekord is törlődik.</span><span class="sxs-lookup"><span data-stu-id="067eb-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="067eb-111">A **PrivateDnsZone** -objektumokat a *PrivateZone* paraméterrel vagy a csővezeték-kezelő használatával is átadhatja, vagy megadhatja a *nevet* és a *ResourceGroupName* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="067eb-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="067eb-112">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="067eb-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="067eb-113">Ha a zónát egy **PrivateDnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **PrivateDnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="067eb-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="067eb-114">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="067eb-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="067eb-115">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="067eb-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="067eb-116">Példák</span><span class="sxs-lookup"><span data-stu-id="067eb-116">EXAMPLES</span></span>

### <span data-ttu-id="067eb-117">1. példa: privát zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="067eb-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="067eb-118">Ez a parancs eltávolítja a myzone.com nevű zónát a MyResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="067eb-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="067eb-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="067eb-119">PARAMETERS</span></span>

### <span data-ttu-id="067eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067eb-120">-DefaultProfile</span></span>
<span data-ttu-id="067eb-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="067eb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="067eb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="067eb-122">-Name</span></span>
<span data-ttu-id="067eb-123">A parancsmag által eltávolított magánhálózati DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="067eb-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="067eb-124">Meg kell adnia a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="067eb-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="067eb-125">Azt is megteheti, hogy a *zóna* paraméterrel megadhatja a DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="067eb-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="067eb-126">-Átír</span><span class="sxs-lookup"><span data-stu-id="067eb-126">-Overwrite</span></span>
<span data-ttu-id="067eb-127">Ha a zónát egy **PrivateDnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **PrivateDnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="067eb-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="067eb-128">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="067eb-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="067eb-129">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="067eb-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="067eb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="067eb-130">-PassThru</span></span>
<span data-ttu-id="067eb-131">A művelet eredményének (logikai) megadására szolgál a saját zóna további törlése a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="067eb-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="067eb-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="067eb-132">-PrivateZone</span></span>
<span data-ttu-id="067eb-133">A törölni kívánt személyes zóna-objektum.</span><span class="sxs-lookup"><span data-stu-id="067eb-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="067eb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="067eb-134">-ResourceGroupName</span></span>
<span data-ttu-id="067eb-135">Az eltávolítandó zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="067eb-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="067eb-136">Meg kell adnia a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="067eb-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="067eb-137">Azt is megteheti, hogy megadhatja a DNS-zónát egy **PrivateDnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="067eb-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="067eb-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="067eb-138">-ResourceId</span></span>
<span data-ttu-id="067eb-139">Privát DNS-zóna ResourceID.</span><span class="sxs-lookup"><span data-stu-id="067eb-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="067eb-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="067eb-140">-Confirm</span></span>
<span data-ttu-id="067eb-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="067eb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="067eb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="067eb-142">-WhatIf</span></span>
<span data-ttu-id="067eb-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="067eb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="067eb-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="067eb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="067eb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067eb-145">CommonParameters</span></span>
<span data-ttu-id="067eb-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="067eb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067eb-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="067eb-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067eb-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="067eb-148">INPUTS</span></span>

### <span data-ttu-id="067eb-149">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="067eb-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="067eb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="067eb-150">System.String</span></span>

## <span data-ttu-id="067eb-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="067eb-151">OUTPUTS</span></span>

### <span data-ttu-id="067eb-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="067eb-152">System.Boolean</span></span>

## <span data-ttu-id="067eb-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="067eb-153">NOTES</span></span>

## <span data-ttu-id="067eb-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="067eb-154">RELATED LINKS</span></span>

[<span data-ttu-id="067eb-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="067eb-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="067eb-156">Új – AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="067eb-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="067eb-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="067eb-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
