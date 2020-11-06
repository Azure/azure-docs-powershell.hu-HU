---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 79fa1522ed0eec95a1e388ed5d113cf98ad7f525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501312"
---
# <span data-ttu-id="20477-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="20477-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="20477-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20477-102">SYNOPSIS</span></span>
<span data-ttu-id="20477-103">Előre definiált Azure-címkéket kap.</span><span class="sxs-lookup"><span data-stu-id="20477-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20477-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20477-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20477-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20477-105">DESCRIPTION</span></span>
<span data-ttu-id="20477-106">A **Get-AzureRmTag** parancsmag előre meghatározott Azure-címkéket kap az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="20477-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="20477-107">Ez a parancsmag alapvető információkat ad a címkékről vagy a címkékről és az azok értékeiről.</span><span class="sxs-lookup"><span data-stu-id="20477-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="20477-108">Minden kimeneti objektum tartalmazza a Count tulajdonságot, amely az erőforrások és az erőforráscsoportok számát adja meg, és a címkéket és az értékeket alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="20477-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>

<span data-ttu-id="20477-109">A **Get-AzureRMTag** Azure címkéi modul segítséget nyújt az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="20477-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="20477-110">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="20477-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="20477-111">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="20477-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="20477-112">Ha az előfizetéshez tartozik egy előre definiált címke, az előfizetésben nem alkalmazhat definiálatlan címkéket vagy értékeket az előfizetésben szereplő erőforrásokra vagy erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="20477-112">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="20477-113">Ha előre definiált címkét szeretne létrehozni, használja az New-AzureRmTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="20477-113">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="20477-114">Ha egy erőforráscsoport számára előre meghatározott címkét szeretne alkalmazni, használja az New-AzureRmTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="20477-114">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="20477-115">Ha egy adott címke vagy név és érték esetén szeretne erőforrás-csoportokat keresni, használja az Get-AzureRMResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="20477-115">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="20477-116">Példák</span><span class="sxs-lookup"><span data-stu-id="20477-116">EXAMPLES</span></span>

### <span data-ttu-id="20477-117">Példa 1: az összes előre definiált címke beolvasása</span><span class="sxs-lookup"><span data-stu-id="20477-117">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="20477-118">Ez a parancs az előfizetésben minden előre definiált címkét kap.</span><span class="sxs-lookup"><span data-stu-id="20477-118">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="20477-119">A Count tulajdonság azt jeleníti meg, hogy hányszor alkalmazta a címkét az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="20477-119">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="20477-120">2. példa: név szerinti címke beszerzése</span><span class="sxs-lookup"><span data-stu-id="20477-120">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="20477-121">Ez a parancs részletes információkat kap a részleg címkéről és annak értékeiről.</span><span class="sxs-lookup"><span data-stu-id="20477-121">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="20477-122">A Count tulajdonság azt jeleníti meg, hogy hányszor lett alkalmazva a címke és az egyes értékek az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="20477-122">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="20477-123">3. példa: az összes címke értékének beolvasása</span><span class="sxs-lookup"><span data-stu-id="20477-123">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="20477-124">Ez a parancs a *részletes* adatokat részletesen részletezi az előfizetésben szereplő összes előre definiált címkével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="20477-124">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="20477-125">A *részletes* paraméter a minden címkéhez tartozó *Name* paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="20477-125">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="20477-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20477-126">PARAMETERS</span></span>

### <span data-ttu-id="20477-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20477-127">-DefaultProfile</span></span>
<span data-ttu-id="20477-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20477-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20477-129">– Részletes</span><span class="sxs-lookup"><span data-stu-id="20477-129">-Detailed</span></span>
<span data-ttu-id="20477-130">Azt jelzi, hogy ez a művelet a kimenetre vonatkozó értékek címkézésével kapcsolatos információkat ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="20477-130">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20477-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20477-131">-Name</span></span>
<span data-ttu-id="20477-132">A beolvasott címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20477-132">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="20477-133">Alapértelmezés szerint a **Get-AzureRmTag** az előfizetésben szereplő összes előre definiált címkére vonatkozó alapvető információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="20477-133">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="20477-134">A *Name* paraméter megadásakor a *részletes* paraméternek nincs eredménye.</span><span class="sxs-lookup"><span data-stu-id="20477-134">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20477-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20477-135">CommonParameters</span></span>
<span data-ttu-id="20477-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20477-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20477-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20477-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20477-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20477-138">INPUTS</span></span>

### <span data-ttu-id="20477-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="20477-139">None</span></span>

## <span data-ttu-id="20477-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20477-140">OUTPUTS</span></span>

### <span data-ttu-id="20477-141">Microsoft. Azure. Command. Tags. Model. PSTag, Microsoft. Azure. commands. Tags</span><span class="sxs-lookup"><span data-stu-id="20477-141">Microsoft.Azure.Commands.Tags.Model.PSTag, Microsoft.Azure.Commands.Tags</span></span>

## <span data-ttu-id="20477-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20477-142">NOTES</span></span>

## <span data-ttu-id="20477-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20477-143">RELATED LINKS</span></span>

[<span data-ttu-id="20477-144">Új – AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="20477-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="20477-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="20477-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


