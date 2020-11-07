---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845877"
---
# <span data-ttu-id="e76ea-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="e76ea-101">New-AzTag</span></span>

## <span data-ttu-id="e76ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e76ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e76ea-103">Előre definiált Azure címkét hoz létre, vagy hozzáadott értékeket egy meglévő címkéhez | A teljes címkéket létrehoz vagy frissít egy erőforrásban vagy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e76ea-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="e76ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e76ea-104">SYNTAX</span></span>

### <span data-ttu-id="e76ea-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="e76ea-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e76ea-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e76ea-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="e76ea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e76ea-107">DESCRIPTION</span></span>

<span data-ttu-id="e76ea-108">**CreatePredefinedTagSet** : a **New-AzTag** parancsmag egy előre definiált, előre meghatározott értéket tartalmazó, előre meghatározott Azure-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e76ea-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="e76ea-109">Azt is megteheti, hogy további értékeket is felvehet a meglévő előre definiált címkékbe.</span><span class="sxs-lookup"><span data-stu-id="e76ea-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="e76ea-110">Ha előre definiált címkét szeretne létrehozni, adjon meg egy egyedi címkét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="e76ea-111">Ha egy meglévő előre definiált címkéhez szeretne értéket hozzáadni, adja meg a meglévő címke nevét és az új értéket.</span><span class="sxs-lookup"><span data-stu-id="e76ea-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="e76ea-112">Ez a parancsmag egy olyan objektumot ad eredményül, amely az új vagy módosított címkét tartalmazza az értékekkel és a hozzájuk rendelt erőforrások számával.</span><span class="sxs-lookup"><span data-stu-id="e76ea-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="e76ea-113">Az Azure címkék modul, amely a **New-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="e76ea-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="e76ea-114">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="e76ea-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="e76ea-115">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="e76ea-116">Ha előre definiált címkét szeretne alkalmazni egy erőforrásra vagy erőforrás-csoportra, használja az New-AzTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="e76ea-117">Ha a megadott címke nevével vagy névvel és értékkel rendelkező erőforráscsoportokat szeretne keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e76ea-118">Minden címkéhez tartozik egy név.</span><span class="sxs-lookup"><span data-stu-id="e76ea-118">Every tag has a name.</span></span>
<span data-ttu-id="e76ea-119">Az értékek nem kötelezők.</span><span class="sxs-lookup"><span data-stu-id="e76ea-119">The values are optional.</span></span>
<span data-ttu-id="e76ea-120">Az előre definiált Azure-címkék több értéket is tartalmazhatnak, de ha a címkét erőforrás-vagy erőforrás-csoportra alkalmazza, akkor a címke nevét és csak egy értékét kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="e76ea-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="e76ea-121">Létrehozhat például egy előre definiált részleg címkét, amely egy értékkel rendelkezik az egyes részlegekhez, például a pénzügyi, az emberi erőforrások és az IT-részleghez.</span><span class="sxs-lookup"><span data-stu-id="e76ea-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="e76ea-122">Amikor az osztály címkét egy erőforrásra alkalmazza, csak egy előre meghatározott értéket (például pénzügy) kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="e76ea-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="e76ea-123">**CreateByResourceIdParameterSet** : a **New-AzTag** parancsmag egy **ResourceId** létrehoz vagy frissít egy erőforrás vagy előfizetés teljes címkéket.</span><span class="sxs-lookup"><span data-stu-id="e76ea-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="e76ea-124">Ez a művelet lehetővé teszi a megadott erőforrás vagy előfizetés teljes csoportjának hozzáadását vagy cseréjét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="e76ea-125">A megadott entitásnak legfeljebb 50 címkéje lehet.</span><span class="sxs-lookup"><span data-stu-id="e76ea-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="e76ea-126">Példák</span><span class="sxs-lookup"><span data-stu-id="e76ea-126">EXAMPLES</span></span>

