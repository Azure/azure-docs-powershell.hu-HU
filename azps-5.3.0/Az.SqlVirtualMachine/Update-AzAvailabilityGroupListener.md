---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476610"
---
# <span data-ttu-id="e4579-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="e4579-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="e4579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4579-102">SYNOPSIS</span></span>
<span data-ttu-id="e4579-103">Frissíti az elérhetőségi csoport hallgatóját.</span><span class="sxs-lookup"><span data-stu-id="e4579-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="e4579-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4579-104">SYNTAX</span></span>

### <span data-ttu-id="e4579-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4579-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4579-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e4579-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4579-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4579-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4579-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="e4579-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4579-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4579-109">DESCRIPTION</span></span>
<span data-ttu-id="e4579-110">A Update-AzAvailabilityGroupListener parancsmag frissíti az elérhetőségi csoport figyelését.</span><span class="sxs-lookup"><span data-stu-id="e4579-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="e4579-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4579-111">EXAMPLES</span></span>

### <span data-ttu-id="e4579-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e4579-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="e4579-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="e4579-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="e4579-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="e4579-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="e4579-115">Frissíti az SQL virtuális gépek listáját az elérhetőségi csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="e4579-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="e4579-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4579-116">PARAMETERS</span></span>

### <span data-ttu-id="e4579-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4579-117">-AsJob</span></span>
<span data-ttu-id="e4579-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="e4579-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e4579-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4579-119">-DefaultProfile</span></span>
<span data-ttu-id="e4579-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4579-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4579-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4579-121">-InputObject</span></span>
<span data-ttu-id="e4579-122">Availability Group Listener objektum.</span><span class="sxs-lookup"><span data-stu-id="e4579-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e4579-123">-Name</span></span>
<span data-ttu-id="e4579-124">Availability Group Listener name (Elérhetőségi csoport hallgatója) neve.</span><span class="sxs-lookup"><span data-stu-id="e4579-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4579-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4579-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4579-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4579-127">-ResourceId</span></span>
<span data-ttu-id="e4579-128">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="e4579-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e4579-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="e4579-130">Sql VM resource-id-ekkel kapcsolatos adatok listája</span><span class="sxs-lookup"><span data-stu-id="e4579-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="e4579-131">-SqlVMGroupName</span></span>
<span data-ttu-id="e4579-132">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4579-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="e4579-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="e4579-134">SQL virtual machine Group objektum.</span><span class="sxs-lookup"><span data-stu-id="e4579-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4579-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4579-135">-Confirm</span></span>
<span data-ttu-id="e4579-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4579-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4579-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4579-137">-WhatIf</span></span>
<span data-ttu-id="e4579-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4579-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4579-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4579-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4579-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4579-140">CommonParameters</span></span>
<span data-ttu-id="e4579-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4579-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4579-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4579-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4579-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4579-143">INPUTS</span></span>

### <span data-ttu-id="e4579-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="e4579-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="e4579-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e4579-145">System.String</span></span>

### <span data-ttu-id="e4579-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e4579-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e4579-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4579-147">OUTPUTS</span></span>

### <span data-ttu-id="e4579-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="e4579-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="e4579-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4579-149">NOTES</span></span>

## <span data-ttu-id="e4579-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4579-150">RELATED LINKS</span></span>
