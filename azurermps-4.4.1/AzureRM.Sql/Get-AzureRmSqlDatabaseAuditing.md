---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 4203609a97a9fc476292fca4020976539eb5d2b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504708"
---
# <span data-ttu-id="e7f94-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="e7f94-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="e7f94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7f94-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f94-103">Egy Azure SQL-adatbázis naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7f94-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7f94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7f94-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7f94-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f94-106">A **Get-AzureRmSqlDatabaseAuditing** parancsmag az Azure SQL-adatbázisok naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7f94-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="e7f94-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="e7f94-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="e7f94-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e7f94-108">EXAMPLES</span></span>

### <span data-ttu-id="e7f94-109">Példa 1: Azure SQL-adatbázis naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="e7f94-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="e7f94-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7f94-110">PARAMETERS</span></span>

### <span data-ttu-id="e7f94-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7f94-111">-DatabaseName</span></span>
<span data-ttu-id="e7f94-112">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e7f94-112">SQL Database name.</span></span>

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

### <span data-ttu-id="e7f94-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f94-113">-ResourceGroupName</span></span>
<span data-ttu-id="e7f94-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7f94-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7f94-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e7f94-115">-ServerName</span></span>
<span data-ttu-id="e7f94-116">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="e7f94-116">SQL Database server name.</span></span>

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

### <span data-ttu-id="e7f94-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7f94-117">-Confirm</span></span>
<span data-ttu-id="e7f94-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7f94-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f94-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f94-119">-WhatIf</span></span>
<span data-ttu-id="e7f94-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7f94-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7f94-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7f94-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f94-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f94-122">-DefaultProfile</span></span>
<span data-ttu-id="e7f94-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7f94-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f94-124">CommonParameters</span></span>
<span data-ttu-id="e7f94-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7f94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f94-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f94-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f94-127">INPUTS</span></span>

## <span data-ttu-id="e7f94-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f94-128">OUTPUTS</span></span>

### <span data-ttu-id="e7f94-129">Microsoft. Azure. Command. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="e7f94-129">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="e7f94-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7f94-130">NOTES</span></span>

## <span data-ttu-id="e7f94-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7f94-131">RELATED LINKS</span></span>

