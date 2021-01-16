---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467982"
---
# <span data-ttu-id="595cb-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="595cb-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="595cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595cb-102">SYNOPSIS</span></span>
<span data-ttu-id="595cb-103">Egy vagy több rendelkezésre állási csoport figyelőjére van beszúrva egy SQL virtuális gépcsoportban.</span><span class="sxs-lookup"><span data-stu-id="595cb-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="595cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="595cb-104">SYNTAX</span></span>

### <span data-ttu-id="595cb-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="595cb-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595cb-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="595cb-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595cb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="595cb-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="595cb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="595cb-108">DESCRIPTION</span></span>
<span data-ttu-id="595cb-109">A Get-AzAvailabilityGroupListener egy vagy több Rendelkezésre állási csoport figyelőt kap az SQL virtuális gépcsoportból.</span><span class="sxs-lookup"><span data-stu-id="595cb-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="595cb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="595cb-110">EXAMPLES</span></span>

### <span data-ttu-id="595cb-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="595cb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="595cb-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="595cb-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="595cb-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="595cb-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="595cb-114">Ez a parancs információkat kap az SqlVmGroup01 sqlvmGroup01 és Resource Group ResourceGroup01 sqlvmGroup01 rendelkezésre állási csoport figyelőjére vonatkozó AgListener01-ről.</span><span class="sxs-lookup"><span data-stu-id="595cb-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="595cb-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="595cb-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="595cb-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="595cb-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="595cb-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="595cb-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="595cb-118">Ez a parancs információkat kap az SQL Virtual Machine Group SqlVmGroup01 és Resource Group ResourceGroup01 rendelkezésre állási csoport figyelőiről.</span><span class="sxs-lookup"><span data-stu-id="595cb-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="595cb-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="595cb-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="595cb-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="595cb-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="595cb-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="595cb-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="595cb-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="595cb-122">PARAMETERS</span></span>

### <span data-ttu-id="595cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595cb-123">-DefaultProfile</span></span>
<span data-ttu-id="595cb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="595cb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="595cb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="595cb-125">-Name</span></span>
<span data-ttu-id="595cb-126">Availability Group Listener name (Elérhetőségi csoport hallgatója) neve.</span><span class="sxs-lookup"><span data-stu-id="595cb-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="595cb-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="595cb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="595cb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="595cb-129">-ResourceId</span></span>
<span data-ttu-id="595cb-130">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="595cb-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="595cb-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="595cb-131">-SqlVMGroupName</span></span>
<span data-ttu-id="595cb-132">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="595cb-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="595cb-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="595cb-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="595cb-134">SQL virtual machine Group objektum.</span><span class="sxs-lookup"><span data-stu-id="595cb-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="595cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595cb-135">CommonParameters</span></span>
<span data-ttu-id="595cb-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595cb-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="595cb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595cb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="595cb-138">INPUTS</span></span>

### <span data-ttu-id="595cb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="595cb-139">System.String</span></span>

### <span data-ttu-id="595cb-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="595cb-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="595cb-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="595cb-141">OUTPUTS</span></span>

### <span data-ttu-id="595cb-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="595cb-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="595cb-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="595cb-143">NOTES</span></span>

## <span data-ttu-id="595cb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="595cb-144">RELATED LINKS</span></span>
