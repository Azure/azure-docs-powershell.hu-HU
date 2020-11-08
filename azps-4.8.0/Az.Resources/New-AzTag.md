---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180964"
---
# <span data-ttu-id="d838a-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="d838a-101">New-AzTag</span></span>

## <span data-ttu-id="d838a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d838a-102">SYNOPSIS</span></span>
<span data-ttu-id="d838a-103">Előre definiált Azure címkét hoz létre, vagy hozzáadott értékeket egy meglévő címkéhez | A teljes címkéket létrehoz vagy frissít egy erőforrásban vagy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d838a-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d838a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d838a-104">SYNTAX</span></span>

### <span data-ttu-id="d838a-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="d838a-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d838a-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d838a-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="d838a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d838a-107">DESCRIPTION</span></span>

<span data-ttu-id="d838a-108">**CreatePredefinedTagSet** : a **New-AzTag** parancsmag egy előre definiált, előre meghatározott értéket tartalmazó, előre meghatározott Azure-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d838a-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="d838a-109">Azt is megteheti, hogy további értékeket is felvehet a meglévő előre definiált címkékbe.</span><span class="sxs-lookup"><span data-stu-id="d838a-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="d838a-110">Ha előre definiált címkét szeretne létrehozni, adjon meg egy egyedi címkét.</span><span class="sxs-lookup"><span data-stu-id="d838a-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="d838a-111">Ha egy meglévő előre definiált címkéhez szeretne értéket hozzáadni, adja meg a meglévő címke nevét és az új értéket.</span><span class="sxs-lookup"><span data-stu-id="d838a-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="d838a-112">Ez a parancsmag egy olyan objektumot ad eredményül, amely az új vagy módosított címkét tartalmazza az értékekkel és a hozzájuk rendelt erőforrások számával.</span><span class="sxs-lookup"><span data-stu-id="d838a-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="d838a-113">Az Azure címkék modul, amely a **New-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="d838a-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="d838a-114">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="d838a-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="d838a-115">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="d838a-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="d838a-116">Ha előre definiált címkét szeretne alkalmazni egy erőforrásra vagy erőforrás-csoportra, használja az New-AzTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="d838a-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="d838a-117">Ha a megadott címke nevével vagy névvel és értékkel rendelkező erőforráscsoportokat szeretne keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="d838a-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d838a-118">Minden címkéhez tartozik egy név.</span><span class="sxs-lookup"><span data-stu-id="d838a-118">Every tag has a name.</span></span>
<span data-ttu-id="d838a-119">Az értékek nem kötelezők.</span><span class="sxs-lookup"><span data-stu-id="d838a-119">The values are optional.</span></span>
<span data-ttu-id="d838a-120">Az előre definiált Azure-címkék több értéket is tartalmazhatnak, de ha a címkét erőforrás-vagy erőforrás-csoportra alkalmazza, akkor a címke nevét és csak egy értékét kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="d838a-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="d838a-121">Létrehozhat például egy előre definiált részleg címkét, amely egy értékkel rendelkezik az egyes részlegekhez, például a pénzügyi, az emberi erőforrások és az IT-részleghez.</span><span class="sxs-lookup"><span data-stu-id="d838a-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="d838a-122">Amikor az osztály címkét egy erőforrásra alkalmazza, csak egy előre meghatározott értéket (például pénzügy) kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="d838a-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="d838a-123">**CreateByResourceIdParameterSet** : a **New-AzTag** parancsmag egy **ResourceId** létrehoz vagy frissít egy erőforrás vagy előfizetés teljes címkéket.</span><span class="sxs-lookup"><span data-stu-id="d838a-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="d838a-124">Ez a művelet lehetővé teszi a megadott erőforrás vagy előfizetés teljes csoportjának hozzáadását vagy cseréjét.</span><span class="sxs-lookup"><span data-stu-id="d838a-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="d838a-125">A megadott entitásnak legfeljebb 50 címkéje lehet.</span><span class="sxs-lookup"><span data-stu-id="d838a-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="d838a-126">Példák</span><span class="sxs-lookup"><span data-stu-id="d838a-126">EXAMPLES</span></span>

