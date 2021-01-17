---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465975"
---
# <span data-ttu-id="11be7-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="11be7-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="11be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11be7-102">SYNOPSIS</span></span>
<span data-ttu-id="11be7-103">Egy példány feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="11be7-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="11be7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11be7-104">SYNTAX</span></span>

### <span data-ttu-id="11be7-105">SwitchInstanceFailoverGroupDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11be7-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11be7-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11be7-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11be7-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11be7-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11be7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11be7-108">DESCRIPTION</span></span>
<span data-ttu-id="11be7-109">Ez a parancs felcseréli a felügyelt példányok szerepkörét egy példány feladatátvételi csoportjában azáltal, hogy feladatátvételt ad a megadott másodlagos régiónak, így az lesz az új elsődleges régió.</span><span class="sxs-lookup"><span data-stu-id="11be7-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="11be7-110">Az elsődleges végponthoz csatlakozó összes új TDS-munkamenet automatikusan át lesz irányítva az új elsődleges régióba.</span><span class="sxs-lookup"><span data-stu-id="11be7-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="11be7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11be7-111">EXAMPLES</span></span>

### <span data-ttu-id="11be7-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="11be7-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
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
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="11be7-113">Feladatátvételi művelettel adatvesztést engedélyez a példány feladatátvételi csoportjában.</span><span class="sxs-lookup"><span data-stu-id="11be7-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="11be7-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="11be7-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
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
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="11be7-115">Olyan legjobb feladatátvételi műveletet ad meg, amely vagy sikeres lesz az adatok elvesztése nélkül, vagy sikertelen lesz, majd visszagördül.</span><span class="sxs-lookup"><span data-stu-id="11be7-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="11be7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11be7-116">PARAMETERS</span></span>

### <span data-ttu-id="11be7-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="11be7-117">-AllowDataLoss</span></span>
<span data-ttu-id="11be7-118">Akkor is befejezheti a feladatátvételt, ha ez adatvesztést okozhat.</span><span class="sxs-lookup"><span data-stu-id="11be7-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="11be7-119">Ez lehetővé teszi a feladatátvételt akkor is, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="11be7-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="11be7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11be7-120">-DefaultProfile</span></span>
<span data-ttu-id="11be7-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11be7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11be7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11be7-122">-InputObject</span></span>
<span data-ttu-id="11be7-123">The Instance Failover Group object to switch</span><span class="sxs-lookup"><span data-stu-id="11be7-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11be7-124">-Location</span><span class="sxs-lookup"><span data-stu-id="11be7-124">-Location</span></span>
<span data-ttu-id="11be7-125">Annak a helyi régiónak a neve, amelyből lekéri a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="11be7-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11be7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="11be7-126">-Name</span></span>
<span data-ttu-id="11be7-127">A Példány feladatátvétele csoport neve.</span><span class="sxs-lookup"><span data-stu-id="11be7-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11be7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11be7-128">-ResourceGroupName</span></span>
<span data-ttu-id="11be7-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11be7-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11be7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11be7-130">-ResourceId</span></span>
<span data-ttu-id="11be7-131">A váltáshoz szükséges példány feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="11be7-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11be7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11be7-132">-Confirm</span></span>
<span data-ttu-id="11be7-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11be7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11be7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11be7-134">-WhatIf</span></span>
<span data-ttu-id="11be7-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11be7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11be7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11be7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11be7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11be7-137">CommonParameters</span></span>
<span data-ttu-id="11be7-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11be7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11be7-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11be7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11be7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11be7-140">INPUTS</span></span>

### <span data-ttu-id="11be7-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="11be7-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="11be7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="11be7-142">System.String</span></span>

## <span data-ttu-id="11be7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11be7-143">OUTPUTS</span></span>

### <span data-ttu-id="11be7-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="11be7-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="11be7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11be7-145">NOTES</span></span>

## <span data-ttu-id="11be7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11be7-146">RELATED LINKS</span></span>
