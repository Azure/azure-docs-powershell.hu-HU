---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470013"
---
# <span data-ttu-id="747a9-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="747a9-101">Remove-AzTag</span></span>

## <span data-ttu-id="747a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="747a9-102">SYNOPSIS</span></span>
<span data-ttu-id="747a9-103">Előre definiált Azure-címkék vagy -értékek törlése | Törli egy erőforrás vagy előfizetés címkéinek teljes készletét.</span><span class="sxs-lookup"><span data-stu-id="747a9-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="747a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="747a9-104">SYNTAX</span></span>

### <span data-ttu-id="747a9-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="747a9-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747a9-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="747a9-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="747a9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="747a9-107">DESCRIPTION</span></span>

<span data-ttu-id="747a9-108">**RemovePredefinedTagSet:** A **Remove-AzTag** parancsmag törli az előre definiált Azure-címkéket és -értékeket az előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="747a9-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="747a9-109">Ha törölni szeretne bizonyos értékeket egy előre definiált címkéből, használja az *Érték paramétert.*</span><span class="sxs-lookup"><span data-stu-id="747a9-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="747a9-110">Alapértelmezés szerint **a Remove-AzTag** törli a megadott címkét és annak összes értékét. Az erőforrás- vagy erőforráscsoportokra jelenleg alkalmazott címkék és értékek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="747a9-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="747a9-111">A **Remove-AzTag** parancsmag  használata előtt a Set-AzResourceGroup parancsmag Címke paraméterével törölje a címkét vagy értékeket az erőforrás- vagy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="747a9-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="747a9-112">Az Azure Tags modul, amely a **Remove-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="747a9-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="747a9-113">Az Azure-címkék olyan névérték-párok, amelyek segítségével kategorizálhatja azure-erőforrásait és erőforráscsoportját, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokra és csoportokra vonatkozó megjegyzéseket vagy megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="747a9-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="747a9-114">Egyetlen lépésben definiálhat és alkalmazhat címkéket, az előre definiált címkékkel azonban szabványos, egységes, kiszámítható neveket és értékeket határozhat meg az előfizetésében szereplő címkékhez.</span><span class="sxs-lookup"><span data-stu-id="747a9-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="747a9-115">**RemoveByResourceIdParameterSet:** A **Remove-AzTag** parancsmag egy **ResourceId** értékkel törli egy erőforrás vagy előfizetés címkéinek teljes készletét.</span><span class="sxs-lookup"><span data-stu-id="747a9-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="747a9-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="747a9-116">EXAMPLES</span></span>

### <span data-ttu-id="747a9-117">1. példa: Előre definiált címke törlése</span><span class="sxs-lookup"><span data-stu-id="747a9-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="747a9-118">Ez a parancs törli a Department (Részleg) nevű előre definiált címkét és annak összes értékét.</span><span class="sxs-lookup"><span data-stu-id="747a9-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="747a9-119">Ha a címkét bármely erőforrásra vagy erőforráscsoportra alkalmazta, a parancs nem fog sikerülni.</span><span class="sxs-lookup"><span data-stu-id="747a9-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="747a9-120">2. példa: Érték törlése egy előre definiált címkéből</span><span class="sxs-lookup"><span data-stu-id="747a9-120">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="747a9-121">Ez a parancs törli a HumanResources értéket az előre definiált Department címkéből.</span><span class="sxs-lookup"><span data-stu-id="747a9-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="747a9-122">Nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="747a9-122">It does not delete the tag.</span></span>
<span data-ttu-id="747a9-123">Ha az értéket valamelyik erőforrásra vagy erőforráscsoportra alkalmazta, a parancs nem fog sikerülni.</span><span class="sxs-lookup"><span data-stu-id="747a9-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="747a9-124">3. példa: Az előfizetés teljes címkéinek törlése</span><span class="sxs-lookup"><span data-stu-id="747a9-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="747a9-125">Ez a parancs törli az előfizetés összes címkéét a(z) {subId} azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="747a9-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="747a9-126">Nem fogja visszaadni a törölt objektumot, ha nem adja át a "-PassThru" adatokat.</span><span class="sxs-lookup"><span data-stu-id="747a9-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="747a9-127">4. példa: Az erőforrás teljes címkéinek törlése</span><span class="sxs-lookup"><span data-stu-id="747a9-127">Example 4: Deletes the entire set of tags on a resource</span></span>

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

<span data-ttu-id="747a9-128">Ezzel a paranccsal az erőforrás összes címkéje törölhető a következővel: {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="747a9-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="747a9-129">Visszaadja a töröltectect értéket, amikor a "-PassThru" értéket adja át.</span><span class="sxs-lookup"><span data-stu-id="747a9-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="747a9-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="747a9-130">PARAMETERS</span></span>

### <span data-ttu-id="747a9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747a9-131">-DefaultProfile</span></span>
<span data-ttu-id="747a9-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="747a9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="747a9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="747a9-133">-Name</span></span>
<span data-ttu-id="747a9-134">Az eltávolítandó előre definiált címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="747a9-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="747a9-135">Alapértelmezés szerint **a Remove-AzTag** eltávolítja a megadott címkét és annak összes értékét.</span><span class="sxs-lookup"><span data-stu-id="747a9-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="747a9-136">Ha törölni szeretné a kijelölt értékeket, de a címkét nem, használja az *Érték paramétert.*</span><span class="sxs-lookup"><span data-stu-id="747a9-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="747a9-137">-Érték</span><span class="sxs-lookup"><span data-stu-id="747a9-137">-Value</span></span>
<span data-ttu-id="747a9-138">Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="747a9-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="747a9-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="747a9-139">-ResourceId</span></span>
<span data-ttu-id="747a9-140">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="747a9-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="747a9-141">Előfordulhat, hogy egy erőforrás, erőforráscsoport vagy előfizetés meg van címkézve.</span><span class="sxs-lookup"><span data-stu-id="747a9-141">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="747a9-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="747a9-142">-PassThru</span></span>
<span data-ttu-id="747a9-143">Visszaad egy objektumot, amely a törölt címkét vagy a törölt értékkel létrehozott címkét jelöli.</span><span class="sxs-lookup"><span data-stu-id="747a9-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="747a9-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="747a9-144">-Confirm</span></span>
<span data-ttu-id="747a9-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="747a9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="747a9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="747a9-146">-WhatIf</span></span>
<span data-ttu-id="747a9-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="747a9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="747a9-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="747a9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="747a9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747a9-149">CommonParameters</span></span>
<span data-ttu-id="747a9-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747a9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747a9-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="747a9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747a9-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="747a9-152">INPUTS</span></span>

### <span data-ttu-id="747a9-153">System.String</span><span class="sxs-lookup"><span data-stu-id="747a9-153">System.String</span></span>

### <span data-ttu-id="747a9-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="747a9-154">System.String[]</span></span>

### <span data-ttu-id="747a9-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="747a9-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="747a9-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="747a9-156">OUTPUTS</span></span>

### <span data-ttu-id="747a9-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="747a9-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="747a9-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="747a9-158">NOTES</span></span>

## <span data-ttu-id="747a9-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="747a9-159">RELATED LINKS</span></span>

[<span data-ttu-id="747a9-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="747a9-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="747a9-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="747a9-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="747a9-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="747a9-162">Update-AzTag</span></span>](./Update-AzTag.md)