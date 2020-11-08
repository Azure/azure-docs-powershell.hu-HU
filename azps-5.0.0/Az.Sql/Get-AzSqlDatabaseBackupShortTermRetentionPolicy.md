---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186690"
---
# <span data-ttu-id="cb485-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb485-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="cb485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb485-102">SYNOPSIS</span></span>
<span data-ttu-id="cb485-103">Rövid távú adatmegőrzési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="cb485-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="cb485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb485-104">SYNTAX</span></span>

### <span data-ttu-id="cb485-105">PolicyByResourceServerDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb485-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb485-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb485-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb485-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb485-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb485-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb485-108">DESCRIPTION</span></span>
<span data-ttu-id="cb485-109">A **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** parancsmag az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb485-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="cb485-110">A házirend az adatmegőrzési időszak napokban, a visszaadott időpontos biztonsági másolatok esetében.</span><span class="sxs-lookup"><span data-stu-id="cb485-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="cb485-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cb485-111">EXAMPLES</span></span>

### <span data-ttu-id="cb485-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb485-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="cb485-113">Ez a parancs a database01 rövid távú adatmegőrzési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb485-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="cb485-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="cb485-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="cb485-115">Ez a parancs beolvassa a database01 rövid távú adatmegőrzési házirendjét egy adatbázis-objektum csővezetékeken keresztül.</span><span class="sxs-lookup"><span data-stu-id="cb485-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="cb485-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb485-116">PARAMETERS</span></span>

### <span data-ttu-id="cb485-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cb485-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="cb485-118">Az adatbázis-objektum a házirend beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="cb485-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="cb485-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb485-119">-DatabaseName</span></span>
<span data-ttu-id="cb485-120">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cb485-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="cb485-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb485-121">-DefaultProfile</span></span>
<span data-ttu-id="cb485-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb485-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb485-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb485-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb485-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb485-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb485-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb485-125">-ResourceId</span></span>
<span data-ttu-id="cb485-126">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cb485-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="cb485-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="cb485-127">-ServerName</span></span>
<span data-ttu-id="cb485-128">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="cb485-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="cb485-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb485-129">CommonParameters</span></span>
<span data-ttu-id="cb485-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb485-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb485-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cb485-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb485-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb485-132">INPUTS</span></span>

### <span data-ttu-id="cb485-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cb485-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="cb485-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cb485-134">System.String</span></span>

## <span data-ttu-id="cb485-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb485-135">OUTPUTS</span></span>

### <span data-ttu-id="cb485-136">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cb485-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="cb485-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb485-137">NOTES</span></span>

## <span data-ttu-id="cb485-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb485-138">RELATED LINKS</span></span>
