---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466434"
---
# <span data-ttu-id="53097-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="53097-101">New-AzTag</span></span>

## <span data-ttu-id="53097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53097-102">SYNOPSIS</span></span>
<span data-ttu-id="53097-103">Előre definiált Azure-címkét hoz létre, vagy értékeket ad hozzá egy meglévő címkéhez | Létrehozza vagy frissíti a címkék teljes készletét egy erőforráson vagy előfizetésen.</span><span class="sxs-lookup"><span data-stu-id="53097-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="53097-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53097-104">SYNTAX</span></span>

### <span data-ttu-id="53097-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="53097-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53097-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53097-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="53097-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53097-107">DESCRIPTION</span></span>

<span data-ttu-id="53097-108">**CreatePredefinedTagSet:** A **New-AzTag** parancsmag létrehoz egy előre definiált Azure-címkét egy opcionális előre definiált értékkel.</span><span class="sxs-lookup"><span data-stu-id="53097-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="53097-109">Emellett további értékeket is hozzáadhat a meglévő előre definiált címkékhez.</span><span class="sxs-lookup"><span data-stu-id="53097-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="53097-110">Előre definiált címke létrehozásához adjon meg egy egyedi címkenevet.</span><span class="sxs-lookup"><span data-stu-id="53097-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="53097-111">Ha egy meglévő előre definiált címkéhez szeretne értéket adni, adja meg a meglévő címke nevét és az új értéket.</span><span class="sxs-lookup"><span data-stu-id="53097-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="53097-112">Ez a parancsmag egy objektumot ad vissza, amely az új vagy módosított címkét adja vissza az értékeivel és az erőforrások számával együtt.</span><span class="sxs-lookup"><span data-stu-id="53097-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="53097-113">Az Azure Címkék modul, amely részét képezi a **New-AzTag,** segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="53097-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="53097-114">Az Azure-címkék olyan névérték-párok, amelyek segítségével kategorizálhatja azure-erőforrásait és erőforráscsoportját, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokra és csoportokra vonatkozó megjegyzéseket vagy megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="53097-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="53097-115">Egyetlen lépésben definiálhat és alkalmazhat címkéket, az előre definiált címkékkel azonban szabványos, egységes, kiszámítható neveket és értékeket határozhat meg az előfizetésében szereplő címkékhez.</span><span class="sxs-lookup"><span data-stu-id="53097-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="53097-116">Ha előre definiált címkét szeretne alkalmazni egy  erőforrásra vagy erőforráscsoportra, használja a New-AzTag címke paraméterét.</span><span class="sxs-lookup"><span data-stu-id="53097-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="53097-117">Ha egy megadott címkenévvel vagy névvel és  értékkel megadott erőforráscsoportokat keres, használja a Get-AzResourceGroup parancsmag címke paraméterét.</span><span class="sxs-lookup"><span data-stu-id="53097-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="53097-118">Minden címkének van neve.</span><span class="sxs-lookup"><span data-stu-id="53097-118">Every tag has a name.</span></span>
<span data-ttu-id="53097-119">Az értékek megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="53097-119">The values are optional.</span></span>
<span data-ttu-id="53097-120">Az előre definiált Azure-címkéknek több értékük is lehet, de amikor a címkét egy erőforrásra vagy erőforráscsoportra alkalmazza, a címke nevét és csak az egyik értékét alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="53097-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="53097-121">Létrehozhat például egy előre definiált Részleg címkét, amely minden részleghez egy-egy értéket (például Pénzügy, Emberi erőforrások és It-részleg) igényel.</span><span class="sxs-lookup"><span data-stu-id="53097-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="53097-122">Amikor a Department címkét egy erőforrásra alkalmazza, csak egy előre definiált értéket (például Pénzügy) alkalmaz.</span><span class="sxs-lookup"><span data-stu-id="53097-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="53097-123">**CreateByResourceIdParameterSet:** A **ResourceId** azonosítóval létrehozott **New-AzTag** parancsmag létrehozza vagy frissíti egy erőforrás vagy előfizetés címkéinek teljes készletét.</span><span class="sxs-lookup"><span data-stu-id="53097-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="53097-124">Ez a művelet lehetővé teszi a címkék teljes készletének hozzáadását vagy cseréjét a megadott erőforráson vagy előfizetésen.</span><span class="sxs-lookup"><span data-stu-id="53097-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="53097-125">A megadott entitás legfeljebb 50 címkével lehet.</span><span class="sxs-lookup"><span data-stu-id="53097-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="53097-126">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53097-126">EXAMPLES</span></span>

