---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 08192eb96b7c0a2dde84a51cf49f3b96e5429ffc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2020
ms.locfileid: "94185128"
---
# <span data-ttu-id="97af8-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="97af8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97af8-102">SYNOPSIS</span></span>
<span data-ttu-id="97af8-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="97af8-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="97af8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97af8-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97af8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97af8-105">DESCRIPTION</span></span>
<span data-ttu-id="97af8-106">Ez a parancs felcseréli a kiszolgálók szerepkörét egy feladatátvevő csoportban, és az összes másodlagos adatbázist átváltja az elsődleges szerepkörre.</span><span class="sxs-lookup"><span data-stu-id="97af8-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="97af8-107">Az új TDS-munkamenetek automatikusan átirányíthatók a másodlagos kiszolgálóra a DNS-ügyfél gyorsítótárának frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="97af8-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="97af8-108">Amikor az eredeti elsődleges kiszolgáló visszatért az internethez, az összes korábbi elsődleges adatbázis a másodlagos szerepkörre vált.</span><span class="sxs-lookup"><span data-stu-id="97af8-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="97af8-109">A feladatátvételi csoport másodlagos kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="97af8-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="97af8-110">Ha a AllowDataLoss paraméter nincs megadva, a parancs mindaddig megvárja, amíg a két szerepkör be nem vált.</span><span class="sxs-lookup"><span data-stu-id="97af8-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="97af8-111">Ha a AllowDataLoss paramétert adja meg, a parancs csak addig vár, amíg az új elsődleges felveszi a szerepkörét.</span><span class="sxs-lookup"><span data-stu-id="97af8-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="97af8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="97af8-112">EXAMPLES</span></span>

### <span data-ttu-id="97af8-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97af8-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="97af8-114">Feladatátvételi művelet kijavítása, amely lehetővé teszi az adatvesztést a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="97af8-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="97af8-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="97af8-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="97af8-116">Kiválaszthatja a legjobb munkafolyamatot, amely az adatvesztés vagy a hiba és a visszalépések nélkül sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="97af8-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="97af8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97af8-117">PARAMETERS</span></span>

### <span data-ttu-id="97af8-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="97af8-118">-AllowDataLoss</span></span>
<span data-ttu-id="97af8-119">Akkor is végezze el a feladatátvételt, ha a művelet az adatvesztést okozhatja.</span><span class="sxs-lookup"><span data-stu-id="97af8-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="97af8-120">Ez lehetővé teszi, hogy a feladatátvétel akkor is folytassa, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="97af8-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="97af8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97af8-121">-AsJob</span></span>
<span data-ttu-id="97af8-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="97af8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97af8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97af8-123">-DefaultProfile</span></span>
<span data-ttu-id="97af8-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97af8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97af8-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="97af8-125">-FailoverGroupName</span></span>
<span data-ttu-id="97af8-126">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="97af8-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="97af8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97af8-127">-ResourceGroupName</span></span>
<span data-ttu-id="97af8-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="97af8-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="97af8-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="97af8-129">-ServerName</span></span>
<span data-ttu-id="97af8-130">A feladatátvételi csoport másodlagos Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="97af8-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="97af8-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97af8-131">-Confirm</span></span>
<span data-ttu-id="97af8-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97af8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97af8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97af8-133">-WhatIf</span></span>
<span data-ttu-id="97af8-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97af8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97af8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97af8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97af8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97af8-136">CommonParameters</span></span>
<span data-ttu-id="97af8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97af8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97af8-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97af8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97af8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97af8-139">INPUTS</span></span>

### <span data-ttu-id="97af8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="97af8-140">System.String</span></span>

## <span data-ttu-id="97af8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97af8-141">OUTPUTS</span></span>

### <span data-ttu-id="97af8-142">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="97af8-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="97af8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97af8-143">NOTES</span></span>

## <span data-ttu-id="97af8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97af8-144">RELATED LINKS</span></span>

[<span data-ttu-id="97af8-145">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="97af8-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="97af8-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="97af8-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="97af8-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="97af8-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="97af8-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="97af8-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="97af8-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
