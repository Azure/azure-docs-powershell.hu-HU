---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939417"
---
# <span data-ttu-id="d58cc-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="d58cc-101">Get-AzTag</span></span>

## <span data-ttu-id="d58cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d58cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d58cc-103">Előre definiált Azure-címkéket | Egy erőforrás vagy előfizetés teljes címkéit beveszi.</span><span class="sxs-lookup"><span data-stu-id="d58cc-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d58cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d58cc-104">SYNTAX</span></span>

### <span data-ttu-id="d58cc-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="d58cc-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d58cc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d58cc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d58cc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d58cc-107">DESCRIPTION</span></span>

<span data-ttu-id="d58cc-108">**GetPredefinedTagSet:** A **Get-AzTag** parancsmag előre definiált Azure-címkéket kap az előfizetésében.</span><span class="sxs-lookup"><span data-stu-id="d58cc-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="d58cc-109">Ez a parancsmag alapvető információkat ad vissza a címkékről vagy a címkékről és azok értékeiről.</span><span class="sxs-lookup"><span data-stu-id="d58cc-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="d58cc-110">Minden kimeneti objektum tartalmaz egy Count tulajdonságot, amely azt jelzi, hogy hány erőforrásra és erőforráscsoportra alkalmazta a címkéket és értékeket.</span><span class="sxs-lookup"><span data-stu-id="d58cc-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="d58cc-111">Az Azure Címkék modul, amely a **Get-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="d58cc-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="d58cc-112">Az Azure-címkék olyan névérték-párok, amelyek segítségével kategorizálhatja Azure-erőforrásait és erőforráscsoportját, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokra és csoportokra vonatkozó megjegyzéseket vagy megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="d58cc-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="d58cc-113">Egyetlen lépésben definiálhat és alkalmazhat címkéket, az előre definiált címkékkel azonban szabványos, egységes, kiszámítható neveket és értékeket határozhat meg az előfizetésében szereplő címkékhez.</span><span class="sxs-lookup"><span data-stu-id="d58cc-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="d58cc-114">Előre definiált címke létrehozásához használja a New-AzTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d58cc-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="d58cc-115">Ha előre definiált címkét szeretne alkalmazni  egy erőforráscsoportra, használja a New-AzTag címke paraméterét.</span><span class="sxs-lookup"><span data-stu-id="d58cc-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="d58cc-116">Ha egy adott címkenevet vagy nevet és értéket  keres az erőforráscsoportokban, használja a Get-AzResourceGroup parancsmag címke paraméterét.</span><span class="sxs-lookup"><span data-stu-id="d58cc-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="d58cc-117">**GetByResourceIdParameterSet:** A **ResourceId** azonosítóval elérhető **Get-AzTag** parancsmag a címkék teljes készletét megkapja egy erőforráson vagy előfizetésen.</span><span class="sxs-lookup"><span data-stu-id="d58cc-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d58cc-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d58cc-118">EXAMPLES</span></span>

### <span data-ttu-id="d58cc-119">1. példa: Az összes előre definiált címke betekintése</span><span class="sxs-lookup"><span data-stu-id="d58cc-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="d58cc-120">Ez a parancs az előfizetésben előre definiált összes címkét megkapja.</span><span class="sxs-lookup"><span data-stu-id="d58cc-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="d58cc-121">A Darab tulajdonság azt mutatja, hogy hányszor lett alkalmazva a címke az előfizetésben található erőforrásokra és erőforráscsoportokra.</span><span class="sxs-lookup"><span data-stu-id="d58cc-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="d58cc-122">2. példa: Címke lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="d58cc-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="d58cc-123">Ez a parancs részletes információkat kap a Részleg címkéről és annak értékeiről.</span><span class="sxs-lookup"><span data-stu-id="d58cc-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="d58cc-124">A Darab tulajdonság azt mutatja, hogy hányszor lett alkalmazva a címke és annak értékei az előfizetésben található erőforrásokra és erőforráscsoportokra.</span><span class="sxs-lookup"><span data-stu-id="d58cc-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="d58cc-125">3. példa: Az összes címke értékeinek lekérte</span><span class="sxs-lookup"><span data-stu-id="d58cc-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="d58cc-126">Ez a parancs a Részletes *paraméter* segítségével részletes információkat kap az előfizetésben előre definiált címkékről.</span><span class="sxs-lookup"><span data-stu-id="d58cc-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="d58cc-127">A Részletes *paraméter* használata egyenértékű azzal, ha a *Name* paramétert minden címkéhez használja.</span><span class="sxs-lookup"><span data-stu-id="d58cc-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="d58cc-128">4. példa: Az előfizetéshez beállított összes címke lekérte</span><span class="sxs-lookup"><span data-stu-id="d58cc-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="d58cc-129">Ez a parancs a(z) {subId} azonosítóval az előfizetés összes címkéjéhez be lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="d58cc-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="d58cc-130">5. példa: Az erőforráshoz beállított címkék teljes készletének be szereznie</span><span class="sxs-lookup"><span data-stu-id="d58cc-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="d58cc-131">Ez a parancs a(z) {resourceId} segítségével az erőforrás összes címkéjéhez be lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="d58cc-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="d58cc-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d58cc-132">PARAMETERS</span></span>

### <span data-ttu-id="d58cc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58cc-133">-DefaultProfile</span></span>
<span data-ttu-id="d58cc-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d58cc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58cc-135">-Részletes</span><span class="sxs-lookup"><span data-stu-id="d58cc-135">-Detailed</span></span>
<span data-ttu-id="d58cc-136">Azt jelzi, hogy ez a művelet információt ad a címkeértékekkel kapcsolatban a kimenethez.</span><span class="sxs-lookup"><span data-stu-id="d58cc-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="d58cc-137">-Name</span><span class="sxs-lookup"><span data-stu-id="d58cc-137">-Name</span></span>
<span data-ttu-id="d58cc-138">Az előre definiált címke neve.</span><span class="sxs-lookup"><span data-stu-id="d58cc-138">Name of the predefined tag.</span></span>
<span data-ttu-id="d58cc-139">A **Get-AzTag** alapértelmezés szerint alapvető információkat kap az előfizetésben előre definiált címkékről.</span><span class="sxs-lookup"><span data-stu-id="d58cc-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="d58cc-140">A Név paraméter *megadásakor* a *Részletes* paraméternek nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="d58cc-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="d58cc-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d58cc-141">-ResourceId</span></span>
<span data-ttu-id="d58cc-142">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d58cc-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="d58cc-143">Előfordulhat, hogy egy erőforrás, erőforráscsoport vagy előfizetés meg van címkézve.</span><span class="sxs-lookup"><span data-stu-id="d58cc-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="d58cc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58cc-144">CommonParameters</span></span>
<span data-ttu-id="d58cc-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58cc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58cc-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d58cc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58cc-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d58cc-147">INPUTS</span></span>

### <span data-ttu-id="d58cc-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d58cc-148">System.String</span></span>

### <span data-ttu-id="d58cc-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d58cc-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d58cc-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d58cc-150">OUTPUTS</span></span>

### <span data-ttu-id="d58cc-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="d58cc-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="d58cc-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d58cc-152">NOTES</span></span>

## <span data-ttu-id="d58cc-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d58cc-153">RELATED LINKS</span></span>

[<span data-ttu-id="d58cc-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="d58cc-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="d58cc-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="d58cc-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="d58cc-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="d58cc-156">Update-AzTag</span></span>](./Update-AzTag.md)
