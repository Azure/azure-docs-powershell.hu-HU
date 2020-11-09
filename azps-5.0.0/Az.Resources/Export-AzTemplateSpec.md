---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300581"
---
# <span data-ttu-id="af77b-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="af77b-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="af77b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af77b-102">SYNOPSIS</span></span>
<span data-ttu-id="af77b-103">Sablon specifikációjának exportálása helyi fájlrendszerre</span><span class="sxs-lookup"><span data-stu-id="af77b-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="af77b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af77b-104">SYNTAX</span></span>

### <span data-ttu-id="af77b-105">ExportByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af77b-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af77b-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af77b-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af77b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af77b-107">DESCRIPTION</span></span>
<span data-ttu-id="af77b-108">Egy adott sablon spec-verziójának exportálása a helyi fájlrendszerbe.</span><span class="sxs-lookup"><span data-stu-id="af77b-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="af77b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af77b-109">EXAMPLES</span></span>

### <span data-ttu-id="af77b-110">1. példa: exportálás név szerint</span><span class="sxs-lookup"><span data-stu-id="af77b-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="af77b-111">A ' MyTemplateSpec ' nevű "myRG" nevű erőforráscsoport "v 1.0" nevű verziójának exportálása a helyi kimeneti mappába: "v1".</span><span class="sxs-lookup"><span data-stu-id="af77b-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="af77b-112">2. példa: erőforrás-azonosító szerint exportálva</span><span class="sxs-lookup"><span data-stu-id="af77b-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="af77b-113">Az "MyTemplateSpec" nevű "myRG" nevű erőforráscsoport "" nevű erőforráscsoporthoz tartozó "v 1.0"-es verzió exportálása a \{ \} "v1" helyi kimeneti mappába.</span><span class="sxs-lookup"><span data-stu-id="af77b-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="af77b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af77b-114">PARAMETERS</span></span>

### <span data-ttu-id="af77b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af77b-115">-DefaultProfile</span></span>
<span data-ttu-id="af77b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af77b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af77b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af77b-117">-Name</span></span>
<span data-ttu-id="af77b-118">Annak a sablonnak a neve, amely a spec nevet adja.</span><span class="sxs-lookup"><span data-stu-id="af77b-118">The name of the template spec.</span></span>

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

### <span data-ttu-id="af77b-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="af77b-119">-OutputFolder</span></span>
<span data-ttu-id="af77b-120">Annak a mappának az elérési útvonala, amelybe a sablon spec verziója lesz a kimenet.</span><span class="sxs-lookup"><span data-stu-id="af77b-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="af77b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af77b-121">-ResourceGroupName</span></span>
<span data-ttu-id="af77b-122">A sablon specifikációja erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af77b-122">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="af77b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af77b-123">-ResourceId</span></span>
<span data-ttu-id="af77b-124">A sablon teljes értékű erőforrás-azonosítója (példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName})</span><span class="sxs-lookup"><span data-stu-id="af77b-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="af77b-125">-Verzió</span><span class="sxs-lookup"><span data-stu-id="af77b-125">-Version</span></span>
<span data-ttu-id="af77b-126">Az exportálandó sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="af77b-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="af77b-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af77b-127">-Confirm</span></span>
<span data-ttu-id="af77b-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af77b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af77b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af77b-129">-WhatIf</span></span>
<span data-ttu-id="af77b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af77b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af77b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af77b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af77b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af77b-132">CommonParameters</span></span>
<span data-ttu-id="af77b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af77b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af77b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af77b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af77b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af77b-135">INPUTS</span></span>

### <span data-ttu-id="af77b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="af77b-136">System.String</span></span>

## <span data-ttu-id="af77b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af77b-137">OUTPUTS</span></span>

### <span data-ttu-id="af77b-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="af77b-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="af77b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af77b-139">NOTES</span></span>

## <span data-ttu-id="af77b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af77b-140">RELATED LINKS</span></span>
