---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 1c7f55bb3f84051326cd102c1c12a2d978a79f71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680294"
---
# <span data-ttu-id="705ff-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="705ff-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="705ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="705ff-102">SYNOPSIS</span></span>
<span data-ttu-id="705ff-103">Előre definiált Azure-címkék vagy-értékek törlése</span><span class="sxs-lookup"><span data-stu-id="705ff-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="705ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="705ff-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="705ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="705ff-105">DESCRIPTION</span></span>
<span data-ttu-id="705ff-106">A **Remove-AzureRmTag** parancsmag előre definiált Azure-címkéket és-értékeket töröl az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="705ff-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="705ff-107">Ha egy előre definiált címkéből szeretne bizonyos értékeket törölni, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="705ff-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="705ff-108">A **Remove-AzureRmTag** alapértelmezés szerint törli a megadott címkét és annak minden értékét. Az erőforrásokra vagy erőforrásokra jelenleg alkalmazott címke vagy érték nem törölhető.</span><span class="sxs-lookup"><span data-stu-id="705ff-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="705ff-109">Mielőtt a **Remove-AzureRmTag** használja, az Set-AzureRMResourceGroup parancsmag *címke* paraméterével törölheti az erőforrás vagy az erőforrás csoport címkéjét vagy értékét.</span><span class="sxs-lookup"><span data-stu-id="705ff-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="705ff-110">Az Azure címkék modul, amely **eltávolítja a-AzureRmTag** része, segíthet az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="705ff-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="705ff-111">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="705ff-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="705ff-112">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="705ff-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="705ff-113">Példák</span><span class="sxs-lookup"><span data-stu-id="705ff-113">EXAMPLES</span></span>

### <span data-ttu-id="705ff-114">Példa 1: előre definiált címke törlése</span><span class="sxs-lookup"><span data-stu-id="705ff-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="705ff-115">Ez a parancs törli a részleg és az összes erőforrása nevű előre definiált címkét.</span><span class="sxs-lookup"><span data-stu-id="705ff-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="705ff-116">Ha a címkét erőforrásokra vagy erőforrás-csoportokra alkalmazta, akkor a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="705ff-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="705ff-117">2. példa: az előre definiált címke értékének törlése</span><span class="sxs-lookup"><span data-stu-id="705ff-117">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="705ff-118">Ez a parancs törli az HumanResources értéket az előre definiált részleg címkéből.</span><span class="sxs-lookup"><span data-stu-id="705ff-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="705ff-119">Nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="705ff-119">It does not delete the tag.</span></span>
<span data-ttu-id="705ff-120">Ha az érték minden erőforrásra vagy erőforrás-csoportra érvényes, a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="705ff-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="705ff-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="705ff-121">PARAMETERS</span></span>

### <span data-ttu-id="705ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705ff-122">-DefaultProfile</span></span>
<span data-ttu-id="705ff-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="705ff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705ff-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="705ff-124">-Name</span></span>
<span data-ttu-id="705ff-125">A törlendő címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="705ff-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="705ff-126">A **Remove-AzureRmTag** alapértelmezés szerint eltávolítja a megadott címkét és annak minden értékét.</span><span class="sxs-lookup"><span data-stu-id="705ff-126">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="705ff-127">Ha törölni szeretné a kijelölt értékeket, de nem szeretné törölni a címkét, használja az *érték* paramétert.</span><span class="sxs-lookup"><span data-stu-id="705ff-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="705ff-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="705ff-128">-PassThru</span></span>
<span data-ttu-id="705ff-129">Egy olyan objektumot ad eredményül, amely a törölt címkét vagy az eredményül kapott címkét jelöli a törölt értékekkel.</span><span class="sxs-lookup"><span data-stu-id="705ff-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="705ff-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="705ff-130">-Value</span></span>
<span data-ttu-id="705ff-131">Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.</span><span class="sxs-lookup"><span data-stu-id="705ff-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="705ff-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="705ff-132">-Confirm</span></span>
<span data-ttu-id="705ff-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="705ff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705ff-134">-WhatIf</span></span>
<span data-ttu-id="705ff-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="705ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="705ff-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="705ff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705ff-137">CommonParameters</span></span>
<span data-ttu-id="705ff-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="705ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705ff-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705ff-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705ff-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="705ff-140">INPUTS</span></span>

### <span data-ttu-id="705ff-141">System. String</span><span class="sxs-lookup"><span data-stu-id="705ff-141">System.String</span></span>

### <span data-ttu-id="705ff-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="705ff-142">System.String[]</span></span>

### <span data-ttu-id="705ff-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="705ff-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="705ff-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="705ff-144">OUTPUTS</span></span>

### <span data-ttu-id="705ff-145">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="705ff-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="705ff-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="705ff-146">NOTES</span></span>

## <span data-ttu-id="705ff-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="705ff-147">RELATED LINKS</span></span>

[<span data-ttu-id="705ff-148">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="705ff-148">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="705ff-149">Új – AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="705ff-149">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


