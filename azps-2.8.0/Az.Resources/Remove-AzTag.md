---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: f9afc10613024d99cfa6b03b260324b3e5d22586
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838109"
---
# <span data-ttu-id="6ca31-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="6ca31-101">Remove-AzTag</span></span>

## <span data-ttu-id="6ca31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ca31-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca31-103">Előre definiált Azure-címkék vagy-értékek törlése</span><span class="sxs-lookup"><span data-stu-id="6ca31-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="6ca31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ca31-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ca31-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca31-106">A **Remove-AzTag** parancsmag előre definiált Azure-címkéket és-értékeket töröl az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="6ca31-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="6ca31-107">Ha egy előre definiált címkéből szeretne bizonyos értékeket törölni, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6ca31-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="6ca31-108">A **Remove-AzTag** alapértelmezés szerint törli a megadott címkét és annak minden értékét. Az erőforrásokra vagy erőforrásokra jelenleg alkalmazott címke vagy érték nem törölhető.</span><span class="sxs-lookup"><span data-stu-id="6ca31-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="6ca31-109">Mielőtt a **Remove-AzTag** használja, az Set-AzResourceGroup parancsmag *címke* paraméterével törölheti az erőforrás vagy az erőforrás csoport címkéjét vagy értékét.</span><span class="sxs-lookup"><span data-stu-id="6ca31-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="6ca31-110">Az Azure címkék modul, amely **eltávolítja a-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="6ca31-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="6ca31-111">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="6ca31-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="6ca31-112">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="6ca31-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="6ca31-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6ca31-113">EXAMPLES</span></span>

### <span data-ttu-id="6ca31-114">Példa 1: előre definiált címke törlése</span><span class="sxs-lookup"><span data-stu-id="6ca31-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="6ca31-115">Ez a parancs törli a részleg és az összes erőforrása nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="6ca31-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="6ca31-116">Ha a címkét erőforrásokra vagy erőforrás-csoportokra alkalmazta, akkor a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="6ca31-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="6ca31-117">2. példa: az előre definiált címke értékének törlése</span><span class="sxs-lookup"><span data-stu-id="6ca31-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="6ca31-118">Ez a parancs törli az HumanResources értéket az előre definiált részleg címkéből.</span><span class="sxs-lookup"><span data-stu-id="6ca31-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="6ca31-119">Nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="6ca31-119">It does not delete the tag.</span></span>
<span data-ttu-id="6ca31-120">Ha az érték minden erőforrásra vagy erőforrás-csoportra érvényes, a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="6ca31-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="6ca31-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ca31-121">PARAMETERS</span></span>

### <span data-ttu-id="6ca31-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca31-122">-DefaultProfile</span></span>
<span data-ttu-id="6ca31-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ca31-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca31-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ca31-124">-Name</span></span>
<span data-ttu-id="6ca31-125">A törlendő címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ca31-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="6ca31-126">A **Remove-AzTag** alapértelmezés szerint eltávolítja a megadott címkét és annak minden értékét.</span><span class="sxs-lookup"><span data-stu-id="6ca31-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="6ca31-127">Ha törölni szeretné a kijelölt értékeket, de nem szeretné törölni a címkét, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6ca31-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="6ca31-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ca31-128">-PassThru</span></span>
<span data-ttu-id="6ca31-129">Egy olyan objektumot ad eredményül, amely a törölt címkét vagy az eredményül kapott címkét jelöli a törölt értékekkel.</span><span class="sxs-lookup"><span data-stu-id="6ca31-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca31-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="6ca31-130">-Value</span></span>
<span data-ttu-id="6ca31-131">Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="6ca31-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca31-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ca31-132">-Confirm</span></span>
<span data-ttu-id="6ca31-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ca31-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca31-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca31-134">-WhatIf</span></span>
<span data-ttu-id="6ca31-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ca31-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca31-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ca31-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca31-137">CommonParameters</span></span>
<span data-ttu-id="6ca31-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ca31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca31-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca31-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca31-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ca31-140">INPUTS</span></span>

### <span data-ttu-id="6ca31-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca31-141">System.String</span></span>

### <span data-ttu-id="6ca31-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="6ca31-142">System.String[]</span></span>

### <span data-ttu-id="6ca31-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ca31-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ca31-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ca31-144">OUTPUTS</span></span>

### <span data-ttu-id="6ca31-145">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="6ca31-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="6ca31-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ca31-146">NOTES</span></span>

## <span data-ttu-id="6ca31-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ca31-147">RELATED LINKS</span></span>

[<span data-ttu-id="6ca31-148">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="6ca31-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="6ca31-149">Új – AzTag</span><span class="sxs-lookup"><span data-stu-id="6ca31-149">New-AzTag</span></span>](./New-AzTag.md)


