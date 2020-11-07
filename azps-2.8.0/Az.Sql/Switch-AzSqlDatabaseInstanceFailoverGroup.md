---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839567"
---
# <span data-ttu-id="c947d-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c947d-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c947d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c947d-102">SYNOPSIS</span></span>
<span data-ttu-id="c947d-103">Egy példány feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="c947d-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="c947d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c947d-104">SYNTAX</span></span>

### <span data-ttu-id="c947d-105">SwitchIFGDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c947d-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c947d-106">Példány feladatátvételi csoportjának váltása erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="c947d-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c947d-107">Példány feladatátvételi csoportjának váltása AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c947d-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c947d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c947d-108">DESCRIPTION</span></span>
<span data-ttu-id="c947d-109">Ez a parancs egy példány-feladatátvételi csoportban a felügyelt példányok szerepkörét elcseréli úgy, hogy a megadott másodlagos régióra nem vonatkozik, így az új elsődleges terület.</span><span class="sxs-lookup"><span data-stu-id="c947d-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="c947d-110">Az elsődleges végponthoz kapcsolódó összes új TDS-munkamenetet automatikusan átirányítja az új elsődleges régióba.</span><span class="sxs-lookup"><span data-stu-id="c947d-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="c947d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c947d-111">EXAMPLES</span></span>

### <span data-ttu-id="c947d-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c947d-112">Example 1</span></span>
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

<span data-ttu-id="c947d-113">Feladatátvételi művelet kijavítása, amely lehetővé teszi az adatvesztést a példány feladatátvétele csoportban.</span><span class="sxs-lookup"><span data-stu-id="c947d-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="c947d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c947d-114">Example 2</span></span>
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

<span data-ttu-id="c947d-115">Kiválaszthatja a legjobb munkafolyamatot, amely az adatvesztés vagy a hiba és a visszalépések nélkül sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="c947d-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="c947d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c947d-116">PARAMETERS</span></span>

### <span data-ttu-id="c947d-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="c947d-117">-AllowDataLoss</span></span>
<span data-ttu-id="c947d-118">Akkor is végezze el a feladatátvételt, ha a művelet az adatvesztést okozhatja.</span><span class="sxs-lookup"><span data-stu-id="c947d-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="c947d-119">Ez lehetővé teszi, hogy a feladatátvétel akkor is folytassa, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="c947d-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c947d-120">-DefaultProfile</span></span>
<span data-ttu-id="c947d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c947d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c947d-122">-InputObject</span></span>
<span data-ttu-id="c947d-123">A példány-feladatátvételi csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="c947d-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="c947d-124">-Location</span></span>
<span data-ttu-id="c947d-125">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="c947d-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c947d-126">-Name</span></span>
<span data-ttu-id="c947d-127">A példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c947d-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c947d-128">-ResourceGroupName</span></span>
<span data-ttu-id="c947d-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c947d-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c947d-130">-ResourceId</span></span>
<span data-ttu-id="c947d-131">Az átváltani kívánt példány-feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c947d-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c947d-132">-Confirm</span></span>
<span data-ttu-id="c947d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c947d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c947d-134">-WhatIf</span></span>
<span data-ttu-id="c947d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c947d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c947d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c947d-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c947d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c947d-137">CommonParameters</span></span>
<span data-ttu-id="c947d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c947d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c947d-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c947d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c947d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c947d-140">INPUTS</span></span>

### <span data-ttu-id="c947d-141">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c947d-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="c947d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c947d-142">System.String</span></span>

## <span data-ttu-id="c947d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c947d-143">OUTPUTS</span></span>

### <span data-ttu-id="c947d-144">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c947d-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c947d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c947d-145">NOTES</span></span>

## <span data-ttu-id="c947d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c947d-146">RELATED LINKS</span></span>
