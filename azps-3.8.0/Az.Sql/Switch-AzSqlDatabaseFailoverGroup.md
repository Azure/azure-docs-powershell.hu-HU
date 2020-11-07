---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 40488a196afb35cbce4bda323b52a17c105ab649
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846497"
---
# <span data-ttu-id="568ec-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="568ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="568ec-102">SYNOPSIS</span></span>
<span data-ttu-id="568ec-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="568ec-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="568ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="568ec-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="568ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="568ec-105">DESCRIPTION</span></span>
<span data-ttu-id="568ec-106">Ez a parancs felcseréli a kiszolgálók szerepkörét egy feladatátvevő csoportban, és az összes másodlagos adatbázist átváltja az elsődleges szerepkörre.</span><span class="sxs-lookup"><span data-stu-id="568ec-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="568ec-107">Az új TDS-munkamenetek automatikusan átirányíthatók a másodlagos kiszolgálóra a DNS-ügyfél gyorsítótárának frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="568ec-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="568ec-108">Amikor az eredeti elsődleges kiszolgáló visszatért az internethez, az összes korábbi elsődleges adatbázis a másodlagos szerepkörre vált.</span><span class="sxs-lookup"><span data-stu-id="568ec-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="568ec-109">A feladatátvételi csoport másodlagos kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="568ec-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="568ec-110">Példák</span><span class="sxs-lookup"><span data-stu-id="568ec-110">EXAMPLES</span></span>

### <span data-ttu-id="568ec-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="568ec-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="568ec-112">Feladatátvételi művelet kijavítása, amely lehetővé teszi az adatvesztést a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="568ec-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="568ec-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="568ec-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="568ec-114">Kiválaszthatja a legjobb munkafolyamatot, amely az adatvesztés vagy a hiba és a visszalépések nélkül sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="568ec-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="568ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="568ec-115">PARAMETERS</span></span>

### <span data-ttu-id="568ec-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="568ec-116">-AllowDataLoss</span></span>
<span data-ttu-id="568ec-117">Akkor is végezze el a feladatátvételt, ha a művelet az adatvesztést okozhatja.</span><span class="sxs-lookup"><span data-stu-id="568ec-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="568ec-118">Ez lehetővé teszi, hogy a feladatátvétel akkor is folytassa, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="568ec-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="568ec-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="568ec-119">-AsJob</span></span>
<span data-ttu-id="568ec-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="568ec-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="568ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568ec-121">-DefaultProfile</span></span>
<span data-ttu-id="568ec-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="568ec-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="568ec-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="568ec-123">-FailoverGroupName</span></span>
<span data-ttu-id="568ec-124">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="568ec-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="568ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="568ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="568ec-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="568ec-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="568ec-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="568ec-127">-ServerName</span></span>
<span data-ttu-id="568ec-128">A feladatátvételi csoport másodlagos Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="568ec-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="568ec-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="568ec-129">-Confirm</span></span>
<span data-ttu-id="568ec-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="568ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="568ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="568ec-131">-WhatIf</span></span>
<span data-ttu-id="568ec-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="568ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="568ec-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="568ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="568ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568ec-134">CommonParameters</span></span>
<span data-ttu-id="568ec-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="568ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568ec-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="568ec-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568ec-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="568ec-137">INPUTS</span></span>

### <span data-ttu-id="568ec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="568ec-138">System.String</span></span>

## <span data-ttu-id="568ec-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="568ec-139">OUTPUTS</span></span>

### <span data-ttu-id="568ec-140">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="568ec-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="568ec-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="568ec-141">NOTES</span></span>

## <span data-ttu-id="568ec-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="568ec-142">RELATED LINKS</span></span>

[<span data-ttu-id="568ec-143">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="568ec-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="568ec-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="568ec-146">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="568ec-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="568ec-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="568ec-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="568ec-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="568ec-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