### <span data-ttu-id="53097-127">1. példa: Előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="53097-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="53097-128">Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="53097-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="53097-129">Ez a címke nem tartalmaz értékeket.</span><span class="sxs-lookup"><span data-stu-id="53097-129">This tag has no values.</span></span>
<span data-ttu-id="53097-130">Az erőforrás- vagy erőforráscsoportokra érték nélkül is alkalmazhat értékeket, illetve a **New-AzTag** segítségével is hozzáadhat értékeket a címkéhez.</span><span class="sxs-lookup"><span data-stu-id="53097-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="53097-131">A címkének az erőforrásra vagy erőforráscsoportra való alkalmazásakor is megadhat egy értéket.</span><span class="sxs-lookup"><span data-stu-id="53097-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="53097-132">2. példa: Előre definiált címke létrehozása értékkel</span><span class="sxs-lookup"><span data-stu-id="53097-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="53097-133">Ez a parancs létrehoz egy Részleg nevű előre definiált címkét pénzügyi értékkel.</span><span class="sxs-lookup"><span data-stu-id="53097-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="53097-134">3. példa: Érték hozzáadása előre definiált címkéhez</span><span class="sxs-lookup"><span data-stu-id="53097-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="53097-135">Ezek a parancsok egy Előre definiált Részleg nevű címkét hoznak létre két értékkel.</span><span class="sxs-lookup"><span data-stu-id="53097-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="53097-136">Ha a címke neve létezik, a **New-AzTag** új címke létrehozása helyett hozzáadja az értéket a meglévő címkéhez.</span><span class="sxs-lookup"><span data-stu-id="53097-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="53097-137">4. példa: Előre definiált címke használata</span><span class="sxs-lookup"><span data-stu-id="53097-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="53097-138">A példában a parancsok előre definiált címkét hoznak létre és használnak.</span><span class="sxs-lookup"><span data-stu-id="53097-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="53097-139">5. példa: Az előfizetés teljes címkéinek beállítása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="53097-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="53097-140">Ez a parancs létrehozza vagy frissíti az előfizetésben található címkék teljes készletét a(z) {subId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="53097-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="53097-141">6. példa: Létrehozza vagy frissíti egy erőforrás teljes címkéit</span><span class="sxs-lookup"><span data-stu-id="53097-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="53097-142">Ez a parancs létrehozza vagy frissíti az erőforrás teljes címkéit a(z) {resourceId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="53097-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="53097-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53097-143">PARAMETERS</span></span>

### <span data-ttu-id="53097-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53097-144">-DefaultProfile</span></span>
<span data-ttu-id="53097-145">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53097-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53097-146">-Name</span><span class="sxs-lookup"><span data-stu-id="53097-146">-Name</span></span>
<span data-ttu-id="53097-147">Az előre definiált címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53097-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="53097-148">Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="53097-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="53097-149">Ha egy meglévő címkéhez szeretne értéket adni, írja be a meglévő címke nevét.</span><span class="sxs-lookup"><span data-stu-id="53097-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="53097-150">Ha egy meglévő előre definiált címkének van a megadott neve, a **New-AzTag** új címke létrehozása helyett hozzáadja a megadott értéket (ha van ilyen) a címkéhez.</span><span class="sxs-lookup"><span data-stu-id="53097-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53097-151">-Érték</span><span class="sxs-lookup"><span data-stu-id="53097-151">-Value</span></span>
<span data-ttu-id="53097-152">Egy előre definiált címkeértéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="53097-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="53097-153">Az előre definiált címkéknek több értékük is lehet, de minden parancsban csak egy értéket lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="53097-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="53097-154">Ez a paraméter nem kötelező, mivel a címkéknek érték nélküli neve is lehet.</span><span class="sxs-lookup"><span data-stu-id="53097-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53097-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53097-155">-ResourceId</span></span>
<span data-ttu-id="53097-156">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53097-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="53097-157">Előfordulhat, hogy egy erőforrás, erőforráscsoport vagy előfizetés meg van címkézve.</span><span class="sxs-lookup"><span data-stu-id="53097-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53097-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="53097-158">-Tag</span></span>
<span data-ttu-id="53097-159">Az erőforrásra vonatkozó címkék.</span><span class="sxs-lookup"><span data-stu-id="53097-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53097-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53097-160">-Confirm</span></span>
<span data-ttu-id="53097-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53097-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53097-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53097-162">-WhatIf</span></span>
<span data-ttu-id="53097-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53097-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53097-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53097-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53097-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53097-165">CommonParameters</span></span>
<span data-ttu-id="53097-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53097-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53097-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53097-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53097-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53097-168">INPUTS</span></span>

### <span data-ttu-id="53097-169">System.String</span><span class="sxs-lookup"><span data-stu-id="53097-169">System.String</span></span>

### <span data-ttu-id="53097-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53097-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53097-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53097-171">OUTPUTS</span></span>

### <span data-ttu-id="53097-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="53097-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="53097-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53097-173">NOTES</span></span>

## <span data-ttu-id="53097-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53097-174">RELATED LINKS</span></span>

[<span data-ttu-id="53097-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="53097-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="53097-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="53097-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="53097-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="53097-177">Update-AzTag</span></span>](./Update-AzTag.md)