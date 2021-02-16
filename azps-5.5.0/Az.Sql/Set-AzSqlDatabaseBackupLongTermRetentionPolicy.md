---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155243"
---
# <span data-ttu-id="d3819-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3819-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d3819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3819-102">SYNOPSIS</span></span>
<span data-ttu-id="d3819-103">Kiszolgálói hosszú távú adatmegőrzési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="d3819-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="d3819-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3819-104">SYNTAX</span></span>

### <span data-ttu-id="d3819-105">WeeklyRetentionRequired (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3819-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3819-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="d3819-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3819-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="d3819-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3819-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="d3819-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3819-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3819-109">DESCRIPTION</span></span>
<span data-ttu-id="d3819-110">A **Set-AzSqlDatabaseBackupLongTermRetentionPolicy parancsmag** beállítja az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="d3819-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="d3819-111">A házirend egy Azure biztonságimásolat-erőforrás, amely a biztonságimásolat-tárolási házirend meghatározásához használatos.</span><span class="sxs-lookup"><span data-stu-id="d3819-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="d3819-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3819-112">EXAMPLES</span></span>

### <span data-ttu-id="d3819-113">1. példa: A hosszú távú adatmegőrzési házirend aktuális verziójának heti megőrzési beállítása</span><span class="sxs-lookup"><span data-stu-id="d3819-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="d3819-114">Ez az adatbázis01 hosszú távú adatmegőrzési házirendje úgy van beállítja, hogy minden heti teljes biztonsági mentést 2 hétig mentsen.</span><span class="sxs-lookup"><span data-stu-id="d3819-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="d3819-115">2. példa: A hosszú távú adatmegőrzési házirend aktuális verziójának havi adatmegőrzési beállítása</span><span class="sxs-lookup"><span data-stu-id="d3819-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="d3819-116">Ez az adatbázis01 hosszú távú adatmegőrzési házirendje úgy van beállítja, hogy minden hónapról 5 évre mentse az első teljes biztonsági másolatot</span><span class="sxs-lookup"><span data-stu-id="d3819-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="d3819-117">3. példa: A hosszú távú adatmegőrzési házirend aktuális verziójának éves megőrzési beállítása</span><span class="sxs-lookup"><span data-stu-id="d3819-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="d3819-118">Ezzel a beállítással az adatbázis01 hosszú távú adatmegőrzési házirendje az év 26. hetében készült teljes biztonsági mentést 10 évre menti.</span><span class="sxs-lookup"><span data-stu-id="d3819-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="d3819-119">4. példa: A hosszú távú adatmegőrzési házirend aktuális verziójának minden adatmegőrzési beállítása</span><span class="sxs-lookup"><span data-stu-id="d3819-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="d3819-120">Ezzel a beállítással az adatbázis01 hosszú távú adatmegőrzési házirendje minden egyes teljes biztonsági mentést 14 napra, az első teljes biztonsági mentést minden hónapról 24 hétre, a teljes biztonsági mentést pedig az év 26. hetének 10 évre</span><span class="sxs-lookup"><span data-stu-id="d3819-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="d3819-121">5. példa: A hosszú távú adatmegőrzési házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d3819-121">Example 5: Remove the long term retention policy</span></span>
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

<span data-ttu-id="d3819-122">Eltávolítja az adatbázis01 házirendet, így a továbbiakban nem ment hosszú távú adatmegőrzési biztonsági másolatokat.</span><span class="sxs-lookup"><span data-stu-id="d3819-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="d3819-123">Ez nincs hatással a már elkért biztonsági másolatok készítésére</span><span class="sxs-lookup"><span data-stu-id="d3819-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="d3819-124">6. példa: A hosszú távú adatmegőrzési házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d3819-124">Example 6: Remove the long term retention policy</span></span>
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

<span data-ttu-id="d3819-125">Ez egy másik módszer az adatbázis01 házirend eltávolítására, így a továbbiakban nem ment hosszú távú adatmegőrzési biztonsági másolatokat.</span><span class="sxs-lookup"><span data-stu-id="d3819-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="d3819-126">Ez nincs hatással a már elkért biztonsági másolatok készítésére</span><span class="sxs-lookup"><span data-stu-id="d3819-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="d3819-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3819-127">PARAMETERS</span></span>

### <span data-ttu-id="d3819-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3819-128">-DatabaseName</span></span>
<span data-ttu-id="d3819-129">A használni használt Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d3819-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="d3819-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3819-130">-DefaultProfile</span></span>
<span data-ttu-id="d3819-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3819-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3819-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="d3819-132">-MonthlyRetention</span></span>
<span data-ttu-id="d3819-133">A havi adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="d3819-133">The Monthly Retention.</span></span>
<span data-ttu-id="d3819-134">Ha iso 8601-es karakterlánc helyett csak egy számot ad át, a napok száma lesz az egység.</span><span class="sxs-lookup"><span data-stu-id="d3819-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="d3819-135">Legalább 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="d3819-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="d3819-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="d3819-136">-RemovePolicy</span></span>
<span data-ttu-id="d3819-137">Ha meg van téve, az adatbázis házirendet eltávolítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d3819-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="d3819-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3819-138">-ResourceGroupName</span></span>
<span data-ttu-id="d3819-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3819-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3819-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3819-140">-ServerName</span></span>
<span data-ttu-id="d3819-141">Annak az Azure SQL Servernek a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="d3819-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="d3819-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="d3819-142">-WeeklyRetention</span></span>
<span data-ttu-id="d3819-143">A heti adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="d3819-143">The Weekly Retention.</span></span>
<span data-ttu-id="d3819-144">Ha iso 8601-es karakterlánc helyett csak egy számot ad át, a napok száma lesz az egység.</span><span class="sxs-lookup"><span data-stu-id="d3819-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="d3819-145">Legalább 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="d3819-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="d3819-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="d3819-146">-WeekOfYear</span></span>
<span data-ttu-id="d3819-147">Az év hetét (1–52) az éves adatmegőrzéshez menteni.</span><span class="sxs-lookup"><span data-stu-id="d3819-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="d3819-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="d3819-148">-YearlyRetention</span></span>
<span data-ttu-id="d3819-149">Az éves adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="d3819-149">The Yearly Retention.</span></span>
<span data-ttu-id="d3819-150">Ha iso 8601-es karakterlánc helyett csak egy számot ad át, a napok száma lesz az egység.</span><span class="sxs-lookup"><span data-stu-id="d3819-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="d3819-151">Legalább 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="d3819-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="d3819-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3819-152">-Confirm</span></span>
<span data-ttu-id="d3819-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3819-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3819-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3819-154">-WhatIf</span></span>
<span data-ttu-id="d3819-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3819-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3819-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3819-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3819-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3819-157">CommonParameters</span></span>
<span data-ttu-id="d3819-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3819-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3819-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3819-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3819-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3819-160">INPUTS</span></span>

### <span data-ttu-id="d3819-161">System.String</span><span class="sxs-lookup"><span data-stu-id="d3819-161">System.String</span></span>

### <span data-ttu-id="d3819-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d3819-162">System.Int32</span></span>

## <span data-ttu-id="d3819-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3819-163">OUTPUTS</span></span>

### <span data-ttu-id="d3819-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d3819-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d3819-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3819-165">NOTES</span></span>

## <span data-ttu-id="d3819-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3819-166">RELATED LINKS</span></span>

[<span data-ttu-id="d3819-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3819-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d3819-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d3819-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d3819-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d3819-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d3819-170">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d3819-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)