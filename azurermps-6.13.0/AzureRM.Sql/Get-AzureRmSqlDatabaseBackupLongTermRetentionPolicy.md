---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672890"
---
# <span data-ttu-id="da5f8-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="da5f8-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="da5f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="da5f8-103">Egy adatbázis hosszú távú adatmegőrzési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da5f8-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da5f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da5f8-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da5f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="da5f8-106">A **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da5f8-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="da5f8-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="da5f8-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="da5f8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="da5f8-108">EXAMPLES</span></span>

### <span data-ttu-id="da5f8-109">Példa 1: a hosszú távú adatmegőrzési házirend jelenlegi verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="da5f8-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="da5f8-110">Ez a parancs a database01 hosszú távú adatmegőrzési házirendjének aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da5f8-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="da5f8-111">2. példa: a hosszú távú adatmegőrzési házirend örökölt verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="da5f8-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="da5f8-112">Ez a parancs a database01 hosszú távú adatmegőrzési házirendjének örökölt verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da5f8-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="da5f8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da5f8-113">PARAMETERS</span></span>

### <span data-ttu-id="da5f8-114">-Current</span><span class="sxs-lookup"><span data-stu-id="da5f8-114">-Current</span></span>
<span data-ttu-id="da5f8-115">Ha nincs megadva, a parancs a régi hosszú távú adatmegőrzési házirend adatait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="da5f8-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="da5f8-116">Ellenkező esetben a parancs a hosszú távú adatmegőrzési házirend aktuális verzióját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="da5f8-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5f8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da5f8-117">-DatabaseName</span></span>
<span data-ttu-id="da5f8-118">A használandó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="da5f8-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="da5f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5f8-119">-DefaultProfile</span></span>
<span data-ttu-id="da5f8-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da5f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da5f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="da5f8-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da5f8-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="da5f8-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="da5f8-123">-ServerName</span></span>
<span data-ttu-id="da5f8-124">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="da5f8-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="da5f8-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da5f8-125">-Confirm</span></span>
<span data-ttu-id="da5f8-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da5f8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da5f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da5f8-127">-WhatIf</span></span>
<span data-ttu-id="da5f8-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da5f8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da5f8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da5f8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da5f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5f8-130">CommonParameters</span></span>
<span data-ttu-id="da5f8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da5f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5f8-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da5f8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5f8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da5f8-133">INPUTS</span></span>

### <span data-ttu-id="da5f8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="da5f8-134">System.String</span></span>

## <span data-ttu-id="da5f8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da5f8-135">OUTPUTS</span></span>

### <span data-ttu-id="da5f8-136">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="da5f8-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="da5f8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da5f8-137">NOTES</span></span>

## <span data-ttu-id="da5f8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da5f8-138">RELATED LINKS</span></span>

[<span data-ttu-id="da5f8-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="da5f8-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="da5f8-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="da5f8-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="da5f8-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="da5f8-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="da5f8-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="da5f8-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
