---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194494"
---
# <span data-ttu-id="24d99-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="24d99-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="24d99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24d99-102">SYNOPSIS</span></span>
<span data-ttu-id="24d99-103">Egy példány feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="24d99-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="24d99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24d99-104">SYNTAX</span></span>

### <span data-ttu-id="24d99-105">SwitchInstanceFailoverGroupDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24d99-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d99-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="24d99-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d99-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="24d99-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d99-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="24d99-108">DESCRIPTION</span></span>
<span data-ttu-id="24d99-109">Ez a parancs egy példány-feladatátvételi csoportban a felügyelt példányok szerepkörét elcseréli úgy, hogy a megadott másodlagos régióra nem vonatkozik, így az új elsődleges terület.</span><span class="sxs-lookup"><span data-stu-id="24d99-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="24d99-110">Az elsődleges végponthoz kapcsolódó összes új TDS-munkamenetet automatikusan átirányítja az új elsődleges régióba.</span><span class="sxs-lookup"><span data-stu-id="24d99-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="24d99-111">Példák</span><span class="sxs-lookup"><span data-stu-id="24d99-111">EXAMPLES</span></span>

### <span data-ttu-id="24d99-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24d99-112">Example 1</span></span>
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

<span data-ttu-id="24d99-113">Feladatátvételi művelet kijavítása, amely lehetővé teszi az adatvesztést a példány feladatátvétele csoportban.</span><span class="sxs-lookup"><span data-stu-id="24d99-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="24d99-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="24d99-114">Example 2</span></span>
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

<span data-ttu-id="24d99-115">Kiválaszthatja a legjobb munkafolyamatot, amely az adatvesztés vagy a hiba és a visszalépések nélkül sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="24d99-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="24d99-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24d99-116">PARAMETERS</span></span>

### <span data-ttu-id="24d99-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="24d99-117">-AllowDataLoss</span></span>
<span data-ttu-id="24d99-118">Akkor is végezze el a feladatátvételt, ha a művelet az adatvesztést okozhatja.</span><span class="sxs-lookup"><span data-stu-id="24d99-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="24d99-119">Ez lehetővé teszi, hogy a feladatátvétel akkor is folytassa, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="24d99-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="24d99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d99-120">-DefaultProfile</span></span>
<span data-ttu-id="24d99-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24d99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d99-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24d99-122">-InputObject</span></span>
<span data-ttu-id="24d99-123">A példány-feladatátvételi csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="24d99-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="24d99-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="24d99-124">-Location</span></span>
<span data-ttu-id="24d99-125">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="24d99-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="24d99-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24d99-126">-Name</span></span>
<span data-ttu-id="24d99-127">A példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="24d99-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="24d99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d99-128">-ResourceGroupName</span></span>
<span data-ttu-id="24d99-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24d99-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="24d99-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24d99-130">-ResourceId</span></span>
<span data-ttu-id="24d99-131">Az átváltani kívánt példány-feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="24d99-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="24d99-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24d99-132">-Confirm</span></span>
<span data-ttu-id="24d99-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24d99-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d99-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d99-134">-WhatIf</span></span>
<span data-ttu-id="24d99-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24d99-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d99-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24d99-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d99-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d99-137">CommonParameters</span></span>
<span data-ttu-id="24d99-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24d99-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d99-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24d99-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d99-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d99-140">INPUTS</span></span>

### <span data-ttu-id="24d99-141">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="24d99-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="24d99-142">System. String</span><span class="sxs-lookup"><span data-stu-id="24d99-142">System.String</span></span>

## <span data-ttu-id="24d99-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d99-143">OUTPUTS</span></span>

### <span data-ttu-id="24d99-144">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="24d99-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="24d99-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24d99-145">NOTES</span></span>

## <span data-ttu-id="24d99-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24d99-146">RELATED LINKS</span></span>