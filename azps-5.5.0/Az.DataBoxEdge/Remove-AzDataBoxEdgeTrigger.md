---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144402"
---
# <span data-ttu-id="cda82-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cda82-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="cda82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cda82-102">SYNOPSIS</span></span>
<span data-ttu-id="cda82-103">Eltávolít egy meglévő eseményindítót az eszközön.</span><span class="sxs-lookup"><span data-stu-id="cda82-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="cda82-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cda82-104">SYNTAX</span></span>

### <span data-ttu-id="cda82-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cda82-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cda82-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cda82-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cda82-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cda82-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda82-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cda82-108">DESCRIPTION</span></span>
<span data-ttu-id="cda82-109">Az **Remove-AzDataBoxEdgeTrigger** parancsmag eltávolít egy meglévő eseményindítót az Adatmező Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="cda82-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="cda82-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cda82-110">EXAMPLES</span></span>

### <span data-ttu-id="cda82-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cda82-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="cda82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cda82-112">PARAMETERS</span></span>

### <span data-ttu-id="cda82-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cda82-113">-AsJob</span></span>
<span data-ttu-id="cda82-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cda82-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cda82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda82-115">-DefaultProfile</span></span>
<span data-ttu-id="cda82-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cda82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cda82-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cda82-117">-DeviceName</span></span>
<span data-ttu-id="cda82-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="cda82-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda82-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cda82-119">-InputObject</span></span>
<span data-ttu-id="cda82-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="cda82-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cda82-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cda82-121">-Name</span></span>
<span data-ttu-id="cda82-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="cda82-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda82-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cda82-123">-PassThru</span></span>
<span data-ttu-id="cda82-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="cda82-124">returns true if successful</span></span>

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

### <span data-ttu-id="cda82-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda82-125">-ResourceGroupName</span></span>
<span data-ttu-id="cda82-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cda82-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda82-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cda82-127">-ResourceId</span></span>
<span data-ttu-id="cda82-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cda82-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda82-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cda82-129">-Confirm</span></span>
<span data-ttu-id="cda82-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cda82-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda82-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda82-131">-WhatIf</span></span>
<span data-ttu-id="cda82-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cda82-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cda82-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cda82-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda82-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda82-134">CommonParameters</span></span>
<span data-ttu-id="cda82-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda82-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda82-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cda82-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda82-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cda82-137">INPUTS</span></span>

### <span data-ttu-id="cda82-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cda82-138">System.String</span></span>

### <span data-ttu-id="cda82-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cda82-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="cda82-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cda82-140">OUTPUTS</span></span>

### <span data-ttu-id="cda82-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cda82-141">System.Boolean</span></span>

## <span data-ttu-id="cda82-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cda82-142">NOTES</span></span>

## <span data-ttu-id="cda82-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cda82-143">RELATED LINKS</span></span>
