---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145531"
---
# <span data-ttu-id="e1192-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="e1192-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="e1192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1192-102">SYNOPSIS</span></span>
<span data-ttu-id="e1192-103">Megszakítja az adatbázis aszinkron frissítésének műveletét.</span><span class="sxs-lookup"><span data-stu-id="e1192-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="e1192-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1192-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1192-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1192-105">DESCRIPTION</span></span>
<span data-ttu-id="e1192-106">A **Stop-AzSqlDatabaseActivity** parancsmag megszakítja az adatbázis aszinkron frissítését.</span><span class="sxs-lookup"><span data-stu-id="e1192-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="e1192-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1192-107">EXAMPLES</span></span>

### <span data-ttu-id="e1192-108">1. példa: Az adatbázis aszinkron frissítésének megszakítása</span><span class="sxs-lookup"><span data-stu-id="e1192-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="e1192-109">Ez a parancs megszakítja az adatbázis aszinkron frissítését.</span><span class="sxs-lookup"><span data-stu-id="e1192-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="e1192-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1192-110">PARAMETERS</span></span>

### <span data-ttu-id="e1192-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1192-111">-DatabaseName</span></span>
<span data-ttu-id="e1192-112">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="e1192-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="e1192-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1192-113">-DefaultProfile</span></span>
<span data-ttu-id="e1192-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1192-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1192-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e1192-115">-ElasticPoolName</span></span>
<span data-ttu-id="e1192-116">Az Azure SQL Rugalmas készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e1192-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="e1192-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e1192-117">-OperationId</span></span>
<span data-ttu-id="e1192-118">A parancsmag által lekért művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e1192-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1192-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1192-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1192-120">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e1192-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e1192-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1192-121">-ServerName</span></span>
<span data-ttu-id="e1192-122">Az adatbázist tartalmazó Microsoft SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="e1192-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e1192-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1192-123">-Confirm</span></span>
<span data-ttu-id="e1192-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e1192-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1192-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1192-125">-WhatIf</span></span>
<span data-ttu-id="e1192-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e1192-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1192-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1192-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1192-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1192-128">CommonParameters</span></span>
<span data-ttu-id="e1192-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1192-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1192-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1192-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1192-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1192-131">INPUTS</span></span>

### <span data-ttu-id="e1192-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e1192-132">System.String</span></span>

### <span data-ttu-id="e1192-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1192-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1192-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1192-134">OUTPUTS</span></span>

### <span data-ttu-id="e1192-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="e1192-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="e1192-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1192-136">NOTES</span></span>

## <span data-ttu-id="e1192-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1192-137">RELATED LINKS</span></span>
