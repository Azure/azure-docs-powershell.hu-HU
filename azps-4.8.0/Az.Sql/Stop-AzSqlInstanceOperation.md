---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017541"
---
# <span data-ttu-id="960bc-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="960bc-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="960bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="960bc-102">SYNOPSIS</span></span>
<span data-ttu-id="960bc-103">Leállít egy SQL-alapú felügyelt példány működését.</span><span class="sxs-lookup"><span data-stu-id="960bc-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="960bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="960bc-104">SYNTAX</span></span>

### <span data-ttu-id="960bc-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="960bc-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="960bc-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="960bc-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="960bc-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="960bc-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="960bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="960bc-108">DESCRIPTION</span></span>
<span data-ttu-id="960bc-109">Az Stop-AzSqlInstanceOperation parancsmag az SQL-alapú felügyelt példányban megadott operáció nevével leáll.</span><span class="sxs-lookup"><span data-stu-id="960bc-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="960bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="960bc-110">EXAMPLES</span></span>

### <span data-ttu-id="960bc-111">Példa 1: speciális művelet beszerzése</span><span class="sxs-lookup"><span data-stu-id="960bc-111">Example 1: Get a specific operation</span></span>
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

<span data-ttu-id="960bc-112">Ez a parancs egy SQL-alapú felügyelt példányban a "d0f5bef5-e2b1-4ef8-bb42-2e54073874f9" névvel nem működik.</span><span class="sxs-lookup"><span data-stu-id="960bc-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="960bc-113">2. példa: műveleti erőforrás-azonosító használata</span><span class="sxs-lookup"><span data-stu-id="960bc-113">Example 2: Using operation resource id</span></span>
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

<span data-ttu-id="960bc-114">Ez a parancs nem működik a $managedInstanceOperation. id azonosítójú erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="960bc-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="960bc-115">3. példa: műveleti objektum használata</span><span class="sxs-lookup"><span data-stu-id="960bc-115">Example 3: Using operation object</span></span>
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

<span data-ttu-id="960bc-116">Ez a parancs nem működik az objektum $managedInstanceOperationval.</span><span class="sxs-lookup"><span data-stu-id="960bc-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="960bc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="960bc-117">PARAMETERS</span></span>

### <span data-ttu-id="960bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960bc-118">-DefaultProfile</span></span>
<span data-ttu-id="960bc-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="960bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="960bc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="960bc-120">-Force</span></span>
<span data-ttu-id="960bc-121">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="960bc-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="960bc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="960bc-122">-InputObject</span></span>
<span data-ttu-id="960bc-123">A lemondás művelete</span><span class="sxs-lookup"><span data-stu-id="960bc-123">The operation to cancel</span></span>

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

### <span data-ttu-id="960bc-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="960bc-124">-ManagedInstanceName</span></span>
<span data-ttu-id="960bc-125">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="960bc-125">The name of the instance.</span></span>

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

### <span data-ttu-id="960bc-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="960bc-126">-Name</span></span>
<span data-ttu-id="960bc-127">A művelet neve.</span><span class="sxs-lookup"><span data-stu-id="960bc-127">The name of the operation.</span></span>

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

### <span data-ttu-id="960bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="960bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="960bc-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="960bc-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="960bc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="960bc-130">-ResourceId</span></span>
<span data-ttu-id="960bc-131">A műveleti objektum erőforrás-azonosítója a leállításhoz</span><span class="sxs-lookup"><span data-stu-id="960bc-131">The resource id of operation object to stop</span></span>

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

### <span data-ttu-id="960bc-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="960bc-132">-Confirm</span></span>
<span data-ttu-id="960bc-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="960bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="960bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="960bc-134">-WhatIf</span></span>
<span data-ttu-id="960bc-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="960bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="960bc-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="960bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="960bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960bc-137">CommonParameters</span></span>
<span data-ttu-id="960bc-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="960bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960bc-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="960bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960bc-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="960bc-140">INPUTS</span></span>

### <span data-ttu-id="960bc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="960bc-141">System.String</span></span>

### <span data-ttu-id="960bc-142">Microsoft. Azure. Command. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="960bc-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="960bc-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="960bc-143">OUTPUTS</span></span>

### <span data-ttu-id="960bc-144">Microsoft. Azure. Command. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="960bc-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="960bc-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="960bc-145">NOTES</span></span>

## <span data-ttu-id="960bc-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="960bc-146">RELATED LINKS</span></span>
