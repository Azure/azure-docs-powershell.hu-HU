---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187041"
---
# <span data-ttu-id="86fdc-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="86fdc-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="86fdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="86fdc-103">Új sablon létrehozása: spec.</span><span class="sxs-lookup"><span data-stu-id="86fdc-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="86fdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86fdc-104">SYNTAX</span></span>

### <span data-ttu-id="86fdc-105">FromJsonStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86fdc-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86fdc-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="86fdc-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86fdc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86fdc-107">DESCRIPTION</span></span>
<span data-ttu-id="86fdc-108">Új sablont hoz létre a megadott ARM-tartalommal.</span><span class="sxs-lookup"><span data-stu-id="86fdc-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="86fdc-109">A tartalom nyers JSON-karakterláncból ( **FromJsonStringParameterSet** -set) vagy egy megadott JSON-fájlból (a **FromJsonFileParameterSet** paraméterrel van beállítva) származhat.</span><span class="sxs-lookup"><span data-stu-id="86fdc-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="86fdc-110">Ha a root sablon specifikációja még nem létezik, akkor az a sablon spec verzióval együtt jön létre.</span><span class="sxs-lookup"><span data-stu-id="86fdc-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="86fdc-111">Ha egy olyan sablon létezik, amely már létezik a megadott névvel, akkor a megadott verzió frissül (a többi meglévő verzió is megmarad).</span><span class="sxs-lookup"><span data-stu-id="86fdc-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="86fdc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="86fdc-112">EXAMPLES</span></span>

### <span data-ttu-id="86fdc-113">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="86fdc-113">Example 1:</span></span>
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

<span data-ttu-id="86fdc-114">A "v 1.0" nevű új sablon létrehozása egy "myTemplateSpec" nevű sablonban.</span><span class="sxs-lookup"><span data-stu-id="86fdc-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="86fdc-115">A megadott verzió a verzió ARM-sablonjának tartalmát fogja $templateJson.</span><span class="sxs-lookup"><span data-stu-id="86fdc-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="86fdc-116">**Megjegyzés:** A példában a kar sablon nem-op, mivel nem tartalmaz tényleges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="86fdc-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="86fdc-117">2. példa:</span><span class="sxs-lookup"><span data-stu-id="86fdc-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="86fdc-118">Egy "v 2.0" nevű új sablont hoz létre a "myTemplateSpec" nevű sablonban.</span><span class="sxs-lookup"><span data-stu-id="86fdc-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="86fdc-119">A megadott verzió a verzió ARM-sablonjának tartalmát tartalmazó helyi myTemplateContent.jsfájlból származó tartalmat fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="86fdc-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="86fdc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86fdc-120">PARAMETERS</span></span>

### <span data-ttu-id="86fdc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86fdc-121">-DefaultProfile</span></span>
<span data-ttu-id="86fdc-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86fdc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86fdc-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="86fdc-123">-Description</span></span>
<span data-ttu-id="86fdc-124">A sablon specifikációjának leírása.</span><span class="sxs-lookup"><span data-stu-id="86fdc-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="86fdc-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86fdc-125">-DisplayName</span></span>
<span data-ttu-id="86fdc-126">A sablon megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="86fdc-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="86fdc-127">-Force</span><span class="sxs-lookup"><span data-stu-id="86fdc-127">-Force</span></span>
<span data-ttu-id="86fdc-128">Ha egy meglévő verziót felülír, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86fdc-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="86fdc-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="86fdc-129">-Location</span></span>
<span data-ttu-id="86fdc-130">A sablon specifikációjának helye. Csak akkor kötelező, ha a specifikációban még nem szerepel a sablon.</span><span class="sxs-lookup"><span data-stu-id="86fdc-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="86fdc-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86fdc-131">-Name</span></span>
<span data-ttu-id="86fdc-132">Annak a sablonnak a neve, amely a spec nevet adja.</span><span class="sxs-lookup"><span data-stu-id="86fdc-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="86fdc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86fdc-133">-ResourceGroupName</span></span>
<span data-ttu-id="86fdc-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86fdc-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="86fdc-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="86fdc-135">-TemplateFile</span></span>
<span data-ttu-id="86fdc-136">A helyi Azure Resource Manager template JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="86fdc-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="86fdc-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="86fdc-137">-TemplateJson</span></span>
<span data-ttu-id="86fdc-138">Az Azure Resource Manager sablon JSON-je.</span><span class="sxs-lookup"><span data-stu-id="86fdc-138">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="86fdc-139">-Verzió</span><span class="sxs-lookup"><span data-stu-id="86fdc-139">-Version</span></span>
<span data-ttu-id="86fdc-140">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="86fdc-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="86fdc-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="86fdc-141">-VersionDescription</span></span>
<span data-ttu-id="86fdc-142">A verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="86fdc-142">The description of the version.</span></span>

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

### <span data-ttu-id="86fdc-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86fdc-143">-Confirm</span></span>
<span data-ttu-id="86fdc-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86fdc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86fdc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86fdc-145">-WhatIf</span></span>
<span data-ttu-id="86fdc-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86fdc-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86fdc-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86fdc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86fdc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86fdc-148">CommonParameters</span></span>
<span data-ttu-id="86fdc-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86fdc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86fdc-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86fdc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86fdc-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86fdc-151">INPUTS</span></span>

### <span data-ttu-id="86fdc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="86fdc-152">System.String</span></span>

## <span data-ttu-id="86fdc-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86fdc-153">OUTPUTS</span></span>

### <span data-ttu-id="86fdc-154">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="86fdc-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="86fdc-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86fdc-155">NOTES</span></span>

## <span data-ttu-id="86fdc-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86fdc-156">RELATED LINKS</span></span>
