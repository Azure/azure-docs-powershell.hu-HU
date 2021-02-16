---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155122"
---
# <span data-ttu-id="5385d-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5385d-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="5385d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5385d-102">SYNOPSIS</span></span>
<span data-ttu-id="5385d-103">Adott műveleteket hív meg egy megosztáson.</span><span class="sxs-lookup"><span data-stu-id="5385d-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="5385d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5385d-104">SYNTAX</span></span>

### <span data-ttu-id="5385d-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5385d-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5385d-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5385d-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5385d-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5385d-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5385d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5385d-108">DESCRIPTION</span></span>
<span data-ttu-id="5385d-109">Az **Invoke-AzStackEdgeShare** parancsmag meghívja a Stack Edge-es eszköz megosztási adatainak frissítésére vonatkozó műveletet.</span><span class="sxs-lookup"><span data-stu-id="5385d-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="5385d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5385d-110">EXAMPLES</span></span>

### <span data-ttu-id="5385d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5385d-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="5385d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5385d-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="5385d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5385d-113">PARAMETERS</span></span>

### <span data-ttu-id="5385d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5385d-114">-AsJob</span></span>
<span data-ttu-id="5385d-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5385d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5385d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5385d-116">-DefaultProfile</span></span>
<span data-ttu-id="5385d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5385d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5385d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5385d-118">-DeviceName</span></span>
<span data-ttu-id="5385d-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="5385d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5385d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5385d-120">-InputObject</span></span>
<span data-ttu-id="5385d-121">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="5385d-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5385d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5385d-122">-Name</span></span>
<span data-ttu-id="5385d-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="5385d-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5385d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5385d-124">-PassThru</span></span>
<span data-ttu-id="5385d-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="5385d-125">returns true if successful</span></span>

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

### <span data-ttu-id="5385d-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="5385d-126">-RefreshData</span></span>
<span data-ttu-id="5385d-127">Metaadatok megosztása a felhőből származó adatokkal</span><span class="sxs-lookup"><span data-stu-id="5385d-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="5385d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5385d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5385d-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5385d-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5385d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5385d-130">-ResourceId</span></span>
<span data-ttu-id="5385d-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5385d-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5385d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5385d-132">-Confirm</span></span>
<span data-ttu-id="5385d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5385d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5385d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5385d-134">-WhatIf</span></span>
<span data-ttu-id="5385d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5385d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5385d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5385d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5385d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5385d-137">CommonParameters</span></span>
<span data-ttu-id="5385d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5385d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5385d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5385d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5385d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5385d-140">INPUTS</span></span>

### <span data-ttu-id="5385d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5385d-141">System.String</span></span>

### <span data-ttu-id="5385d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5385d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="5385d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5385d-143">OUTPUTS</span></span>

### <span data-ttu-id="5385d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5385d-144">System.Boolean</span></span>

## <span data-ttu-id="5385d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5385d-145">NOTES</span></span>

## <span data-ttu-id="5385d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5385d-146">RELATED LINKS</span></span>
