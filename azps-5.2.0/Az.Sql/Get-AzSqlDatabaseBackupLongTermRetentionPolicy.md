---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368561"
---
# <span data-ttu-id="869d3-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="869d3-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="869d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="869d3-102">SYNOPSIS</span></span>
<span data-ttu-id="869d3-103">Hosszú távú adatmegőrzési házirendet kap az adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="869d3-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="869d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="869d3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="869d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="869d3-105">DESCRIPTION</span></span>
<span data-ttu-id="869d3-106">A **Get-AzSqlDatabaseBackupLongTermRetentionPolicy parancsmag** megkapja az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="869d3-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="869d3-107">A házirend egy Azure biztonságimásolat-erőforrás, amely a biztonságimásolat-tárolási házirend meghatározásához használatos.</span><span class="sxs-lookup"><span data-stu-id="869d3-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="869d3-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="869d3-108">EXAMPLES</span></span>

### <span data-ttu-id="869d3-109">1. példa: A hosszú távú adatmegőrzési házirend aktuális verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="869d3-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


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

<span data-ttu-id="869d3-110">Ez a parancs az adatbázis01 hosszú távú adatmegőrzési házirendje aktuális verzióját kapja meg</span><span class="sxs-lookup"><span data-stu-id="869d3-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="869d3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="869d3-111">PARAMETERS</span></span>

### <span data-ttu-id="869d3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="869d3-112">-DatabaseName</span></span>
<span data-ttu-id="869d3-113">A használni használt Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="869d3-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="869d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869d3-114">-DefaultProfile</span></span>
<span data-ttu-id="869d3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="869d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="869d3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="869d3-116">-ResourceGroupName</span></span>
<span data-ttu-id="869d3-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="869d3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="869d3-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="869d3-118">-ServerName</span></span>
<span data-ttu-id="869d3-119">Annak az Azure SQL Servernek a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="869d3-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="869d3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="869d3-120">-Confirm</span></span>
<span data-ttu-id="869d3-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="869d3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="869d3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="869d3-122">-WhatIf</span></span>
<span data-ttu-id="869d3-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="869d3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="869d3-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="869d3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="869d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869d3-125">CommonParameters</span></span>
<span data-ttu-id="869d3-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869d3-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="869d3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869d3-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="869d3-128">INPUTS</span></span>

### <span data-ttu-id="869d3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="869d3-129">System.String</span></span>

## <span data-ttu-id="869d3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="869d3-130">OUTPUTS</span></span>

### <span data-ttu-id="869d3-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="869d3-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="869d3-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="869d3-132">NOTES</span></span>

## <span data-ttu-id="869d3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="869d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="869d3-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="869d3-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="869d3-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="869d3-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="869d3-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="869d3-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="869d3-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="869d3-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)