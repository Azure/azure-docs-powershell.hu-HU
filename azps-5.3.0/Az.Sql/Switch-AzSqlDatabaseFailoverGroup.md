---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467997"
---
# <span data-ttu-id="8e2db-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="8e2db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2db-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2db-103">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="8e2db-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="8e2db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e2db-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e2db-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e2db-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2db-106">Ez a parancs felcseréli a kiszolgálók szerepkörét egy feladatátvételi csoportban, és az összes másodlagos adatbázist az elsődleges szerepkörre cseréli.</span><span class="sxs-lookup"><span data-stu-id="8e2db-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="8e2db-107">A DNS-ügyfél gyorsítótárának frissítése után a rendszer minden új TDS-munkamenetet automatikusan a másodlagos kiszolgálóra irányít át.</span><span class="sxs-lookup"><span data-stu-id="8e2db-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="8e2db-108">Amikor az eredeti elsődleges kiszolgáló újra online állapotba vált, a korábban benne található összes elsődleges adatbázis másodlagos szerepkörre vált.</span><span class="sxs-lookup"><span data-stu-id="8e2db-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="8e2db-109">A parancs végrehajtásához a feladatátvevő csoport másodlagos kiszolgálóját kell használni.</span><span class="sxs-lookup"><span data-stu-id="8e2db-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="8e2db-110">Ha az AllowDataLoss paraméter nincs megadva, ez a parancs a két szerepkör közötti váltásig vár.</span><span class="sxs-lookup"><span data-stu-id="8e2db-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="8e2db-111">Ha az AllowDataLoss paraméter meg van adva, a parancs csak addig vár, amíg az új elsődleges felhasználó fel nem fogja vállalni a szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="8e2db-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="8e2db-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e2db-112">EXAMPLES</span></span>

### <span data-ttu-id="8e2db-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e2db-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="8e2db-114">Feladatátvételi művelettel adatvesztést engedélyez a feladatátvételi csoportban.</span><span class="sxs-lookup"><span data-stu-id="8e2db-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="8e2db-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e2db-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="8e2db-116">Olyan legjobb feladatátvételi műveletet ad meg, amely vagy sikeres lesz az adatok elvesztése nélkül, vagy sikertelen lesz, és visszavesz.</span><span class="sxs-lookup"><span data-stu-id="8e2db-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="8e2db-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e2db-117">PARAMETERS</span></span>

### <span data-ttu-id="8e2db-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="8e2db-118">-AllowDataLoss</span></span>
<span data-ttu-id="8e2db-119">Akkor is befejezheti a feladatátvételt, ha ez adatvesztést okozhat.</span><span class="sxs-lookup"><span data-stu-id="8e2db-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="8e2db-120">Ez lehetővé teszi a feladatátvételt akkor is, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="8e2db-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2db-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e2db-121">-AsJob</span></span>
<span data-ttu-id="8e2db-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8e2db-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e2db-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2db-123">-DefaultProfile</span></span>
<span data-ttu-id="8e2db-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e2db-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e2db-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2db-125">-FailoverGroupName</span></span>
<span data-ttu-id="8e2db-126">Az Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="8e2db-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2db-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2db-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e2db-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e2db-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2db-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e2db-129">-ServerName</span></span>
<span data-ttu-id="8e2db-130">A feladatátvételi csoport másodlagos Azure SQL Database Server-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="8e2db-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2db-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e2db-131">-Confirm</span></span>
<span data-ttu-id="8e2db-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e2db-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2db-133">-WhatIf</span></span>
<span data-ttu-id="8e2db-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e2db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e2db-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e2db-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2db-136">CommonParameters</span></span>
<span data-ttu-id="8e2db-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2db-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e2db-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2db-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2db-139">INPUTS</span></span>

### <span data-ttu-id="8e2db-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2db-140">System.String</span></span>

## <span data-ttu-id="8e2db-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2db-141">OUTPUTS</span></span>

### <span data-ttu-id="8e2db-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8e2db-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="8e2db-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e2db-143">NOTES</span></span>

## <span data-ttu-id="8e2db-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e2db-144">RELATED LINKS</span></span>

[<span data-ttu-id="8e2db-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e2db-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e2db-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e2db-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="8e2db-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="8e2db-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e2db-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e2db-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8e2db-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
