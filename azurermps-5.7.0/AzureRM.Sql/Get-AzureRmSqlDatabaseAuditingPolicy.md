---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 4d15400da4105f719f5948a53512f6c33cbd3bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679248"
---
# <span data-ttu-id="3b3b1-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3b1-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="3b3b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3b1-103">Egy adatbázis naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b3b1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b3b1-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3b1-106">A **Get-AzureRmSqlDatabaseAuditingPolicy** parancsmag egy Azure SQL-adatbázis naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="3b3b1-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="3b3b1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3b3b1-108">EXAMPLES</span></span>

### <span data-ttu-id="3b3b1-109">1. példa: az Azure SQL-adatbázisok naplózási házirendjének beszerzése az Ön által meghatározott táblázatos naplózással</span><span class="sxs-lookup"><span data-stu-id="3b3b1-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="3b3b1-110">2. példa: az Azure SQL-adatbázis naplózási házirendjének beszerzése a blob-naplózással</span><span class="sxs-lookup"><span data-stu-id="3b3b1-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="3b3b1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b3b1-111">PARAMETERS</span></span>

### <span data-ttu-id="3b3b1-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b3b1-112">-DatabaseName</span></span>
<span data-ttu-id="3b3b1-113">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-113">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3b1-114">-DefaultProfile</span></span>
<span data-ttu-id="3b3b1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3b3b1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3b1-116">-ResourceGroupName</span></span>
<span data-ttu-id="3b3b1-117">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-117">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b1-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3b3b1-118">-ServerName</span></span>
<span data-ttu-id="3b3b1-119">Annak a kiszolgálónak a nevét adja meg, ahol az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-119">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b1-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b3b1-120">-Confirm</span></span>
<span data-ttu-id="3b3b1-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3b1-122">-WhatIf</span></span>
<span data-ttu-id="3b3b1-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3b1-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3b1-125">CommonParameters</span></span>
<span data-ttu-id="3b3b1-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b3b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3b1-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3b1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3b1-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b3b1-128">INPUTS</span></span>

### <span data-ttu-id="3b3b1-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="3b3b1-129">None</span></span>
<span data-ttu-id="3b3b1-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3b3b1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b3b1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b3b1-131">OUTPUTS</span></span>

### <span data-ttu-id="3b3b1-132">Microsoft. Azure. Command. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3b3b1-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="3b3b1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b3b1-133">NOTES</span></span>

## <span data-ttu-id="3b3b1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b3b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="3b3b1-135">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3b3b1-135">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="3b3b1-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3b1-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



