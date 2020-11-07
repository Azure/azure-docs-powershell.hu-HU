---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: f51411c4683a79283ad5e0a73554f6db3ce7e52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672000"
---
# <span data-ttu-id="ff325-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ff325-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="ff325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff325-102">SYNOPSIS</span></span>
<span data-ttu-id="ff325-103">Előre definiált Azure-címkék vagy-értékek törlése</span><span class="sxs-lookup"><span data-stu-id="ff325-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff325-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff325-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff325-105">DESCRIPTION</span></span>
<span data-ttu-id="ff325-106">A **Remove-AzureRmTag** parancsmag előre definiált Azure-címkéket és-értékeket töröl az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="ff325-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="ff325-107">Ha egy előre definiált címkéből szeretne bizonyos értékeket törölni, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="ff325-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="ff325-108">A **Remove-AzureRmTag** alapértelmezés szerint törli a megadott címkét és annak minden értékét. Az erőforrásokra vagy erőforrásokra jelenleg alkalmazott címke vagy érték nem törölhető.</span><span class="sxs-lookup"><span data-stu-id="ff325-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="ff325-109">Mielőtt a **Remove-AzureRmTag** használja, az Set-AzureRMResourceGroup parancsmag *címke* paraméterével törölheti az erőforrás vagy az erőforrás csoport címkéjét vagy értékét.</span><span class="sxs-lookup"><span data-stu-id="ff325-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="ff325-110">Az Azure címkék modul, amely **eltávolítja a-AzureRmTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="ff325-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="ff325-111">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="ff325-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="ff325-112">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="ff325-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="ff325-113">Ha az előfizetéshez tartozik egy előre definiált címke, az előfizetésben nem alkalmazhat definiálatlan címkéket vagy értékeket az előfizetésben szereplő erőforrásokra vagy erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="ff325-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="ff325-114">Példák</span><span class="sxs-lookup"><span data-stu-id="ff325-114">EXAMPLES</span></span>

### <span data-ttu-id="ff325-115">Példa 1: előre definiált címke törlése</span><span class="sxs-lookup"><span data-stu-id="ff325-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="ff325-116">Ez a parancs törli a részleg és az összes erőforrása nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="ff325-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="ff325-117">Ha a címkét erőforrásokra vagy erőforrás-csoportokra alkalmazta, akkor a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="ff325-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="ff325-118">2. példa: az előre definiált címke értékének törlése</span><span class="sxs-lookup"><span data-stu-id="ff325-118">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="ff325-119">Ez a parancs törli az HumanResources értéket az előre definiált részleg címkéből.</span><span class="sxs-lookup"><span data-stu-id="ff325-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="ff325-120">Nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="ff325-120">It does not delete the tag.</span></span>
<span data-ttu-id="ff325-121">Ha az érték minden erőforrásra vagy erőforrás-csoportra érvényes, a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="ff325-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="ff325-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff325-122">PARAMETERS</span></span>

### <span data-ttu-id="ff325-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff325-123">-DefaultProfile</span></span>
<span data-ttu-id="ff325-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff325-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff325-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff325-125">-Name</span></span>
<span data-ttu-id="ff325-126">A törlendő címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff325-126">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="ff325-127">A **Remove-AzureRmTag** alapértelmezés szerint eltávolítja a megadott címkét és annak minden értékét.</span><span class="sxs-lookup"><span data-stu-id="ff325-127">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="ff325-128">Ha törölni szeretné a kijelölt értékeket, de nem szeretné törölni a címkét, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="ff325-128">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="ff325-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff325-129">-PassThru</span></span>
<span data-ttu-id="ff325-130">Egy olyan objektumot ad eredményül, amely a törölt címkét vagy az eredményül kapott címkét jelöli a törölt értékekkel.</span><span class="sxs-lookup"><span data-stu-id="ff325-130">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="ff325-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="ff325-131">-Value</span></span>
<span data-ttu-id="ff325-132">Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="ff325-132">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff325-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff325-133">-Confirm</span></span>
<span data-ttu-id="ff325-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff325-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff325-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff325-135">-WhatIf</span></span>
<span data-ttu-id="ff325-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff325-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff325-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff325-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff325-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff325-138">CommonParameters</span></span>
<span data-ttu-id="ff325-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff325-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff325-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff325-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff325-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff325-141">INPUTS</span></span>

### <span data-ttu-id="ff325-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="ff325-142">None</span></span>

## <span data-ttu-id="ff325-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff325-143">OUTPUTS</span></span>

### <span data-ttu-id="ff325-144">Nincs vagy Microsoft. Azure. Command. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="ff325-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="ff325-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff325-145">NOTES</span></span>

## <span data-ttu-id="ff325-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff325-146">RELATED LINKS</span></span>

[<span data-ttu-id="ff325-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ff325-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="ff325-148">Új – AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ff325-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


