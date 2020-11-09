---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301067"
---
# <span data-ttu-id="ec8ca-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec8ca-101">Get-AzTag</span></span>

## <span data-ttu-id="ec8ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8ca-103">Előre definiált Azure-címkéket kap | A teljes címkéket lekapja egy erőforrásra vagy előfizetésre.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="ec8ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec8ca-104">SYNTAX</span></span>

### <span data-ttu-id="ec8ca-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec8ca-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec8ca-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec8ca-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec8ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec8ca-107">DESCRIPTION</span></span>

<span data-ttu-id="ec8ca-108">**GetPredefinedTagSet** : a **Get-AzTag** parancsmag előre meghatározott Azure-címkéket kap az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="ec8ca-109">Ez a parancsmag alapvető információkat ad a címkékről vagy a címkékről és az azok értékeiről.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="ec8ca-110">Minden kimeneti objektum tartalmazza a Count tulajdonságot, amely az erőforrások és az erőforráscsoportok számát adja meg, és a címkéket és az értékeket alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="ec8ca-111">A **Get-AzTag** Azure címkéi modul segítséget nyújt az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="ec8ca-112">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="ec8ca-113">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="ec8ca-114">Ha előre definiált címkét szeretne létrehozni, használja az New-AzTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="ec8ca-115">Ha egy erőforráscsoport számára előre meghatározott címkét szeretne alkalmazni, használja az New-AzTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="ec8ca-116">Ha egy adott címke vagy név és érték esetén szeretne erőforrás-csoportokat keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="ec8ca-117">**GetByResourceIdParameterSet** : a **Get-AzTag** parancsmag egy **ResourceId** megkapja a teljes címkéket egy erőforrásra vagy előfizetésre.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="ec8ca-118">Példák</span><span class="sxs-lookup"><span data-stu-id="ec8ca-118">EXAMPLES</span></span>

### <span data-ttu-id="ec8ca-119">Példa 1: az összes előre definiált címke beolvasása</span><span class="sxs-lookup"><span data-stu-id="ec8ca-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="ec8ca-120">Ez a parancs az előfizetésben minden előre definiált címkét kap.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="ec8ca-121">A Count tulajdonság azt jeleníti meg, hogy hányszor alkalmazta a címkét az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="ec8ca-122">2. példa: név szerinti címke beszerzése</span><span class="sxs-lookup"><span data-stu-id="ec8ca-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="ec8ca-123">Ez a parancs részletes információkat kap a részleg címkéről és annak értékeiről.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="ec8ca-124">A Count tulajdonság azt jeleníti meg, hogy hányszor lett alkalmazva a címke és az egyes értékek az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="ec8ca-125">3. példa: az összes címke értékének beolvasása</span><span class="sxs-lookup"><span data-stu-id="ec8ca-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

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

<span data-ttu-id="ec8ca-126">Ez a parancs a *részletes* adatokat részletesen részletezi az előfizetésben szereplő összes előre definiált címkével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="ec8ca-127">A *részletes* paraméter a minden címkéhez tartozó *Name* paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="ec8ca-128">Példa 4: az előfizetéshez tartozó címkék teljes csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ec8ca-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="ec8ca-129">Ez a parancs a teljes címkéket az előfizetéshez ({subId}) kapja.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="ec8ca-130">Példa 5: az erőforrás teljes csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ec8ca-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="ec8ca-131">Ez a parancs a teljes címkéket az erőforráshoz tartozó {resourceId} értékkel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="ec8ca-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec8ca-132">PARAMETERS</span></span>

### <span data-ttu-id="ec8ca-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8ca-133">-DefaultProfile</span></span>
<span data-ttu-id="ec8ca-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec8ca-135">– Részletes</span><span class="sxs-lookup"><span data-stu-id="ec8ca-135">-Detailed</span></span>
<span data-ttu-id="ec8ca-136">Azt jelzi, hogy ez a művelet a kimenetre vonatkozó értékek címkézésével kapcsolatos információkat ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8ca-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec8ca-137">-Name</span></span>
<span data-ttu-id="ec8ca-138">Az előre definiált címke neve.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-138">Name of the predefined tag.</span></span>
<span data-ttu-id="ec8ca-139">Alapértelmezés szerint a **Get-AzTag** az előfizetésben szereplő összes előre definiált címkére vonatkozó alapvető információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="ec8ca-140">A *Name* paraméter megadásakor a *részletes* paraméternek nincs eredménye.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8ca-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec8ca-141">-ResourceId</span></span>
<span data-ttu-id="ec8ca-142">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="ec8ca-143">Lehet, hogy egy erőforrás, egy erőforráscsoport vagy egy előfizetés címkézve van.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8ca-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8ca-144">CommonParameters</span></span>
<span data-ttu-id="ec8ca-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec8ca-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8ca-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec8ca-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8ca-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec8ca-147">INPUTS</span></span>

### <span data-ttu-id="ec8ca-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ec8ca-148">System.String</span></span>

### <span data-ttu-id="ec8ca-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec8ca-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec8ca-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec8ca-150">OUTPUTS</span></span>

### <span data-ttu-id="ec8ca-151">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag | Microsoft. Azure. Command. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="ec8ca-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="ec8ca-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec8ca-152">NOTES</span></span>

## <span data-ttu-id="ec8ca-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec8ca-153">RELATED LINKS</span></span>

[<span data-ttu-id="ec8ca-154">Új – AzTag</span><span class="sxs-lookup"><span data-stu-id="ec8ca-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="ec8ca-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec8ca-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="ec8ca-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec8ca-156">Update-AzTag</span></span>](./Update-AzTag.md)
