---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: e7659c6437e9566a4793e12518a30067aa73297a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005077"
---
# <span data-ttu-id="ff66d-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ff66d-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="ff66d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff66d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff66d-103">Eltávolít egy meglévő eseményindítót az eszközön.</span><span class="sxs-lookup"><span data-stu-id="ff66d-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="ff66d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff66d-104">SYNTAX</span></span>

### <span data-ttu-id="ff66d-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff66d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff66d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff66d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff66d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff66d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff66d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff66d-108">DESCRIPTION</span></span>
<span data-ttu-id="ff66d-109">A **Remove-AzStackEdgeTrigger** parancsmag eltávolít egy meglévő eseményindítót a Stack Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="ff66d-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="ff66d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff66d-110">EXAMPLES</span></span>

### <span data-ttu-id="ff66d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ff66d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="ff66d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff66d-112">PARAMETERS</span></span>

### <span data-ttu-id="ff66d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff66d-113">-AsJob</span></span>
<span data-ttu-id="ff66d-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ff66d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff66d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff66d-115">-DefaultProfile</span></span>
<span data-ttu-id="ff66d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff66d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff66d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ff66d-117">-DeviceName</span></span>
<span data-ttu-id="ff66d-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="ff66d-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff66d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff66d-119">-InputObject</span></span>
<span data-ttu-id="ff66d-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="ff66d-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff66d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ff66d-121">-Name</span></span>
<span data-ttu-id="ff66d-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="ff66d-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff66d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff66d-123">-PassThru</span></span>
<span data-ttu-id="ff66d-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="ff66d-124">returns true if successful</span></span>

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

### <span data-ttu-id="ff66d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff66d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff66d-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ff66d-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff66d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff66d-127">-ResourceId</span></span>
<span data-ttu-id="ff66d-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff66d-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ff66d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff66d-129">-Confirm</span></span>
<span data-ttu-id="ff66d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ff66d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff66d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff66d-131">-WhatIf</span></span>
<span data-ttu-id="ff66d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ff66d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff66d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff66d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff66d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff66d-134">CommonParameters</span></span>
<span data-ttu-id="ff66d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff66d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff66d-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff66d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff66d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff66d-137">INPUTS</span></span>

### <span data-ttu-id="ff66d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ff66d-138">System.String</span></span>

### <span data-ttu-id="ff66d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ff66d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="ff66d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff66d-140">OUTPUTS</span></span>

### <span data-ttu-id="ff66d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff66d-141">System.Boolean</span></span>

## <span data-ttu-id="ff66d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff66d-142">NOTES</span></span>

## <span data-ttu-id="ff66d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff66d-143">RELATED LINKS</span></span>
