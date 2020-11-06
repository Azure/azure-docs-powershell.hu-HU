---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501311"
---
# <span data-ttu-id="8b11f-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="8b11f-101">New-AzureRmTag</span></span>

## <span data-ttu-id="8b11f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b11f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b11f-103">Előre definiált Azure címkét hoz létre, vagy értékeket ad hozzá egy meglévő címkéhez.</span><span class="sxs-lookup"><span data-stu-id="8b11f-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b11f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b11f-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b11f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b11f-105">DESCRIPTION</span></span>
<span data-ttu-id="8b11f-106">A **New-AzureRmTag** parancsmag egy előre definiált, előre meghatározott értéket tartalmazó Azure címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8b11f-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="8b11f-107">Azt is megteheti, hogy további értékeket is felvehet a meglévő előre definiált címkékbe.</span><span class="sxs-lookup"><span data-stu-id="8b11f-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="8b11f-108">Ha előre definiált címkét szeretne létrehozni, adjon meg egy egyedi címkét.</span><span class="sxs-lookup"><span data-stu-id="8b11f-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="8b11f-109">Ha egy meglévő előre definiált címkéhez szeretne értéket hozzáadni, adja meg a meglévő címke nevét és az új értéket.</span><span class="sxs-lookup"><span data-stu-id="8b11f-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="8b11f-110">Ez a parancsmag egy olyan objektumot ad eredményül, amely az új vagy módosított címkét tartalmazza az értékekkel és a hozzájuk rendelt erőforrások számával.</span><span class="sxs-lookup"><span data-stu-id="8b11f-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="8b11f-111">Az Azure címkék modul, amely a **New-AzureRmTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="8b11f-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="8b11f-112">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="8b11f-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="8b11f-113">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="8b11f-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="8b11f-114">Ha az előfizetéshez tartozik egy előre definiált címke, az előfizetésben nem alkalmazhat definiálatlan címkéket vagy értékeket az előfizetésben szereplő erőforrásokra vagy erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="8b11f-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="8b11f-115">Ha előre definiált címkét szeretne alkalmazni egy erőforrásra vagy erőforrás-csoportra, használja az New-AzureRmTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="8b11f-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="8b11f-116">Ha a megadott címke nevével vagy névvel és értékkel rendelkező erőforráscsoportokat szeretne keresni, használja az Get-AzureRMResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="8b11f-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="8b11f-117">Minden címkéhez tartozik egy név.</span><span class="sxs-lookup"><span data-stu-id="8b11f-117">Every tag has a name.</span></span>
<span data-ttu-id="8b11f-118">Az értékek nem kötelezők.</span><span class="sxs-lookup"><span data-stu-id="8b11f-118">The values are optional.</span></span>
<span data-ttu-id="8b11f-119">Az előre definiált Azure-címkék több értéket is tartalmazhatnak, de ha a címkét erőforrás-vagy erőforrás-csoportra alkalmazza, akkor a címke nevét és csak egy értékét kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="8b11f-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="8b11f-120">Létrehozhat például egy előre definiált részleg címkét, amely egy értékkel rendelkezik az egyes részlegekhez, például a pénzügyi, az emberi erőforrások és az IT-részleghez.</span><span class="sxs-lookup"><span data-stu-id="8b11f-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="8b11f-121">Amikor az osztály címkét egy erőforrásra alkalmazza, csak egy előre meghatározott értéket (például pénzügy) kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="8b11f-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="8b11f-122">Példák</span><span class="sxs-lookup"><span data-stu-id="8b11f-122">EXAMPLES</span></span>

### <span data-ttu-id="8b11f-123">Példa 1: előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="8b11f-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="8b11f-124">Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="8b11f-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="8b11f-125">Ebben a címkében nincs érték.</span><span class="sxs-lookup"><span data-stu-id="8b11f-125">This tag has no values.</span></span>
<span data-ttu-id="8b11f-126">Egy erőforrás vagy erőforráscsoport értékeit nem tartalmazó címkét alkalmazhat, illetve a **New-AzureRmTag** segítségével értékeket adhat a címkéhez.</span><span class="sxs-lookup"><span data-stu-id="8b11f-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="8b11f-127">Ha a címkét az erőforrás vagy az erőforrás csoportra alkalmazza, akkor megadhat egy értéket is.</span><span class="sxs-lookup"><span data-stu-id="8b11f-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="8b11f-128">2. példa: egy értékkel rendelkező előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="8b11f-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="8b11f-129">A parancs a Pénzügy nevű osztály nevű előre definiált címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8b11f-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="8b11f-130">3. példa: érték hozzáadása egy előre definiált címkéhez</span><span class="sxs-lookup"><span data-stu-id="8b11f-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="8b11f-131">Ezek a parancsok két értékkel rendelkező részleg nevű előre definiált címkét hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="8b11f-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="8b11f-132">Ha létezik a címke neve, a **New-AzureRmTag** hozzáadja az értéket a meglévő címkéhez, nem pedig új létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="8b11f-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="8b11f-133">4. példa: előre definiált címke használata</span><span class="sxs-lookup"><span data-stu-id="8b11f-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="8b11f-134">Az ebben a példában szereplő parancsok az előre definiált címke létrehozása és használata.</span><span class="sxs-lookup"><span data-stu-id="8b11f-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="8b11f-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b11f-135">PARAMETERS</span></span>

### <span data-ttu-id="8b11f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b11f-136">-DefaultProfile</span></span>
<span data-ttu-id="8b11f-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b11f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b11f-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b11f-138">-Name</span></span>
<span data-ttu-id="8b11f-139">A címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b11f-139">Specifies the tag name.</span></span>
<span data-ttu-id="8b11f-140">Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="8b11f-140">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="8b11f-141">Ha egy meglévő címkéhez értéket szeretne hozzáadni, írja be a meglévő címke nevét.</span><span class="sxs-lookup"><span data-stu-id="8b11f-141">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="8b11f-142">Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzureRmTag** hozzáadja az adott nevet tartalmazó címkét az új címke létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="8b11f-142">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b11f-143">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="8b11f-143">-Value</span></span>
<span data-ttu-id="8b11f-144">A címke értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b11f-144">Specifies a tag value.</span></span>
<span data-ttu-id="8b11f-145">Az előre definiált címkék több értéket is tartalmazhatnak, de mindegyik parancsban csak egy érték adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="8b11f-145">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="8b11f-146">Ez a paraméter nem kötelező, mert a címkék értékek nélküli neveket is tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="8b11f-146">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b11f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b11f-147">CommonParameters</span></span>
<span data-ttu-id="8b11f-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b11f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b11f-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b11f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b11f-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b11f-150">INPUTS</span></span>

### <span data-ttu-id="8b11f-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b11f-151">None</span></span>

## <span data-ttu-id="8b11f-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b11f-152">OUTPUTS</span></span>

### <span data-ttu-id="8b11f-153">Microsoft. Azure. Command. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="8b11f-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="8b11f-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b11f-154">NOTES</span></span>

## <span data-ttu-id="8b11f-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b11f-155">RELATED LINKS</span></span>

[<span data-ttu-id="8b11f-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="8b11f-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="8b11f-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="8b11f-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


