---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143922"
---
# <span data-ttu-id="059ae-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="059ae-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="059ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059ae-102">SYNOPSIS</span></span>
<span data-ttu-id="059ae-103">Eltávolítja egy eszköz sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="059ae-103">Removes the order for a device.</span></span>

## <span data-ttu-id="059ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="059ae-104">SYNTAX</span></span>

### <span data-ttu-id="059ae-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="059ae-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059ae-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="059ae-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059ae-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="059ae-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059ae-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="059ae-108">DESCRIPTION</span></span>
<span data-ttu-id="059ae-109">A **Remove-AzStackEdgeOrder** parancsmag törli egy Stack Edge-eszköz meglévő sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="059ae-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="059ae-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="059ae-110">EXAMPLES</span></span>

### <span data-ttu-id="059ae-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="059ae-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="059ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="059ae-112">PARAMETERS</span></span>

### <span data-ttu-id="059ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="059ae-113">-AsJob</span></span>
<span data-ttu-id="059ae-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="059ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="059ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059ae-115">-DefaultProfile</span></span>
<span data-ttu-id="059ae-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="059ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059ae-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="059ae-117">-DeviceName</span></span>
<span data-ttu-id="059ae-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="059ae-118">Device Name</span></span>

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

### <span data-ttu-id="059ae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="059ae-119">-InputObject</span></span>
<span data-ttu-id="059ae-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="059ae-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="059ae-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="059ae-121">-PassThru</span></span>
<span data-ttu-id="059ae-122">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="059ae-122">returns true if successful</span></span>

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

### <span data-ttu-id="059ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="059ae-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="059ae-124">Resource Group Name</span></span>

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

### <span data-ttu-id="059ae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="059ae-125">-ResourceId</span></span>
<span data-ttu-id="059ae-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="059ae-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="059ae-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="059ae-127">-Confirm</span></span>
<span data-ttu-id="059ae-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="059ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059ae-129">-WhatIf</span></span>
<span data-ttu-id="059ae-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="059ae-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059ae-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="059ae-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059ae-132">CommonParameters</span></span>
<span data-ttu-id="059ae-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059ae-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="059ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059ae-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="059ae-135">INPUTS</span></span>

### <span data-ttu-id="059ae-136">System.String</span><span class="sxs-lookup"><span data-stu-id="059ae-136">System.String</span></span>

### <span data-ttu-id="059ae-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="059ae-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="059ae-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="059ae-138">OUTPUTS</span></span>

### <span data-ttu-id="059ae-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="059ae-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="059ae-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="059ae-140">NOTES</span></span>

## <span data-ttu-id="059ae-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="059ae-141">RELATED LINKS</span></span>
