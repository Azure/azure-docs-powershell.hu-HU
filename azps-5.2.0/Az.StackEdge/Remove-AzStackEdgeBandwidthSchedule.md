---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352289"
---
# <span data-ttu-id="fe52c-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fe52c-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="fe52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe52c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe52c-103">Eltávolítja a sávszélesség-ütemezést.</span><span class="sxs-lookup"><span data-stu-id="fe52c-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="fe52c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe52c-104">SYNTAX</span></span>

### <span data-ttu-id="fe52c-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe52c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe52c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe52c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe52c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe52c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe52c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe52c-108">DESCRIPTION</span></span>
<span data-ttu-id="fe52c-109">A **Remove-AzStackEdgeBandwidthSchedule** parancsmag eltávolítja a Stack Edge-eszközök sávszélesség-ütemezését.</span><span class="sxs-lookup"><span data-stu-id="fe52c-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="fe52c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe52c-110">EXAMPLES</span></span>

### <span data-ttu-id="fe52c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fe52c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="fe52c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe52c-112">PARAMETERS</span></span>

### <span data-ttu-id="fe52c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe52c-113">-AsJob</span></span>
<span data-ttu-id="fe52c-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fe52c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe52c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe52c-115">-DefaultProfile</span></span>
<span data-ttu-id="fe52c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe52c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe52c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fe52c-117">-DeviceName</span></span>
<span data-ttu-id="fe52c-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="fe52c-118">Device Name</span></span>

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

### <span data-ttu-id="fe52c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe52c-119">-InputObject</span></span>
<span data-ttu-id="fe52c-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="fe52c-120">Input Object</span></span>

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

### <span data-ttu-id="fe52c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe52c-121">-Name</span></span>
<span data-ttu-id="fe52c-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fe52c-122">Resource Name</span></span>

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

### <span data-ttu-id="fe52c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe52c-123">-PassThru</span></span>
<span data-ttu-id="fe52c-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="fe52c-124">returns true if successful</span></span>

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

### <span data-ttu-id="fe52c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe52c-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe52c-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fe52c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fe52c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe52c-127">-ResourceId</span></span>
<span data-ttu-id="fe52c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe52c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="fe52c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe52c-129">-Confirm</span></span>
<span data-ttu-id="fe52c-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe52c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe52c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe52c-131">-WhatIf</span></span>
<span data-ttu-id="fe52c-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fe52c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe52c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe52c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe52c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe52c-134">CommonParameters</span></span>
<span data-ttu-id="fe52c-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe52c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe52c-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe52c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe52c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe52c-137">INPUTS</span></span>

### <span data-ttu-id="fe52c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fe52c-138">System.String</span></span>

### <span data-ttu-id="fe52c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fe52c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="fe52c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe52c-140">OUTPUTS</span></span>

### <span data-ttu-id="fe52c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe52c-141">System.Boolean</span></span>

## <span data-ttu-id="fe52c-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe52c-142">NOTES</span></span>

## <span data-ttu-id="fe52c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe52c-143">RELATED LINKS</span></span>
