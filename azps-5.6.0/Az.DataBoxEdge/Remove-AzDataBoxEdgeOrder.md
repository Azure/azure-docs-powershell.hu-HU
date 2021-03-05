---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 8fe4787ca14d26b7e734a0ac081cdbaef8eddbd9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012245"
---
# <span data-ttu-id="cb69c-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="cb69c-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="cb69c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb69c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb69c-103">Eltávolítja egy eszköz sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="cb69c-103">Removes the order for a device.</span></span>

## <span data-ttu-id="cb69c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb69c-104">SYNTAX</span></span>

### <span data-ttu-id="cb69c-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb69c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb69c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb69c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb69c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb69c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb69c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb69c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb69c-109">Az **Remove-AzDataBoxEdgeOrder** parancsmag törli egy Adatdoboz Edge-eszköz meglévő sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="cb69c-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="cb69c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb69c-110">EXAMPLES</span></span>

### <span data-ttu-id="cb69c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cb69c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="cb69c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb69c-112">PARAMETERS</span></span>

### <span data-ttu-id="cb69c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb69c-113">-AsJob</span></span>
<span data-ttu-id="cb69c-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cb69c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb69c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb69c-115">-DefaultProfile</span></span>
<span data-ttu-id="cb69c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb69c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb69c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cb69c-117">-DeviceName</span></span>
<span data-ttu-id="cb69c-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="cb69c-118">Device Name</span></span>

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

### <span data-ttu-id="cb69c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb69c-119">-InputObject</span></span>
<span data-ttu-id="cb69c-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="cb69c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb69c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb69c-121">-PassThru</span></span>
<span data-ttu-id="cb69c-122">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="cb69c-122">returns true if successful</span></span>

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

### <span data-ttu-id="cb69c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb69c-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb69c-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cb69c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cb69c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb69c-125">-ResourceId</span></span>
<span data-ttu-id="cb69c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb69c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="cb69c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb69c-127">-Confirm</span></span>
<span data-ttu-id="cb69c-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cb69c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb69c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb69c-129">-WhatIf</span></span>
<span data-ttu-id="cb69c-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cb69c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb69c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb69c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb69c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb69c-132">CommonParameters</span></span>
<span data-ttu-id="cb69c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb69c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb69c-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb69c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb69c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb69c-135">INPUTS</span></span>

### <span data-ttu-id="cb69c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cb69c-136">System.String</span></span>

### <span data-ttu-id="cb69c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="cb69c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="cb69c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb69c-138">OUTPUTS</span></span>

### <span data-ttu-id="cb69c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="cb69c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="cb69c-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb69c-140">NOTES</span></span>

## <span data-ttu-id="cb69c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb69c-141">RELATED LINKS</span></span>
