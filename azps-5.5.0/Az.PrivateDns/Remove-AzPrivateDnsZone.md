---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160331"
---
# <span data-ttu-id="38932-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="38932-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="38932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38932-102">SYNOPSIS</span></span>
<span data-ttu-id="38932-103">Eltávolít egy privát DNS-zónát egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="38932-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="38932-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38932-104">SYNTAX</span></span>

### <span data-ttu-id="38932-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38932-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38932-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="38932-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38932-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38932-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38932-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38932-108">DESCRIPTION</span></span>
<span data-ttu-id="38932-109">Az **Remove-AzPrivateDnsZone** parancsmag véglegesen töröl egy privát DNS-zónát egy adott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="38932-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="38932-110">A zónában található összes rekordkészlet is törlődik.</span><span class="sxs-lookup"><span data-stu-id="38932-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="38932-111">A **PrivateDnsZone-objektumokat** a *PrivateZone* paraméterrel vagy a folyamat műveleti jelével, illetve a *Name* and *ResourceGroupName* paraméter megadásával is átadhatja.</span><span class="sxs-lookup"><span data-stu-id="38932-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="38932-112">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="38932-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="38932-113">Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **PrivateDnsZone** objektum beolvasása óta (csak a DNS-zóna erőforrásszámán végrehajtott műveletek száma változásként, a rekordkészletek műveletei a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="38932-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="38932-114">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="38932-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="38932-115">Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="38932-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="38932-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38932-116">EXAMPLES</span></span>

### <span data-ttu-id="38932-117">1. példa: Privát zóna eltávolítása</span><span class="sxs-lookup"><span data-stu-id="38932-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="38932-118">Ez a parancs eltávolítja a myzone.com myResourceGroup nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="38932-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="38932-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38932-119">PARAMETERS</span></span>

### <span data-ttu-id="38932-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38932-120">-DefaultProfile</span></span>
<span data-ttu-id="38932-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38932-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38932-122">-Name</span><span class="sxs-lookup"><span data-stu-id="38932-122">-Name</span></span>
<span data-ttu-id="38932-123">A parancsmag által eltávolított privát DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="38932-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="38932-124">Az *ResourceGroupName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="38932-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="38932-125">Másik lehetőségként megadhatja a DNS-zónát a *Zone paraméter* használatával.</span><span class="sxs-lookup"><span data-stu-id="38932-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="38932-126">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="38932-126">-Overwrite</span></span>
<span data-ttu-id="38932-127">Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **PrivateDnsZone** objektum beolvasása óta (csak a DNS-zóna erőforrásszámán végrehajtott műveletek száma változásként, a rekordkészletek műveletei a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="38932-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="38932-128">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="38932-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="38932-129">Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="38932-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="38932-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38932-130">-PassThru</span></span>
<span data-ttu-id="38932-131">A művelet eredményének (logikai) a folyamaton belül távolabbi privát zóna törlésére használható.</span><span class="sxs-lookup"><span data-stu-id="38932-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="38932-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="38932-132">-PrivateZone</span></span>
<span data-ttu-id="38932-133">A törölni kívánt privát zónaobjektum.</span><span class="sxs-lookup"><span data-stu-id="38932-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="38932-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38932-134">-ResourceGroupName</span></span>
<span data-ttu-id="38932-135">Az eltávolítható zónát tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38932-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="38932-136">A *ZoneName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="38932-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="38932-137">Másik lehetőségként megadhatja a DNS-zóna értékét egy **PrivateDnsZone** objektummal, amely vagy a folyamaton, vagy a Zone paraméteren keresztül *továbbítható.*</span><span class="sxs-lookup"><span data-stu-id="38932-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="38932-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38932-138">-ResourceId</span></span>
<span data-ttu-id="38932-139">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="38932-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="38932-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38932-140">-Confirm</span></span>
<span data-ttu-id="38932-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="38932-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38932-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38932-142">-WhatIf</span></span>
<span data-ttu-id="38932-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="38932-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38932-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38932-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38932-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38932-145">CommonParameters</span></span>
<span data-ttu-id="38932-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38932-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38932-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38932-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38932-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38932-148">INPUTS</span></span>

### <span data-ttu-id="38932-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="38932-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="38932-150">System.String</span><span class="sxs-lookup"><span data-stu-id="38932-150">System.String</span></span>

## <span data-ttu-id="38932-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38932-151">OUTPUTS</span></span>

### <span data-ttu-id="38932-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38932-152">System.Boolean</span></span>

## <span data-ttu-id="38932-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38932-153">NOTES</span></span>

## <span data-ttu-id="38932-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38932-154">RELATED LINKS</span></span>

[<span data-ttu-id="38932-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="38932-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="38932-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="38932-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="38932-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="38932-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
