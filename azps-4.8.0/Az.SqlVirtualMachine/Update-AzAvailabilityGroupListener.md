---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181281"
---
# <span data-ttu-id="3f6eb-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="3f6eb-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="3f6eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6eb-103">Frissíti az elérhetőségi csoport figyelőjét.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="3f6eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f6eb-104">SYNTAX</span></span>

### <span data-ttu-id="3f6eb-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f6eb-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f6eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3f6eb-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f6eb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6eb-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f6eb-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="3f6eb-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f6eb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f6eb-109">DESCRIPTION</span></span>
<span data-ttu-id="3f6eb-110">Az Update-AzAvailabilityGroupListener parancsmag egy elérhetőségi csoport figyelőt frissít.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="3f6eb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3f6eb-111">EXAMPLES</span></span>

### <span data-ttu-id="3f6eb-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3f6eb-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="3f6eb-113">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6eb-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3f6eb-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3f6eb-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3f6eb-115">Frissíti a lista SQL virtuális gépek listáját az elérhetőség csoport hallgatója számára.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="3f6eb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f6eb-116">PARAMETERS</span></span>

### <span data-ttu-id="3f6eb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f6eb-117">-AsJob</span></span>
<span data-ttu-id="3f6eb-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3f6eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6eb-119">-DefaultProfile</span></span>
<span data-ttu-id="3f6eb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f6eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f6eb-121">-InputObject</span></span>
<span data-ttu-id="3f6eb-122">Elérhetőség csoport Listener objektuma.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="3f6eb-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f6eb-123">-Name</span></span>
<span data-ttu-id="3f6eb-124">Az elérhetőség csoport Listener neve</span><span class="sxs-lookup"><span data-stu-id="3f6eb-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="3f6eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f6eb-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f6eb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6eb-127">-ResourceId</span></span>
<span data-ttu-id="3f6eb-128">Elérhetőség csoport figyelő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3f6eb-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="3f6eb-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3f6eb-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="3f6eb-130">Az SQL VM erőforrás-azonosítók listája</span><span class="sxs-lookup"><span data-stu-id="3f6eb-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="3f6eb-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6eb-131">-SqlVMGroupName</span></span>
<span data-ttu-id="3f6eb-132">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="3f6eb-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="3f6eb-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="3f6eb-134">SQL virtuálisgép-csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="3f6eb-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f6eb-135">-Confirm</span></span>
<span data-ttu-id="3f6eb-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f6eb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f6eb-137">-WhatIf</span></span>
<span data-ttu-id="3f6eb-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f6eb-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f6eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6eb-140">CommonParameters</span></span>
<span data-ttu-id="3f6eb-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f6eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6eb-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f6eb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6eb-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f6eb-143">INPUTS</span></span>

### <span data-ttu-id="3f6eb-144">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3f6eb-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="3f6eb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3f6eb-145">System.String</span></span>

### <span data-ttu-id="3f6eb-146">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="3f6eb-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="3f6eb-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f6eb-147">OUTPUTS</span></span>

### <span data-ttu-id="3f6eb-148">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3f6eb-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="3f6eb-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f6eb-149">NOTES</span></span>

## <span data-ttu-id="3f6eb-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f6eb-150">RELATED LINKS</span></span>
