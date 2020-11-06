---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 1b4f72a5d57884975d6beb0d4676a0cbe5863681
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499355"
---
# <span data-ttu-id="fb308-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fb308-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="fb308-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb308-102">SYNOPSIS</span></span>
<span data-ttu-id="fb308-103">Az SQL Server naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb308-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb308-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb308-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb308-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb308-105">DESCRIPTION</span></span>
<span data-ttu-id="fb308-106">A **Get-AzureRmSqlServerAuditingPolicy** parancsmag az Azure SQL Server-kiszolgálók naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb308-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="fb308-107">Adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="fb308-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fb308-108">Ez a parancsmag olyan házirendet ad eredményül, amely a megadott Azure SQL-kiszolgálón definiált, és a naplózási házirend segítségével használható az Azure SQL-adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="fb308-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="fb308-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fb308-109">EXAMPLES</span></span>

### <span data-ttu-id="fb308-110">1. példa: az Azure SQL Server naplózási házirendjének beszerzése az Ön által meghatározott táblázatos naplózással</span><span class="sxs-lookup"><span data-stu-id="fb308-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="fb308-111">2. példa: az Azure SQL Server naplózási házirendjének beszerzése a blob-naplózással</span><span class="sxs-lookup"><span data-stu-id="fb308-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

## <span data-ttu-id="fb308-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb308-112">PARAMETERS</span></span>

### <span data-ttu-id="fb308-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb308-113">-DefaultProfile</span></span>
<span data-ttu-id="fb308-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb308-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb308-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb308-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb308-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="fb308-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="fb308-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fb308-117">-ServerName</span></span>
<span data-ttu-id="fb308-118">Annak az Azure SQL Server-kiszolgálónak a neve, amelyhez a parancsmag a naplózási házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="fb308-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb308-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb308-119">-Confirm</span></span>
<span data-ttu-id="fb308-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb308-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb308-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb308-121">-WhatIf</span></span>
<span data-ttu-id="fb308-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb308-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb308-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb308-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb308-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb308-124">CommonParameters</span></span>
<span data-ttu-id="fb308-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb308-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb308-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb308-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb308-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb308-127">INPUTS</span></span>

### <span data-ttu-id="fb308-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb308-128">System.String</span></span>

## <span data-ttu-id="fb308-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb308-129">OUTPUTS</span></span>

### <span data-ttu-id="fb308-130">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fb308-130">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="fb308-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb308-131">NOTES</span></span>

## <span data-ttu-id="fb308-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb308-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb308-133">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fb308-133">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="fb308-134">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fb308-134">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="fb308-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fb308-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


