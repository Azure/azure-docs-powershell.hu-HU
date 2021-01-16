---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354030"
---
# <span data-ttu-id="87385-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="87385-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="87385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87385-102">SYNOPSIS</span></span>
<span data-ttu-id="87385-103">Módosítja a sablon specifikációját.</span><span class="sxs-lookup"><span data-stu-id="87385-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="87385-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87385-104">SYNTAX</span></span>

### <span data-ttu-id="87385-105">FromJsonStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87385-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87385-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87385-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87385-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="87385-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87385-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="87385-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87385-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87385-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87385-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="87385-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87385-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="87385-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87385-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87385-112">DESCRIPTION</span></span>
<span data-ttu-id="87385-113">Módosítja az Templace Spec függvényt. Ha a megadott nevű és/vagy adott verziójú sablon specifikációja még nem létezik, akkor létrejön.</span><span class="sxs-lookup"><span data-stu-id="87385-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="87385-114">Ha módosítja egy sablon specifikációs verziójának ARM-sablonjának tartalmát, a tartalom vagy egy nyers JSON karakterláncból (az **UpdateVersionByNameFromJsonParameterSet** paraméterkészletből) vagy egy megadott JSON-fájlból **(az UpdateVersionByNameFromJsonFileParameterSet** paraméterkészletből) is lehet.</span><span class="sxs-lookup"><span data-stu-id="87385-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="87385-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87385-115">EXAMPLES</span></span>

### <span data-ttu-id="87385-116">1. példa:</span><span class="sxs-lookup"><span data-stu-id="87385-116">Example 1:</span></span>
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

<span data-ttu-id="87385-117">Módosítja a "myTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját.</span><span class="sxs-lookup"><span data-stu-id="87385-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="87385-118">A megadott verzió a $templateJson sablon tartalmának ARM lesz.</span><span class="sxs-lookup"><span data-stu-id="87385-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="87385-119">Ha a fő sablon specifikációja és/vagy verziója még nem létezik, a rendszer létrehoz egy sablont.</span><span class="sxs-lookup"><span data-stu-id="87385-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="87385-120">**Megjegyzések:**</span><span class="sxs-lookup"><span data-stu-id="87385-120">**Notes:**</span></span> 

* <span data-ttu-id="87385-121">A ARM sablon nem művelet, mivel nem tartalmaz tényleges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="87385-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="87385-122">Hely csak akkor szükséges, ha a sablon specifikációja még nem létezik</span><span class="sxs-lookup"><span data-stu-id="87385-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="87385-123">2. példa:</span><span class="sxs-lookup"><span data-stu-id="87385-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="87385-124">Módosítja a "myTemplateSpec" nevű sablon specifikációjának "v2.0" verzióját.</span><span class="sxs-lookup"><span data-stu-id="87385-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="87385-125">A megadott verzióban a helyi fájl tartalma "be van myTemplateContent.js" lesz, mint a ARM sablon tartalma.</span><span class="sxs-lookup"><span data-stu-id="87385-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="87385-126">Ha a fő sablon specifikációja és/vagy verziója még nem létezik, a rendszer létrehoz egy sablont.</span><span class="sxs-lookup"><span data-stu-id="87385-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="87385-127">**Megjegyzés:** Hely csak akkor szükséges, ha a sablon specifikációja még nem létezik</span><span class="sxs-lookup"><span data-stu-id="87385-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="87385-128">3. példa:</span><span class="sxs-lookup"><span data-stu-id="87385-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="87385-129">Módosítja a "myTemplateSpec" nevű sablon specifikációjának leírását a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="87385-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="87385-130">Ha a Sablon specifikációja még nem létezik, a sablon létrejön.</span><span class="sxs-lookup"><span data-stu-id="87385-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="87385-131">**Megjegyzés:** Hely csak akkor szükséges, ha a sablon specifikációja még nem létezik</span><span class="sxs-lookup"><span data-stu-id="87385-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="87385-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87385-132">PARAMETERS</span></span>

### <span data-ttu-id="87385-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87385-133">-DefaultProfile</span></span>
<span data-ttu-id="87385-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87385-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87385-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="87385-135">-Description</span></span>
<span data-ttu-id="87385-136">A sablon specifikációjának leírása.</span><span class="sxs-lookup"><span data-stu-id="87385-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="87385-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="87385-137">-DisplayName</span></span>
<span data-ttu-id="87385-138">A sablon specifikációjának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="87385-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="87385-139">-Location</span><span class="sxs-lookup"><span data-stu-id="87385-139">-Location</span></span>
<span data-ttu-id="87385-140">A sablon specifikációjának helye. Csak akkor szükséges, ha a sablon specifikációja még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="87385-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="87385-141">-Name</span><span class="sxs-lookup"><span data-stu-id="87385-141">-Name</span></span>
<span data-ttu-id="87385-142">A sablon specifikációjának neve.</span><span class="sxs-lookup"><span data-stu-id="87385-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="87385-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87385-143">-ResourceGroupName</span></span>
<span data-ttu-id="87385-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87385-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="87385-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87385-145">-ResourceId</span></span>
<span data-ttu-id="87385-146">A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="87385-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="87385-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="87385-147">-Tag</span></span>
<span data-ttu-id="87385-148">Címkék hashtable for the template spec and/or version</span><span class="sxs-lookup"><span data-stu-id="87385-148">Hashtable of tags for the template spec and/or version</span></span>

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

### <span data-ttu-id="87385-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="87385-149">-TemplateFile</span></span>
<span data-ttu-id="87385-150">A helyi Azure Resource Manager-sablon JSON-fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="87385-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="87385-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="87385-151">-TemplateJson</span></span>
<span data-ttu-id="87385-152">Az Azure Resource Manager JSON sablonja.</span><span class="sxs-lookup"><span data-stu-id="87385-152">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="87385-153">-Version</span><span class="sxs-lookup"><span data-stu-id="87385-153">-Version</span></span>
<span data-ttu-id="87385-154">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="87385-154">The version of the template spec.</span></span>

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

### <span data-ttu-id="87385-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="87385-155">-VersionDescription</span></span>
<span data-ttu-id="87385-156">A verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="87385-156">The description of the version.</span></span>

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

### <span data-ttu-id="87385-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87385-157">-Confirm</span></span>
<span data-ttu-id="87385-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="87385-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87385-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87385-159">-WhatIf</span></span>
<span data-ttu-id="87385-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="87385-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87385-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87385-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87385-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87385-162">CommonParameters</span></span>
<span data-ttu-id="87385-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87385-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87385-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87385-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87385-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87385-165">INPUTS</span></span>

### <span data-ttu-id="87385-166">System.String</span><span class="sxs-lookup"><span data-stu-id="87385-166">System.String</span></span>

## <span data-ttu-id="87385-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87385-167">OUTPUTS</span></span>

### <span data-ttu-id="87385-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="87385-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="87385-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87385-169">NOTES</span></span>

## <span data-ttu-id="87385-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87385-170">RELATED LINKS</span></span>
