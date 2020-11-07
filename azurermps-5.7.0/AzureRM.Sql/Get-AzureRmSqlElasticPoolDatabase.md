---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: 3068b3a406414eb7302d76d5d053658dcf0e6245
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672831"
---
# <span data-ttu-id="e9b58-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b58-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="e9b58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9b58-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b58-103">Elasztikus adatbázisokat kap egy rugalmas készletben és a hozzájuk tartozó tulajdonsági értékeken.</span><span class="sxs-lookup"><span data-stu-id="e9b58-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9b58-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9b58-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b58-106">A **Get-AzureRmSqlElasticPoolDatabase** parancsmag rugalmasan változó adatbázisokat és a hozzájuk tartozó tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e9b58-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="e9b58-107">Az Azure SQL-adatbázisban megadhatja a rugalmas adatbázis nevét úgy, hogy csak az adott adatbázishoz tartozó tulajdonságértékeket láthassa.</span><span class="sxs-lookup"><span data-stu-id="e9b58-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="e9b58-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e9b58-108">EXAMPLES</span></span>

### <span data-ttu-id="e9b58-109">Példa 1: az összes adatbázis beszerzése rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="e9b58-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e9b58-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet minden adatbázisát bekapja.</span><span class="sxs-lookup"><span data-stu-id="e9b58-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="e9b58-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9b58-111">PARAMETERS</span></span>

### <span data-ttu-id="e9b58-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9b58-112">-DatabaseName</span></span>
<span data-ttu-id="e9b58-113">Annak az SQL-adatbázisnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="e9b58-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e9b58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b58-114">-DefaultProfile</span></span>
<span data-ttu-id="e9b58-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e9b58-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9b58-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e9b58-116">-ElasticPoolName</span></span>
<span data-ttu-id="e9b58-117">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b58-117">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="e9b58-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b58-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9b58-119">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e9b58-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="e9b58-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e9b58-120">-ServerName</span></span>
<span data-ttu-id="e9b58-121">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b58-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="e9b58-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9b58-122">-Confirm</span></span>
<span data-ttu-id="e9b58-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9b58-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b58-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b58-124">-WhatIf</span></span>
<span data-ttu-id="e9b58-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9b58-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b58-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9b58-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b58-127">CommonParameters</span></span>
<span data-ttu-id="e9b58-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9b58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b58-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b58-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b58-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b58-130">INPUTS</span></span>

### <span data-ttu-id="e9b58-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9b58-131">None</span></span>
<span data-ttu-id="e9b58-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e9b58-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9b58-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b58-133">OUTPUTS</span></span>

### <span data-ttu-id="e9b58-134">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9b58-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e9b58-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9b58-135">NOTES</span></span>

## <span data-ttu-id="e9b58-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9b58-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9b58-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e9b58-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e9b58-138">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e9b58-138">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="e9b58-139">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e9b58-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e9b58-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e9b58-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e9b58-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e9b58-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

