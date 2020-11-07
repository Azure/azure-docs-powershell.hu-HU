---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: ce7bf498dc005f6cae8bfff28f0e470cacff71ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839264"
---
# <span data-ttu-id="a0007-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0007-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="a0007-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0007-102">SYNOPSIS</span></span>
<span data-ttu-id="a0007-103">Egy adatbázis hosszú távú adatmegőrzési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0007-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="a0007-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0007-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0007-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0007-105">DESCRIPTION</span></span>
<span data-ttu-id="a0007-106">A **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0007-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="a0007-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a0007-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="a0007-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a0007-108">EXAMPLES</span></span>

### <span data-ttu-id="a0007-109">Példa 1: a hosszú távú adatmegőrzési házirend jelenlegi verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0007-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="a0007-110">Ez a parancs a database01 hosszú távú adatmegőrzési házirendjének aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0007-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="a0007-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0007-111">PARAMETERS</span></span>

### <span data-ttu-id="a0007-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0007-112">-DatabaseName</span></span>
<span data-ttu-id="a0007-113">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a0007-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="a0007-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0007-114">-DefaultProfile</span></span>
<span data-ttu-id="a0007-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0007-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0007-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0007-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0007-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a0007-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0007-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a0007-118">-ServerName</span></span>
<span data-ttu-id="a0007-119">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="a0007-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="a0007-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0007-120">-Confirm</span></span>
<span data-ttu-id="a0007-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0007-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0007-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0007-122">-WhatIf</span></span>
<span data-ttu-id="a0007-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0007-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0007-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0007-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0007-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0007-125">CommonParameters</span></span>
<span data-ttu-id="a0007-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0007-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0007-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0007-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0007-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0007-128">INPUTS</span></span>

### <span data-ttu-id="a0007-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a0007-129">System.String</span></span>

## <span data-ttu-id="a0007-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0007-130">OUTPUTS</span></span>

### <span data-ttu-id="a0007-131">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a0007-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="a0007-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0007-132">NOTES</span></span>

## <span data-ttu-id="a0007-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0007-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0007-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a0007-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a0007-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a0007-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a0007-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0007-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="a0007-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a0007-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)