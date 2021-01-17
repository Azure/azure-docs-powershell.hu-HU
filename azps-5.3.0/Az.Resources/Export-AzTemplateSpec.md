---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466565"
---
# <span data-ttu-id="0e421-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="0e421-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="0e421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e421-102">SYNOPSIS</span></span>
<span data-ttu-id="0e421-103">Sablon specifikációjának exportálása a helyi fájlrendszerbe</span><span class="sxs-lookup"><span data-stu-id="0e421-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="0e421-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e421-104">SYNTAX</span></span>

### <span data-ttu-id="0e421-105">ExportByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e421-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e421-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e421-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e421-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e421-107">DESCRIPTION</span></span>
<span data-ttu-id="0e421-108">Egy adott Sablon specifikációs verzióját exportálja a helyi fájlrendszerbe.</span><span class="sxs-lookup"><span data-stu-id="0e421-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="0e421-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e421-109">EXAMPLES</span></span>

### <span data-ttu-id="0e421-110">1. példa: Exportálás név szerint</span><span class="sxs-lookup"><span data-stu-id="0e421-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="0e421-111">Exportálja a "myRG" erőforráscsoport "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját a "v1" helyi kimeneti mappába.</span><span class="sxs-lookup"><span data-stu-id="0e421-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="0e421-112">2. példa: Exportálás erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="0e421-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="0e421-113">Exportálja a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját az előfizetési alazonosító "myRG" erőforráscsoportjába a \{ \} "v1" helyi kimeneti mappába.</span><span class="sxs-lookup"><span data-stu-id="0e421-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="0e421-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e421-114">PARAMETERS</span></span>

### <span data-ttu-id="0e421-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e421-115">-DefaultProfile</span></span>
<span data-ttu-id="0e421-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e421-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e421-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0e421-117">-Name</span></span>
<span data-ttu-id="0e421-118">A sablon specifikációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0e421-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e421-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="0e421-119">-OutputFolder</span></span>
<span data-ttu-id="0e421-120">Annak a mappának az elérési útja, amelybe a sablon specifikációs verziója fog kimenetet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="0e421-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="0e421-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e421-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e421-122">A sablon specifikációjának erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="0e421-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e421-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e421-123">-ResourceId</span></span>
<span data-ttu-id="0e421-124">A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="0e421-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e421-125">-Version</span><span class="sxs-lookup"><span data-stu-id="0e421-125">-Version</span></span>
<span data-ttu-id="0e421-126">Az exportálni kívánt sablonverzió.</span><span class="sxs-lookup"><span data-stu-id="0e421-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="0e421-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e421-127">-Confirm</span></span>
<span data-ttu-id="0e421-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e421-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e421-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e421-129">-WhatIf</span></span>
<span data-ttu-id="0e421-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e421-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e421-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e421-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e421-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e421-132">CommonParameters</span></span>
<span data-ttu-id="0e421-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e421-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e421-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e421-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e421-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e421-135">INPUTS</span></span>

### <span data-ttu-id="0e421-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0e421-136">System.String</span></span>

## <span data-ttu-id="0e421-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e421-137">OUTPUTS</span></span>

### <span data-ttu-id="0e421-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0e421-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0e421-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e421-139">NOTES</span></span>

## <span data-ttu-id="0e421-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e421-140">RELATED LINKS</span></span>
