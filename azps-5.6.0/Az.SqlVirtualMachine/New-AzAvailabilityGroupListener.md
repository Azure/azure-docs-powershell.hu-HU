---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: f187a2704ed1f23d6cc5ac7dded1c8d9cd8ae954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008326"
---
# <span data-ttu-id="bd6d8-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="bd6d8-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="bd6d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6d8-103">Létrehoz egy új rendelkezésre állási csoport felhasználóját.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="bd6d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd6d8-104">SYNTAX</span></span>

### <span data-ttu-id="bd6d8-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd6d8-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd6d8-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="bd6d8-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd6d8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd6d8-107">DESCRIPTION</span></span>
<span data-ttu-id="bd6d8-108">A New-AzAvailabilityGroupListener parancsmag létrehoz egy új elérhetőségi csoport figyelőt.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="bd6d8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd6d8-109">EXAMPLES</span></span>

### <span data-ttu-id="bd6d8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bd6d8-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="bd6d8-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6d8-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="bd6d8-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="bd6d8-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="bd6d8-113">Létrehozza az Sql Virtual Machine Group SqlVmGroup01 rendelkezésre állási csoportjának Availability Group AvailabilityGroup01 szolgáltatásának AgListener01 rendelkezésre állási csoportját.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="bd6d8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd6d8-114">PARAMETERS</span></span>

### <span data-ttu-id="bd6d8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd6d8-115">-AsJob</span></span>
<span data-ttu-id="bd6d8-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bd6d8-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6d8-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="bd6d8-118">Elérhetőségi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-118">Availability Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6d8-119">-DefaultProfile</span></span>
<span data-ttu-id="bd6d8-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd6d8-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="bd6d8-121">-IpAddress</span></span>
<span data-ttu-id="bd6d8-122">Privát IP-cím</span><span class="sxs-lookup"><span data-stu-id="bd6d8-122">Private Ip Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="bd6d8-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="bd6d8-124">Load Balancer Id</span><span class="sxs-lookup"><span data-stu-id="bd6d8-124">Load Balancer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bd6d8-125">-Name</span></span>
<span data-ttu-id="bd6d8-126">Elérhetőségi csoport hallgatója neve.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-127">-Port</span><span class="sxs-lookup"><span data-stu-id="bd6d8-127">-Port</span></span>
<span data-ttu-id="bd6d8-128">Az AG-hallgató portszáma.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-128">Port number of AG Listener.</span></span> <span data-ttu-id="bd6d8-129">Az alapértelmezett érték 1433.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-130">-Az 10000000</span><span class="sxs-lookup"><span data-stu-id="bd6d8-130">-ProbePort</span></span>
<span data-ttu-id="bd6d8-131">Portszám</span><span class="sxs-lookup"><span data-stu-id="bd6d8-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="bd6d8-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="bd6d8-133">Nyilvános IP-cím erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bd6d8-133">Public Ip Address Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6d8-134">-ResourceGroupName</span></span>
<span data-ttu-id="bd6d8-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd6d8-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="bd6d8-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="bd6d8-137">Sql VM resource-id-ekkel kapcsolatos adatok listája</span><span class="sxs-lookup"><span data-stu-id="bd6d8-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6d8-138">-SqlVMGroupName</span></span>
<span data-ttu-id="bd6d8-139">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="bd6d8-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="bd6d8-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="bd6d8-141">SQL virtual machine Group objektum.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="bd6d8-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bd6d8-142">-SubnetId</span></span>
<span data-ttu-id="bd6d8-143">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="bd6d8-143">Subnet Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6d8-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd6d8-144">-Confirm</span></span>
<span data-ttu-id="bd6d8-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd6d8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd6d8-146">-WhatIf</span></span>
<span data-ttu-id="bd6d8-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd6d8-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd6d8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6d8-149">CommonParameters</span></span>
<span data-ttu-id="bd6d8-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd6d8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6d8-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd6d8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6d8-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd6d8-152">INPUTS</span></span>

### <span data-ttu-id="bd6d8-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="bd6d8-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="bd6d8-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd6d8-154">OUTPUTS</span></span>

### <span data-ttu-id="bd6d8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="bd6d8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="bd6d8-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd6d8-156">NOTES</span></span>

## <span data-ttu-id="bd6d8-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd6d8-157">RELATED LINKS</span></span>
