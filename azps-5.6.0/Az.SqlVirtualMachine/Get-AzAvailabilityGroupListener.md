---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: be20b280dccccae6f6afcc1a18514ad3dfb89ba2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008341"
---
# <span data-ttu-id="6b8e2-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="6b8e2-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="6b8e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8e2-103">Egy vagy több rendelkezésre állási csoport figyelőjére van beszúrva egy SQL virtuális gépcsoportban.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="6b8e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b8e2-104">SYNTAX</span></span>

### <span data-ttu-id="6b8e2-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b8e2-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8e2-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="6b8e2-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8e2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8e2-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b8e2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b8e2-108">DESCRIPTION</span></span>
<span data-ttu-id="6b8e2-109">A Get-AzAvailabilityGroupListener egy vagy több Rendelkezésre állási csoport figyelőt kap az SQL virtuális gépcsoportból.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="6b8e2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b8e2-110">EXAMPLES</span></span>

### <span data-ttu-id="6b8e2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b8e2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="6b8e2-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8e2-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="6b8e2-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="6b8e2-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="6b8e2-114">Ez a parancs információkat kap az SqlVmGroup01 sqlvmGroup01 és Resource Group ResourceGroup01 sqlvmGroup01 rendelkezésre állási csoport figyelőjére vonatkozó AgListener01-ről.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="6b8e2-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="6b8e2-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="6b8e2-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8e2-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="6b8e2-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="6b8e2-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="6b8e2-118">Ez a parancs információkat kap az SQL Virtual Machine Group SqlVmGroup01 és Resource Group ResourceGroup01 rendelkezésre állási csoport figyelőiről.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="6b8e2-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="6b8e2-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="6b8e2-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8e2-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="6b8e2-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="6b8e2-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="6b8e2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b8e2-122">PARAMETERS</span></span>

### <span data-ttu-id="6b8e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8e2-123">-DefaultProfile</span></span>
<span data-ttu-id="6b8e2-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b8e2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6b8e2-125">-Name</span></span>
<span data-ttu-id="6b8e2-126">Elérhetőségi csoport hallgatója neve.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="6b8e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b8e2-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b8e2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b8e2-129">-ResourceId</span></span>
<span data-ttu-id="6b8e2-130">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="6b8e2-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="6b8e2-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8e2-131">-SqlVMGroupName</span></span>
<span data-ttu-id="6b8e2-132">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="6b8e2-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="6b8e2-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="6b8e2-134">SQL virtual machine Group objektum.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="6b8e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8e2-135">CommonParameters</span></span>
<span data-ttu-id="6b8e2-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8e2-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b8e2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8e2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b8e2-138">INPUTS</span></span>

### <span data-ttu-id="6b8e2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6b8e2-139">System.String</span></span>

### <span data-ttu-id="6b8e2-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="6b8e2-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="6b8e2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b8e2-141">OUTPUTS</span></span>

### <span data-ttu-id="6b8e2-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="6b8e2-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="6b8e2-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b8e2-143">NOTES</span></span>

## <span data-ttu-id="6b8e2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b8e2-144">RELATED LINKS</span></span>
