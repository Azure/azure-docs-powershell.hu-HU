---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466001"
---
# <span data-ttu-id="6cb9f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6cb9f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="6cb9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb9f-103">Biztonsági másolatot készít rövid távú adatmegőrzési házirendről.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="6cb9f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cb9f-104">SYNTAX</span></span>

### <span data-ttu-id="6cb9f-105">PolicyByResourceServerDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb9f-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6cb9f-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb9f-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6cb9f-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb9f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cb9f-108">DESCRIPTION</span></span>
<span data-ttu-id="6cb9f-109">A **Set-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmag** megkapja az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="6cb9f-110">A házirend az időkorrekciós biztonsági másolatok megőrzési ideje napokban.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="6cb9f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cb9f-111">EXAMPLES</span></span>

### <span data-ttu-id="6cb9f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6cb9f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="6cb9f-113">Ez a parancs 35 napra állítja be az adatbázis01 rövid távú adatmegőrzési házirendját.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="6cb9f-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6cb9f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="6cb9f-115">Ez a parancs egy adatbázis-objektum pipázásával 35 napra állítja be az adatbázis01 rövid távú adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="6cb9f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cb9f-116">PARAMETERS</span></span>

### <span data-ttu-id="6cb9f-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6cb9f-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="6cb9f-118">Az adatbázis-objektum, amelyről le kell szerezni a házirendet.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="6cb9f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cb9f-119">-DatabaseName</span></span>
<span data-ttu-id="6cb9f-120">A használni használt Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="6cb9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb9f-121">-DefaultProfile</span></span>
<span data-ttu-id="6cb9f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6cb9f-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cb9f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cb9f-125">-ResourceId</span></span>
<span data-ttu-id="6cb9f-126">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="6cb9f-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6cb9f-127">-RetentionDays</span></span>
<span data-ttu-id="6cb9f-128">A biztonsági mentés adatmegőrzési beállítása napokban.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="6cb9f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6cb9f-129">-ServerName</span></span>
<span data-ttu-id="6cb9f-130">Annak az Azure SQL Servernek a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="6cb9f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cb9f-131">-Confirm</span></span>
<span data-ttu-id="6cb9f-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb9f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb9f-133">-WhatIf</span></span>
<span data-ttu-id="6cb9f-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb9f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb9f-136">CommonParameters</span></span>
<span data-ttu-id="6cb9f-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb9f-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb9f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cb9f-139">INPUTS</span></span>

### <span data-ttu-id="6cb9f-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6cb9f-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="6cb9f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb9f-141">System.String</span></span>

## <span data-ttu-id="6cb9f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb9f-142">OUTPUTS</span></span>

### <span data-ttu-id="6cb9f-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6cb9f-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="6cb9f-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cb9f-144">NOTES</span></span>

## <span data-ttu-id="6cb9f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cb9f-145">RELATED LINKS</span></span>
