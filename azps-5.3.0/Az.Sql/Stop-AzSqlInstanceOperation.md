---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468382"
---
# <span data-ttu-id="ed502-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="ed502-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="ed502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed502-102">SYNOPSIS</span></span>
<span data-ttu-id="ed502-103">Leállítja egy SQL által felügyelt példány műveleteit.</span><span class="sxs-lookup"><span data-stu-id="ed502-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="ed502-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed502-104">SYNTAX</span></span>

### <span data-ttu-id="ed502-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed502-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed502-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed502-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed502-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed502-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed502-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed502-108">DESCRIPTION</span></span>
<span data-ttu-id="ed502-109">A Stop-AzSqlInstanceOperation leállítja a műveletet az SQL felügyelt példányon megadott műveletnévvel.</span><span class="sxs-lookup"><span data-stu-id="ed502-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="ed502-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed502-110">EXAMPLES</span></span>

### <span data-ttu-id="ed502-111">1. példa: Adott művelet lekérte</span><span class="sxs-lookup"><span data-stu-id="ed502-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="ed502-112">Ez a parancs leállítja a "d0f5bef5-e2b1-4ef8-bb42-2e54073874f9" nevű műveletet egy SQL-kezelt példányon.</span><span class="sxs-lookup"><span data-stu-id="ed502-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="ed502-113">2. példa: Művelet típusú erőforrás-azonosító használata</span><span class="sxs-lookup"><span data-stu-id="ed502-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="ed502-114">Ez a parancs leállítja a műveletet $managedInstanceOperation.Id.</span><span class="sxs-lookup"><span data-stu-id="ed502-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="ed502-115">3. példa: Műveleti objektum használata</span><span class="sxs-lookup"><span data-stu-id="ed502-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="ed502-116">Ez a parancs leállítja a műveletet az objektum $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="ed502-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="ed502-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed502-117">PARAMETERS</span></span>

### <span data-ttu-id="ed502-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed502-118">-DefaultProfile</span></span>
<span data-ttu-id="ed502-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed502-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed502-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ed502-120">-Force</span></span>
<span data-ttu-id="ed502-121">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="ed502-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ed502-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed502-122">-InputObject</span></span>
<span data-ttu-id="ed502-123">A megszakítani szükséges művelet</span><span class="sxs-lookup"><span data-stu-id="ed502-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed502-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="ed502-124">-ManagedInstanceName</span></span>
<span data-ttu-id="ed502-125">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="ed502-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed502-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ed502-126">-Name</span></span>
<span data-ttu-id="ed502-127">A művelet neve.</span><span class="sxs-lookup"><span data-stu-id="ed502-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed502-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed502-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed502-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed502-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed502-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed502-130">-ResourceId</span></span>
<span data-ttu-id="ed502-131">A leállítni szükséges műveletobjektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ed502-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed502-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed502-132">-Confirm</span></span>
<span data-ttu-id="ed502-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed502-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed502-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed502-134">-WhatIf</span></span>
<span data-ttu-id="ed502-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ed502-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed502-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed502-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed502-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed502-137">CommonParameters</span></span>
<span data-ttu-id="ed502-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed502-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed502-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed502-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed502-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed502-140">INPUTS</span></span>

### <span data-ttu-id="ed502-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ed502-141">System.String</span></span>

### <span data-ttu-id="ed502-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="ed502-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="ed502-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed502-143">OUTPUTS</span></span>

### <span data-ttu-id="ed502-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="ed502-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="ed502-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed502-145">NOTES</span></span>

## <span data-ttu-id="ed502-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed502-146">RELATED LINKS</span></span>
