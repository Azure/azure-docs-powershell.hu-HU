---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186692"
---
# <span data-ttu-id="157b3-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="157b3-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="157b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="157b3-102">SYNOPSIS</span></span>
<span data-ttu-id="157b3-103">Egy adatbázis hosszú távú adatmegőrzési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="157b3-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="157b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="157b3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="157b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="157b3-105">DESCRIPTION</span></span>
<span data-ttu-id="157b3-106">A **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="157b3-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="157b3-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="157b3-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="157b3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="157b3-108">EXAMPLES</span></span>

### <span data-ttu-id="157b3-109">Példa 1: a hosszú távú adatmegőrzési házirend jelenlegi verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="157b3-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="157b3-110">Ez a parancs a database01 hosszú távú adatmegőrzési házirendjének aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="157b3-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="157b3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="157b3-111">PARAMETERS</span></span>

### <span data-ttu-id="157b3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="157b3-112">-DatabaseName</span></span>
<span data-ttu-id="157b3-113">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="157b3-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="157b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157b3-114">-DefaultProfile</span></span>
<span data-ttu-id="157b3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="157b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="157b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="157b3-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="157b3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="157b3-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="157b3-118">-ServerName</span></span>
<span data-ttu-id="157b3-119">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="157b3-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="157b3-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="157b3-120">-Confirm</span></span>
<span data-ttu-id="157b3-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="157b3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="157b3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="157b3-122">-WhatIf</span></span>
<span data-ttu-id="157b3-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="157b3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="157b3-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="157b3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="157b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157b3-125">CommonParameters</span></span>
<span data-ttu-id="157b3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="157b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157b3-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="157b3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157b3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="157b3-128">INPUTS</span></span>

### <span data-ttu-id="157b3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="157b3-129">System.String</span></span>

## <span data-ttu-id="157b3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="157b3-130">OUTPUTS</span></span>

### <span data-ttu-id="157b3-131">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="157b3-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="157b3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="157b3-132">NOTES</span></span>

## <span data-ttu-id="157b3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="157b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="157b3-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="157b3-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="157b3-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="157b3-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="157b3-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="157b3-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="157b3-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="157b3-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)