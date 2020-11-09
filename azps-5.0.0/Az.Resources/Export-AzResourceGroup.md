---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300587"
---
# <span data-ttu-id="67f3d-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="67f3d-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="67f3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="67f3d-103">Egy erőforráscsoportot sablonként rögzít, és egy fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="67f3d-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="67f3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67f3d-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67f3d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67f3d-105">DESCRIPTION</span></span>
<span data-ttu-id="67f3d-106">Az **export-AzResourceGroup** parancsmag sablonként rögzíti a megadott erőforráscsoportot, és egy JSON-fájlba menti. Ez olyan esetekben lehet hasznos, amikor már létrehozott néhány erőforrást az erőforráscsoport-ban, és ki szeretné használni a sablonon alapuló telepített példányok használatának előnyeit.</span><span class="sxs-lookup"><span data-stu-id="67f3d-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="67f3d-107">Ezzel a parancsmaggal megkönnyítheti a meglévő erőforrások sablonjának generálását az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="67f3d-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="67f3d-108">Bizonyos esetekben előfordulhat, hogy ez a parancsmag nem hoz létre a sablon bizonyos részeit.</span><span class="sxs-lookup"><span data-stu-id="67f3d-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="67f3d-109">A figyelmeztető üzenetek tájékoztatni fogják a sikertelen erőforrásokról.</span><span class="sxs-lookup"><span data-stu-id="67f3d-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="67f3d-110">A sablon továbbra is létrejön a sikeres részekhez.</span><span class="sxs-lookup"><span data-stu-id="67f3d-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="67f3d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="67f3d-111">EXAMPLES</span></span>

### <span data-ttu-id="67f3d-112">1. példa: erőforráscsoport exportálása</span><span class="sxs-lookup"><span data-stu-id="67f3d-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="67f3d-113">Ez a parancs rögzíti az TestGroup nevű erőforráscsoportot sablonként, és egy JSON-fájlba menti az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="67f3d-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="67f3d-114">2. példa: egyetlen erőforrás exportálása egy erőforrás-csoportból</span><span class="sxs-lookup"><span data-stu-id="67f3d-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="67f3d-115">Ez a parancs rögzíti a "TestVirtualMachine" nevű virtuális gép erőforrását a "TestGroup" erőforráscsoport sablonként, és egy JSON-fájlba menti az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="67f3d-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="67f3d-116">3. példa: kijelölt erőforrások exportálása egy erőforrás-csoportból</span><span class="sxs-lookup"><span data-stu-id="67f3d-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="67f3d-117">Ez a parancs két erőforrást rögzít a "TestGroup" erőforráscsoport sablonként, és egy JSON-fájlba menti az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="67f3d-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="67f3d-118">A generált sablon nem tartalmaz generált paramétereket.</span><span class="sxs-lookup"><span data-stu-id="67f3d-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="67f3d-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67f3d-119">PARAMETERS</span></span>

### <span data-ttu-id="67f3d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="67f3d-120">-ApiVersion</span></span>
<span data-ttu-id="67f3d-121">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="67f3d-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="67f3d-122">Ha nem adja meg, akkor a program a legújabb API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="67f3d-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="67f3d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f3d-123">-DefaultProfile</span></span>
<span data-ttu-id="67f3d-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67f3d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f3d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="67f3d-125">-Force</span></span>
<span data-ttu-id="67f3d-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="67f3d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67f3d-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="67f3d-127">-IncludeComments</span></span>
<span data-ttu-id="67f3d-128">Jelzi, hogy a művelet a megjegyzésekkel exportálja a sablont.</span><span class="sxs-lookup"><span data-stu-id="67f3d-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="67f3d-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="67f3d-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="67f3d-130">Azt jelzi, hogy a művelet az alapértelmezett értékkel exportálja a Template paramétert.</span><span class="sxs-lookup"><span data-stu-id="67f3d-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="67f3d-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="67f3d-131">-Path</span></span>
<span data-ttu-id="67f3d-132">A sablonfájl kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="67f3d-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="67f3d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="67f3d-133">-Pre</span></span>
<span data-ttu-id="67f3d-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-t használja, amikor automatikusan meghatározza, hogy melyik API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="67f3d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="67f3d-135">-Resource (erőforrás)</span><span class="sxs-lookup"><span data-stu-id="67f3d-135">-Resource</span></span>
<span data-ttu-id="67f3d-136">Az eredmény kiszűrésére szolgáló resourceIds listája.</span><span class="sxs-lookup"><span data-stu-id="67f3d-136">A list of resourceIds to filter the results by.</span></span>

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

### <span data-ttu-id="67f3d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f3d-137">-ResourceGroupName</span></span>
<span data-ttu-id="67f3d-138">Az exportálandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67f3d-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="67f3d-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="67f3d-139">-SkipAllParameterization</span></span>
<span data-ttu-id="67f3d-140">Az összes paraméterezése kihagyása</span><span class="sxs-lookup"><span data-stu-id="67f3d-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="67f3d-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="67f3d-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="67f3d-142">Hagyja ki az erőforrás neve paraméterezése.</span><span class="sxs-lookup"><span data-stu-id="67f3d-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="67f3d-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67f3d-143">-Confirm</span></span>
<span data-ttu-id="67f3d-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67f3d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f3d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67f3d-145">-WhatIf</span></span>
<span data-ttu-id="67f3d-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67f3d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f3d-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67f3d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f3d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f3d-148">CommonParameters</span></span>
<span data-ttu-id="67f3d-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67f3d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f3d-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67f3d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f3d-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f3d-151">INPUTS</span></span>

### <span data-ttu-id="67f3d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="67f3d-152">System.String</span></span>

## <span data-ttu-id="67f3d-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f3d-153">OUTPUTS</span></span>

### <span data-ttu-id="67f3d-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="67f3d-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="67f3d-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67f3d-155">NOTES</span></span>

## <span data-ttu-id="67f3d-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67f3d-156">RELATED LINKS</span></span>

[<span data-ttu-id="67f3d-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="67f3d-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


