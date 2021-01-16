---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338490"
---
# <span data-ttu-id="1b691-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1b691-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="1b691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b691-102">SYNOPSIS</span></span>
<span data-ttu-id="1b691-103">Eltávolítja egy eszköz iot-szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="1b691-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="1b691-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b691-104">SYNTAX</span></span>

### <span data-ttu-id="1b691-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b691-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b691-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b691-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b691-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b691-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b691-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b691-108">DESCRIPTION</span></span>
<span data-ttu-id="1b691-109">A **Remove-AzDataBoxEdgeRole** parancsmag eltávolítja a társított IoT-szerepkört egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="1b691-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="1b691-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b691-110">EXAMPLES</span></span>

### <span data-ttu-id="1b691-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1b691-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="1b691-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b691-112">PARAMETERS</span></span>

### <span data-ttu-id="1b691-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b691-113">-AsJob</span></span>
<span data-ttu-id="1b691-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1b691-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b691-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b691-115">-DefaultProfile</span></span>
<span data-ttu-id="1b691-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b691-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b691-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1b691-117">-DeviceName</span></span>
<span data-ttu-id="1b691-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="1b691-118">Device Name</span></span>

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

### <span data-ttu-id="1b691-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b691-119">-InputObject</span></span>
<span data-ttu-id="1b691-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="1b691-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b691-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1b691-121">-Name</span></span>
<span data-ttu-id="1b691-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="1b691-122">Resource Name</span></span>

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

### <span data-ttu-id="1b691-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b691-123">-PassThru</span></span>
<span data-ttu-id="1b691-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="1b691-124">returns true if successful</span></span>

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

### <span data-ttu-id="1b691-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b691-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b691-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1b691-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1b691-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b691-127">-ResourceId</span></span>
<span data-ttu-id="1b691-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b691-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1b691-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b691-129">-Confirm</span></span>
<span data-ttu-id="1b691-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1b691-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b691-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b691-131">-WhatIf</span></span>
<span data-ttu-id="1b691-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1b691-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b691-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b691-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b691-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b691-134">CommonParameters</span></span>
<span data-ttu-id="1b691-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b691-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b691-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b691-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b691-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b691-137">INPUTS</span></span>

### <span data-ttu-id="1b691-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1b691-138">System.String</span></span>

### <span data-ttu-id="1b691-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1b691-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="1b691-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b691-140">OUTPUTS</span></span>

### <span data-ttu-id="1b691-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1b691-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="1b691-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b691-142">NOTES</span></span>

## <span data-ttu-id="1b691-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b691-143">RELATED LINKS</span></span>
