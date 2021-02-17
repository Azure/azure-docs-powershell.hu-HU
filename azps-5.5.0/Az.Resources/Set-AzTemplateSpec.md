---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205966"
---
# <span data-ttu-id="f3b6b-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f3b6b-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="f3b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b6b-103">Módosítja a sablon specifikációját.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="f3b6b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3b6b-104">SYNTAX</span></span>

### <span data-ttu-id="f3b6b-105">FromJsonStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3b6b-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3b6b-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b6b-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b6b-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b6b-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b6b-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b6b-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b6b-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b6b-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b6b-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b6b-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b6b-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b6b-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3b6b-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3b6b-112">DESCRIPTION</span></span>
<span data-ttu-id="f3b6b-113">Módosít egy Templace Spec et. Ha a megadott nevű és/vagy adott verziójú sablon specifikációja még nem létezik, akkor létrejön.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="f3b6b-114">Ha módosítja egy sablon specifikációs verziójának ARM-sablonjának tartalmát, a tartalom vagy egy nyers JSON karakterláncból (az **UpdateVersionByNameFromJsonParameterSet** paraméterkészletből) vagy egy megadott JSON-fájlból **(az UpdateVersionByNameFromJsonFileParameterSet** paraméterkészletből) is lehet.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="f3b6b-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3b6b-115">EXAMPLES</span></span>

### <span data-ttu-id="f3b6b-116">1. példa:</span><span class="sxs-lookup"><span data-stu-id="f3b6b-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="f3b6b-117">Módosítja a "myTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="f3b6b-118">A megadott verzió a $templateJson sablon tartalmaként ARM lesz.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="f3b6b-119">Ha a fő sablon specifikációja és/vagy verziója még nem létezik, a rendszer létrehoz egy sablont.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="f3b6b-120">**Megjegyzések:**</span><span class="sxs-lookup"><span data-stu-id="f3b6b-120">**Notes:**</span></span> 

* <span data-ttu-id="f3b6b-121">A ARM sablon nem művelet, mivel nem tartalmaz tényleges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="f3b6b-122">Hely csak akkor szükséges, ha a sablon specifikációja még nem létezik</span><span class="sxs-lookup"><span data-stu-id="f3b6b-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="f3b6b-123">2. példa:</span><span class="sxs-lookup"><span data-stu-id="f3b6b-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="f3b6b-124">Módosítja a "myTemplateSpec" nevű sablon specifikációjának "v2.0" verzióját.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="f3b6b-125">A megadott verzióban a helyi fájl tartalma "be van myTemplateContent.js" lesz, mint a ARM sablon tartalma.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="f3b6b-126">Ha a fő sablon specifikációja és/vagy verziója még nem létezik, a rendszer létrehoz egy sablont.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="f3b6b-127">**Megjegyzés:** Hely csak akkor szükséges, ha a sablon specifikációja még nem létezik</span><span class="sxs-lookup"><span data-stu-id="f3b6b-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="f3b6b-128">3. példa:</span><span class="sxs-lookup"><span data-stu-id="f3b6b-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="f3b6b-129">Módosítja a "myTemplateSpec" nevű sablon specifikációjának leírását a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="f3b6b-130">Ha a Sablon specifikációja még nem létezik, a sablon létrejön.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="f3b6b-131">**Megjegyzés:** Hely csak akkor szükséges, ha a sablon specifikációja még nem létezik</span><span class="sxs-lookup"><span data-stu-id="f3b6b-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="f3b6b-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3b6b-132">PARAMETERS</span></span>

### <span data-ttu-id="f3b6b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b6b-133">-DefaultProfile</span></span>
<span data-ttu-id="f3b6b-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3b6b-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f3b6b-135">-Description</span></span>
<span data-ttu-id="f3b6b-136">A sablon specifikációjának leírása.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3b6b-137">-DisplayName</span></span>
<span data-ttu-id="f3b6b-138">A sablon specifikációjának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-139">-Location</span><span class="sxs-lookup"><span data-stu-id="f3b6b-139">-Location</span></span>
<span data-ttu-id="f3b6b-140">A sablon specifikációjának helye. Csak akkor szükséges, ha a sablon specifikációja még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-141">-Name</span><span class="sxs-lookup"><span data-stu-id="f3b6b-141">-Name</span></span>
<span data-ttu-id="f3b6b-142">A sablon specifikációjának neve.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b6b-143">-ResourceGroupName</span></span>
<span data-ttu-id="f3b6b-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3b6b-145">-ResourceId</span></span>
<span data-ttu-id="f3b6b-146">A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="f3b6b-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3b6b-147">-Tag</span></span>
<span data-ttu-id="f3b6b-148">Címkék hashtable for the template spec and/or version</span><span class="sxs-lookup"><span data-stu-id="f3b6b-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f3b6b-149">-TemplateFile</span></span>
<span data-ttu-id="f3b6b-150">A helyi Azure Resource Manager-sablon JSON-fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="f3b6b-151">-TemplateJson</span></span>
<span data-ttu-id="f3b6b-152">Az Azure Resource Manager JSON sablonja.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-153">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f3b6b-153">-Version</span></span>
<span data-ttu-id="f3b6b-154">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="f3b6b-155">-VersionDescription</span></span>
<span data-ttu-id="f3b6b-156">A verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b6b-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3b6b-157">-Confirm</span></span>
<span data-ttu-id="f3b6b-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b6b-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b6b-159">-WhatIf</span></span>
<span data-ttu-id="f3b6b-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3b6b-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b6b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b6b-162">CommonParameters</span></span>
<span data-ttu-id="f3b6b-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b6b-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3b6b-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b6b-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3b6b-165">INPUTS</span></span>

### <span data-ttu-id="f3b6b-166">System.String</span><span class="sxs-lookup"><span data-stu-id="f3b6b-166">System.String</span></span>

## <span data-ttu-id="f3b6b-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3b6b-167">OUTPUTS</span></span>

### <span data-ttu-id="f3b6b-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f3b6b-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="f3b6b-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3b6b-169">NOTES</span></span>

## <span data-ttu-id="f3b6b-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3b6b-170">RELATED LINKS</span></span>
