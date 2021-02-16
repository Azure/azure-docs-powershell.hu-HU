---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143914"
---
# <span data-ttu-id="950e1-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="950e1-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="950e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="950e1-102">SYNOPSIS</span></span>
<span data-ttu-id="950e1-103">Eltávolít egy meglévő eseményindítót az eszközön.</span><span class="sxs-lookup"><span data-stu-id="950e1-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="950e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="950e1-104">SYNTAX</span></span>

### <span data-ttu-id="950e1-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="950e1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="950e1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="950e1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="950e1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="950e1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="950e1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="950e1-108">DESCRIPTION</span></span>
<span data-ttu-id="950e1-109">A **Remove-AzStackEdgeTrigger** parancsmag eltávolít egy meglévő eseményindítót a Stack Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="950e1-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="950e1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="950e1-110">EXAMPLES</span></span>

### <span data-ttu-id="950e1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="950e1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="950e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="950e1-112">PARAMETERS</span></span>

### <span data-ttu-id="950e1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="950e1-113">-AsJob</span></span>
<span data-ttu-id="950e1-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="950e1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="950e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="950e1-115">-DefaultProfile</span></span>
<span data-ttu-id="950e1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="950e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="950e1-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="950e1-117">-DeviceName</span></span>
<span data-ttu-id="950e1-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="950e1-118">Device Name</span></span>

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

### <span data-ttu-id="950e1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="950e1-119">-InputObject</span></span>
<span data-ttu-id="950e1-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="950e1-120">Input Object</span></span>

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

### <span data-ttu-id="950e1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="950e1-121">-Name</span></span>
<span data-ttu-id="950e1-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="950e1-122">Resource Name</span></span>

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

### <span data-ttu-id="950e1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="950e1-123">-PassThru</span></span>
<span data-ttu-id="950e1-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="950e1-124">returns true if successful</span></span>

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

### <span data-ttu-id="950e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="950e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="950e1-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="950e1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="950e1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="950e1-127">-ResourceId</span></span>
<span data-ttu-id="950e1-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="950e1-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="950e1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="950e1-129">-Confirm</span></span>
<span data-ttu-id="950e1-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="950e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="950e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="950e1-131">-WhatIf</span></span>
<span data-ttu-id="950e1-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="950e1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="950e1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="950e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="950e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="950e1-134">CommonParameters</span></span>
<span data-ttu-id="950e1-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="950e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="950e1-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="950e1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="950e1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="950e1-137">INPUTS</span></span>

### <span data-ttu-id="950e1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="950e1-138">System.String</span></span>

### <span data-ttu-id="950e1-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="950e1-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="950e1-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="950e1-140">OUTPUTS</span></span>

### <span data-ttu-id="950e1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="950e1-141">System.Boolean</span></span>

## <span data-ttu-id="950e1-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="950e1-142">NOTES</span></span>

## <span data-ttu-id="950e1-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="950e1-143">RELATED LINKS</span></span>
