---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334422"
---
# <span data-ttu-id="1fe98-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="1fe98-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="1fe98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe98-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe98-103">Az elérhetőségi csoportokat hallgató felhasználó törlése.</span><span class="sxs-lookup"><span data-stu-id="1fe98-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="1fe98-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1fe98-104">SYNTAX</span></span>

### <span data-ttu-id="1fe98-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fe98-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fe98-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe98-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe98-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe98-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe98-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="1fe98-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe98-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1fe98-109">DESCRIPTION</span></span>
<span data-ttu-id="1fe98-110">A Remove-AzAvailabilityGroupListener parancsmag töröl egy rendelkezésre állási csoport figyelőt.</span><span class="sxs-lookup"><span data-stu-id="1fe98-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="1fe98-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1fe98-111">EXAMPLES</span></span>

### <span data-ttu-id="1fe98-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1fe98-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="1fe98-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe98-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="1fe98-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="1fe98-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="1fe98-115">Törli az Elérhetőségi csoport hallgatója az AgListener01 csoportot az Elérhetőségi csoport rendelkezésre állása Csoport01 csoportjában.</span><span class="sxs-lookup"><span data-stu-id="1fe98-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="1fe98-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fe98-116">PARAMETERS</span></span>

### <span data-ttu-id="1fe98-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fe98-117">-AsJob</span></span>
<span data-ttu-id="1fe98-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="1fe98-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1fe98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe98-119">-DefaultProfile</span></span>
<span data-ttu-id="1fe98-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fe98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe98-121">-InputObject</span></span>
<span data-ttu-id="1fe98-122">Availability Group Listener objektum.</span><span class="sxs-lookup"><span data-stu-id="1fe98-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="1fe98-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1fe98-123">-Name</span></span>
<span data-ttu-id="1fe98-124">Availability Group Listener name (Elérhetőségi csoport hallgatója) neve.</span><span class="sxs-lookup"><span data-stu-id="1fe98-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="1fe98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe98-125">-PassThru</span></span>
<span data-ttu-id="1fe98-126">Azt adja meg, hogy a parancsmag végrehajtása után kimenetként adja-e meg a törölt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="1fe98-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="1fe98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe98-127">-ResourceGroupName</span></span>
<span data-ttu-id="1fe98-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fe98-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fe98-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe98-129">-ResourceId</span></span>
<span data-ttu-id="1fe98-130">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="1fe98-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="1fe98-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe98-131">-SqlVMGroupName</span></span>
<span data-ttu-id="1fe98-132">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fe98-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="1fe98-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="1fe98-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="1fe98-134">SQL virtual machine Group objektum.</span><span class="sxs-lookup"><span data-stu-id="1fe98-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="1fe98-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fe98-135">-Confirm</span></span>
<span data-ttu-id="1fe98-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1fe98-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe98-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe98-137">-WhatIf</span></span>
<span data-ttu-id="1fe98-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1fe98-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe98-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1fe98-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe98-140">CommonParameters</span></span>
<span data-ttu-id="1fe98-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe98-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fe98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe98-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fe98-143">INPUTS</span></span>

### <span data-ttu-id="1fe98-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="1fe98-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="1fe98-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe98-145">System.String</span></span>

### <span data-ttu-id="1fe98-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="1fe98-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="1fe98-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe98-147">OUTPUTS</span></span>

### <span data-ttu-id="1fe98-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="1fe98-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="1fe98-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1fe98-149">NOTES</span></span>

## <span data-ttu-id="1fe98-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fe98-150">RELATED LINKS</span></span>
