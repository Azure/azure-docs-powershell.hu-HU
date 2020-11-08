---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194487"
---
# <span data-ttu-id="82325-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="82325-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="82325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82325-102">SYNOPSIS</span></span>
<span data-ttu-id="82325-103">Új elérhetőségi csoport figyelőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82325-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="82325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82325-104">SYNTAX</span></span>

### <span data-ttu-id="82325-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82325-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82325-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="82325-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82325-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="82325-107">DESCRIPTION</span></span>
<span data-ttu-id="82325-108">Az New-AzAvailabilityGroupListener parancsmag új elérhetőségi csoport figyelőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82325-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="82325-109">Példák</span><span class="sxs-lookup"><span data-stu-id="82325-109">EXAMPLES</span></span>

### <span data-ttu-id="82325-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="82325-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="82325-111">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="82325-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="82325-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="82325-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="82325-113">Új elérhetőségi csoport figyelő AgListener01 hoz létre az elérhetőség csoport AvailabilityGroup01 az SQL Virtual Machine Group SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="82325-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="82325-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82325-114">PARAMETERS</span></span>

### <span data-ttu-id="82325-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82325-115">-AsJob</span></span>
<span data-ttu-id="82325-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="82325-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="82325-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="82325-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="82325-118">Elérhetőségi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="82325-118">Availability Group name.</span></span>

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

### <span data-ttu-id="82325-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82325-119">-DefaultProfile</span></span>
<span data-ttu-id="82325-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82325-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82325-121">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="82325-121">-IpAddress</span></span>
<span data-ttu-id="82325-122">Privát IP-cím</span><span class="sxs-lookup"><span data-stu-id="82325-122">Private Ip Address</span></span>

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

### <span data-ttu-id="82325-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="82325-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="82325-124">Terheléselosztó azonosító</span><span class="sxs-lookup"><span data-stu-id="82325-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="82325-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82325-125">-Name</span></span>
<span data-ttu-id="82325-126">Az elérhetőség csoport Listener neve</span><span class="sxs-lookup"><span data-stu-id="82325-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="82325-127">-Port</span><span class="sxs-lookup"><span data-stu-id="82325-127">-Port</span></span>
<span data-ttu-id="82325-128">Az AG-figyelő portjának száma.</span><span class="sxs-lookup"><span data-stu-id="82325-128">Port number of AG Listener.</span></span> <span data-ttu-id="82325-129">Az alapértelmezett érték a 1433.</span><span class="sxs-lookup"><span data-stu-id="82325-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="82325-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="82325-130">-ProbePort</span></span>
<span data-ttu-id="82325-131">Szonda port</span><span class="sxs-lookup"><span data-stu-id="82325-131">Probe Port</span></span>

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

### <span data-ttu-id="82325-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="82325-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="82325-133">Nyilvános IP-cím erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="82325-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="82325-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82325-134">-ResourceGroupName</span></span>
<span data-ttu-id="82325-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="82325-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="82325-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="82325-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="82325-137">Az SQL VM erőforrás-azonosítók listája</span><span class="sxs-lookup"><span data-stu-id="82325-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="82325-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="82325-138">-SqlVMGroupName</span></span>
<span data-ttu-id="82325-139">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="82325-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="82325-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="82325-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="82325-141">SQL virtuálisgép-csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="82325-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="82325-142">– NetI</span><span class="sxs-lookup"><span data-stu-id="82325-142">-SubnetId</span></span>
<span data-ttu-id="82325-143">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="82325-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="82325-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82325-144">-Confirm</span></span>
<span data-ttu-id="82325-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82325-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82325-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82325-146">-WhatIf</span></span>
<span data-ttu-id="82325-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82325-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82325-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82325-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82325-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82325-149">CommonParameters</span></span>
<span data-ttu-id="82325-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82325-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82325-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="82325-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82325-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82325-152">INPUTS</span></span>

### <span data-ttu-id="82325-153">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="82325-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="82325-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82325-154">OUTPUTS</span></span>

### <span data-ttu-id="82325-155">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="82325-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="82325-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82325-156">NOTES</span></span>

## <span data-ttu-id="82325-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82325-157">RELATED LINKS</span></span>
