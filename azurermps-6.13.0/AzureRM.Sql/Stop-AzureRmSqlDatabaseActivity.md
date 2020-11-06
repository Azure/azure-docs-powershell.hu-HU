---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: af2f10b371eb21558a4b675331ec97f797611d26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494862"
---
# <span data-ttu-id="220e7-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="220e7-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="220e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="220e7-102">SYNOPSIS</span></span>
<span data-ttu-id="220e7-103">Törli az adatbázis aszinkron frissítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="220e7-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="220e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="220e7-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="220e7-105">DESCRIPTION</span></span>
<span data-ttu-id="220e7-106">A **stop-AzureRmSqlDatabaseActivity** parancsmag lemondja az adatbázis aszinkron frissítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="220e7-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="220e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="220e7-107">EXAMPLES</span></span>

### <span data-ttu-id="220e7-108">1. példa: az aszinkron frissítési művelet megszakítása az adatbázison</span><span class="sxs-lookup"><span data-stu-id="220e7-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="220e7-109">Ez a parancs lemondja az adatbázis aszinkron frissítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="220e7-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="220e7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="220e7-110">PARAMETERS</span></span>

### <span data-ttu-id="220e7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="220e7-111">-DatabaseName</span></span>
<span data-ttu-id="220e7-112">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="220e7-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="220e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220e7-113">-DefaultProfile</span></span>
<span data-ttu-id="220e7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="220e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="220e7-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="220e7-115">-ElasticPoolName</span></span>
<span data-ttu-id="220e7-116">Az Azure SQL elasztikus Pool neve.</span><span class="sxs-lookup"><span data-stu-id="220e7-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220e7-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="220e7-117">-OperationId</span></span>
<span data-ttu-id="220e7-118">Annak a műveletnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="220e7-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="220e7-120">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="220e7-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="220e7-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="220e7-121">-ServerName</span></span>
<span data-ttu-id="220e7-122">Az adatbázist tároló Microsoft SQL Server-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="220e7-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="220e7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="220e7-123">-Confirm</span></span>
<span data-ttu-id="220e7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="220e7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220e7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220e7-125">-WhatIf</span></span>
<span data-ttu-id="220e7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="220e7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="220e7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="220e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220e7-128">CommonParameters</span></span>
<span data-ttu-id="220e7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="220e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220e7-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="220e7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220e7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="220e7-131">INPUTS</span></span>

### <span data-ttu-id="220e7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="220e7-132">System.String</span></span>

### <span data-ttu-id="220e7-133">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="220e7-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="220e7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="220e7-134">OUTPUTS</span></span>

### <span data-ttu-id="220e7-135">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="220e7-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="220e7-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="220e7-136">NOTES</span></span>

## <span data-ttu-id="220e7-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="220e7-137">RELATED LINKS</span></span>
