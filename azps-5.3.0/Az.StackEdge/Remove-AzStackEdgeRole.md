---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376402"
---
# <span data-ttu-id="e30da-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e30da-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="e30da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e30da-102">SYNOPSIS</span></span>
<span data-ttu-id="e30da-103">Eltávolítja egy eszköz iot-szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="e30da-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="e30da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e30da-104">SYNTAX</span></span>

### <span data-ttu-id="e30da-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e30da-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e30da-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e30da-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e30da-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e30da-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30da-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e30da-108">DESCRIPTION</span></span>
<span data-ttu-id="e30da-109">A **Remove-AzStackEdgeRole** parancsmag eltávolítja egy Stack Edge-eszköz iot-szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="e30da-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="e30da-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e30da-110">EXAMPLES</span></span>

### <span data-ttu-id="e30da-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e30da-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="e30da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e30da-112">PARAMETERS</span></span>

### <span data-ttu-id="e30da-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e30da-113">-AsJob</span></span>
<span data-ttu-id="e30da-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e30da-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e30da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30da-115">-DefaultProfile</span></span>
<span data-ttu-id="e30da-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e30da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e30da-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e30da-117">-DeviceName</span></span>
<span data-ttu-id="e30da-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="e30da-118">Device Name</span></span>

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

### <span data-ttu-id="e30da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e30da-119">-InputObject</span></span>
<span data-ttu-id="e30da-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="e30da-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e30da-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e30da-121">-Name</span></span>
<span data-ttu-id="e30da-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e30da-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e30da-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e30da-123">-PassThru</span></span>
<span data-ttu-id="e30da-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="e30da-124">returns true if successful</span></span>

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

### <span data-ttu-id="e30da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30da-125">-ResourceGroupName</span></span>
<span data-ttu-id="e30da-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e30da-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e30da-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e30da-127">-ResourceId</span></span>
<span data-ttu-id="e30da-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e30da-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e30da-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e30da-129">-Confirm</span></span>
<span data-ttu-id="e30da-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e30da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e30da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30da-131">-WhatIf</span></span>
<span data-ttu-id="e30da-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e30da-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e30da-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e30da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e30da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30da-134">CommonParameters</span></span>
<span data-ttu-id="e30da-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e30da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30da-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e30da-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30da-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e30da-137">INPUTS</span></span>

### <span data-ttu-id="e30da-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e30da-138">System.String</span></span>

### <span data-ttu-id="e30da-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e30da-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="e30da-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e30da-140">OUTPUTS</span></span>

### <span data-ttu-id="e30da-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e30da-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="e30da-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e30da-142">NOTES</span></span>

## <span data-ttu-id="e30da-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e30da-143">RELATED LINKS</span></span>
