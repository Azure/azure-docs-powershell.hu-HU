---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172758"
---
# <span data-ttu-id="d1cb6-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1cb6-101">Update-AzTag</span></span>

## <span data-ttu-id="d1cb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1cb6-102">SYNOPSIS</span></span>

<span data-ttu-id="d1cb6-103">Szelektíven frissíti egy erőforrás vagy előfizetés címkéit.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d1cb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1cb6-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="d1cb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1cb6-105">DESCRIPTION</span></span>

<span data-ttu-id="d1cb6-106">Az **Update-AzTag** parancsmag **ResourceId** szelektíven frissíti az erőforrás vagy az előfizetés címkéit.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="d1cb6-107">Ezzel a művelettel a megadott erőforrás vagy előfizetés címkéit cserélheti, egyesítheti vagy szelektíven törölheti.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="d1cb6-108">A megadott entitás legfeljebb 50 címkét tartalmazhat a művelet végén.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="d1cb6-109">A "csere" parancs a meglévő címkék teljes halmazát egy új halmazra cseréli.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="d1cb6-110">Az "Egyesítés" parancs lehetővé teszi címkék hozzáadását új nevekkel és a meglévő nevekkel rendelkező címkék értékének frissítésével.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="d1cb6-111">A "Törlés" parancs lehetővé teszi a címkék szelektív törlését a megadott nevek vagy név/érték párok alapján.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="d1cb6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d1cb6-112">EXAMPLES</span></span>

### <span data-ttu-id="d1cb6-113">1. példa: szelektíven frissíti a címkéket egy előfizetésben az "Egyesítés" művelettel.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="d1cb6-114">Ez a parancs az előfizetéshez tartozó címkéket az {subId} értékkel egyesíti.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="d1cb6-115">2. példa: szelektíven frissíti a címkéket egy előfizetésben a "csere" művelettel.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="d1cb6-116">Ez a parancs az előfizetéshez tartozó címkéket Repalces {subId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="d1cb6-117">3. példa: szelektíven frissíti a címkéket egy előfizetésben a "Delete" művelettel.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="d1cb6-118">Ez a parancs törli az előfizetéshez tartozó címkéket {subId} értékkel.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="d1cb6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1cb6-119">PARAMETERS</span></span>

### <span data-ttu-id="d1cb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cb6-120">-DefaultProfile</span></span>
<span data-ttu-id="d1cb6-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1cb6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1cb6-122">-ResourceId</span></span>
<span data-ttu-id="d1cb6-123">A címkézett entitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="d1cb6-124">Lehet, hogy egy erőforrás, egy erőforráscsoport vagy egy előfizetés címkézve van.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-124">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="d1cb6-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="d1cb6-125">-Tag</span></span>
<span data-ttu-id="d1cb6-126">A frissítéshez használandó címkék halmaza.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="d1cb6-127">-Művelet</span><span class="sxs-lookup"><span data-stu-id="d1cb6-127">-Operation</span></span>
<span data-ttu-id="d1cb6-128">A frissítési művelet.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-128">The update operation.</span></span> <span data-ttu-id="d1cb6-129">A beállítások egyesítés, csere és törlés.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb6-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1cb6-130">-Confirm</span></span>
<span data-ttu-id="d1cb6-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1cb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1cb6-132">-WhatIf</span></span>
<span data-ttu-id="d1cb6-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1cb6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1cb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cb6-135">CommonParameters</span></span>
<span data-ttu-id="d1cb6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1cb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cb6-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cb6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1cb6-138">INPUTS</span></span>

### <span data-ttu-id="d1cb6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1cb6-139">System.String</span></span>

### <span data-ttu-id="d1cb6-140">Microsoft. Azure. Command. Tags. Model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="d1cb6-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="d1cb6-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1cb6-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d1cb6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1cb6-142">OUTPUTS</span></span>

### <span data-ttu-id="d1cb6-143">Microsoft. Azure. Command. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="d1cb6-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="d1cb6-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1cb6-144">NOTES</span></span>

## <span data-ttu-id="d1cb6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1cb6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d1cb6-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1cb6-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="d1cb6-147">Új – AzTag</span><span class="sxs-lookup"><span data-stu-id="d1cb6-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="d1cb6-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1cb6-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