### <span data-ttu-id="d838a-127">Példa 1: előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="d838a-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="d838a-128">Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="d838a-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="d838a-129">Ebben a címkében nincs érték.</span><span class="sxs-lookup"><span data-stu-id="d838a-129">This tag has no values.</span></span>
<span data-ttu-id="d838a-130">Egy erőforrás vagy erőforráscsoport értékeit nem tartalmazó címkét alkalmazhat, illetve a **New-AzTag** segítségével értékeket adhat a címkéhez.</span><span class="sxs-lookup"><span data-stu-id="d838a-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="d838a-131">Ha a címkét az erőforrás vagy az erőforrás csoportra alkalmazza, akkor megadhat egy értéket is.</span><span class="sxs-lookup"><span data-stu-id="d838a-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="d838a-132">2. példa: egy értékkel rendelkező előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="d838a-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="d838a-133">A parancs a Pénzügy nevű osztály nevű előre definiált címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d838a-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="d838a-134">3. példa: érték hozzáadása egy előre definiált címkéhez</span><span class="sxs-lookup"><span data-stu-id="d838a-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="d838a-135">Ezek a parancsok két értékkel rendelkező részleg nevű előre definiált címkét hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="d838a-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="d838a-136">Ha létezik a címke neve, a **New-AzTag** hozzáadja az értéket a meglévő címkéhez, nem pedig új létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="d838a-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="d838a-137">4. példa: előre definiált címke használata</span><span class="sxs-lookup"><span data-stu-id="d838a-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="d838a-138">Az ebben a példában szereplő parancsok az előre definiált címke létrehozása és használata.</span><span class="sxs-lookup"><span data-stu-id="d838a-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="d838a-139">Példa 5: az előfizetéshez tartozó címkék teljes készletének létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="d838a-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="d838a-140">Ezzel a paranccsal létrehozhatja vagy frissítheti az előfizetéshez tartozó teljes címkéket {subId}.</span><span class="sxs-lookup"><span data-stu-id="d838a-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="d838a-141">6. példa: az erőforrásokban a teljes címkéket hozza létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="d838a-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="d838a-142">Ezzel a paranccsal létrehozhatja vagy frissítheti az erőforrás teljes csoportját {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="d838a-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="d838a-143">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d838a-143">PARAMETERS</span></span>

### <span data-ttu-id="d838a-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d838a-144">-DefaultProfile</span></span>
<span data-ttu-id="d838a-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d838a-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d838a-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d838a-146">-Name</span></span>
<span data-ttu-id="d838a-147">Az előre definiált címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d838a-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="d838a-148">Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="d838a-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="d838a-149">Ha egy meglévő címkéhez értéket szeretne hozzáadni, írja be a meglévő címke nevét.</span><span class="sxs-lookup"><span data-stu-id="d838a-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="d838a-150">Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzTag** hozzáadja az adott nevet tartalmazó címkét az új címke létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="d838a-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="d838a-151">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="d838a-151">-Value</span></span>
<span data-ttu-id="d838a-152">Az előre definiált címke értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d838a-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="d838a-153">Az előre definiált címkék több értéket is tartalmazhatnak, de mindegyik parancsban csak egy érték adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="d838a-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="d838a-154">Ez a paraméter nem kötelező, mert a címkék értékek nélküli neveket is tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="d838a-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="d838a-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d838a-155">-ResourceId</span></span>
<span data-ttu-id="d838a-156">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d838a-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="d838a-157">Lehet, hogy egy erőforrás, egy erőforráscsoport vagy egy előfizetés címkézve van.</span><span class="sxs-lookup"><span data-stu-id="d838a-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="d838a-158">-Címke</span><span class="sxs-lookup"><span data-stu-id="d838a-158">-Tag</span></span>
<span data-ttu-id="d838a-159">Az erőforrásra helyezett címkék.</span><span class="sxs-lookup"><span data-stu-id="d838a-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="d838a-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d838a-160">-Confirm</span></span>
<span data-ttu-id="d838a-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d838a-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d838a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d838a-162">-WhatIf</span></span>
<span data-ttu-id="d838a-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d838a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d838a-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d838a-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d838a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d838a-165">CommonParameters</span></span>
<span data-ttu-id="d838a-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d838a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d838a-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d838a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d838a-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d838a-168">INPUTS</span></span>

### <span data-ttu-id="d838a-169">System. String</span><span class="sxs-lookup"><span data-stu-id="d838a-169">System.String</span></span>

### <span data-ttu-id="d838a-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d838a-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d838a-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d838a-171">OUTPUTS</span></span>

### <span data-ttu-id="d838a-172">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag | Microsoft. Azure. Command. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="d838a-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="d838a-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d838a-173">NOTES</span></span>

## <span data-ttu-id="d838a-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d838a-174">RELATED LINKS</span></span>

[<span data-ttu-id="d838a-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="d838a-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="d838a-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="d838a-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="d838a-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="d838a-177">Update-AzTag</span></span>](./Update-AzTag.md)
