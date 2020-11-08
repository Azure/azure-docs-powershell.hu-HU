---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194490"
---
# <span data-ttu-id="3c72e-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="3c72e-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="3c72e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c72e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c72e-103">Egy vagy több elérhetőségi csoport hallgatójának beszerzése egy SQL-virtuálisgép-csoportban</span><span class="sxs-lookup"><span data-stu-id="3c72e-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="3c72e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c72e-104">SYNTAX</span></span>

### <span data-ttu-id="3c72e-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c72e-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c72e-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="3c72e-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c72e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c72e-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c72e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c72e-108">DESCRIPTION</span></span>
<span data-ttu-id="3c72e-109">A Get-AzAvailabilityGroupListener egy vagy több elérhetőségi csoport hallgatóját kapja az SQL virtuálisgép-csoportból.</span><span class="sxs-lookup"><span data-stu-id="3c72e-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="3c72e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c72e-110">EXAMPLES</span></span>

### <span data-ttu-id="3c72e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c72e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="3c72e-112">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3c72e-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3c72e-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3c72e-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3c72e-114">Ez a parancs információt kap az elérhetőségi csoport figyelő AgListener01 az SQL Virtual Machine Group SqlVmGroup01 és az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3c72e-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="3c72e-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="3c72e-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="3c72e-116">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3c72e-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3c72e-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3c72e-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3c72e-118">Ez a parancs információkat kap az összes elérhetőségi csoport Figyelőkről az SQL Virtual Machine Group SqlVmGroup01 és az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3c72e-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="3c72e-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="3c72e-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="3c72e-120">Név ResourceGroupName csoportnév AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3c72e-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3c72e-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3c72e-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="3c72e-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c72e-122">PARAMETERS</span></span>

### <span data-ttu-id="3c72e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c72e-123">-DefaultProfile</span></span>
<span data-ttu-id="3c72e-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c72e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c72e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c72e-125">-Name</span></span>
<span data-ttu-id="3c72e-126">Az elérhetőség csoport Listener neve</span><span class="sxs-lookup"><span data-stu-id="3c72e-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="3c72e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c72e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c72e-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c72e-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c72e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c72e-129">-ResourceId</span></span>
<span data-ttu-id="3c72e-130">Elérhetőség csoport figyelő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3c72e-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="3c72e-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="3c72e-131">-SqlVMGroupName</span></span>
<span data-ttu-id="3c72e-132">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c72e-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="3c72e-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="3c72e-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="3c72e-134">SQL virtuálisgép-csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="3c72e-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="3c72e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c72e-135">CommonParameters</span></span>
<span data-ttu-id="3c72e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c72e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c72e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c72e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c72e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c72e-138">INPUTS</span></span>

### <span data-ttu-id="3c72e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3c72e-139">System.String</span></span>

### <span data-ttu-id="3c72e-140">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="3c72e-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="3c72e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c72e-141">OUTPUTS</span></span>

### <span data-ttu-id="3c72e-142">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3c72e-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="3c72e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c72e-143">NOTES</span></span>

## <span data-ttu-id="3c72e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c72e-144">RELATED LINKS</span></span>
