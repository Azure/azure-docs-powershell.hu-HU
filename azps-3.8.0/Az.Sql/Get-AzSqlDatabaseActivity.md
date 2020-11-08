---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011572"
---
# <span data-ttu-id="b7b56-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="b7b56-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="b7b56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7b56-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b56-103">Megkapja az adatbázis-műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="b7b56-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="b7b56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7b56-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7b56-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b56-106">A **Get-AzSqlDatabaseActivity** parancsmag az adatbázis-műveletek állapotát az Azure SQL-adatbázisban kapja.</span><span class="sxs-lookup"><span data-stu-id="b7b56-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="b7b56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7b56-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b56-108">Példa 1: az összes SQL-adatbázis-példány állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="b7b56-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b7b56-109">Ez a parancs a ElasticPool01 nevű rugalmas készletben minden SQL adatbázis-példány műveleti állapotát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="b7b56-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="b7b56-110">2. példa: az összes SQL-adatbázis-művelet állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="b7b56-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b7b56-111">Ez a parancs az adatbázis összes SQL-adatbázis-műveletének állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b7b56-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="b7b56-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7b56-112">PARAMETERS</span></span>

### <span data-ttu-id="b7b56-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7b56-113">-DatabaseName</span></span>
<span data-ttu-id="b7b56-114">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="b7b56-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="b7b56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b56-115">-DefaultProfile</span></span>
<span data-ttu-id="b7b56-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7b56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b56-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b7b56-117">-ElasticPoolName</span></span>
<span data-ttu-id="b7b56-118">Annak a rugalmas adatbázis-készletnek a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="b7b56-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="b7b56-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b7b56-119">-OperationId</span></span>
<span data-ttu-id="b7b56-120">Annak a műveletnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b7b56-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7b56-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b56-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7b56-122">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b7b56-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b7b56-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b7b56-123">-ServerName</span></span>
<span data-ttu-id="b7b56-124">Az adatbázist tároló Microsoft SQL Server-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7b56-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="b7b56-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7b56-125">-Confirm</span></span>
<span data-ttu-id="b7b56-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7b56-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b56-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b56-127">-WhatIf</span></span>
<span data-ttu-id="b7b56-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7b56-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b56-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7b56-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b56-130">CommonParameters</span></span>
<span data-ttu-id="b7b56-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7b56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b56-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7b56-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b56-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7b56-133">INPUTS</span></span>

### <span data-ttu-id="b7b56-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b56-134">System.String</span></span>

### <span data-ttu-id="b7b56-135">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b7b56-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b7b56-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7b56-136">OUTPUTS</span></span>

### <span data-ttu-id="b7b56-137">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="b7b56-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="b7b56-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7b56-138">NOTES</span></span>

## <span data-ttu-id="b7b56-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7b56-139">RELATED LINKS</span></span>
