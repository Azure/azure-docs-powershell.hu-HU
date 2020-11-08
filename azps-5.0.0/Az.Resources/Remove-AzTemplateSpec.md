---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195534"
---
# <span data-ttu-id="7cf2d-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="7cf2d-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="7cf2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf2d-103">Sablon eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7cf2d-103">Removes a Template Spec</span></span>

## <span data-ttu-id="7cf2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cf2d-104">SYNTAX</span></span>

### <span data-ttu-id="7cf2d-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cf2d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf2d-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf2d-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf2d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cf2d-107">DESCRIPTION</span></span>
<span data-ttu-id="7cf2d-108">A megadott sablon eltávolítása. Ha a verziószám **paramétert** adja meg, a program csak a megadott verziót távolítja el.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="7cf2d-109">Ha nincs megadva konkrét verzió, a program eltávolítja a sablont, a specifikációt és annak minden verzióját.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="7cf2d-110">Ha a **-erő** jelölője látható, akkor a program nem kér megerősítést az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="7cf2d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7cf2d-111">EXAMPLES</span></span>

### <span data-ttu-id="7cf2d-112">1. példa: adott verzió eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="7cf2d-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="7cf2d-113">Eltávolítja a "MyTemplateSpec" nevű "myRG" erőforráscsoporthoz tartozó "v 1.0" nevű sablont.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="7cf2d-114">2. példa: adott verzió erőforrás-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7cf2d-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="7cf2d-115">Eltávolítja a "MyTemplateSpec" nevű "myRG" nevű erőforráscsoport "v 1.0" verzióját az előfizetés \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="7cf2d-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="7cf2d-116">3. példa: a sablon specifikációjának és minden verziójának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="7cf2d-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="7cf2d-117">Eltávolítja a ' MyTemplateSpec ' nevű sablont és annak minden verzióját az "myRG" erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="7cf2d-118">3. példa: a sablon és az összes verzió erőforrás-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7cf2d-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="7cf2d-119">Eltávolítja a "MyTemplateSpec" nevű sablont, valamint az előfizetés subId erőforráscsoport "myRG" csoportjába tartozó összes verziót \{ \} .</span><span class="sxs-lookup"><span data-stu-id="7cf2d-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="7cf2d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cf2d-120">PARAMETERS</span></span>

### <span data-ttu-id="7cf2d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf2d-121">-DefaultProfile</span></span>
<span data-ttu-id="7cf2d-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf2d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf2d-123">-Force</span></span>
<span data-ttu-id="7cf2d-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-124">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cf2d-125">-Name</span></span>
<span data-ttu-id="7cf2d-126">Annak a sablonnak a neve, amely a spec nevet adja.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="7cf2d-128">A sablon specifikációja erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf2d-129">-ResourceId</span></span>
<span data-ttu-id="7cf2d-130">A sablon teljes értékű erőforrás-azonosítója (példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName})</span><span class="sxs-lookup"><span data-stu-id="7cf2d-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7cf2d-131">-Version</span></span>
<span data-ttu-id="7cf2d-132">A törlendő sablon verziószáma.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cf2d-133">-Confirm</span></span>
<span data-ttu-id="7cf2d-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf2d-135">-WhatIf</span></span>
<span data-ttu-id="7cf2d-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cf2d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf2d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf2d-138">CommonParameters</span></span>
<span data-ttu-id="7cf2d-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cf2d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf2d-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7cf2d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf2d-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf2d-141">INPUTS</span></span>

### <span data-ttu-id="7cf2d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf2d-142">System.String</span></span>

## <span data-ttu-id="7cf2d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf2d-143">OUTPUTS</span></span>

### <span data-ttu-id="7cf2d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cf2d-144">System.Boolean</span></span>

## <span data-ttu-id="7cf2d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cf2d-145">NOTES</span></span>

## <span data-ttu-id="7cf2d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cf2d-146">RELATED LINKS</span></span>
