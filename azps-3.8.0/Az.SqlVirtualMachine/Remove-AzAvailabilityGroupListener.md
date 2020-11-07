---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846394"
---
# <span data-ttu-id="66d65-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="66d65-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="66d65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66d65-102">SYNOPSIS</span></span>
<span data-ttu-id="66d65-103">Az elérhetőségi csoportok figyelésének törlése.</span><span class="sxs-lookup"><span data-stu-id="66d65-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="66d65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66d65-104">SYNTAX</span></span>

### <span data-ttu-id="66d65-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66d65-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66d65-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="66d65-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d65-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="66d65-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d65-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="66d65-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d65-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="66d65-109">DESCRIPTION</span></span>
<span data-ttu-id="66d65-110">Az Remove-AzAvailabilityGroupListener parancsmag törli az elérhetőségi csoport figyelőjét.</span><span class="sxs-lookup"><span data-stu-id="66d65-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="66d65-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66d65-111">EXAMPLES</span></span>

### <span data-ttu-id="66d65-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66d65-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="66d65-113">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="66d65-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="66d65-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="66d65-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="66d65-115">Törli az elérhetőség csoport figyelő AgListener01 az elérhetőség csoport AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="66d65-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="66d65-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66d65-116">PARAMETERS</span></span>

### <span data-ttu-id="66d65-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66d65-117">-AsJob</span></span>
<span data-ttu-id="66d65-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="66d65-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="66d65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d65-119">-DefaultProfile</span></span>
<span data-ttu-id="66d65-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66d65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d65-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66d65-121">-InputObject</span></span>
<span data-ttu-id="66d65-122">Elérhetőség csoport Listener objektuma.</span><span class="sxs-lookup"><span data-stu-id="66d65-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="66d65-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66d65-123">-Name</span></span>
<span data-ttu-id="66d65-124">Az elérhetőség csoport Listener neve</span><span class="sxs-lookup"><span data-stu-id="66d65-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="66d65-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66d65-125">-PassThru</span></span>
<span data-ttu-id="66d65-126">Azt adja meg, hogy a törölt erőforrás kimenete a parancsmag-végrehajtás végén történjen-e.</span><span class="sxs-lookup"><span data-stu-id="66d65-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="66d65-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d65-127">-ResourceGroupName</span></span>
<span data-ttu-id="66d65-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66d65-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="66d65-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66d65-129">-ResourceId</span></span>
<span data-ttu-id="66d65-130">Elérhetőség csoport figyelő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="66d65-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d65-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="66d65-131">-SqlVMGroupName</span></span>
<span data-ttu-id="66d65-132">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="66d65-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="66d65-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="66d65-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="66d65-134">SQL virtuálisgép-csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="66d65-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="66d65-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66d65-135">-Confirm</span></span>
<span data-ttu-id="66d65-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66d65-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d65-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d65-137">-WhatIf</span></span>
<span data-ttu-id="66d65-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66d65-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d65-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66d65-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d65-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d65-140">CommonParameters</span></span>
<span data-ttu-id="66d65-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66d65-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d65-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66d65-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d65-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d65-143">INPUTS</span></span>

### <span data-ttu-id="66d65-144">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="66d65-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="66d65-145">System. String</span><span class="sxs-lookup"><span data-stu-id="66d65-145">System.String</span></span>

### <span data-ttu-id="66d65-146">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="66d65-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="66d65-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d65-147">OUTPUTS</span></span>

### <span data-ttu-id="66d65-148">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="66d65-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="66d65-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66d65-149">NOTES</span></span>

## <span data-ttu-id="66d65-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66d65-150">RELATED LINKS</span></span>
