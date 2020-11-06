---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 64d8dae1b12630c6ef0086ab2648fcd424c0389d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501376"
---
# <span data-ttu-id="b13d5-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="b13d5-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="b13d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b13d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b13d5-103">Megkapja az adatbázis-műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="b13d5-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b13d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b13d5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b13d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b13d5-106">A **Get-AzureRmSqlDatabaseActivity** parancsmag az adatbázis-műveletek állapotát az Azure SQL-adatbázisban kapja.</span><span class="sxs-lookup"><span data-stu-id="b13d5-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="b13d5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b13d5-107">EXAMPLES</span></span>

### <span data-ttu-id="b13d5-108">Példa 1: az összes SQL-adatbázis-példány állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="b13d5-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b13d5-109">Ez a parancs a ElasticPool01 nevű rugalmas készletben minden SQL adatbázis-példány műveleti állapotát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="b13d5-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="b13d5-110">2. példa: az összes SQL-adatbázis-művelet állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="b13d5-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b13d5-111">Ez a parancs az adatbázis összes SQL-adatbázis-műveletének állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b13d5-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="b13d5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b13d5-112">PARAMETERS</span></span>

### <span data-ttu-id="b13d5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b13d5-113">-DatabaseName</span></span>
<span data-ttu-id="b13d5-114">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="b13d5-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13d5-115">-DefaultProfile</span></span>
<span data-ttu-id="b13d5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b13d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b13d5-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b13d5-117">-ElasticPoolName</span></span>
<span data-ttu-id="b13d5-118">Annak a rugalmas adatbázis-készletnek a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="b13d5-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13d5-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b13d5-119">-OperationId</span></span>
<span data-ttu-id="b13d5-120">Annak a műveletnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b13d5-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="b13d5-122">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b13d5-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b13d5-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b13d5-123">-ServerName</span></span>
<span data-ttu-id="b13d5-124">Az adatbázist tároló Microsoft SQL Server-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b13d5-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="b13d5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b13d5-125">-Confirm</span></span>
<span data-ttu-id="b13d5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b13d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13d5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13d5-127">-WhatIf</span></span>
<span data-ttu-id="b13d5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b13d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13d5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b13d5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13d5-130">CommonParameters</span></span>
<span data-ttu-id="b13d5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b13d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13d5-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13d5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b13d5-133">INPUTS</span></span>

### <span data-ttu-id="b13d5-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="b13d5-134">None</span></span>
<span data-ttu-id="b13d5-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b13d5-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b13d5-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b13d5-136">OUTPUTS</span></span>

### <span data-ttu-id="b13d5-137">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="b13d5-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="b13d5-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b13d5-138">NOTES</span></span>

## <span data-ttu-id="b13d5-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b13d5-139">RELATED LINKS</span></span>
