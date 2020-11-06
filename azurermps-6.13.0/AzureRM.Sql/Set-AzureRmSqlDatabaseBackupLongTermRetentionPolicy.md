---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a9389999bdbd93b332a3186ede1003c896552d1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493608"
---
# <span data-ttu-id="57575-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="57575-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="57575-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57575-102">SYNOPSIS</span></span>
<span data-ttu-id="57575-103">Kiszolgáló hosszú távú adatmegőrzési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="57575-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57575-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57575-104">SYNTAX</span></span>

### <span data-ttu-id="57575-105">WeeklyRetentionRequired (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57575-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57575-106">Régi</span><span class="sxs-lookup"><span data-stu-id="57575-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57575-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="57575-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57575-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="57575-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57575-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="57575-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57575-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="57575-110">DESCRIPTION</span></span>
<span data-ttu-id="57575-111">A **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="57575-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="57575-112">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="57575-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="57575-113">Példák</span><span class="sxs-lookup"><span data-stu-id="57575-113">EXAMPLES</span></span>

### <span data-ttu-id="57575-114">Példa 1: a hosszú távú adatmegőrzési házirend jelenlegi verziójának heti adatmegőrzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="57575-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="57575-115">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét rögzíti, hogy minden héten két teljes biztonsági mentést mentsen</span><span class="sxs-lookup"><span data-stu-id="57575-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="57575-116">2. példa: a hosszú távú adatmegőrzési házirend jelenlegi verziójához tartozó havi adatmegőrzés beállítása</span><span class="sxs-lookup"><span data-stu-id="57575-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="57575-117">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét rögzíti az egyes hónapok első teljes biztonsági másolatának 5 éve mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="57575-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="57575-118">3. példa: a hosszú távú adatmegőrzési házirend jelenlegi verziójának éves megőrzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="57575-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="57575-119">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét határozza meg, hogy a teljes biztonsági mentés 10 évig az év 26.</span><span class="sxs-lookup"><span data-stu-id="57575-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="57575-120">Példa 4: a hosszú távú adatmegőrzési házirend aktuális verziójához tartozó minden adatmegőrzési szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="57575-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="57575-121">Ez a cikk a database01 hosszú távú adatmegőrzési házirendjét állítja be, hogy minden teljes biztonsági másolatot 14 napra mentsen, az egyes hónapok első teljes biztonsági másolatát 24 hét után, valamint a teljes biztonsági másolatot, amelyet az év 26.</span><span class="sxs-lookup"><span data-stu-id="57575-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="57575-122">4. példa: a hosszú távú adatmegőrzési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="57575-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="57575-123">Eltávolítja a házirendet a database01, hogy többé ne mentse a hosszú távú adatmegőrzési biztonsági mentéseket.</span><span class="sxs-lookup"><span data-stu-id="57575-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="57575-124">Ez a funkció nem befolyásolja a már elvégzett biztonsági mentést</span><span class="sxs-lookup"><span data-stu-id="57575-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="57575-125">4. példa: a hosszú távú adatmegőrzési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="57575-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="57575-126">Ez egy másik módszer a database01 házirend eltávolítására, így többé nem menti a hosszú távú adatmegőrzési biztonsági másolatokat.</span><span class="sxs-lookup"><span data-stu-id="57575-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="57575-127">Ez a funkció nem befolyásolja a már elvégzett biztonsági mentést</span><span class="sxs-lookup"><span data-stu-id="57575-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="57575-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57575-128">PARAMETERS</span></span>

### <span data-ttu-id="57575-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57575-129">-DatabaseName</span></span>
<span data-ttu-id="57575-130">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="57575-130">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="57575-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57575-131">-DefaultProfile</span></span>
<span data-ttu-id="57575-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57575-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57575-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="57575-133">-MonthlyRetention</span></span>
<span data-ttu-id="57575-134">A havi adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="57575-134">The Monthly Retention.</span></span>
<span data-ttu-id="57575-135">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="57575-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="57575-136">7 nap és legfeljebb 10 év minumum van.</span><span class="sxs-lookup"><span data-stu-id="57575-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="57575-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="57575-137">-RemovePolicy</span></span>
<span data-ttu-id="57575-138">Ha meg van határozva, az adatbázis házirendje törlődik.</span><span class="sxs-lookup"><span data-stu-id="57575-138">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="57575-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57575-139">-ResourceGroupName</span></span>
<span data-ttu-id="57575-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57575-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="57575-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57575-141">-ResourceId</span></span>
<span data-ttu-id="57575-142">A hosszú távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57575-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57575-143">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="57575-143">-ServerName</span></span>
<span data-ttu-id="57575-144">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="57575-144">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="57575-145">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="57575-145">-State</span></span>
<span data-ttu-id="57575-146">A hosszú távú adatmegőrzési házirend állapota, "engedélyezve" vagy "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="57575-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57575-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="57575-147">-WeeklyRetention</span></span>
<span data-ttu-id="57575-148">A heti adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="57575-148">The Weekly Retention.</span></span>
<span data-ttu-id="57575-149">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="57575-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="57575-150">7 nap és legfeljebb 10 év minumum van.</span><span class="sxs-lookup"><span data-stu-id="57575-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="57575-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="57575-151">-WeekOfYear</span></span>
<span data-ttu-id="57575-152">Az év hete, 1 – 52, az éves adatmegőrzésre való mentéshez.</span><span class="sxs-lookup"><span data-stu-id="57575-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="57575-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="57575-153">-YearlyRetention</span></span>
<span data-ttu-id="57575-154">Az éves adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="57575-154">The Yearly Retention.</span></span>
<span data-ttu-id="57575-155">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="57575-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="57575-156">7 nap és legfeljebb 10 év minumum van.</span><span class="sxs-lookup"><span data-stu-id="57575-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="57575-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57575-157">-Confirm</span></span>
<span data-ttu-id="57575-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57575-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57575-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57575-159">-WhatIf</span></span>
<span data-ttu-id="57575-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57575-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57575-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57575-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57575-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57575-162">CommonParameters</span></span>
<span data-ttu-id="57575-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57575-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57575-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57575-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57575-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57575-165">INPUTS</span></span>

### <span data-ttu-id="57575-166">System. String</span><span class="sxs-lookup"><span data-stu-id="57575-166">System.String</span></span>

### <span data-ttu-id="57575-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="57575-167">System.Int32</span></span>

## <span data-ttu-id="57575-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57575-168">OUTPUTS</span></span>

### <span data-ttu-id="57575-169">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="57575-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="57575-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57575-170">NOTES</span></span>

## <span data-ttu-id="57575-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57575-171">RELATED LINKS</span></span>

[<span data-ttu-id="57575-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="57575-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="57575-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="57575-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="57575-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="57575-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="57575-175">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="57575-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
