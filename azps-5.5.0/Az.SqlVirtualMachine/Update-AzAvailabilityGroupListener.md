---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155162"
---
# <span data-ttu-id="13bc0-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="13bc0-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="13bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="13bc0-103">Frissíti az elérhetőségi csoport hallgatóját.</span><span class="sxs-lookup"><span data-stu-id="13bc0-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="13bc0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13bc0-104">SYNTAX</span></span>

### <span data-ttu-id="13bc0-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13bc0-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13bc0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="13bc0-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13bc0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13bc0-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13bc0-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="13bc0-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13bc0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13bc0-109">DESCRIPTION</span></span>
<span data-ttu-id="13bc0-110">A Update-AzAvailabilityGroupListener parancsmag frissíti az elérhetőségi csoport figyelését.</span><span class="sxs-lookup"><span data-stu-id="13bc0-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="13bc0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13bc0-111">EXAMPLES</span></span>

### <span data-ttu-id="13bc0-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="13bc0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="13bc0-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="13bc0-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="13bc0-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="13bc0-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="13bc0-115">Frissíti az SQL virtuális gépek listáját az elérhetőségi csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="13bc0-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="13bc0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13bc0-116">PARAMETERS</span></span>

### <span data-ttu-id="13bc0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13bc0-117">-AsJob</span></span>
<span data-ttu-id="13bc0-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="13bc0-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="13bc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bc0-119">-DefaultProfile</span></span>
<span data-ttu-id="13bc0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13bc0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13bc0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13bc0-121">-InputObject</span></span>
<span data-ttu-id="13bc0-122">Availability Group Listener objektum.</span><span class="sxs-lookup"><span data-stu-id="13bc0-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="13bc0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="13bc0-123">-Name</span></span>
<span data-ttu-id="13bc0-124">Elérhetőségi csoport hallgatója neve.</span><span class="sxs-lookup"><span data-stu-id="13bc0-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="13bc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13bc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="13bc0-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13bc0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="13bc0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13bc0-127">-ResourceId</span></span>
<span data-ttu-id="13bc0-128">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="13bc0-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="13bc0-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="13bc0-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="13bc0-130">Sql VM resource-id-ekkel kapcsolatos adatok listája</span><span class="sxs-lookup"><span data-stu-id="13bc0-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="13bc0-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="13bc0-131">-SqlVMGroupName</span></span>
<span data-ttu-id="13bc0-132">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13bc0-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="13bc0-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="13bc0-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="13bc0-134">SQL virtual machine Group objektum.</span><span class="sxs-lookup"><span data-stu-id="13bc0-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="13bc0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13bc0-135">-Confirm</span></span>
<span data-ttu-id="13bc0-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13bc0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13bc0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13bc0-137">-WhatIf</span></span>
<span data-ttu-id="13bc0-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13bc0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13bc0-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13bc0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13bc0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bc0-140">CommonParameters</span></span>
<span data-ttu-id="13bc0-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bc0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bc0-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13bc0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bc0-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13bc0-143">INPUTS</span></span>

### <span data-ttu-id="13bc0-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="13bc0-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="13bc0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="13bc0-145">System.String</span></span>

### <span data-ttu-id="13bc0-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="13bc0-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="13bc0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13bc0-147">OUTPUTS</span></span>

### <span data-ttu-id="13bc0-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="13bc0-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="13bc0-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13bc0-149">NOTES</span></span>

## <span data-ttu-id="13bc0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13bc0-150">RELATED LINKS</span></span>
