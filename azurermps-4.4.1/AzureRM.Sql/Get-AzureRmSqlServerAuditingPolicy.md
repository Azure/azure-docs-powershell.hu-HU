---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496815"
---
# <span data-ttu-id="15a10-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="15a10-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="15a10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15a10-102">SYNOPSIS</span></span>
<span data-ttu-id="15a10-103">Az SQL Server naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15a10-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15a10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15a10-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15a10-105">DESCRIPTION</span></span>
<span data-ttu-id="15a10-106">A **Get-AzureRmSqlServerAuditingPolicy** parancsmag az Azure SQL Server-kiszolgálók naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15a10-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="15a10-107">Adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="15a10-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="15a10-108">Ez a parancsmag olyan házirendet ad eredményül, amely a megadott Azure SQL-kiszolgálón definiált, és a naplózási házirend segítségével használható az Azure SQL-adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="15a10-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="15a10-109">Példák</span><span class="sxs-lookup"><span data-stu-id="15a10-109">EXAMPLES</span></span>

### <span data-ttu-id="15a10-110">1. példa: az Azure SQL Server naplózási házirendjének beszerzése az Ön által meghatározott táblázatos naplózással</span><span class="sxs-lookup"><span data-stu-id="15a10-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
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

### <span data-ttu-id="15a10-111">2. példa: az Azure SQL Server naplózási házirendjének beszerzése a blob-naplózással</span><span class="sxs-lookup"><span data-stu-id="15a10-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="15a10-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15a10-112">PARAMETERS</span></span>

### <span data-ttu-id="15a10-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a10-113">-ResourceGroupName</span></span>
<span data-ttu-id="15a10-114">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="15a10-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="15a10-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="15a10-115">-ServerName</span></span>
<span data-ttu-id="15a10-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyhez a parancsmag a naplózási házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="15a10-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="15a10-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15a10-117">-Confirm</span></span>
<span data-ttu-id="15a10-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15a10-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a10-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a10-119">-WhatIf</span></span>
<span data-ttu-id="15a10-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15a10-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a10-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15a10-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a10-122">-DefaultProfile</span></span>
<span data-ttu-id="15a10-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a10-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a10-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a10-124">CommonParameters</span></span>
<span data-ttu-id="15a10-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15a10-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a10-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a10-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a10-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a10-127">INPUTS</span></span>

## <span data-ttu-id="15a10-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a10-128">OUTPUTS</span></span>

### <span data-ttu-id="15a10-129">Microsoft. Azure. Command. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="15a10-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="15a10-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15a10-130">NOTES</span></span>

## <span data-ttu-id="15a10-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a10-131">RELATED LINKS</span></span>

[<span data-ttu-id="15a10-132">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="15a10-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="15a10-133">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="15a10-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="15a10-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="15a10-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


