---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204823"
---
# <span data-ttu-id="a7789-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-101">Restart-AzVM</span></span>

## <span data-ttu-id="a7789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7789-102">SYNOPSIS</span></span>
<span data-ttu-id="a7789-103">Újraindít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a7789-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="a7789-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a7789-104">SYNTAX</span></span>

### <span data-ttu-id="a7789-105">RestartResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7789-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7789-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7789-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7789-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7789-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7789-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7789-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7789-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a7789-109">DESCRIPTION</span></span>
<span data-ttu-id="a7789-110">Az **Restart-AzVM** parancsmag újraindít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a7789-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="a7789-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a7789-111">EXAMPLES</span></span>

### <span data-ttu-id="a7789-112">1. példa: Virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="a7789-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a7789-113">Ez a parancs újraindítja a VirtualMachine07 nevű virtuális gépet az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="a7789-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a7789-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7789-114">PARAMETERS</span></span>

### <span data-ttu-id="a7789-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7789-115">-AsJob</span></span>
<span data-ttu-id="a7789-116">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a7789-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a7789-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7789-117">-DefaultProfile</span></span>
<span data-ttu-id="a7789-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7789-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7789-119">-Id</span><span class="sxs-lookup"><span data-stu-id="a7789-119">-Id</span></span>
<span data-ttu-id="a7789-120">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a7789-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7789-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a7789-121">-Name</span></span>
<span data-ttu-id="a7789-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="a7789-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7789-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7789-123">-NoWait</span></span>
<span data-ttu-id="a7789-124">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="a7789-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a7789-125">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="a7789-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a7789-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="a7789-126">-PerformMaintenance</span></span>
<span data-ttu-id="a7789-127">A virtuális gép karbantartásának végrehajtása.</span><span class="sxs-lookup"><span data-stu-id="a7789-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7789-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7789-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7789-129">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7789-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7789-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7789-130">-Confirm</span></span>
<span data-ttu-id="a7789-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a7789-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7789-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7789-132">-WhatIf</span></span>
<span data-ttu-id="a7789-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a7789-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7789-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7789-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7789-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7789-135">CommonParameters</span></span>
<span data-ttu-id="a7789-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7789-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7789-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7789-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7789-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7789-138">INPUTS</span></span>

### <span data-ttu-id="a7789-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a7789-139">System.String</span></span>

### <span data-ttu-id="a7789-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7789-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7789-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7789-141">OUTPUTS</span></span>

### <span data-ttu-id="a7789-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a7789-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a7789-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a7789-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a7789-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a7789-144">NOTES</span></span>

## <span data-ttu-id="a7789-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7789-145">RELATED LINKS</span></span>

[<span data-ttu-id="a7789-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a7789-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a7789-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a7789-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a7789-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a7789-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7789-151">Update-AzVM</span></span>](./Update-AzVM.md)


