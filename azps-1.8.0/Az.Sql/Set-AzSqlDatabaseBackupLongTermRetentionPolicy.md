---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c11d8de5f7cd60bd71f759feeceaf043c4fd869b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668800"
---
# <span data-ttu-id="59760-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59760-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="59760-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59760-102">SYNOPSIS</span></span>
<span data-ttu-id="59760-103">Kiszolgáló hosszú távú adatmegőrzési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="59760-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="59760-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59760-104">SYNTAX</span></span>

### <span data-ttu-id="59760-105">WeeklyRetentionRequired (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59760-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59760-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="59760-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59760-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="59760-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59760-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="59760-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59760-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="59760-109">DESCRIPTION</span></span>
<span data-ttu-id="59760-110">A **set-AzSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="59760-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="59760-111">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="59760-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="59760-112">Példák</span><span class="sxs-lookup"><span data-stu-id="59760-112">EXAMPLES</span></span>

### <span data-ttu-id="59760-113">Példa 1: a hosszú távú adatmegőrzési házirend jelenlegi verziójának heti adatmegőrzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="59760-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="59760-114">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét rögzíti, hogy minden héten két teljes biztonsági mentést mentsen</span><span class="sxs-lookup"><span data-stu-id="59760-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="59760-115">2. példa: a hosszú távú adatmegőrzési házirend jelenlegi verziójához tartozó havi adatmegőrzés beállítása</span><span class="sxs-lookup"><span data-stu-id="59760-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="59760-116">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét rögzíti az egyes hónapok első teljes biztonsági másolatának 5 éve mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="59760-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="59760-117">3. példa: a hosszú távú adatmegőrzési házirend jelenlegi verziójának éves megőrzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="59760-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="59760-118">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét határozza meg, hogy a teljes biztonsági mentés 10 évig az év 26.</span><span class="sxs-lookup"><span data-stu-id="59760-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="59760-119">Példa 4: a hosszú távú adatmegőrzési házirend aktuális verziójához tartozó minden adatmegőrzési szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="59760-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="59760-120">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét állítja be, hogy minden teljes biztonsági másolatot 14 napra mentsen, az egyes hónapok első teljes biztonsági másolatát 24 hét után, valamint a teljes biztonsági másolatot, amelyet az év 26.</span><span class="sxs-lookup"><span data-stu-id="59760-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="59760-121">4. példa: a hosszú távú adatmegőrzési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59760-121">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="59760-122">Eltávolítja a házirendet a database01, hogy többé ne mentse a hosszú távú adatmegőrzési biztonsági mentéseket.</span><span class="sxs-lookup"><span data-stu-id="59760-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="59760-123">Ez a funkció nem befolyásolja a már elvégzett biztonsági mentést</span><span class="sxs-lookup"><span data-stu-id="59760-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="59760-124">4. példa: a hosszú távú adatmegőrzési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59760-124">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="59760-125">Ez egy másik módszer a database01 házirend eltávolítására, így többé nem menti a hosszú távú adatmegőrzési biztonsági másolatokat.</span><span class="sxs-lookup"><span data-stu-id="59760-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="59760-126">Ez a funkció nem befolyásolja a már elvégzett biztonsági mentést</span><span class="sxs-lookup"><span data-stu-id="59760-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="59760-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59760-127">PARAMETERS</span></span>

### <span data-ttu-id="59760-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59760-128">-DatabaseName</span></span>
<span data-ttu-id="59760-129">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="59760-129">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59760-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59760-130">-DefaultProfile</span></span>
<span data-ttu-id="59760-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59760-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59760-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="59760-132">-MonthlyRetention</span></span>
<span data-ttu-id="59760-133">A havi adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="59760-133">The Monthly Retention.</span></span>
<span data-ttu-id="59760-134">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="59760-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="59760-135">7 nap és legfeljebb 10 év minumum van.</span><span class="sxs-lookup"><span data-stu-id="59760-135">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59760-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="59760-136">-RemovePolicy</span></span>
<span data-ttu-id="59760-137">Ha meg van határozva, az adatbázis házirendje törlődik.</span><span class="sxs-lookup"><span data-stu-id="59760-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59760-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59760-138">-ResourceGroupName</span></span>
<span data-ttu-id="59760-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="59760-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="59760-140">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="59760-140">-ServerName</span></span>
<span data-ttu-id="59760-141">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="59760-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="59760-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="59760-142">-WeeklyRetention</span></span>
<span data-ttu-id="59760-143">A heti adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="59760-143">The Weekly Retention.</span></span>
<span data-ttu-id="59760-144">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="59760-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="59760-145">7 nap és legfeljebb 10 év minumum van.</span><span class="sxs-lookup"><span data-stu-id="59760-145">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59760-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="59760-146">-WeekOfYear</span></span>
<span data-ttu-id="59760-147">Az év hete, 1 – 52, az éves adatmegőrzésre való mentéshez.</span><span class="sxs-lookup"><span data-stu-id="59760-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59760-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="59760-148">-YearlyRetention</span></span>
<span data-ttu-id="59760-149">Az éves adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="59760-149">The Yearly Retention.</span></span>
<span data-ttu-id="59760-150">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="59760-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="59760-151">7 nap és legfeljebb 10 év minumum van.</span><span class="sxs-lookup"><span data-stu-id="59760-151">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59760-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59760-152">-Confirm</span></span>
<span data-ttu-id="59760-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59760-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59760-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59760-154">-WhatIf</span></span>
<span data-ttu-id="59760-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59760-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59760-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59760-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59760-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59760-157">CommonParameters</span></span>
<span data-ttu-id="59760-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59760-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59760-159">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59760-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59760-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59760-160">INPUTS</span></span>

### <span data-ttu-id="59760-161">System. String</span><span class="sxs-lookup"><span data-stu-id="59760-161">System.String</span></span>

### <span data-ttu-id="59760-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="59760-162">System.Int32</span></span>

## <span data-ttu-id="59760-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59760-163">OUTPUTS</span></span>

### <span data-ttu-id="59760-164">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="59760-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="59760-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59760-165">NOTES</span></span>

## <span data-ttu-id="59760-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59760-166">RELATED LINKS</span></span>

[<span data-ttu-id="59760-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59760-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="59760-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="59760-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="59760-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="59760-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="59760-170">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59760-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)