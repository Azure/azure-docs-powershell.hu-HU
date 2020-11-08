---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195532"
---
# <span data-ttu-id="192c8-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="192c8-101">Remove-AzTag</span></span>

## <span data-ttu-id="192c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="192c8-102">SYNOPSIS</span></span>
<span data-ttu-id="192c8-103">Előre definiált Azure-címkék vagy-értékek törlése | A teljes címkék törlése egy erőforrásra vagy előfizetésre</span><span class="sxs-lookup"><span data-stu-id="192c8-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="192c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="192c8-104">SYNTAX</span></span>

### <span data-ttu-id="192c8-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="192c8-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c8-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="192c8-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="192c8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="192c8-107">DESCRIPTION</span></span>

<span data-ttu-id="192c8-108">**RemovePredefinedTagSet** : a **Remove-AzTag** parancsmag előre definiált Azure-címkéket és-értékeket töröl az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="192c8-108">**RemovePredefinedTagSet** : The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="192c8-109">Ha egy előre definiált címkéből szeretne bizonyos értékeket törölni, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="192c8-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="192c8-110">A **Remove-AzTag** alapértelmezés szerint törli a megadott címkét és annak minden értékét. Az erőforrásokra vagy erőforrásokra jelenleg alkalmazott címke vagy érték nem törölhető.</span><span class="sxs-lookup"><span data-stu-id="192c8-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="192c8-111">Mielőtt a **Remove-AzTag** használja, az Set-AzResourceGroup parancsmag *címke* paraméterével törölheti az erőforrás vagy az erőforrás csoport címkéjét vagy értékét.</span><span class="sxs-lookup"><span data-stu-id="192c8-111">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="192c8-112">Az Azure címkék modul, amely **eltávolítja a-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="192c8-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="192c8-113">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="192c8-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="192c8-114">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="192c8-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="192c8-115">**RemoveByResourceIdParameterSet** : a **Remove-AzTag** parancsmag egy **ResourceId** törli a teljes címkéket egy erőforrásban vagy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="192c8-115">**RemoveByResourceIdParameterSet** : The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="192c8-116">Példák</span><span class="sxs-lookup"><span data-stu-id="192c8-116">EXAMPLES</span></span>

### <span data-ttu-id="192c8-117">Példa 1: előre definiált címke törlése</span><span class="sxs-lookup"><span data-stu-id="192c8-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="192c8-118">Ez a parancs törli a részleg és annak összes értékének előre definiált címkéjét.</span><span class="sxs-lookup"><span data-stu-id="192c8-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="192c8-119">Ha a címkét erőforrásokra vagy erőforrás-csoportokra alkalmazta, akkor a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="192c8-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="192c8-120">2. példa: az előre definiált címke értékének törlése</span><span class="sxs-lookup"><span data-stu-id="192c8-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="192c8-121">Ez a parancs törli az HumanResources értéket az előre definiált részleg címkéből.</span><span class="sxs-lookup"><span data-stu-id="192c8-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="192c8-122">Nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="192c8-122">It does not delete the tag.</span></span>
<span data-ttu-id="192c8-123">Ha az érték minden erőforrásra vagy erőforrás-csoportra érvényes, a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="192c8-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="192c8-124">3. példa: az előfizetéshez tartozó címkék teljes csoportjának törlése</span><span class="sxs-lookup"><span data-stu-id="192c8-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="192c8-125">Ez a parancs törli az előfizetéshez tartozó teljes címkéket {subId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="192c8-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="192c8-126">Ha nem a "-PassThru" lép át, a program nem adja vissza az objektumot.</span><span class="sxs-lookup"><span data-stu-id="192c8-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="192c8-127">4. példa: a teljes címkék törlése egy erőforráson</span><span class="sxs-lookup"><span data-stu-id="192c8-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="192c8-128">Ez a parancs törli az erőforrás teljes csoportját {resourceId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="192c8-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="192c8-129">A törölt ojekt adja eredményül, amikor a "-PassThru" értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="192c8-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="192c8-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="192c8-130">PARAMETERS</span></span>

### <span data-ttu-id="192c8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192c8-131">-DefaultProfile</span></span>
<span data-ttu-id="192c8-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="192c8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="192c8-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="192c8-133">-Name</span></span>
<span data-ttu-id="192c8-134">Az eltávolítandó előre definiált címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="192c8-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="192c8-135">A **Remove-AzTag** alapértelmezés szerint eltávolítja a megadott címkét és annak minden értékét.</span><span class="sxs-lookup"><span data-stu-id="192c8-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="192c8-136">Ha törölni szeretné a kijelölt értékeket, de nem szeretné törölni a címkét, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="192c8-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192c8-137">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="192c8-137">-Value</span></span>
<span data-ttu-id="192c8-138">Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="192c8-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192c8-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="192c8-139">-ResourceId</span></span>
<span data-ttu-id="192c8-140">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="192c8-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="192c8-141">Lehet, hogy egy erőforrás, egy erőforráscsoport vagy egy előfizetés címkézve van.</span><span class="sxs-lookup"><span data-stu-id="192c8-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192c8-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="192c8-142">-PassThru</span></span>
<span data-ttu-id="192c8-143">Egy olyan objektumot ad eredményül, amely a törölt címkét vagy az eredményül kapott címkét jelöli a törölt értékekkel.</span><span class="sxs-lookup"><span data-stu-id="192c8-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192c8-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="192c8-144">-Confirm</span></span>
<span data-ttu-id="192c8-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="192c8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="192c8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="192c8-146">-WhatIf</span></span>
<span data-ttu-id="192c8-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="192c8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="192c8-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="192c8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="192c8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192c8-149">CommonParameters</span></span>
<span data-ttu-id="192c8-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="192c8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192c8-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="192c8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192c8-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="192c8-152">INPUTS</span></span>

### <span data-ttu-id="192c8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="192c8-153">System.String</span></span>

### <span data-ttu-id="192c8-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="192c8-154">System.String[]</span></span>

### <span data-ttu-id="192c8-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="192c8-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="192c8-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="192c8-156">OUTPUTS</span></span>

### <span data-ttu-id="192c8-157">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag | Microsoft. Azure. Command. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="192c8-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="192c8-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="192c8-158">NOTES</span></span>

## <span data-ttu-id="192c8-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="192c8-159">RELATED LINKS</span></span>

[<span data-ttu-id="192c8-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="192c8-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="192c8-161">Új – AzTag</span><span class="sxs-lookup"><span data-stu-id="192c8-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="192c8-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="192c8-162">Update-AzTag</span></span>](./Update-AzTag.md)