---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168602"
---
# <span data-ttu-id="0ca99-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0ca99-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="0ca99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca99-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca99-103">Eltávolítja egy eszköz iot-szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="0ca99-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="0ca99-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ca99-104">SYNTAX</span></span>

### <span data-ttu-id="0ca99-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ca99-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca99-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca99-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca99-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca99-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ca99-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ca99-108">DESCRIPTION</span></span>
<span data-ttu-id="0ca99-109">A **Remove-AzStackEdgeRole** parancsmag eltávolítja a stack edge-es eszközök iot-szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="0ca99-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="0ca99-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ca99-110">EXAMPLES</span></span>

### <span data-ttu-id="0ca99-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ca99-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="0ca99-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ca99-112">PARAMETERS</span></span>

### <span data-ttu-id="0ca99-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ca99-113">-AsJob</span></span>
<span data-ttu-id="0ca99-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0ca99-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ca99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca99-115">-DefaultProfile</span></span>
<span data-ttu-id="0ca99-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ca99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ca99-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0ca99-117">-DeviceName</span></span>
<span data-ttu-id="0ca99-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="0ca99-118">Device Name</span></span>

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

### <span data-ttu-id="0ca99-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ca99-119">-InputObject</span></span>
<span data-ttu-id="0ca99-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="0ca99-120">Input Object</span></span>

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

### <span data-ttu-id="0ca99-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0ca99-121">-Name</span></span>
<span data-ttu-id="0ca99-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="0ca99-122">Resource Name</span></span>

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

### <span data-ttu-id="0ca99-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ca99-123">-PassThru</span></span>
<span data-ttu-id="0ca99-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="0ca99-124">returns true if successful</span></span>

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

### <span data-ttu-id="0ca99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca99-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ca99-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0ca99-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0ca99-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca99-127">-ResourceId</span></span>
<span data-ttu-id="0ca99-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca99-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="0ca99-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ca99-129">-Confirm</span></span>
<span data-ttu-id="0ca99-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ca99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca99-131">-WhatIf</span></span>
<span data-ttu-id="0ca99-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ca99-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ca99-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ca99-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca99-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca99-134">CommonParameters</span></span>
<span data-ttu-id="0ca99-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca99-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca99-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ca99-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca99-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ca99-137">INPUTS</span></span>

### <span data-ttu-id="0ca99-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0ca99-138">System.String</span></span>

### <span data-ttu-id="0ca99-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0ca99-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="0ca99-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ca99-140">OUTPUTS</span></span>

### <span data-ttu-id="0ca99-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0ca99-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="0ca99-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ca99-142">NOTES</span></span>

## <span data-ttu-id="0ca99-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ca99-143">RELATED LINKS</span></span>
