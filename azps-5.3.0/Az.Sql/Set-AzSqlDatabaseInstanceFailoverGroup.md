---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465994"
---
# <span data-ttu-id="e4295-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e4295-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="e4295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4295-102">SYNOPSIS</span></span>
<span data-ttu-id="e4295-103">Módosítja egy példány feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e4295-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="e4295-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4295-104">SYNTAX</span></span>

### <span data-ttu-id="e4295-105">SetInstanceFailoverGroupDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4295-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4295-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e4295-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4295-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="e4295-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4295-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4295-108">DESCRIPTION</span></span>
<span data-ttu-id="e4295-109">Ez a parancs módosítja egy példány feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e4295-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="e4295-110">A parancs végrehajtásához a Példány feladatátvétele csoport elsődleges régióját kell használni.</span><span class="sxs-lookup"><span data-stu-id="e4295-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="e4295-111">A "-GracePeriodWithDataLossHours" paraméter csak az 1 óránál nem kisebb értékeket támogatja a Példány feladatátvételi csoportok funkció előzetes verziója esetén.</span><span class="sxs-lookup"><span data-stu-id="e4295-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="e4295-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4295-112">EXAMPLES</span></span>

### <span data-ttu-id="e4295-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="e4295-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="e4295-114">A feladatátvételi csoport feladatátvételi házirendjének "Kézi" beállítását állítja be a feladatátvételi csoportban.</span><span class="sxs-lookup"><span data-stu-id="e4295-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="e4295-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4295-115">PARAMETERS</span></span>

### <span data-ttu-id="e4295-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="e4295-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="e4295-117">A másodlagos kiszolgálón a kimaradás az írásra csak olvasható végpont automatikus feladatátvételét váltja-e ki.</span><span class="sxs-lookup"><span data-stu-id="e4295-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="e4295-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4295-118">-DefaultProfile</span></span>
<span data-ttu-id="e4295-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4295-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4295-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e4295-120">-FailoverPolicy</span></span>
<span data-ttu-id="e4295-121">A példány feladatátvételi csoportjának feladatátvételi házirende.</span><span class="sxs-lookup"><span data-stu-id="e4295-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e4295-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="e4295-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="e4295-123">Az automatikus feladatátvétel indításakor eltelt időintervallum, ha kimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem fejezhető be adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="e4295-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4295-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4295-124">-InputObject</span></span>
<span data-ttu-id="e4295-125">The Instance Failover Group object to set</span><span class="sxs-lookup"><span data-stu-id="e4295-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4295-126">-Location</span><span class="sxs-lookup"><span data-stu-id="e4295-126">-Location</span></span>
<span data-ttu-id="e4295-127">Annak a helyi régiónak a neve, amelyből lekéri a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="e4295-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4295-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e4295-128">-Name</span></span>
<span data-ttu-id="e4295-129">A Példány feladatátvétele csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4295-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4295-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4295-130">-ResourceGroupName</span></span>
<span data-ttu-id="e4295-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4295-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4295-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4295-132">-ResourceId</span></span>
<span data-ttu-id="e4295-133">A beállítani szükséges példány feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e4295-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4295-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4295-134">-Confirm</span></span>
<span data-ttu-id="e4295-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4295-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4295-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4295-136">-WhatIf</span></span>
<span data-ttu-id="e4295-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4295-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4295-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4295-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4295-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4295-139">CommonParameters</span></span>
<span data-ttu-id="e4295-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4295-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4295-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4295-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4295-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4295-142">INPUTS</span></span>

### <span data-ttu-id="e4295-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e4295-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="e4295-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e4295-144">System.String</span></span>

## <span data-ttu-id="e4295-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4295-145">OUTPUTS</span></span>

### <span data-ttu-id="e4295-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e4295-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="e4295-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4295-147">NOTES</span></span>

## <span data-ttu-id="e4295-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4295-148">RELATED LINKS</span></span>
