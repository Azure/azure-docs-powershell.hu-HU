---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 6020466feb5231c9634b01a5ccf5f8251616478f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005205"
---
# <span data-ttu-id="25ffc-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="25ffc-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="25ffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="25ffc-103">Eltávolítja a sávszélesség-ütemezést.</span><span class="sxs-lookup"><span data-stu-id="25ffc-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="25ffc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25ffc-104">SYNTAX</span></span>

### <span data-ttu-id="25ffc-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25ffc-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25ffc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25ffc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25ffc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25ffc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25ffc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25ffc-108">DESCRIPTION</span></span>
<span data-ttu-id="25ffc-109">A **Remove-AzStackEdgeBandwidthSchedule** parancsmag eltávolítja a Stack Edge-eszközök sávszélesség-ütemezését.</span><span class="sxs-lookup"><span data-stu-id="25ffc-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="25ffc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25ffc-110">EXAMPLES</span></span>

### <span data-ttu-id="25ffc-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="25ffc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="25ffc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25ffc-112">PARAMETERS</span></span>

### <span data-ttu-id="25ffc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25ffc-113">-AsJob</span></span>
<span data-ttu-id="25ffc-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="25ffc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25ffc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ffc-115">-DefaultProfile</span></span>
<span data-ttu-id="25ffc-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25ffc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25ffc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="25ffc-117">-DeviceName</span></span>
<span data-ttu-id="25ffc-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="25ffc-118">Device Name</span></span>

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

### <span data-ttu-id="25ffc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25ffc-119">-InputObject</span></span>
<span data-ttu-id="25ffc-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="25ffc-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25ffc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="25ffc-121">-Name</span></span>
<span data-ttu-id="25ffc-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="25ffc-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ffc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ffc-123">-PassThru</span></span>
<span data-ttu-id="25ffc-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="25ffc-124">returns true if successful</span></span>

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

### <span data-ttu-id="25ffc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ffc-125">-ResourceGroupName</span></span>
<span data-ttu-id="25ffc-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="25ffc-126">Resource Group Name</span></span>

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

### <span data-ttu-id="25ffc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25ffc-127">-ResourceId</span></span>
<span data-ttu-id="25ffc-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="25ffc-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ffc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25ffc-129">-Confirm</span></span>
<span data-ttu-id="25ffc-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25ffc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ffc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ffc-131">-WhatIf</span></span>
<span data-ttu-id="25ffc-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25ffc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25ffc-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25ffc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ffc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ffc-134">CommonParameters</span></span>
<span data-ttu-id="25ffc-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ffc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ffc-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25ffc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ffc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25ffc-137">INPUTS</span></span>

### <span data-ttu-id="25ffc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="25ffc-138">System.String</span></span>

### <span data-ttu-id="25ffc-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="25ffc-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="25ffc-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25ffc-140">OUTPUTS</span></span>

### <span data-ttu-id="25ffc-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25ffc-141">System.Boolean</span></span>

## <span data-ttu-id="25ffc-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25ffc-142">NOTES</span></span>

## <span data-ttu-id="25ffc-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25ffc-143">RELATED LINKS</span></span>