### <span data-ttu-id="e76ea-127">Példa 1: előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="e76ea-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="e76ea-128">Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="e76ea-129">Ebben a címkében nincs érték.</span><span class="sxs-lookup"><span data-stu-id="e76ea-129">This tag has no values.</span></span>
<span data-ttu-id="e76ea-130">Egy erőforrás vagy erőforráscsoport értékeit nem tartalmazó címkét alkalmazhat, illetve a **New-AzTag** segítségével értékeket adhat a címkéhez.</span><span class="sxs-lookup"><span data-stu-id="e76ea-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="e76ea-131">Ha a címkét az erőforrás vagy az erőforrás csoportra alkalmazza, akkor megadhat egy értéket is.</span><span class="sxs-lookup"><span data-stu-id="e76ea-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="e76ea-132">2. példa: egy értékkel rendelkező előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="e76ea-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="e76ea-133">A parancs a Pénzügy nevű osztály nevű előre definiált címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e76ea-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="e76ea-134">3. példa: érték hozzáadása egy előre definiált címkéhez</span><span class="sxs-lookup"><span data-stu-id="e76ea-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="e76ea-135">Ezek a parancsok két értékkel rendelkező részleg nevű előre definiált címkét hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="e76ea-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="e76ea-136">Ha létezik a címke neve, a **New-AzTag** hozzáadja az értéket a meglévő címkéhez, nem pedig új létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="e76ea-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="e76ea-137">4. példa: előre definiált címke használata</span><span class="sxs-lookup"><span data-stu-id="e76ea-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="e76ea-138">Az ebben a példában szereplő parancsok az előre definiált címke létrehozása és használata.</span><span class="sxs-lookup"><span data-stu-id="e76ea-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="e76ea-139">Példa 5: az előfizetéshez tartozó címkék teljes készletének létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="e76ea-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="e76ea-140">Ezzel a paranccsal létrehozhatja vagy frissítheti az előfizetéshez tartozó teljes címkéket {subId}.</span><span class="sxs-lookup"><span data-stu-id="e76ea-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="e76ea-141">6. példa: az erőforrásokban a teljes címkéket hozza létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="e76ea-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="e76ea-142">Ezzel a paranccsal létrehozhatja vagy frissítheti az erőforrás teljes csoportját {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="e76ea-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="e76ea-143">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e76ea-143">PARAMETERS</span></span>

### <span data-ttu-id="e76ea-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76ea-144">-DefaultProfile</span></span>
<span data-ttu-id="e76ea-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e76ea-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e76ea-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e76ea-146">-Name</span></span>
<span data-ttu-id="e76ea-147">Az előre definiált címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e76ea-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="e76ea-148">Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="e76ea-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="e76ea-149">Ha egy meglévő címkéhez értéket szeretne hozzáadni, írja be a meglévő címke nevét.</span><span class="sxs-lookup"><span data-stu-id="e76ea-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="e76ea-150">Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzTag** hozzáadja az adott nevet tartalmazó címkét az új címke létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="e76ea-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="e76ea-151">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="e76ea-151">-Value</span></span>
<span data-ttu-id="e76ea-152">Az előre definiált címke értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e76ea-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="e76ea-153">Az előre definiált címkék több értéket is tartalmazhatnak, de mindegyik parancsban csak egy érték adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="e76ea-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="e76ea-154">Ez a paraméter nem kötelező, mert a címkék értékek nélküli neveket is tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="e76ea-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="e76ea-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e76ea-155">-ResourceId</span></span>
<span data-ttu-id="e76ea-156">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e76ea-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="e76ea-157">Lehet, hogy egy erőforrás, egy erőforráscsoport vagy egy előfizetés címkézve van.</span><span class="sxs-lookup"><span data-stu-id="e76ea-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="e76ea-158">-Címke</span><span class="sxs-lookup"><span data-stu-id="e76ea-158">-Tag</span></span>
<span data-ttu-id="e76ea-159">Az erőforrásra helyezett címkék.</span><span class="sxs-lookup"><span data-stu-id="e76ea-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="e76ea-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e76ea-160">-Confirm</span></span>
<span data-ttu-id="e76ea-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e76ea-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e76ea-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76ea-162">-WhatIf</span></span>
<span data-ttu-id="e76ea-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e76ea-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76ea-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e76ea-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e76ea-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76ea-165">CommonParameters</span></span>
<span data-ttu-id="e76ea-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e76ea-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76ea-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e76ea-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76ea-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e76ea-168">INPUTS</span></span>

### <span data-ttu-id="e76ea-169">System. String</span><span class="sxs-lookup"><span data-stu-id="e76ea-169">System.String</span></span>

### <span data-ttu-id="e76ea-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e76ea-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e76ea-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e76ea-171">OUTPUTS</span></span>

### <span data-ttu-id="e76ea-172">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag | Microsoft. Azure. Command. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="e76ea-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="e76ea-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e76ea-173">NOTES</span></span>

## <span data-ttu-id="e76ea-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e76ea-174">RELATED LINKS</span></span>

[<span data-ttu-id="e76ea-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="e76ea-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="e76ea-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="e76ea-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="e76ea-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="e76ea-177">Update-AzTag</span></span>](./Update-AzTag.md)
