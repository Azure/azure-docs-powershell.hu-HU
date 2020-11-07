---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 242f207faa98c6165e4c64f095f9b171f1d72d5c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843317"
---
# <span data-ttu-id="1204f-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="1204f-101">New-AzTag</span></span>

## <span data-ttu-id="1204f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1204f-102">SYNOPSIS</span></span>
<span data-ttu-id="1204f-103">Előre definiált Azure címkét hoz létre, vagy értékeket ad hozzá egy meglévő címkéhez.</span><span class="sxs-lookup"><span data-stu-id="1204f-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

## <span data-ttu-id="1204f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1204f-104">SYNTAX</span></span>

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1204f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1204f-105">DESCRIPTION</span></span>
<span data-ttu-id="1204f-106">A **New-AzTag** parancsmag egy előre definiált, előre meghatározott értéket tartalmazó Azure címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1204f-106">The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="1204f-107">Azt is megteheti, hogy további értékeket is felvehet a meglévő előre definiált címkékbe.</span><span class="sxs-lookup"><span data-stu-id="1204f-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="1204f-108">Ha előre definiált címkét szeretne létrehozni, adjon meg egy egyedi címkét.</span><span class="sxs-lookup"><span data-stu-id="1204f-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="1204f-109">Ha egy meglévő előre definiált címkéhez szeretne értéket hozzáadni, adja meg a meglévő címke nevét és az új értéket.</span><span class="sxs-lookup"><span data-stu-id="1204f-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="1204f-110">Ez a parancsmag egy olyan objektumot ad eredményül, amely az új vagy módosított címkét tartalmazza az értékekkel és a hozzájuk rendelt erőforrások számával.</span><span class="sxs-lookup"><span data-stu-id="1204f-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="1204f-111">Az Azure címkék modul, amely a **New-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="1204f-111">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="1204f-112">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="1204f-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="1204f-113">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="1204f-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="1204f-114">Ha előre definiált címkét szeretne alkalmazni egy erőforrásra vagy erőforrás-csoportra, használja az New-AzTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="1204f-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="1204f-115">Ha a megadott címke nevével vagy névvel és értékkel rendelkező erőforráscsoportokat szeretne keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="1204f-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1204f-116">Minden címkéhez tartozik egy név.</span><span class="sxs-lookup"><span data-stu-id="1204f-116">Every tag has a name.</span></span>
<span data-ttu-id="1204f-117">Az értékek nem kötelezők.</span><span class="sxs-lookup"><span data-stu-id="1204f-117">The values are optional.</span></span>
<span data-ttu-id="1204f-118">Az előre definiált Azure-címkék több értéket is tartalmazhatnak, de ha a címkét erőforrás-vagy erőforrás-csoportra alkalmazza, akkor a címke nevét és csak egy értékét kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="1204f-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="1204f-119">Létrehozhat például egy előre definiált részleg címkét, amely egy értékkel rendelkezik az egyes részlegekhez, például a pénzügyi, az emberi erőforrások és az IT-részleghez.</span><span class="sxs-lookup"><span data-stu-id="1204f-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="1204f-120">Amikor az osztály címkét egy erőforrásra alkalmazza, csak egy előre meghatározott értéket (például pénzügy) kell alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="1204f-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="1204f-121">Példák</span><span class="sxs-lookup"><span data-stu-id="1204f-121">EXAMPLES</span></span>

### <span data-ttu-id="1204f-122">Példa 1: előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="1204f-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="1204f-123">Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="1204f-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="1204f-124">Ebben a címkében nincs érték.</span><span class="sxs-lookup"><span data-stu-id="1204f-124">This tag has no values.</span></span>
<span data-ttu-id="1204f-125">Egy erőforrás vagy erőforráscsoport értékeit nem tartalmazó címkét alkalmazhat, illetve a **New-AzTag** segítségével értékeket adhat a címkéhez.</span><span class="sxs-lookup"><span data-stu-id="1204f-125">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="1204f-126">Ha a címkét az erőforrás vagy az erőforrás csoportra alkalmazza, akkor megadhat egy értéket is.</span><span class="sxs-lookup"><span data-stu-id="1204f-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="1204f-127">2. példa: egy értékkel rendelkező előre definiált címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="1204f-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="1204f-128">A parancs a Pénzügy nevű osztály nevű előre definiált címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1204f-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="1204f-129">3. példa: érték hozzáadása egy előre definiált címkéhez</span><span class="sxs-lookup"><span data-stu-id="1204f-129">Example 3: Add a value to a predefined tag</span></span>
```
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

<span data-ttu-id="1204f-130">Ezek a parancsok két értékkel rendelkező részleg nevű előre definiált címkét hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="1204f-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="1204f-131">Ha létezik a címke neve, a **New-AzTag** hozzáadja az értéket a meglévő címkéhez, nem pedig új létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="1204f-131">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="1204f-132">4. példa: előre definiált címke használata</span><span class="sxs-lookup"><span data-stu-id="1204f-132">Example 4: Use a predefined tag</span></span>
```
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

<span data-ttu-id="1204f-133">Az ebben a példában szereplő parancsok az előre definiált címke létrehozása és használata.</span><span class="sxs-lookup"><span data-stu-id="1204f-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="1204f-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1204f-134">PARAMETERS</span></span>

### <span data-ttu-id="1204f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1204f-135">-DefaultProfile</span></span>
<span data-ttu-id="1204f-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1204f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1204f-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1204f-137">-Name</span></span>
<span data-ttu-id="1204f-138">A címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1204f-138">Specifies the tag name.</span></span>
<span data-ttu-id="1204f-139">Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.</span><span class="sxs-lookup"><span data-stu-id="1204f-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="1204f-140">Ha egy meglévő címkéhez értéket szeretne hozzáadni, írja be a meglévő címke nevét.</span><span class="sxs-lookup"><span data-stu-id="1204f-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="1204f-141">Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzTag** hozzáadja az adott nevet tartalmazó címkét az új címke létrehozása helyett.</span><span class="sxs-lookup"><span data-stu-id="1204f-141">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1204f-142">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="1204f-142">-Value</span></span>
<span data-ttu-id="1204f-143">A címke értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1204f-143">Specifies a tag value.</span></span>
<span data-ttu-id="1204f-144">Az előre definiált címkék több értéket is tartalmazhatnak, de mindegyik parancsban csak egy érték adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="1204f-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="1204f-145">Ez a paraméter nem kötelező, mert a címkék értékek nélküli neveket is tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="1204f-145">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1204f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1204f-146">CommonParameters</span></span>
<span data-ttu-id="1204f-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1204f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1204f-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1204f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1204f-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1204f-149">INPUTS</span></span>

### <span data-ttu-id="1204f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1204f-150">System.String</span></span>

## <span data-ttu-id="1204f-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1204f-151">OUTPUTS</span></span>

### <span data-ttu-id="1204f-152">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="1204f-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="1204f-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1204f-153">NOTES</span></span>

## <span data-ttu-id="1204f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1204f-154">RELATED LINKS</span></span>

[<span data-ttu-id="1204f-155">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="1204f-155">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="1204f-156">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="1204f-156">Remove-AzTag</span></span>](./Remove-AzTag.md)

