---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167851"
---
# <span data-ttu-id="c16f1-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="c16f1-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="c16f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c16f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c16f1-103">Ez a parancsmag a virtuális gép méretarányára beállított összes bővítményhez a legújabb elérhető verzióra frissít egy frissítéssel.</span><span class="sxs-lookup"><span data-stu-id="c16f1-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="c16f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c16f1-104">SYNTAX</span></span>

### <span data-ttu-id="c16f1-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="c16f1-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c16f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c16f1-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c16f1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c16f1-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c16f1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c16f1-108">DESCRIPTION</span></span>
<span data-ttu-id="c16f1-109">Egy folyamatos frissítést kezd, hogy a virtuális gép méretarányán az összes bővítményt a legújabb elérhető verzióra állítsa át.</span><span class="sxs-lookup"><span data-stu-id="c16f1-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="c16f1-110">Azok a bővítmények, amelyek már a legújabb elérhető verziót futtatják, nem érintik.</span><span class="sxs-lookup"><span data-stu-id="c16f1-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="c16f1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c16f1-111">EXAMPLES</span></span>

### <span data-ttu-id="c16f1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c16f1-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="c16f1-113">Ebben a példában a "MyVmssName" virtuális gép méretaránykészlete található, és egy bővítményt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="c16f1-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="c16f1-114">Az utolsó parancs futtatja a bővítmény frissítésének folyamatban lévő folyamatát.</span><span class="sxs-lookup"><span data-stu-id="c16f1-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="c16f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c16f1-115">PARAMETERS</span></span>

### <span data-ttu-id="c16f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c16f1-116">-AsJob</span></span>
<span data-ttu-id="c16f1-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c16f1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c16f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16f1-118">-DefaultProfile</span></span>
<span data-ttu-id="c16f1-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c16f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c16f1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c16f1-120">-ResourceGroupName</span></span>
<span data-ttu-id="c16f1-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c16f1-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16f1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c16f1-122">-ResourceId</span></span>
<span data-ttu-id="c16f1-123">A VM méretaránykészlet-objektumának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c16f1-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c16f1-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c16f1-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c16f1-125">A VM méretarány-beállítása objektum.</span><span class="sxs-lookup"><span data-stu-id="c16f1-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c16f1-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c16f1-126">-VMScaleSetName</span></span>
<span data-ttu-id="c16f1-127">A VM-méretkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="c16f1-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16f1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c16f1-128">-Confirm</span></span>
<span data-ttu-id="c16f1-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c16f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c16f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c16f1-130">-WhatIf</span></span>
<span data-ttu-id="c16f1-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c16f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c16f1-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c16f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c16f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16f1-133">CommonParameters</span></span>
<span data-ttu-id="c16f1-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16f1-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c16f1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16f1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c16f1-136">INPUTS</span></span>

### <span data-ttu-id="c16f1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c16f1-137">System.String</span></span>

### <span data-ttu-id="c16f1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c16f1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c16f1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c16f1-139">OUTPUTS</span></span>

### <span data-ttu-id="c16f1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c16f1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c16f1-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c16f1-141">NOTES</span></span>

## <span data-ttu-id="c16f1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c16f1-142">RELATED LINKS</span></span>
