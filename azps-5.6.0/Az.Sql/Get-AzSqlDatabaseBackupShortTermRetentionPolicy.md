---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 4cb97982ed3649502bcf11ce471cef0231ae3058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926369"
---
# <span data-ttu-id="3e482-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3e482-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="3e482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e482-102">SYNOPSIS</span></span>
<span data-ttu-id="3e482-103">Biztonsági másolatot kap rövid távú adatmegőrzési házirendről.</span><span class="sxs-lookup"><span data-stu-id="3e482-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="3e482-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e482-104">SYNTAX</span></span>

### <span data-ttu-id="3e482-105">PolicyByResourceServerDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e482-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e482-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e482-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e482-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e482-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e482-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e482-108">DESCRIPTION</span></span>
<span data-ttu-id="3e482-109">A **Get-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmag** megkapja az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="3e482-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="3e482-110">A házirend az időkorrekciós biztonsági másolatok megőrzési ideje napokban.</span><span class="sxs-lookup"><span data-stu-id="3e482-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="3e482-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e482-111">EXAMPLES</span></span>

### <span data-ttu-id="3e482-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3e482-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="3e482-113">Ez a parancs az adatbázis01 rövid távú adatmegőrzési házirendje.</span><span class="sxs-lookup"><span data-stu-id="3e482-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="3e482-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3e482-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="3e482-115">Ez a parancs az adatbázis01 rövid távú adatmegőrzési házirendét kapja meg egy adatbázis-objektum pipázásával.</span><span class="sxs-lookup"><span data-stu-id="3e482-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="3e482-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e482-116">PARAMETERS</span></span>

### <span data-ttu-id="3e482-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3e482-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="3e482-118">Az adatbázis-objektum, amelyről le kell szerezni a házirendet.</span><span class="sxs-lookup"><span data-stu-id="3e482-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="3e482-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e482-119">-DatabaseName</span></span>
<span data-ttu-id="3e482-120">A használni használt Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3e482-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="3e482-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e482-121">-DefaultProfile</span></span>
<span data-ttu-id="3e482-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e482-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e482-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e482-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e482-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e482-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e482-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e482-125">-ResourceId</span></span>
<span data-ttu-id="3e482-126">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e482-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="3e482-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3e482-127">-ServerName</span></span>
<span data-ttu-id="3e482-128">Annak az Azure SQL Servernek a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="3e482-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="3e482-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e482-129">CommonParameters</span></span>
<span data-ttu-id="3e482-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e482-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e482-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e482-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e482-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e482-132">INPUTS</span></span>

### <span data-ttu-id="3e482-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3e482-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="3e482-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3e482-134">System.String</span></span>

## <span data-ttu-id="3e482-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e482-135">OUTPUTS</span></span>

### <span data-ttu-id="3e482-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3e482-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3e482-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e482-137">NOTES</span></span>

## <span data-ttu-id="3e482-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e482-138">RELATED LINKS</span></span>
