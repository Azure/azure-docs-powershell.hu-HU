---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194509"
---
# <span data-ttu-id="6d832-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d832-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="6d832-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d832-102">SYNOPSIS</span></span>
<span data-ttu-id="6d832-103">Biztonsági rövid távú adatmegőrzési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="6d832-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="6d832-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d832-104">SYNTAX</span></span>

### <span data-ttu-id="6d832-105">PolicyByResourceServerDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d832-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d832-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6d832-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d832-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6d832-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d832-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d832-108">DESCRIPTION</span></span>
<span data-ttu-id="6d832-109">A **set-AzSqlDatabaseBackupShortTermRetentionPolicy** parancsmag az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6d832-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="6d832-110">A házirend az adatmegőrzési időszak napokban, a visszaadott időpontos biztonsági másolatok esetében.</span><span class="sxs-lookup"><span data-stu-id="6d832-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="6d832-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6d832-111">EXAMPLES</span></span>

### <span data-ttu-id="6d832-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6d832-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="6d832-113">Ez a parancs a database01 rövid távú adatmegőrzési házirendjét állítja be a 35 napokra.</span><span class="sxs-lookup"><span data-stu-id="6d832-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="6d832-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6d832-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="6d832-115">Ez a parancs a database01 rövid távú adatmegőrzési házirendjét állítja be egy adatbázis-objektumon keresztül az 35-ös napokra.</span><span class="sxs-lookup"><span data-stu-id="6d832-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="6d832-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d832-116">PARAMETERS</span></span>

### <span data-ttu-id="6d832-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6d832-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="6d832-118">Az adatbázis-objektum a házirend beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="6d832-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d832-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d832-119">-DatabaseName</span></span>
<span data-ttu-id="6d832-120">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6d832-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d832-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d832-121">-DefaultProfile</span></span>
<span data-ttu-id="6d832-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d832-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d832-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d832-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d832-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d832-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d832-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d832-125">-ResourceId</span></span>
<span data-ttu-id="6d832-126">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d832-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d832-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6d832-127">-RetentionDays</span></span>
<span data-ttu-id="6d832-128">A biztonsági mentés adatmegőrzési beállítása napokban.</span><span class="sxs-lookup"><span data-stu-id="6d832-128">The backup retention setting, in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d832-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6d832-129">-ServerName</span></span>
<span data-ttu-id="6d832-130">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="6d832-130">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d832-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d832-131">-Confirm</span></span>
<span data-ttu-id="6d832-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d832-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d832-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d832-133">-WhatIf</span></span>
<span data-ttu-id="6d832-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d832-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d832-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d832-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d832-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d832-136">CommonParameters</span></span>
<span data-ttu-id="6d832-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d832-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d832-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d832-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d832-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d832-139">INPUTS</span></span>

### <span data-ttu-id="6d832-140">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6d832-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="6d832-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6d832-141">System.String</span></span>

## <span data-ttu-id="6d832-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d832-142">OUTPUTS</span></span>

### <span data-ttu-id="6d832-143">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6d832-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="6d832-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d832-144">NOTES</span></span>

## <span data-ttu-id="6d832-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d832-145">RELATED LINKS</span></span>