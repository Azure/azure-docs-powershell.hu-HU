---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479209"
---
# <span data-ttu-id="28cd9-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="28cd9-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="28cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="28cd9-103">Sablon specifikációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="28cd9-103">Removes a Template Spec</span></span>

## <span data-ttu-id="28cd9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28cd9-104">SYNTAX</span></span>

### <span data-ttu-id="28cd9-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28cd9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cd9-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28cd9-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cd9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28cd9-107">DESCRIPTION</span></span>
<span data-ttu-id="28cd9-108">Eltávolít egy adott sablon specifikációját. Ha a **version -Version paraméter** meg van adva, csak a megadott verzió lesz eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="28cd9-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="28cd9-109">Ha nem ad meg konkrét verziót, a Sablon specifikációja és annak összes verziója törlődik.</span><span class="sxs-lookup"><span data-stu-id="28cd9-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="28cd9-110">Ha a **-Force** jelölő jelen van, nem lesz eltávolításra vonatkozó megerősítő üzenet.</span><span class="sxs-lookup"><span data-stu-id="28cd9-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="28cd9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28cd9-111">EXAMPLES</span></span>

### <span data-ttu-id="28cd9-112">1. példa: Egy adott verzió eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="28cd9-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="28cd9-113">Eltávolítja a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="28cd9-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="28cd9-114">2. példa: Adott verzió eltávolítása erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="28cd9-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="28cd9-115">Eltávolítja a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját az előfizetés alazonosítójának "myRG" \{ erőforráscsoportján \} belül.</span><span class="sxs-lookup"><span data-stu-id="28cd9-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="28cd9-116">3. példa: Sablon specifikációjának és minden verziójának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="28cd9-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="28cd9-117">Eltávolítja a "MyTemplateSpec" nevű sablon specifikációját és annak összes verzióját a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="28cd9-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="28cd9-118">3. példa: Sablon specifikációjának és minden verziójának eltávolítása erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="28cd9-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="28cd9-119">Eltávolítja a "MyTemplateSpec" nevű sablont és annak összes verzióját az előfizetés alazonosítójának "myRG" \{ erőforráscsoportján \} belül.</span><span class="sxs-lookup"><span data-stu-id="28cd9-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="28cd9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28cd9-120">PARAMETERS</span></span>

### <span data-ttu-id="28cd9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cd9-121">-DefaultProfile</span></span>
<span data-ttu-id="28cd9-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28cd9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28cd9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="28cd9-123">-Force</span></span>
<span data-ttu-id="28cd9-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28cd9-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28cd9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="28cd9-125">-Name</span></span>
<span data-ttu-id="28cd9-126">A sablon specifikációjának neve.</span><span class="sxs-lookup"><span data-stu-id="28cd9-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="28cd9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cd9-127">-ResourceGroupName</span></span>
<span data-ttu-id="28cd9-128">A sablon specifikációjának erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="28cd9-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="28cd9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28cd9-129">-ResourceId</span></span>
<span data-ttu-id="28cd9-130">A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="28cd9-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="28cd9-131">-Version</span><span class="sxs-lookup"><span data-stu-id="28cd9-131">-Version</span></span>
<span data-ttu-id="28cd9-132">A törölni kívánt sablonverzió.</span><span class="sxs-lookup"><span data-stu-id="28cd9-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="28cd9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28cd9-133">-Confirm</span></span>
<span data-ttu-id="28cd9-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="28cd9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cd9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cd9-135">-WhatIf</span></span>
<span data-ttu-id="28cd9-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="28cd9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28cd9-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28cd9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cd9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cd9-138">CommonParameters</span></span>
<span data-ttu-id="28cd9-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cd9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cd9-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28cd9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cd9-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28cd9-141">INPUTS</span></span>

### <span data-ttu-id="28cd9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="28cd9-142">System.String</span></span>

## <span data-ttu-id="28cd9-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28cd9-143">OUTPUTS</span></span>

### <span data-ttu-id="28cd9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28cd9-144">System.Boolean</span></span>

## <span data-ttu-id="28cd9-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28cd9-145">NOTES</span></span>

## <span data-ttu-id="28cd9-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28cd9-146">RELATED LINKS</span></span>
