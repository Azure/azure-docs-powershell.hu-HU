---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466433"
---
# <span data-ttu-id="2a104-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2a104-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="2a104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a104-102">SYNOPSIS</span></span>
<span data-ttu-id="2a104-103">Létrehoz egy új sablon specifikációt.</span><span class="sxs-lookup"><span data-stu-id="2a104-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="2a104-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a104-104">SYNTAX</span></span>

### <span data-ttu-id="2a104-105">FromJsonStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a104-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a104-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a104-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a104-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a104-107">DESCRIPTION</span></span>
<span data-ttu-id="2a104-108">Létrehoz egy új Sablon specifikációs verziót a megadott ARM sablontartalommal.</span><span class="sxs-lookup"><span data-stu-id="2a104-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="2a104-109">A tartalom egy nyers JSON-karakterláncból **(FromJsonStringParameterSet** paraméterkészlet használatával) vagy egy megadott JSON-fájlból **(FromJsonFileParameterSet** paraméterkészlet használatával) is lehet.</span><span class="sxs-lookup"><span data-stu-id="2a104-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="2a104-110">Ha a fő sablon specifikációja még nem létezik, akkor a Sablon specifikációja verzióval együtt jön létre.</span><span class="sxs-lookup"><span data-stu-id="2a104-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="2a104-111">Ha a Sablon specifikációja már létezik a megadott névvel, akkor a megadott verzió frissül (a többi meglévő verzió megőrzve marad).</span><span class="sxs-lookup"><span data-stu-id="2a104-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="2a104-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a104-112">EXAMPLES</span></span>

### <span data-ttu-id="2a104-113">1. példa:</span><span class="sxs-lookup"><span data-stu-id="2a104-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="2a104-114">Létrehoz egy új "v1.0" sablonverziót a "myTemplateSpec" nevű sablon specifikációban.</span><span class="sxs-lookup"><span data-stu-id="2a104-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="2a104-115">A megadott verzió a $templateJson sablon tartalmának ARM lesz.</span><span class="sxs-lookup"><span data-stu-id="2a104-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="2a104-116">**Megjegyzés:** A ARM sablon nem művelet, mivel nem tartalmaz tényleges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2a104-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="2a104-117">2. példa:</span><span class="sxs-lookup"><span data-stu-id="2a104-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="2a104-118">Létrehoz egy új "v2.0" sablonverziót a "myTemplateSpec" nevű sablon specifikációban.</span><span class="sxs-lookup"><span data-stu-id="2a104-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="2a104-119">A megadott verzióban a helyi fájl tartalma "be van myTemplateContent.js" lesz, mint a ARM sablon tartalma.</span><span class="sxs-lookup"><span data-stu-id="2a104-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="2a104-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a104-120">PARAMETERS</span></span>

### <span data-ttu-id="2a104-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a104-121">-DefaultProfile</span></span>
<span data-ttu-id="2a104-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a104-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a104-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2a104-123">-Description</span></span>
<span data-ttu-id="2a104-124">A sablon specifikációjának leírása.</span><span class="sxs-lookup"><span data-stu-id="2a104-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="2a104-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a104-125">-DisplayName</span></span>
<span data-ttu-id="2a104-126">A sablon specifikációjának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="2a104-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="2a104-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2a104-127">-Force</span></span>
<span data-ttu-id="2a104-128">Ne kérjen megerősítést egy meglévő verzió felülírásakor.</span><span class="sxs-lookup"><span data-stu-id="2a104-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="2a104-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2a104-129">-Location</span></span>
<span data-ttu-id="2a104-130">A sablon specifikációjának helye. Csak akkor szükséges, ha a sablon specifikációja még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="2a104-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="2a104-131">-Name</span><span class="sxs-lookup"><span data-stu-id="2a104-131">-Name</span></span>
<span data-ttu-id="2a104-132">A sablon specifikációjának neve.</span><span class="sxs-lookup"><span data-stu-id="2a104-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a104-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a104-133">-ResourceGroupName</span></span>
<span data-ttu-id="2a104-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a104-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a104-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a104-135">-Tag</span></span>
<span data-ttu-id="2a104-136">Címkék hashtable for the new template spec resource(s).</span><span class="sxs-lookup"><span data-stu-id="2a104-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="2a104-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2a104-137">-TemplateFile</span></span>
<span data-ttu-id="2a104-138">A helyi Azure Resource Manager-sablon JSON-fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2a104-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a104-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="2a104-139">-TemplateJson</span></span>
<span data-ttu-id="2a104-140">Az Azure Resource Manager JSON sablonja.</span><span class="sxs-lookup"><span data-stu-id="2a104-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a104-141">-Version</span><span class="sxs-lookup"><span data-stu-id="2a104-141">-Version</span></span>
<span data-ttu-id="2a104-142">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="2a104-142">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a104-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="2a104-143">-VersionDescription</span></span>
<span data-ttu-id="2a104-144">A verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="2a104-144">The description of the version.</span></span>

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

### <span data-ttu-id="2a104-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a104-145">-Confirm</span></span>
<span data-ttu-id="2a104-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2a104-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a104-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a104-147">-WhatIf</span></span>
<span data-ttu-id="2a104-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2a104-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a104-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a104-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a104-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a104-150">CommonParameters</span></span>
<span data-ttu-id="2a104-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a104-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a104-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a104-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a104-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a104-153">INPUTS</span></span>

### <span data-ttu-id="2a104-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2a104-154">System.String</span></span>

## <span data-ttu-id="2a104-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a104-155">OUTPUTS</span></span>

### <span data-ttu-id="2a104-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2a104-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="2a104-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a104-157">NOTES</span></span>

## <span data-ttu-id="2a104-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a104-158">RELATED LINKS</span></span>
