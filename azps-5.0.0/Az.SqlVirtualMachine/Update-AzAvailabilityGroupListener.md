---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186519"
---
# <span data-ttu-id="ad26c-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="ad26c-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="ad26c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad26c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad26c-103">Frissíti az elérhetőségi csoport figyelőjét.</span><span class="sxs-lookup"><span data-stu-id="ad26c-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="ad26c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad26c-104">SYNTAX</span></span>

### <span data-ttu-id="ad26c-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad26c-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad26c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad26c-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad26c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad26c-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad26c-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="ad26c-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad26c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad26c-109">DESCRIPTION</span></span>
<span data-ttu-id="ad26c-110">Az Update-AzAvailabilityGroupListener parancsmag egy elérhetőségi csoport figyelőt frissít.</span><span class="sxs-lookup"><span data-stu-id="ad26c-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="ad26c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ad26c-111">EXAMPLES</span></span>

### <span data-ttu-id="ad26c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad26c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="ad26c-113">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ad26c-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ad26c-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ad26c-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="ad26c-115">Frissíti a lista SQL virtuális gépek listáját az elérhetőség csoport hallgatója számára.</span><span class="sxs-lookup"><span data-stu-id="ad26c-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="ad26c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad26c-116">PARAMETERS</span></span>

### <span data-ttu-id="ad26c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad26c-117">-AsJob</span></span>
<span data-ttu-id="ad26c-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="ad26c-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ad26c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad26c-119">-DefaultProfile</span></span>
<span data-ttu-id="ad26c-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad26c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad26c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad26c-121">-InputObject</span></span>
<span data-ttu-id="ad26c-122">Elérhetőség csoport Listener objektuma.</span><span class="sxs-lookup"><span data-stu-id="ad26c-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="ad26c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad26c-123">-Name</span></span>
<span data-ttu-id="ad26c-124">Az elérhetőség csoport Listener neve</span><span class="sxs-lookup"><span data-stu-id="ad26c-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="ad26c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad26c-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad26c-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad26c-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad26c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad26c-127">-ResourceId</span></span>
<span data-ttu-id="ad26c-128">Elérhetőség csoport figyelő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ad26c-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="ad26c-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ad26c-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="ad26c-130">Az SQL VM erőforrás-azonosítók listája</span><span class="sxs-lookup"><span data-stu-id="ad26c-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="ad26c-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="ad26c-131">-SqlVMGroupName</span></span>
<span data-ttu-id="ad26c-132">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad26c-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ad26c-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="ad26c-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="ad26c-134">SQL virtuálisgép-csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="ad26c-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="ad26c-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad26c-135">-Confirm</span></span>
<span data-ttu-id="ad26c-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad26c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad26c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad26c-137">-WhatIf</span></span>
<span data-ttu-id="ad26c-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad26c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad26c-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad26c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad26c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad26c-140">CommonParameters</span></span>
<span data-ttu-id="ad26c-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad26c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad26c-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad26c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad26c-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad26c-143">INPUTS</span></span>

### <span data-ttu-id="ad26c-144">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ad26c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="ad26c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ad26c-145">System.String</span></span>

### <span data-ttu-id="ad26c-146">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ad26c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ad26c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad26c-147">OUTPUTS</span></span>

### <span data-ttu-id="ad26c-148">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ad26c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="ad26c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad26c-149">NOTES</span></span>

## <span data-ttu-id="ad26c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad26c-150">RELATED LINKS</span></span>