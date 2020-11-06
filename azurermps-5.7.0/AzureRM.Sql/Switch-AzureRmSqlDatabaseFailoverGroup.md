---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: b11478e02baa515fdbd3f3625392616245f2b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501339"
---
# <span data-ttu-id="de6cb-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="de6cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="de6cb-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="de6cb-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de6cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de6cb-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de6cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de6cb-105">DESCRIPTION</span></span>
<span data-ttu-id="de6cb-106">Ez a parancs felcseréli a kiszolgálók szerepkörét egy feladatátvevő csoportban, és az összes másodlagos adatbázist átváltja az elsődleges szerepkörre.</span><span class="sxs-lookup"><span data-stu-id="de6cb-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="de6cb-107">Az új TDS-munkamenetek automatikusan átirányíthatók a másodlagos kiszolgálóra a DNS-ügyfél gyorsítótárának frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="de6cb-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="de6cb-108">Amikor az eredeti elsődleges kiszolgáló visszatért az internethez, az összes korábbi elsődleges adatbázis a másodlagos szerepkörre vált.</span><span class="sxs-lookup"><span data-stu-id="de6cb-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="de6cb-109">A feladatátvételi csoport másodlagos kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="de6cb-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="de6cb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="de6cb-110">EXAMPLES</span></span>

### <span data-ttu-id="de6cb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de6cb-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="de6cb-112">Feladatátvételi művelet kijavítása, amely lehetővé teszi az adatvesztést a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="de6cb-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="de6cb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="de6cb-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="de6cb-114">Kiválaszthatja a legjobb munkafolyamatot, amely az adatvesztés vagy a hiba és a visszalépések nélkül sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="de6cb-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="de6cb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de6cb-115">PARAMETERS</span></span>

### <span data-ttu-id="de6cb-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="de6cb-116">-AllowDataLoss</span></span>
<span data-ttu-id="de6cb-117">Akkor is végezze el a feladatátvételt, ha a művelet az adatvesztést okozhatja.</span><span class="sxs-lookup"><span data-stu-id="de6cb-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="de6cb-118">Ez lehetővé teszi, hogy a feladatátvétel akkor is folytassa, ha az elsődleges adatbázis nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="de6cb-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6cb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de6cb-119">-AsJob</span></span>
<span data-ttu-id="de6cb-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="de6cb-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="de6cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6cb-121">-DefaultProfile</span></span>
<span data-ttu-id="de6cb-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="de6cb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de6cb-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="de6cb-123">-FailoverGroupName</span></span>
<span data-ttu-id="de6cb-124">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="de6cb-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de6cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="de6cb-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de6cb-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de6cb-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="de6cb-127">-ServerName</span></span>
<span data-ttu-id="de6cb-128">A feladatátvételi csoport másodlagos Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="de6cb-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de6cb-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de6cb-129">-Confirm</span></span>
<span data-ttu-id="de6cb-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de6cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6cb-131">-WhatIf</span></span>
<span data-ttu-id="de6cb-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de6cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6cb-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de6cb-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6cb-134">CommonParameters</span></span>
<span data-ttu-id="de6cb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de6cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6cb-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6cb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6cb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de6cb-137">INPUTS</span></span>

### <span data-ttu-id="de6cb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de6cb-138">System.String</span></span>

## <span data-ttu-id="de6cb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de6cb-139">OUTPUTS</span></span>

### <span data-ttu-id="de6cb-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="de6cb-140">System.Object</span></span>

## <span data-ttu-id="de6cb-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de6cb-141">NOTES</span></span>

## <span data-ttu-id="de6cb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de6cb-142">RELATED LINKS</span></span>

[<span data-ttu-id="de6cb-143">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de6cb-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de6cb-145">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de6cb-146">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="de6cb-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="de6cb-148">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de6cb-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de6cb-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="de6cb-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
