---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: ff2911c1fd8e49e5057c13c086f68a2b3489ad2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187038"
---
# <span data-ttu-id="220b0-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="220b0-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="220b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="220b0-102">SYNOPSIS</span></span>
<span data-ttu-id="220b0-103">Sablon specifikációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="220b0-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="220b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="220b0-104">SYNTAX</span></span>

### <span data-ttu-id="220b0-105">FromJsonStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="220b0-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="220b0-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b0-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220b0-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b0-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220b0-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b0-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220b0-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b0-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220b0-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b0-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220b0-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b0-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220b0-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="220b0-112">DESCRIPTION</span></span>
<span data-ttu-id="220b0-113">Módosítja a Templace specifikációt. Ha a megadott nevű és/vagy adott verzióhoz tartozó specifikáció nem létezik, akkor a program hozza létre.</span><span class="sxs-lookup"><span data-stu-id="220b0-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="220b0-114">Ha módosítja egy sablon spec verziójának sablonjának tartalmát, a tartalmat nyers JSON-karakterláncból ( **UpdateVersionByNameFromJsonParameterSet** -set-set) vagy egy megadott JSON-fájlból (a **UpdateVersionByNameFromJsonFileParameterSet** paraméterrel) lehet megállapítani.</span><span class="sxs-lookup"><span data-stu-id="220b0-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="220b0-115">Példák</span><span class="sxs-lookup"><span data-stu-id="220b0-115">EXAMPLES</span></span>

### <span data-ttu-id="220b0-116">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="220b0-116">Example 1:</span></span>
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

<span data-ttu-id="220b0-117">A "myTemplateSpec" nevű sablon "v 1.0" verziójának módosítása.</span><span class="sxs-lookup"><span data-stu-id="220b0-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="220b0-118">A megadott verzió a verzió ARM-sablonjának tartalmát fogja $templateJson.</span><span class="sxs-lookup"><span data-stu-id="220b0-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="220b0-119">Ha a root sablon specifikációja és/vagy verziója még nem létezik, akkor létrejön a program.</span><span class="sxs-lookup"><span data-stu-id="220b0-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="220b0-120">**Megjegyzi**</span><span class="sxs-lookup"><span data-stu-id="220b0-120">**Notes:**</span></span> 

* <span data-ttu-id="220b0-121">A példában a kar sablon nem-op, mivel nem tartalmaz tényleges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="220b0-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="220b0-122">A hely csak akkor szükséges, ha a specifikáció nem létezik a sablonban.</span><span class="sxs-lookup"><span data-stu-id="220b0-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="220b0-123">2. példa:</span><span class="sxs-lookup"><span data-stu-id="220b0-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="220b0-124">A "myTemplateSpec" nevű sablon "v 2.0" verziójának módosítása.</span><span class="sxs-lookup"><span data-stu-id="220b0-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="220b0-125">A megadott verzió a verzió ARM-sablonjának tartalmát tartalmazó helyi myTemplateContent.jsfájlból származó tartalmat fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="220b0-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="220b0-126">Ha a root sablon specifikációja és/vagy verziója még nem létezik, akkor létrejön a program.</span><span class="sxs-lookup"><span data-stu-id="220b0-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="220b0-127">**Megjegyzés:** A hely csak akkor szükséges, ha a specifikáció nem létezik a sablonban.</span><span class="sxs-lookup"><span data-stu-id="220b0-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="220b0-128">3. példa:</span><span class="sxs-lookup"><span data-stu-id="220b0-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="220b0-129">Módosítja a "myTemplateSpec" nevű "myRG" erőforráscsoporthoz tartozó "" "nevű sablon leírását.</span><span class="sxs-lookup"><span data-stu-id="220b0-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="220b0-130">Ha a sablon specifikációja még nem létezik, akkor létrejön a program.</span><span class="sxs-lookup"><span data-stu-id="220b0-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="220b0-131">**Megjegyzés:** A hely csak akkor szükséges, ha a specifikáció nem létezik a sablonban.</span><span class="sxs-lookup"><span data-stu-id="220b0-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="220b0-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="220b0-132">PARAMETERS</span></span>

### <span data-ttu-id="220b0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220b0-133">-DefaultProfile</span></span>
<span data-ttu-id="220b0-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="220b0-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="220b0-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="220b0-135">-Description</span></span>
<span data-ttu-id="220b0-136">A sablon specifikációjának leírása.</span><span class="sxs-lookup"><span data-stu-id="220b0-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="220b0-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="220b0-137">-DisplayName</span></span>
<span data-ttu-id="220b0-138">A sablon megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="220b0-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="220b0-139">-Hely</span><span class="sxs-lookup"><span data-stu-id="220b0-139">-Location</span></span>
<span data-ttu-id="220b0-140">A sablon specifikációjának helye. Csak akkor kötelező, ha a specifikációban még nem szerepel a sablon.</span><span class="sxs-lookup"><span data-stu-id="220b0-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="220b0-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="220b0-141">-Name</span></span>
<span data-ttu-id="220b0-142">Annak a sablonnak a neve, amely a spec nevet adja.</span><span class="sxs-lookup"><span data-stu-id="220b0-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="220b0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220b0-143">-ResourceGroupName</span></span>
<span data-ttu-id="220b0-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="220b0-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="220b0-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="220b0-145">-ResourceId</span></span>
<span data-ttu-id="220b0-146">A sablon teljes értékű erőforrás-azonosítója (példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName})</span><span class="sxs-lookup"><span data-stu-id="220b0-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="220b0-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="220b0-147">-TemplateFile</span></span>
<span data-ttu-id="220b0-148">A helyi Azure Resource Manager template JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="220b0-148">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="220b0-149">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="220b0-149">-TemplateJson</span></span>
<span data-ttu-id="220b0-150">Az Azure Resource Manager sablon JSON-je.</span><span class="sxs-lookup"><span data-stu-id="220b0-150">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="220b0-151">-Verzió</span><span class="sxs-lookup"><span data-stu-id="220b0-151">-Version</span></span>
<span data-ttu-id="220b0-152">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="220b0-152">The version of the template spec.</span></span>

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

### <span data-ttu-id="220b0-153">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="220b0-153">-VersionDescription</span></span>
<span data-ttu-id="220b0-154">A verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="220b0-154">The description of the version.</span></span>

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

### <span data-ttu-id="220b0-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="220b0-155">-Confirm</span></span>
<span data-ttu-id="220b0-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="220b0-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220b0-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220b0-157">-WhatIf</span></span>
<span data-ttu-id="220b0-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="220b0-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="220b0-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="220b0-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220b0-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220b0-160">CommonParameters</span></span>
<span data-ttu-id="220b0-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="220b0-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220b0-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="220b0-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220b0-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="220b0-163">INPUTS</span></span>

### <span data-ttu-id="220b0-164">System. String</span><span class="sxs-lookup"><span data-stu-id="220b0-164">System.String</span></span>

## <span data-ttu-id="220b0-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="220b0-165">OUTPUTS</span></span>

### <span data-ttu-id="220b0-166">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="220b0-166">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="220b0-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="220b0-167">NOTES</span></span>

## <span data-ttu-id="220b0-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="220b0-168">RELATED LINKS</span></span>
