---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 3423331e36fd9fbd636a1ae877275badd5912324
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467206"
---
# <span data-ttu-id="9faa5-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="9faa5-101">Update-AzTag</span></span>

## <span data-ttu-id="9faa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9faa5-102">SYNOPSIS</span></span>

<span data-ttu-id="9faa5-103">Szelektíven frissíti egy erőforrás vagy előfizetés címkéinek készletét.</span><span class="sxs-lookup"><span data-stu-id="9faa5-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="9faa5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9faa5-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="9faa5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9faa5-105">DESCRIPTION</span></span>

<span data-ttu-id="9faa5-106">A **ResourceId** azonosítóval tagolt **Update-AzTag** parancsmag szelektíven frissíti egy erőforrás vagy előfizetés címkéinek készletét.</span><span class="sxs-lookup"><span data-stu-id="9faa5-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="9faa5-107">Ez a művelet lehetővé teszi a megadott erőforrás vagy előfizetés címkéinek cseréjét, egyesítését vagy szelektív törlését.</span><span class="sxs-lookup"><span data-stu-id="9faa5-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="9faa5-108">A megadott entitás legfeljebb 50 címkével lehet a művelet végén.</span><span class="sxs-lookup"><span data-stu-id="9faa5-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="9faa5-109">A "Csere" lehetőség a meglévő címkék teljes halmazát lecseréli egy új készletre.</span><span class="sxs-lookup"><span data-stu-id="9faa5-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="9faa5-110">Az "egyesítés" beállítás lehetővé teszi új névvel kiegészítve címkék hozzáadását, valamint a meglévő névvel kiegészítve a címkék értékeinek frissítését.</span><span class="sxs-lookup"><span data-stu-id="9faa5-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="9faa5-111">A "törlés" beállítás lehetővé teszi a megadott nevek vagy név/érték párok alapján történő címkék szelektív törlését.</span><span class="sxs-lookup"><span data-stu-id="9faa5-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="9faa5-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9faa5-112">EXAMPLES</span></span>

### <span data-ttu-id="9faa5-113">1. példa: Az előfizetés címkekészletének szelektív frissítése az "Egyesítés" művelettel</span><span class="sxs-lookup"><span data-stu-id="9faa5-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="9faa5-114">Ezzel a paranccsal egyesítheti az előfizetés címkéit a(z) {subId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="9faa5-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="9faa5-115">2. példa: Az előfizetés címkekészletének szelektív frissítése a "Csere" művelettel</span><span class="sxs-lookup"><span data-stu-id="9faa5-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="9faa5-116">Ez a parancs a(z) {subId} címkéinek halmazát adja vissza az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="9faa5-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="9faa5-117">3. példa: Az előfizetés címkéinek szelektív frissítése a "Törlés" művelettel</span><span class="sxs-lookup"><span data-stu-id="9faa5-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="9faa5-118">Ez a parancs törli a ({subId}) előfizetés címkéit.</span><span class="sxs-lookup"><span data-stu-id="9faa5-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="9faa5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9faa5-119">PARAMETERS</span></span>

### <span data-ttu-id="9faa5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9faa5-120">-DefaultProfile</span></span>
<span data-ttu-id="9faa5-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9faa5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9faa5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9faa5-122">-ResourceId</span></span>
<span data-ttu-id="9faa5-123">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9faa5-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="9faa5-124">Előfordulhat, hogy egy erőforrás, erőforráscsoport vagy előfizetés meg van címkézve.</span><span class="sxs-lookup"><span data-stu-id="9faa5-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9faa5-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9faa5-125">-Tag</span></span>
<span data-ttu-id="9faa5-126">A frissítéshez használt címkék készlete.</span><span class="sxs-lookup"><span data-stu-id="9faa5-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9faa5-127">-Művelet</span><span class="sxs-lookup"><span data-stu-id="9faa5-127">-Operation</span></span>
<span data-ttu-id="9faa5-128">A frissítési művelet.</span><span class="sxs-lookup"><span data-stu-id="9faa5-128">The update operation.</span></span> <span data-ttu-id="9faa5-129">A beállítások az Egyesítés, a Csere és a Törlés.</span><span class="sxs-lookup"><span data-stu-id="9faa5-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9faa5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9faa5-130">-Confirm</span></span>
<span data-ttu-id="9faa5-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9faa5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9faa5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9faa5-132">-WhatIf</span></span>
<span data-ttu-id="9faa5-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9faa5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9faa5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9faa5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9faa5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9faa5-135">CommonParameters</span></span>
<span data-ttu-id="9faa5-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9faa5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9faa5-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9faa5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9faa5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9faa5-138">INPUTS</span></span>

### <span data-ttu-id="9faa5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9faa5-139">System.String</span></span>

### <span data-ttu-id="9faa5-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="9faa5-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="9faa5-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9faa5-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9faa5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9faa5-142">OUTPUTS</span></span>

### <span data-ttu-id="9faa5-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="9faa5-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="9faa5-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9faa5-144">NOTES</span></span>

## <span data-ttu-id="9faa5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9faa5-145">RELATED LINKS</span></span>

[<span data-ttu-id="9faa5-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="9faa5-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="9faa5-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="9faa5-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="9faa5-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="9faa5-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
