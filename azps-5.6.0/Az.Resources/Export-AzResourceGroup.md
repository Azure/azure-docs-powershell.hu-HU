---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 1f4f518cb203414392fe8d3f01fc0031be7f79e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929858"
---
# <span data-ttu-id="fa6e5-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa6e5-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="fa6e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6e5-103">Sablonként rögzít egy erőforráscsoportot, és fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="fa6e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa6e5-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa6e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa6e5-105">DESCRIPTION</span></span>
<span data-ttu-id="fa6e5-106">Az **Export-AzResourceGroup** parancsmag sablonként rögzíti a megadott erőforráscsoportot, és egy JSON-fájlba menti. Ez olyan helyzetekben lehet hasznos, amikor már létrehozott néhány erőforrást az erőforráscsoportban, majd ki szeretné használni a sablonnal készített, háttérbeépítések használatának előnyeit.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="fa6e5-107">Ez a parancsmag egyszerű kezdést biztosít, ha létrehozza a sablont a meglévő erőforrásokhoz az erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="fa6e5-108">Előfordulhat, hogy a parancsmag nem hozza létre a sablon bizonyos részeit.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="fa6e5-109">A figyelmeztető üzenetek értesítik a sikertelen erőforrásokról.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="fa6e5-110">A sablon továbbra is létrejön a sikeres részekhez.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="fa6e5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa6e5-111">EXAMPLES</span></span>

### <span data-ttu-id="fa6e5-112">1. példa: Erőforráscsoport exportálása</span><span class="sxs-lookup"><span data-stu-id="fa6e5-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="fa6e5-113">Ez a parancs sablonként rögzíti a TestGroup nevű erőforráscsoportot, és egy JSON-fájlba menti azt az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="fa6e5-114">2. példa: Egyetlen erőforrás exportálása egy erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="fa6e5-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="fa6e5-115">Ez a parancs sablonként rögzíti a "TestGroup" erőforráscsoport "TestVirtualMachine" nevű virtuális gép típusú erőforrását, és az aktuális címtárban lévő JSON-fájlba menti azt.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="fa6e5-116">3. példa: Kijelölt erőforrások exportálása erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="fa6e5-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="fa6e5-117">Ez a parancs a "TestGroup" erőforráscsoport két erőforrását sablonként rögzíti, és egy JSON-fájlba menti az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="fa6e5-118">A létrehozott sablon nem tartalmazni fogja a létrehozott paramétereket.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="fa6e5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa6e5-119">PARAMETERS</span></span>

### <span data-ttu-id="fa6e5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fa6e5-120">-ApiVersion</span></span>
<span data-ttu-id="fa6e5-121">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fa6e5-122">Ha nincs megadva, akkor a legújabb API-verziót használja a program.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-122">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa6e5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6e5-123">-DefaultProfile</span></span>
<span data-ttu-id="fa6e5-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fa6e5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa6e5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fa6e5-125">-Force</span></span>
<span data-ttu-id="fa6e5-126">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa6e5-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="fa6e5-127">-IncludeComments</span></span>
<span data-ttu-id="fa6e5-128">Azt jelzi, hogy a művelet megjegyzésekkel együtt exportálja a sablont.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="fa6e5-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="fa6e5-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="fa6e5-130">Azt jelzi, hogy ez a művelet exportálja a sablon paraméterét az alapértelmezett értékkel.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="fa6e5-131">-Path</span><span class="sxs-lookup"><span data-stu-id="fa6e5-131">-Path</span></span>
<span data-ttu-id="fa6e5-132">A sablonfájl kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="fa6e5-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="fa6e5-133">-Pre</span></span>
<span data-ttu-id="fa6e5-134">Azt jelzi, hogy ez a parancsmag megjelenés előtti API-verziókat használ, amikor automatikusan meghatározza, hogy melyik API-verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="fa6e5-135">-Erőforrás</span><span class="sxs-lookup"><span data-stu-id="fa6e5-135">-Resource</span></span>
<span data-ttu-id="fa6e5-136">Az eredmények szűréséhez szükséges erőforrásazonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa6e5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa6e5-137">-ResourceGroupName</span></span>
<span data-ttu-id="fa6e5-138">Az exportálni szükséges erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa6e5-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="fa6e5-139">-SkipAllParameterization</span></span>
<span data-ttu-id="fa6e5-140">Az összes paraméterezés kihagyása</span><span class="sxs-lookup"><span data-stu-id="fa6e5-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="fa6e5-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="fa6e5-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="fa6e5-142">Az erőforrásnév paraméterezésének kihagyása</span><span class="sxs-lookup"><span data-stu-id="fa6e5-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="fa6e5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa6e5-143">-Confirm</span></span>
<span data-ttu-id="fa6e5-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa6e5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa6e5-145">-WhatIf</span></span>
<span data-ttu-id="fa6e5-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa6e5-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa6e5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6e5-148">CommonParameters</span></span>
<span data-ttu-id="fa6e5-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa6e5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6e5-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa6e5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6e5-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa6e5-151">INPUTS</span></span>

### <span data-ttu-id="fa6e5-152">System.String</span><span class="sxs-lookup"><span data-stu-id="fa6e5-152">System.String</span></span>

## <span data-ttu-id="fa6e5-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa6e5-153">OUTPUTS</span></span>

### <span data-ttu-id="fa6e5-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="fa6e5-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fa6e5-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa6e5-155">NOTES</span></span>

## <span data-ttu-id="fa6e5-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa6e5-156">RELATED LINKS</span></span>

[<span data-ttu-id="fa6e5-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa6e5-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


